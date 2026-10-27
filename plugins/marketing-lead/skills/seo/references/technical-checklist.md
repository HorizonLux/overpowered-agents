# Technical checklist: why, how to check, how to fix

Read this before writing the Job C report in `SKILL.md`. The codes [G..], [H..], [B1] and [R1] are the same as in its Sources list; exact quotes are in `sources.md`.

Order of work: **crawl, render, understand, trust.** Fix in the same order, because a problem early in the chain hides everything after it.

Who usually does a fix:
- **Owner:** anything inside Search Console, and decisions about which pages exist.
- **Site editor:** titles, descriptions, alt text and page content in the website builder or CMS.
- **Developer or host:** robots.txt, redirects, status codes, HTTP headers, rendering.

On many website builders the owner is all three. Say which setting to look for, but do not claim to know where a given builder keeps it: ask the user, or tell them to check the builder's own help pages.

---

## Crawl

### C1. Search Console is set up
- **Why.** Search Console is free, and a site does not need it to appear in Google [H1]. It is still where Google reports which pages it indexed and why others were not [H4], and it holds the URL Inspection tool [H3].
- **How to check.** Ask the owner. You cannot check this yourself.
- **Fix.** The owner adds the site. A Domain property is verified with a DNS record at the domain provider [H8]. Then the owner opens the Page indexing report and shares what it lists under pages not indexed, with the reasons Google gives [H4].

### C2. robots.txt
- **Why.** Google's technical requirements start with Googlebot not being blocked [G5]. robots.txt manages crawling. Do not use it to block CSS, JavaScript or images a page needs, or Google will not analyse that page well [G6].
- **How to check.** Fetch `https://<site>/robots.txt`. Read each `Disallow:` line and list the important pages or files it matches. A missing robots.txt is not an error in itself. UNVERIFIED in this skill: what Google does when the file answers with an error status other than 404; open [G9] if that case comes up.
- **Fix.** Remove the `Disallow` rules that match pages meant for search, or the files those pages need.

### C3. Pages kept out of search
- **Why.** robots.txt is not a way to keep a page out of Google: a blocked URL can still be indexed if other pages link to it [G6]. To keep a page out, use `noindex` or put the page behind a password [G6]. `noindex` works as a meta tag or as an HTTP response header [G7], and only if robots.txt does not block the page, because Google has to crawl the page to see the rule [G7].
- **How to check.** For each page the owner wants out of search (thank-you pages, internal search results, test pages, staging copies), fetch it and look for `<meta name="robots" content="noindex">` in the HTML or an `X-Robots-Tag: noindex` header. Then check C2: the same page must not be disallowed.
- **Also check the opposite.** No page that should be in search carries `noindex`. Website builders often have a "hide from search engines" switch, per page or for the whole site; ask the owner to look.
- **Fix.** Add `noindex` to pages that must stay out, and remove any robots.txt rule that blocks them. For staging or test copies, a password is the safer choice.

### C4. Links
- **Why.** Google can generally crawl a link only if it is an `<a>` element with an `href` attribute [G16].
- **How to check.** In the HTML of the key pages, confirm that menu and in-page links are `<a href="...">`. Flag navigation that only works through scripts or buttons. Flag key pages that no other page links to.
- **Fix.** Use real links for navigation. Link every important page from at least one other page, with anchor text that describes the target [G1].

### C5. Status codes
- **Why.** Google indexes only pages served with HTTP 200 [G5]. Google does not index URLs that return a 4xx code, and treats all 4xx codes except 429 the same [G9]. A "page not found" message served with a 200 code is a soft 404, and Google recommends a real 404 code for pages that do not exist [H4]. 301 and 308 redirects are a strong signal that the target should be processed; 302 and 307 are a weak one [G9][G10]. 5xx and 429 errors make Google slow down its crawling [G9].
- **How to check.** Request the key pages and one made-up address (for example `https://<site>/this-page-does-not-exist-123/`). Note each status code and where redirects lead.
- **Pass.** Live pages answer 200. The made-up address answers 404 or 410. Moved pages answer 301 or 308 and reach the new address in one step.
- **Fix.** Change temporary redirects to permanent ones for permanent moves. Make the "not found" page return a real 404. Server errors go to the developer or host.

### C6. Sitemap
- **Why.** A site of about 500 pages or fewer, where Google can reach every important page by following links from the home page, may not need a sitemap [G13]. A sitemap does not guarantee that every listed URL will be crawled and indexed [G13]. If there is one, it should list the URLs you want in Google's results [G14], as full absolute URLs [G14], and robots.txt can point to it with a `Sitemap:` line [G14]. Google ignores `<priority>` and `<changefreq>` [G14], and `<lastmod>` should reflect the last significant update to the page [G14].
- **How to check.** Look for a `Sitemap:` line in robots.txt, or fetch `https://<site>/sitemap.xml`. Compare a few entries with C3 and C5: no `noindex` pages, no redirects, no 404s, no duplicate address forms.
- **Fix.** Remove entries that do not belong. The owner submits the sitemap in Search Console's Sitemaps report.

## Render

