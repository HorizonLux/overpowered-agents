---
name: outreach
description: Builds a prospect list from lawful sources, drafts an honest first sales email and plans up to two follow-ups for a one-person business or small team, with a compliance check against US (CAN-SPAM), UK (PECR, UK GDPR) and EU (ePrivacy, GDPR) email rules. Use when the user asks for a prospect or lead list, a cold or first outreach email, a follow-up email, or whether they may email a business. It drafts; the user sends.
license: MIT
metadata:
  author: Get Overpowered
  version: "1.0"
  source: https://getoverpowered.ai/skills/
---

# Outreach: prospect lists, first emails and follow-ups

This skill helps a one-person business, or a small team, write to the businesses most likely to need what it sells. It produces three things:

1. a short prospect list of companies that fit, built from sources the user may use, with where and when each one was found;
2. a first email that says honestly who is writing, why, and how to say no;
3. at most two follow-ups by default, with clear rules for when to stop.

**You draft. The user checks, decides and sends.**

> **General information, not legal advice.** The email rules this skill relies on are quoted, with their official sources, in `references/rules-by-region.md`. They were read on 23 October 2026, and rules change. For anything that matters, the user re-reads the current official page or asks a lawyer.

Bracketed IDs such as [US-1] or [UK-1] point to the sources table at the end of `references/rules-by-region.md`, where each has its URL.

## Ground rules

Apply these throughout. They are why the user can trust the drafts.

1. **Draft only.** Never send, schedule or queue an email, submit a contact form, connect with someone or message them on a platform, even if a tool you have access to could. Hand every draft to the user.
2. **Only true content.** Use facts the user gives you or that a company publishes about itself. Never invent statistics, reply rates, results, customers, testimonials, mutual contacts, past conversations, or a reason to write ("I saw your talk…") that did not happen. If the user has no proof yet, the email makes no claim. That is fine.
3. **Companies first, people last.** Collect only what the outreach needs. No private email addresses or phone numbers, home addresses, photos, or notes about anyone's private life. Never guess an email address from a name pattern.
4. **Lawful sources only.** Read a site's terms before collecting anything from it. No scraping where the terms forbid it, and no collection from LinkedIn by an agent or a script: its User Agreement forbids scraping profiles and automated messaging [P-1].
5. **An opt-out is final.** Anyone who opted out or objected is never drafted for again.
6. **Unknown is a valid answer.** If a country or a type of recipient is not covered in the rules file, say so and stop for that row. Never assume it is allowed.

## Step 1: Ask first

Ask these questions in one short message before anything else. Do not build the list or write a draft until questions 1 to 4 are answered.

1. **Your offer.** What do you sell, in one sentence, and what problem does it solve for the buyer?
2. **Your buyer.** What kind of business buys it, what size, and what is the role of the person who says yes?
3. **You.** Which country are you based in, and do you trade as a company, a sole trader or a partnership? Which name, business name and postal address will appear in your emails?
4. **Your prospects' location.** Which countries are they in?
5. **Your prospects' form.** Are they mostly companies, or single people such as sole traders and freelancers?
6. **Contacts you already have.** Where did each group come from: your own customers, people who asked you, people you met, a list you bought or were given, something else?
7. **Proof.** What can you honestly point to: a result you can show, a public example, a free trial, or nothing yet?
8. **Sending.** What will you send from (your own mailbox or an email tool)? Do you have a working way to opt out, a privacy notice you can link, and a do-not-contact list?

Questions 3 and 4 decide which rules apply and what every email must contain. If the user cannot answer them, explain that and wait.

Then summarise the answers in five lines (offer, buyer, sender's country and form, prospects' countries, contact sources) and ask the user to confirm before you go on.

## Step 2: Check the rules for each region

Read `references/rules-by-region.md`. For each prospect country and type, set one label. The prospect list carries it in the "Rules check" column.

| Label | Applies to | What you do |
|---|---|---|
| OK to email, rules apply | Recipients in the US [US-1]; people at UK companies, including LLPs [UK-1] | Draft. Every message meets the "always" rules |
| Consent needed | UK sole traders and some partnerships [UK-1][UK-2]; natural persons in the EU, which usually includes sole traders [EU-1]. Exception: the user's own existing customers, under the UK soft opt-in or EU Article 13(2), if its conditions are met [UK-2][EU-1] | No cold email. Offer another route (Step 3.5) |
| Check national rule | People at companies in an EU country: each country sets its own rule [EU-1] | You may draft, marked "Not cleared: check the rule for <country>", until the user confirms they have checked it |
| Not covered | Any other country | Ask the user to read that country's official rules first. Draft only after they have, labelled "Rules for <country> not checked by this skill" |

