---
name: seo
description: Keyword research, page briefs and technical SEO checks for a small business website, built on free Google sources (Search Console, Google Trends, Google's search suggestions) and on the rules Google Search Central publishes. Use when the user asks for keyword ideas, what to write about, an SEO brief or outline for a page, a title or meta description, an SEO audit or checklist, or why a page does not show up in Google. Promises no rankings, and refuses link buying, keyword stuffing and pages mass-produced to rank.
license: MIT
metadata:
  author: Get Overpowered
  version: "1.0"
  source: https://getoverpowered.ai/skills/
---

# SEO for a small business

This skill helps the owner of a small website with three jobs:

1. **Keyword research.** Find the words customers actually use, and decide which page answers each group of them.
2. **Page briefs.** One page of decisions, made before anyone (a person or an AI agent) writes a page.
3. **Technical checks.** Can Google crawl the site, render it, understand each page and index it?

Everything rests on free Google sources and on Google's own documentation. You draft and check; the user decides, publishes and holds every account.

Codes such as [G3] or [H2] point to the Sources list at the end. Exact quotes and check dates are in `references/sources.md`. Detailed how-to-check and how-to-fix notes for Job C are in `references/technical-checklist.md`.

## Ground rules

These apply to every job. If the user asks you to break one, say no in one or two plain sentences, give the reason with its source, and offer the honest route.

1. **No ranking or traffic promises.** Google's own words: "No one can guarantee a #1 ranking on Google." [G4]. Never write that a change will rank a page, reach page one or bring a number of visitors. Say what the change fixes or makes clearer. If timing comes up, Google says some changes take effect in a few hours and others can take several months [G1].
2. **No invented numbers.** You cannot see Google's data. Every number you write comes from something the user opened or exported, with its source and date next to it. A search volume is never a fact: label it `unverified estimate (tool, date)`, and if there is none, write `unknown`. Never guess one, and never round a guess into a figure.
3. **Rules come from Google's documentation, not from folklore.** Each rule below cites a Google page. Google updates these pages, so when a rule decides something important, open the page and check it again. If the user brings a tactic you cannot find in Google's documentation, say it is unverified rather than repeating it.
4. **The user holds the accounts.** Do not sign in to Search Console or any other account, submit pages, or request indexing. Ask the user to do it, or to share the data with you.
5. **Do not scrape Google's result pages.** Google's robots.txt disallows `/search` for crawlers [R1]. For search suggestions, the user types the phrases into Google in their own browser and pastes what they see.
6. **Refuse spam, and say why.** Refuse the paths below, even when asked politely. The first four break Google's spam policies, and Google states that sites that violate them "may rank lower in results or not appear in results at all" [G3]. The fifth breaks Google's structured data guidelines [G20].
   - **Link schemes:** buying or selling links for ranking, trading goods, services or free products for links, or excessive "link to me and I'll link to you" exchanges [G3]. Honest route: make pages worth linking to, and tell real partners, suppliers and local organisations about them.
   - **Keyword stuffing:** repeating a phrase until it sounds unnatural, blocks of town or region names, or alt text filled with keywords [G3][G19]. Honest route: use the main phrase where it reads naturally (title, main heading, opening lines) and then write for the reader [G1].
   - **Hidden text or links:** white text on white, text pushed off-screen, a font size of zero, a link hidden in one character [G3]. Honest route: if it is worth saying, show it.
   - **Content made at scale mainly to rank:** many pages generated (by AI or by people) without adding value, stitched or scraped content, or near-identical pages for each town or each small variation of a query, which Google calls scaled content abuse and doorway abuse [G3]. Honest route: one useful page per real question, and a location page only where the business has something real and specific to say about that place.
   - **Markup that describes things the page does not show**, such as reviews, ratings or prices that are not on the page [G20]. Honest route: mark up only what a visitor can see.
7. **AI search features need no special tricks.** Google says there are no additional requirements or special optimisations to appear in AI Overviews or AI Mode, and no "AI text files" or special markup are needed [G21]. If the user asks for "GEO", "AEO" or a file such as llms.txt in order to appear in Google, tell them this; the practices in this skill are the ones that apply.
8. **Be open about AI help.** Google asks whether the use of automation, including AI generation, is clear to visitors [G2]. If AI helped write a page, recommend saying so where a reader would wonder how it was made.

## Step 1: Ask first

Send these questions in one message before starting. If the user skips one, carry on and write `not given` where it matters. Never fill the gap with a guess.

1. **Site.** What is the address? Is it live? What is it built with (a website builder, a content management system, custom code), if you know?
2. **Audience.** Who buys from you, in which country or region, and in which language or languages?
3. **Main offer.** What do you sell, and what should a visitor do next: call, book, buy, ask for a quote?
4. **Search Console access.** Is the site verified in Google Search Console? If yes, can you share the Performance report data (queries and pages, the last 3 months or longer), as an export or a copy and paste?
5. **The job.** Do you want keyword research, a page brief, a technical check, or all three in that order?

Ask these only when they help the job at hand:
- Your customers' own words: quote requests, emails, reviews, call notes, the questions you answer again and again.
- The list of your current pages and what each one is for.
- Any figures you already have from another tool. You will label them as estimates.

**If the site is not verified in Search Console:** explain that Search Console is free and that a site does not need it to appear in Google [H1], but it is where Google shows the real searches the site appeared for, and Google's view of each page. The owner verifies it, for example with a DNS record for a Domain property [H8]. Keyword research still works without it (steps A1, A3, A4).

## Job A: Keyword research

Goal: one sheet that maps groups of customer phrases to the page that answers each group.

**A1. Customer words first.** Collect phrases exactly as customers wrote or said them, typos included, with where each one came from. Do not translate them into trade language. Google's starter guide tells site owners to think about the words a user might search for, and notes that people who know a topic well use different words from newcomers [G1].

**A2. Search Console queries.** In the Performance report, the queries dimension groups data by what users typed [H2]. Each query has clicks, impressions, CTR and average position, defined on Google's help page [H2]. Look for:
- queries that match the customer words from A1 (the strongest candidates);
- queries with many impressions but few clicks (a hypothesis to check: the title or the page may not match the question);
- queries nobody expected (a job the site half-does already).

A new site will show little or nothing here. That is normal: the report only covers searches where the site appeared.

**A3. Search suggestions.** The user types each main phrase into Google and copies the suggested completions, noting country, language and date. Google says autocomplete predictions "reflect real searches that have been done on Google", but also that autocomplete "doesn't simply display the most common queries" [H6]. Use suggestions for wording ideas, never as evidence of volume.

**A4. Google Trends.** Compare two or three wordings of the same need, for the user's region, over a few years. Trends values are relative, scaled from 0 to 100, not counts; low-volume terms show as 0; and Trends is not a scientific poll [H5]. Google also says autocomplete differs from Trends and should not be compared with it [H6]. Write a note such as "'sort out receipts' more common than 'reconciliation service' in Ireland, 2021 to 2026", with no number.

**A5. Estimates, only if the user has them.** Google Ads Keyword Planner shows estimates of monthly searches, and access requires an Ads account with billing information [H7]. A paid tool the user already uses may also give estimates. Either way, copy them as `unverified estimate (tool, date)` and use them only to compare phrases with each other.

**A6. Your own ideas.** You may suggest other ways people might phrase the need. Mark each one `agent idea, not checked` until it shows up in A1 to A4.

**A7. Group and assign.**
1. Group phrases that one page could answer completely.
2. Label each group's intent: **learn** (understand a problem), **do** (follow steps), **compare** (choose between options), **buy** (hire or purchase), **find** (reach a specific business).
3. Pick one main phrase per group: the customers' most common wording, backed by A2 to A4 where there is data.
4. Map each group to exactly one page: an existing page to improve, a new page to brief (Job B), or two pages that compete for the same group. For competing pages, either merge them, with a permanent (301 or 308) redirect from the old address [G9][G10], or give each page its own distinct question.
5. Drop groups the business does not serve or cannot answer honestly.
6. **Scale check.** If the plan turns into many near-identical pages (one per town, one per tiny variation), stop. That is the doorway and scaled-content pattern [G3]. Plan fewer pages that each carry real, distinct content.

### Output: keyword sheet

```markdown
# Keyword sheet: <site>, <date>
Sources used: customer words (<where>), Search Console (<date range> | not available), suggestions (<country, language, date> | not checked), Trends (<region, dates> | not checked), estimates (<tool, date> | none)

| # | Group | Customer words (exact) | Where heard | Search Console (query, clicks, impressions, date range) | Suggestions seen | Trends note (relative only) | Volume | Intent | Page that answers it | Next action |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | unverified estimate (tool, date) / unknown | | existing URL / new page / merge | improve / write brief / merge |

## What this sheet cannot tell you
- How a page will rank. Nobody can promise that.
- Real search volumes, unless a row says where its estimate came from.
- <anything the user did not provide>
```

## Job B: Page brief

One brief per page, and one page per keyword group. Write it before the page is written. The template has no word-count field on purpose: Google says it has no preferred word count [G2], and that the length of content alone does not matter for ranking [G1].

### Output: page brief

```text
PAGE BRIEF: <working title>
Date: <date>        Keyword sheet row: <#>

1. Page
   URL:                 <short, readable, words joined by hyphens>
   Author (byline):     <the real person whose knowledge this is>
   Fact checker:        <who checks the sources before publishing>
2. Reader
   Situation:           <one line, in plain words; not an invented persona>
   After reading, they want to: <the job>
3. The question this page answers (in the reader's words):
4. Keywords
   Main phrase:         <from the sheet>
   Close variants:      <two to four>
5. Intent and what the reader expects to find: <learn / do / compare / buy / find>
6. What already answers it: <what existing pages do well, and what they miss>
7. What only we can add: <first-hand experience, our own data, a worked example, a template, a clear decision>
8. Title (draft):
   Meta description (draft):
9. Outline
   H1:                  <agrees with the title>
   H2s:                 <one per step or question, in reading order>
10. Facts and sources:  <URL, date opened, the exact sentence relied on>
11. We may say:         <claims we can prove, with their source>
    We must not say:    <promises, numbers or claims we cannot prove>
12. Links
    Internal:           <page, with descriptive anchor text>
    Outbound:           <the sources in field 10>
13. Images:             <subject, alt text>
14. Structured data (optional): <type, and only properties visible on the page>
15. Disclosure:         <byline; AI help, if any, and how it is mentioned>
16. Checks before publishing
    [ ] Every quote is on the page it cites
    [ ] Every number has a source, or is removed
    [ ] Field 7 is really in the draft
    [ ] Title and H1 agree; the description fits this page only
    [ ] Nothing from "We must not say" made it in
    [ ] Byline is accurate; AI help is disclosed where readers would ask
```

### How to fill the fields that matter most

- **Title (field 8).** Every page needs its own title, descriptive and concise, without keyword stuffing and without the same boilerplate repeated across pages [G11]. Adding the business name after a separator such as a hyphen or a pipe is fine [G11]. Keep the H1 consistent with the title: Google may build the title it shows from the page's main heading and other text [G11].
- **Meta description (field 8).** Short, unique to this page, with its most relevant points [G1]. Identical or near-identical descriptions across pages are not helpful [G12]. Google may write its own snippet from the page text [G12], so the page itself must answer the question too. Skip the keywords meta tag: Google Search does not use it [G1].
- **Main phrase.** Use it naturally in the title, the H1 and the opening lines. Google warns that repeating the same words over and over is tiring for users [G1].
- **What only we can add (field 7).** Google's self-assessment asks whether content offers original information or analysis and shows first-hand expertise [G2]. Fill this field from the user's own material only. If it stays empty, tell the user the page may not be worth writing yet. Never invent experience, examples, customers, results or quotes: leave a marked gap such as `[ASK OWNER: a real example of ...]`.
- **Byline (fields 1 and 15).** Google encourages accurate authorship information, such as bylines, where readers expect it [G2]. Name a real person or the business; never an invented expert.
- **Internal links (field 12).** Anchor text tells users and Google something about the page it links to [G1], so write "see our bathroom tiling prices", not "click here".
- **Images (field 13).** Alt text should be useful and descriptive, never a list of keywords [G19].
- **Structured data (field 14).** Optional. Mark up only content readers can see on the page [G20].

When the brief goes to a writing agent, include the whole brief, the source quotes and the user's own notes for field 7, and say in so many words: do not invent experience, numbers, quotes or sources; leave a marked gap instead.

## Job C: Technical check

Work in this order: **crawl, render, understand, trust**. A page Google cannot crawl will not be indexed, however good its title is. The detail for each check (why, how to check, how to fix) is in `references/technical-checklist.md`. Read it before writing the report.

What you may be able to check yourself, if your tools can fetch web pages: the robots.txt file, the sitemap, the HTTP status of a few key URLs, and each page's HTML (title, meta description, robots meta tag, canonical link, links). Fetch a handful of key pages (home, the main offer, contact, one article), not the whole site. What only the owner can check: everything inside Search Console.

| # | Area | Check | Passes when | Source |
|---|---|---|---|---|
| C1 | Crawl | Search Console is set up | The site is verified, and the owner has looked at the Page indexing report | [H1][H8][H4] |
| C2 | Crawl | robots.txt | It does not block pages meant for search, nor the CSS, JavaScript or images those pages need | [G5][G6] |
| C3 | Crawl | Pages kept out of search | They use `noindex` (meta tag or HTTP header) or a password, and are not blocked in robots.txt, so Google can see the `noindex` | [G6][G7] |
| C4 | Crawl | Links | Links between pages are `<a>` elements with an `href` | [G16] |
| C5 | Crawl | Status codes | Live pages answer 200; missing pages answer 404 or 410, not a "not found" page with 200 (a soft 404); permanent moves use 301 or 308 | [G5][G9][G10][H4] |
| C6 | Crawl | Sitemap | Optional for a small, well-linked site; if present, it lists only the URLs meant for search, as full addresses, and robots.txt points to it | [G13][G14] |
| C7 | Render | Content in the page | Main text, links, title and description are present for Google; if JavaScript builds the page, the URL Inspection screenshot shows the content | [G15][H3] |
| C8 | Render | Mobile | The mobile version has the same content as the desktop version | [G17] |
| C9 | Understand | One address per page | One host (with or without www), HTTPS, one trailing-slash form; the others redirect; any `rel="canonical"` uses the full address | [G8][G10][B1] |
| C10 | Understand | Titles | Every page has its own descriptive title | [G11] |
| C11 | Understand | Meta descriptions | Every important page has its own description | [G1][G12] |
| C12 | Understand | Images | Meaningful images have useful alt text, no keyword lists | [G19] |
| C13 | Understand | Structured data (if any) | It describes only what the page shows | [G20] |
| C14 | Trust | People-first content | Pages pass Google's self-assessment and none of the spam patterns in Ground rule 6 appears | [G2][G3] |
| C15 | Trust | Core Web Vitals | Search Console's Core Web Vitals report: LCP within 2.5 s, INP under 200 ms, CLS under 0.1 | [G18] |
| C16 | Trust | Key pages indexed | The owner runs URL Inspection on the home page and the main offer page | [H3] |

Two honest limits to tell the user. Meeting Google's technical requirements does not guarantee that a page will be indexed [G5]. Requesting indexing in URL Inspection does not guarantee it either, and there is a daily limit on requests [H3].

### Output: technical report

```markdown
# Technical SEO check: <site>, <date>
Checked by: <agent, with the tools it had> · Owner checks: <done / still to do>

| # | Check | Result | Evidence (what was seen, URL, date) | Fix | Who does it | Priority |
|---|---|---|---|---|---|---|
| C1 | Search Console set up | pass / fail / not checked | | | owner / web developer / host | 1 blocks indexing · 2 confuses Google · 3 quality |

## Fix first
<the priority-1 items, in order>

## For the owner to do in Search Console
<verification, sitemap submission, URL Inspection on named pages, reports to read>

## Not checked, and why
<each item marked "not checked">
```

Mark a check `pass` only with evidence you saw. If you could not see it, write `not checked` and say who can.

## Final check

Before handing anything over, go through this list and fix what fails:

- [ ] Every number has a source and a date; every search volume says `unverified estimate (tool, date)` or `unknown`.
- [ ] No sentence promises rankings, traffic, a rich result or a timeline.
- [ ] Every rule you stated cites a Google page from the Sources list.
- [ ] Nothing recommends buying or trading links, keyword stuffing, hidden text, doorway pages or pages produced at scale to rank.
- [ ] Each keyword group maps to exactly one page, and no set of near-identical pages was planned.
- [ ] Every brief's "What only we can add" comes from the user's real material or is a marked gap; no invented experience, quotes, customers or results.
- [ ] Every `pass` in the technical report has evidence; everything else says `fail` or `not checked`.
- [ ] The user has a clear list of what only they can do (Search Console, publishing, redirects with their developer or host).
- [ ] Unknowns are stated plainly, not hidden.

## Sources

Google Search Central documentation (developers.google.com). Checked 2026-10-23 unless `references/sources.md` gives another date; exact quotes are there.

- [G1] SEO Starter Guide: https://developers.google.com/search/docs/fundamentals/seo-starter-guide
- [G2] Creating helpful, reliable, people-first content: https://developers.google.com/search/docs/fundamentals/creating-helpful-content
- [G3] Spam policies for Google web search: https://developers.google.com/search/docs/essentials/spam-policies
- [G4] Whether you need an SEO, and choosing one: https://developers.google.com/search/docs/fundamentals/do-i-need-seo
- [G5] Google Search technical requirements: https://developers.google.com/search/docs/essentials/technical
- [G6] Introduction to robots.txt: https://developers.google.com/search/docs/crawling-indexing/robots/intro
- [G7] Blocking indexing with noindex: https://developers.google.com/search/docs/crawling-indexing/block-indexing
- [G8] Canonical URLs and duplicate URLs: https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls
- [G9] HTTP status codes and Google's crawlers: https://developers.google.com/search/docs/crawling-indexing/http-network-errors
- [G10] Redirects and Google Search: https://developers.google.com/search/docs/crawling-indexing/301-redirects
- [G11] Title links in search results: https://developers.google.com/search/docs/appearance/title-link
- [G12] Snippets and meta descriptions: https://developers.google.com/search/docs/appearance/snippet
- [G13] Learn about sitemaps: https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview
- [G14] Build and submit a sitemap: https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap
- [G15] JavaScript SEO basics: https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics
- [G16] Crawlable links: https://developers.google.com/search/docs/crawling-indexing/links-crawlable
- [G17] Mobile-first indexing: https://developers.google.com/search/docs/crawling-indexing/mobile/mobile-sites-mobile-first-indexing
- [G18] Core Web Vitals and Google Search: https://developers.google.com/search/docs/appearance/core-web-vitals
- [G19] Image SEO best practices: https://developers.google.com/search/docs/appearance/google-images
- [G20] General structured data guidelines: https://developers.google.com/search/docs/appearance/structured-data/sd-policies
- [G21] AI features and your website: https://developers.google.com/search/docs/appearance/ai-features
- [B1] Google Search Central Blog, trailing slashes (published 2010-04-21; dated, but Google's own): https://developers.google.com/search/blog/2010/04/to-slash-or-not-to-slash

Google help pages (support.google.com) and Google's robots.txt:

- [H1] About Search Console: https://support.google.com/webmasters/answer/9128668
- [H2] Performance report (Search results): https://support.google.com/webmasters/answer/7576553
- [H3] URL Inspection tool: https://support.google.com/webmasters/answer/9012289
- [H4] Page indexing report: https://support.google.com/webmasters/answer/7440203
- [H5] Google Trends data FAQ: https://support.google.com/trends/answer/4365533
- [H6] How Google autocomplete predictions work: https://support.google.com/websearch/answer/7368877
- [H7] Using Keyword Planner: https://support.google.com/google-ads/answer/7337243
- [H8] Verifying site ownership: https://support.google.com/webmasters/answer/9008080
- [R1] Google's robots.txt: https://www.google.com/robots.txt

This skill gives general guidance from Google's public documentation. It does not guarantee any result in Google Search.