### C7. Content reaches Google
- **Why.** Google recommends server-side rendering or pre-rendering, partly because not all bots can run JavaScript [G15]. When Google sees `noindex`, it may skip rendering and JavaScript [G15], so a script cannot be relied on to remove a `noindex`.
- **How to check.** Fetch the page's HTML without running scripts. If the main text, links, title and description are already there, this passes. If the HTML is nearly empty and scripts build the page, ask the owner to run a live test in URL Inspection and look at the screenshot of the rendered page [H3].
- **Fix.** For a script-built site, the developer moves the key pages to server-side rendering or pre-rendering [G15], or at least confirms with the URL Inspection screenshot that Google sees the content.

### C8. Mobile
- **Why.** Google uses the mobile version of a site's content for indexing and ranking, and asks that the mobile site contain the same content as the desktop site [G17].
- **How to check.** Compare the main text, headings and links on a phone-sized screen with the desktop version. Flag content that exists only on desktop.
- **Fix.** Show the same content on mobile. A different layout is fine.

## Understand

### C9. One address per page
- **Why.** Redirects and `rel="canonical"` are strong signals for which address Google should treat as the main one; inclusion in a sitemap is a weak signal [G8]. Google prefers HTTPS over HTTP as the canonical [G8]. Use absolute URLs in `rel="canonical"` [G8], and do not use robots.txt to choose a canonical [G8]. Google treats addresses with and without a trailing slash as different URLs, except the root, and advises a 301 from the duplicate to the preferred form [B1].
- **How to check.** Request the four forms of the home page (`http://`, `https://`, with and without `www.`) and one inner page with and without its trailing slash. Each extra form should end at one chosen address with a 301 or 308. Then read `<link rel="canonical">` on key pages: if present, it holds the full `https://` address of the page itself (or of the main version, for real duplicates).
- **Fix.** The host or developer sets the redirects. The site editor fixes canonical tags that point to the wrong page, or to a relative address.

### C10. Titles
- **Why.** Every page should have a title in the `<title>` element, descriptive and concise, without keyword stuffing and without boilerplate repeated across pages [G11]. Google may build the title it shows from other text on the page, such as the main heading [G11].
- **How to check.** List the `<title>` of each key page. Flag missing, duplicated, vague ("Home", "Services") or stuffed titles, and titles that disagree with the page's H1.
- **Fix.** Write one title per page from its brief (Job B). The business name may follow a separator [G11].

### C11. Meta descriptions
- **Why.** A good description is short, unique to one page and covers its most relevant points [G1]. Identical or similar descriptions on every page are not helpful [G12]. Google may still write its own snippet from the page text [G12].
- **How to check.** List the `<meta name="description">` of each key page. Flag missing or repeated ones.
- **Fix.** Write one per page from its brief.

### C12. Images
- **Why.** Alt text should be useful and information-rich, using keywords appropriately; filling `alt` attributes with keywords gives a bad user experience [G19].
- **How to check.** List the `alt` text of meaningful images on key pages. Flag empty alt text on meaningful images, and keyword lists.
- **Fix.** Describe what the image shows, in the context of the page.

### C13. Structured data, if any
- **Why.** Markup must not describe content that readers cannot see on the page [G20].
- **How to check.** Find `<script type="application/ld+json">` blocks. Compare each value (name, prices, ratings, dates, authors) with the visible page.
- **Fix.** Remove any value the page does not show. Structured data is optional; a site can skip it.

## Trust

### C14. People-first content
- **Why.** Google offers a self-assessment for content: who made it, how, and why [G2]. Among its warning signs is producing lots of content on many topics in the hope that some of it performs in search [G2]. Scaled content, doorway pages, keyword stuffing, hidden text and link schemes are spam [G3].
- **How to check.** Read the key pages against the questions in [G2]. Look for the patterns listed in Ground rule 6 of `SKILL.md`: sets of near-identical pages (one per town or variation), blocks of place names, repeated phrases, hidden text, paid or swapped links.
- **Fix.** Merge or remove thin, near-identical pages (with permanent redirects where they had visitors [G10]); rewrite stuffed text for readers; remove hidden text and paid links. Recommend, never do: the owner decides which pages go.

### C15. Core Web Vitals
- **Why.** Google highly recommends good Core Web Vitals. Its targets are LCP within 2.5 seconds, INP under 200 milliseconds and CLS under 0.1 [G18]. Google points to Search Console's Core Web Vitals report to see how pages perform [G18].
- **How to check.** Ask the owner for the Core Web Vitals report. A new or small site may have too little data to show; then write `unknown`, not a number. Never present a lab test score you ran as the field result.
- **Fix.** Hand the failing pages and metrics to the developer. Common causes are outside this skill.

### C16. Key pages indexed
- **Why.** URL Inspection shows Google's indexed version of a page, and can run a live test [H3]. Meeting the technical requirements does not guarantee indexing [G5]. Requesting indexing does not guarantee it either, and there is a daily limit on requests [H3].
- **How to check.** The owner inspects the home page and the main offer page, and shares whether each is indexed and, if not, the reason shown.
- **Fix.** Follow the reason Google gives, then fix the matching check above. Only after a real change, request indexing once.

---

## Quick reference: robots.txt versus noindex

| Goal | Use | Do not use |
|---|---|---|
| Keep a page out of Google's results | `noindex` (meta tag or header), or a password [G6][G7] | robots.txt `Disallow` alone [G6] |
| Stop Google crawling unimportant URLs | robots.txt `Disallow` [G6] | `noindex` on pages Google cannot crawl [G7] |
| Choose the main address of a page | 301 or 308 redirect, `rel="canonical"` [G8] | robots.txt [G8] |