Two more points:

- **Different regions.** If the user and a prospect are in different regions, more than one set of rules can apply. Follow every set that may apply, or the user asks a lawyer which one does.
- **Named people in the UK or the EU.** The user also needs a lawful basis for holding the person's details. The ICO says the two most relevant are consent and legitimate interests, and legitimate interests needs its three-part test first [UK-1]. The person must be told where their details came from. Because this skill uses the details to write to them, the deadline in both the UK and the EU is the first message at the latest [EU-2][UK-6]. The draft in Step 4 has a line for this.

## Step 3: Build the prospect list

**3.1 Write a fit rule.** One sentence the user can test against a website in two minutes:

> [type of business] in [country], about [size], that shows [a sign you can see from outside].

The last part does the work: the services a company lists, the jobs it advertises, the tools it names, the markets it serves. "Small agencies" cannot be tested; "agencies of 2 to 10 people whose site lists a service the user's offer complements" can.

**3.2 Find companies in sources the user may use.**
- The company's own website: what it does, who it serves, how it wants to be contacted.
- Official company registers. In the UK, Companies House gives some company details for free [UK-5], and shows whether a business is a company or not, which matters in Step 2.
- Public statistics, to choose where to look (not whom to write to). In the US, the Census Bureau's County Business Patterns provides "subnational economic data for establishments with paid employees" by industry and employment size ([US Census Bureau](https://www.census.gov/programs-surveys/cbp.html), page revised 5 August 2026). The Small Business Administration says "There are many reliable sources that provide customer and market information at no cost" and names NAICS, the U.S. Census Business Builder and Statistics of U.S. Businesses ([SBA, Market research and competitive analysis](https://www.sba.gov/business-guide/plan-your-business/market-research-competitive-analysis)).
- Member, exhibitor or partner directories that a trade body or event publishes, after reading their terms.
- The user's own network: customers, people who asked, people met at events, introductions.

**3.3 Check each company against the fit rule.** Write one true, specific line: why this company, now. If you cannot write it, drop the company. That line opens the first email, so it must be something the company published, not a guess.

**3.4 Record the source URL and the date found for every row.** It lets the user re-check later, and in the UK and the EU the person must be told where their details came from [EU-2][UK-6].

**3.5 Choose the contact route last.** A generic company address (such as info@), a named person at a company, an introduction, or an event. For rows labelled "Consent needed", do not plan a cold email. Suggest an introduction, meeting at an event, replying publicly to something they published, or inviting them to sign up for something useful. Treat a social-media direct message like an email for these rows: the ICO counts "direct messages via social media" as electronic mail [UK-1]. Whether a message sent through a website contact form counts too is UNVERIFIED: no regulator page we found says, although the official definitions point that way (see "Contact forms" in the rules file). So treat it the same way.

**3.6 Add named people last,** only for the companies the user will contact in this round. Use a work address the company or the person published. Recommend that the user keeps named contacts in their own tool, separate from the company list, so the company list can be shared without spreading anyone's details.

**3.7 Remove anyone on the do-not-contact list** before drafting.

**How long?** There is no right number, and this skill will not quote one. A useful limit: as many companies as the user can research properly and write to personally in the next two weeks.

**A bought or borrowed list.** Ask where it came from and on what basis. In the EU, a company using a list from someone else "must be able to demonstrate that the data was obtained in compliance with the General Data Protection Regulation", and where the list rests on consent, that consent should have covered passing the data on for other recipients' marketing [EU-6]. In the UK, the use of any personal data on a bought list "must comply with the UK GDPR" [UK-1]. Gmail's sender guidelines say "Don't purchase email addresses from other companies." [P-2] If the user cannot show a lawful basis, do not draft for that list; offer to build a fresh one instead.

**Prospect list template** (one row per company; placeholders in brackets):

| Column | What goes in it | Example |
|---|---|---|
| Company | Registered or trading name | [Example Studio Ltd] |
| Website | Home page | [https://example.com] |
| Country | Where the business is based | [UK] |
| Business type | Company, sole trader, partnership, unknown | [Company] |
| Size band | A range, from their site or a register | [2 to 10] |
| Why them, now | One true, specific line | [Lists brand design; no copywriting service; hiring a project lead] |
| Source URL | Page where you found them | [https://example.com/about] |
| Date found | YYYY-MM-DD | [2026-10-23] |
| Contact route | Generic address, named person, introduction, event | [Generic address] |
| Rules check | OK to email, rules apply · Consent needed · Check national rule · Not covered | [OK to email, rules apply] |
| Status | Not contacted · Email 1 sent · Follow-up 1 sent · Follow-up 2 sent · Replied · Closed | [Not contacted] |
| Opted out | Yes or no. "Yes" is permanent | [No] |

## Step 4: Write the first email

Rules for every first email:

- **Real sender.** The user's real name and business, from an address they control, with a display name that is really theirs [US-1][UK-2][EU-1][P-2].
- **Honest subject line** that describes the email. No "Re:" or "Fwd:" on a new message, no false urgency, no bait [US-1][P-2].
- **Why them**: the true line from the list.
- **Say it is an offer**, in plain words such as "I'm writing to offer…". The FTC requires a commercial email to be identified as an ad [US-1].
- **At most one claim**, true, and one the user can back up. No proof, no claim.
- **One easy ask.**
- **Where you found their address**, for named people in the UK or the EU, in this first email [EU-2][UK-6].
- **The opt-out on its own line**, separate from everything else [EU-3], working, and honoured [US-1][UK-1][EU-1].
- **Footer**: name and business; postal address for US recipients [US-1] (a good habit everywhere); privacy notice link for named people in the UK or the EU [EU-2][UK-1].
- **No tracking pixels or tracked links** for EU recipients unless the user has checked them against ePrivacy Article 5(3) [EU-7].
- **Short**: aim for 120 words or fewer in the body. That is a habit, not a rule.

**First email template:**

```text
Subject: [What the email is about, in plain words, e.g. "Copywriting for [Company]'s client projects"]

Hi [first name, or "the [Company] team" for a generic address],

[Why them: one true line, e.g. "Your site lists brand and web design, and your new project lead role mentions client copy."]

I'm writing to offer [the offer in the buyer's terms, one sentence]. [One true claim the user can back up, or delete this sentence.]

[One easy ask, e.g. "Would a 15-minute call next week be useful?" or "Shall I send a one-page outline?"]

[Your name]
[Business name] · [website]
[Postal address: required for US recipients]
[EU/UK named person: "I found your work address on [source]. Privacy notice: [link]"]

If you'd rather not hear from me, reply "no thanks" and I won't contact you again.
```

## Step 5: Follow up

**Default: at most two follow-ups, then stop.** That is a courtesy to the reader and the user's choice, not the law: none of the rules quoted in the rules file sets a number. The user may choose fewer. Leave several business days between messages; the user picks the gap.

Every follow-up:
- adds something new and useful (an answer to a likely question, a short example) or simply closes the loop;
- keeps the sender's identity, the footer and the opt-out line;
- never adds "Re:" or "Fwd:" to a new message [P-2]; sending the follow-up as a reply in the user's own thread is a real reply;
- has no guilt, pressure or invented deadline ("last chance", "closing your file").

**Stop rules:**
- **Any reply** stops the sequence. The user answers personally.
- **An opt-out or objection** stops all messages for good. The user adds the address to the do-not-contact list the same day. US law allows at most 10 business days [US-1][US-2]; the right to object in the UK and the EU is absolute [UK-1][EU-3].
- **A bounce** removes the address.
- **After the second follow-up**, mark the row "Closed". No further messages.

**Follow-up templates:**

```text
Subject: [Same subject as email 1 if sent in the same thread; otherwise a new honest subject]

Hi [first name],

[One new, useful thing, e.g. "One question I often hear is how long this takes to set up; the short answer for [type of business] is [true answer from the user]."]

[The same easy ask, or a smaller one.]

[Signature and footer as in email 1]

If you'd rather not hear from me, reply "no thanks" and I won't contact you again.
```

```text
Subject: [Same thread, or a new honest subject]

Hi [first name],

I won't keep writing about this. If [the problem] becomes a priority later, my details are below.

[Signature and footer as in email 1]

If you'd rather not hear from me, reply "no thanks" and I won't contact you again.
```

## Step 6: Compliance check

Run this for every draft before you hand it over. **General information, not legal advice.** Details and quotes: `references/rules-by-region.md`.

| Check | US | UK | EU |
|---|---|---|---|
| Recipient's region and type known, rules label set | Yes | Yes | Yes |
| No cold email to consent-needed recipients | — | Sole traders, some partnerships [UK-1] | Natural persons [EU-1] |
| National rule checked for people at companies | — | — | Yes [EU-1] |
| Lawful basis noted for named people | — | Yes [UK-1] | Yes [EU-4] |
| Real sender, nothing disguised | [US-1] | [UK-2] | [EU-1] |
| Honest header and subject | [US-1] | May be required (not covered); check [UK-7] | May be required (not covered); check |
| Identified as an offer | [US-1] | May be required (not covered); check [UK-7] | May be required (not covered); check |
| Physical postal address | [US-1][US-2] | Good practice | Good practice |
| Where the address was found, by the first message | — | Yes [UK-6] | Yes [EU-2] |
| Opt-out on its own line, working | [US-1] | [UK-1] | [EU-1][EU-3] |
| Privacy notice link for named people | — | Yes [UK-1] | Yes [EU-2] |
| No tracking pixels or tracked links unless checked | — | User checks the ICO | [EU-7] |
| Do-not-contact list applied | [US-1] | [UK-1][UK-4] | [EU-3] |

"May be required (not covered); check": e-commerce rules on commercial communications may require an honest, clearly identifiable commercial email that names who it is from. Whether they apply to the user is a question for the user's adviser, and this skill does not cover them (UK pointer: [UK-7]; EU equivalent not checked). Do these things anyway; the drafts in Steps 4 and 5 already do.

The FTC page cited as [US-1] is CAN-SPAM guidance from the US Federal Trade Commission. [UK-6] and [UK-7] are UK legislation on legislation.gov.uk. [UK-1] and [UK-2] are ICO pages, which the ICO marks as under review after the Data (Use and Access) Act; re-check them before each campaign. [EU-1] to [EU-4] are the ePrivacy Directive and the GDPR (official text on EUR-Lex).

## What this skill refuses, and why

If the user asks for any of the following, say no in one sentence that names the reason, then offer the lawful route. Do not lecture.

| Request | Why not | Offer instead |
|---|---|---|
| Send to a large list nobody checked, without identity or opt-out (spam) | Breaks the identity and opt-out rules in all three regions [US-1][UK-1][EU-1] | A short, checked list and personal emails |
| Cold email a UK sole trader or an EU natural person without consent | Consent is required [UK-1][UK-2][UK-3][EU-1] | An introduction, an event, a public reply, or an invitation to sign up |
| Use a bought, rented or borrowed list with no lawful basis | The user must show the data was lawfully obtained and may be used [EU-6][UK-1]; mailbox providers say not to buy addresses [P-2] | Build a fresh list from Step 3 |
| Scrape LinkedIn or a site whose terms forbid it; automate connection requests or messages | Against the platform's terms [P-1] | Company websites, registers, manual messages sent by the user |
| Guess email addresses from name patterns | There is no source to tell the person [EU-2], and it may not even be their address | A generic address or the contact route the company publishes |
| Write as someone else: a fake name or company, a misleading display name, posing as a customer, journalist or recruiter, or "as we discussed" when no conversation happened | Impersonation and a disguised sender [US-1][UK-2][EU-1][P-2] | The user's real identity and the true reason for writing |
| Fake "Re:" or "Fwd:", false urgency, a subject that misleads | Deceptive subject lines [US-1][P-2] | A plain subject that matches the email |
| Invent statistics, results, testimonials or reply rates | They are untrue, and the user signs the email | The user's real proof, or no claim |
| Write again to someone who opted out | An objection is final [EU-3][UK-1]; US opt-outs must be honoured [US-1] | Nothing. Keep them on the do-not-contact list |
| Hide, remove or complicate the opt-out | Required in all three regions [US-1][UK-1][EU-1][EU-3] | One clear line on its own |

## What you hand back

In this order:

1. The five-line summary from Step 1, as confirmed by the user.
2. The rules check: one line per country and recipient type, with its label.
3. The prospect list (company rows; named people only in the user's own tool).
4. The first email for each segment or row, with merge fields left for the user's sending tool.
5. Up to two follow-ups, the gaps the user chose, and the stop rules.
6. A short send checklist for the user: suppression list applied, opt-out tested, footer complete, drafts read and edited by the user.

End with: "These are drafts. You check them and send them yourself. General information, not legal advice."

## Final check

Before you hand anything over, confirm each line. Fix what fails, or tell the user plainly what is still open.

- [ ] Questions 1 to 4 are answered and the user confirmed the summary.
- [ ] Every list row has a country, a business type, a rules label, a source URL and a date.
- [ ] No row labelled "Consent needed" has a cold email; no "Not covered" row has a draft unless the user checked that country's rules.
- [ ] No contact was bought without a lawful basis, scraped against a site's terms, or guessed; the do-not-contact list was applied.
- [ ] Every draft has the real sender, an honest subject, a true "why them" line, plain words saying it is an offer, at most one true claim, one ask, the opt-out on its own line, and the footer each region needs.
- [ ] At most two follow-ups by default, with stop rules written out.
- [ ] No invented numbers, results, names, quotes or conversations anywhere.
- [ ] Nothing was sent, scheduled or submitted. The user sends.
- [ ] Anything not covered here (a country, a contact form, a sender outside the recipient's region) is named as unchecked, not as allowed.
