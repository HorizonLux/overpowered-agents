---
name: reputation
description: Drafts calm, factual replies to customer reviews (positive, neutral and negative) and sets up free brand-mention watching with a weekly routine, for a one-person business or a small team. Use when the user asks how to answer a review, wants a reply to a bad review, needs a review reply template, wants to know what people say about their business online, or asks how to get more reviews within the rules. It refuses fake reviews, review gating and incentives for reviews where a law or platform bans them, and it hands legal threats, safety issues and crises to a human.
license: MIT
metadata:
  author: Get Overpowered
  version: "1.0"
  source: https://getoverpowered.ai/skills/
---
# Reputation: review replies and brand mentions

This skill helps a small business answer its reviews well and notice what people say about it. You (the agent) write drafts. The user reads them, changes what they want, and posts them. Do not post, send or publish anything yourself, even if you have a tool that could.

The rules on fake reviews quoted here are general information, not legal advice. Each rule links to its official source; the user should read the current page, and ask a lawyer about a specific case. The full list of sources, with the exact words this skill relies on, is in [references/rules-and-sources.md](references/rules-and-sources.md).

## Ground rules for every draft

1. **Facts come from the user.** Never invent details about an order, a visit, a person or a fix. If you need a fact, ask for it.
2. **Never argue.** A reply is read by many future customers, not only by the reviewer. Be calm, brief and polite, even when the review is unfair.
3. **Keep private details private.** Never put an order number, a diagnosis, an address, a phone number, a booking date or anything else that identifies the reviewer into a public reply. Google's review policy says: "Do not distribute or post personal information without consent." ([Google Maps content policy](https://support.google.com/contributionpolicy/answer/7400114))
4. **Promise only what the user allows.** Refunds, replacements, fixes and dates appear only if the reputation profile (step 1) allows them.
5. **No invented numbers.** Do not tell the user how many customers read reviews or how much a reply raises sales. If they ask, say you have no verified figure.
6. **No made-up reviews, ever.** See "Fair reviews" (step 7).

## Step 1: Ask first

Before the first draft, ask these questions in one message. Keep the answers as the **reputation profile** and reuse them; ask again only when something changes. If the user does not know an answer, write "not decided" and draft more cautiously.

1. **Business.** Name, what you sell, and the country or countries you sell in (the rules differ).
2. **Platforms.** Where do customers leave reviews (for example Google Business Profile, Yelp, Trustpilot, Facebook, an app store, a marketplace, an industry site)? Where do people talk about you (social networks, forums, community groups)?
3. **Voice.** Three words for how you sound. "I" or "we"? Which name signs the replies? Words you never use? Which languages do you reply in?
4. **What you may promise.** Refunds (yes, no, under what conditions)? Replacements or redoing the work? Fixes to the product, with or without a date? A callback? Who approves anything outside these rules?
5. **Private contact route.** A business email address or phone number that you publish, for taking a conversation out of public view. Use a business address, not a personal one.
6. **Confidential work.** Is your work covered by confidentiality (health, therapy, law, finance, childcare, or similar)? If yes, replies never confirm that the reviewer is or was a client.
7. **Escalation contact.** Who handles legal threats, safety issues and crises (step 6), and how do you reach them quickly?
8. **Reply time.** How soon can you realistically answer a review (same day, within two days, weekly)?

Reputation profile template:

```markdown
# Reputation profile (updated YYYY-MM-DD)
- Business: <name>, <what you sell>, <countries>
- Review platforms: <list>
- Where people talk: <list>
- Voice: <three words>; <"I" or "we">; signed <name>; never say <words>; languages <list>
- May promise: refunds <rule>; replacements <rule>; fixes <rule>; callbacks <rule>
- Needs approval from: <person> for anything else
- Private contact route: <business email or phone>
- Confidential work: <yes or no>
- Escalation contact: <name, role, how to reach>
- Reply time we can keep: <time>
```

## Step 2: Read the review before you write

For each review or mention the user shares:

1. **Check for escalation first.** If anything in step 6 applies, stop drafting a normal reply and follow step 6.
2. **Sort it:** positive, neutral (mixed or short), or negative.
3. **Separate facts from feelings.** What does the reviewer say happened? What do they feel? What do they want (an answer, a fix, a refund, to warn others)?
4. **Ask the user what is true.** For example: "Do you have a record of this order?" or "Was the delivery late on your side?" Do not guess.
5. **Spot personal data** in the review itself (a staff member's full name, a phone number). Never repeat it. If the review exposes someone's private details, tell the user they can report it to the platform.

## Step 3: Draft the reply

Google's own tips for replies are to be professional and polite, keep it short and simple, reply promptly, and avoid using the reply to offer deals or promotions ([Google Business Profile, tips](https://support.google.com/business/answer/3474122)). On Google, an approved reply "will be publicly posted under the customer's review" ([Google Business Profile, manage reviews](https://support.google.com/business/answer/3474050)), so write for every future reader.

Shape of every reply:
- Thank the person (every reply, including the angry ones).
- Mention one specific thing from their review, so it does not read like a form letter.
- For problems: acknowledge, say what you are doing (only what the profile allows), and offer the private contact route.
- Two to five sentences. No marketing, no discount codes, no links to sales pages.
- Sign with the name from the profile.

### Template A: positive review

```
Thank you, <first name or "for your review">. <One sentence about the specific thing they liked>. <Optional: one short line that is true and useful, e.g. what they can expect next time>. <Sign-off>
```

### Template B: neutral or mixed review

```
Thank you for taking the time to write this, <first name>. We're glad <the part that went well>. You're right that <the part that fell short, in plain words>; <what we are doing about it, only if true and allowed>. If you'd like to tell us more, you can reach us at <private contact route>. <Sign-off>
```

### Template C: negative review, fair complaint

```
<First name>, thank you for telling us, and I'm sorry <the experience, in their terms, without repeating private details>. That isn't the standard we aim for. <What we are doing: a fix, a check, a change, only if true and allowed>. Please contact us at <private contact route> so we can <make it right / look into your order>. <Sign-off>
```

### Template D: negative review, the facts are wrong

Correct one fact, calmly, once. Do not accuse, do not list evidence in public, do not reveal anything private.

```
Thank you for your feedback, <first name>. <One neutral sentence of correct fact, e.g. "Our opening hours on Sundays are 10 to 4.">. We'd still like to understand what happened, so please contact us at <private contact route>. <Sign-off>
```

### Template E: you believe the reviewer was never a customer

Do not call the review fake in public, and never accuse the reviewer of something you do not know to be true, or that you have not checked: the FTC's guidance on its review rule says it "prohibits making a false accusation about the reviewer if you know that the accusation is false" (part of a sentence), which continues "or make it with reckless disregard as to its truth or falsity." ([FTC Q&A](https://www.ftc.gov/business-guidance/resources/consumer-reviews-testimonials-rule-questions-answers)).

```
Thank you for your review. We can't find a record that matches what you describe, and we'd like to understand it. Please contact us at <private contact route>. <Sign-off>
```

Then tell the user how to report it through the platform's own tool. On Google: "If you believe that a review violates Google's content policies, you can flag it." ([Google Business Profile, manage reviews](https://support.google.com/business/answer/3474050))

### Confidential work (profile question 6)

If the business works under confidentiality, the reply must not confirm a relationship. Use a general reply such as:

```
Thank you for your feedback. We take every concern seriously, but to protect privacy we never discuss anyone's care or case in public. Please contact us at <private contact route>. <Sign-off>
```

### Never write in a reply
- Anything that blames, mocks, threatens or diagnoses the reviewer.
- Private details, even ones the reviewer posted themselves.
- An offer in exchange for changing or removing the review. Yelp says "you can't offer incentives for users to remove reviews" ([Yelp](https://biz.yelp.com/support-center/Reviews/Best_Practices/Don-t-Ask-for-Reviews/en-US)), and the FTC says "paying consumers to change or remove truthful negative reviews may violate the FTC Act" ([FTC Q&A](https://www.ftc.gov/business-guidance/resources/consumer-reviews-testimonials-rule-questions-answers)).
- Legal language ("defamation", "our lawyers"). If the user wants to say that, it is an escalation (step 6).
- Admissions of legal fault for injuries, damage or losses. Saying sorry for an experience is fine; deciding who is legally responsible is for the escalation contact.

### Output for each draft

```markdown
### Reply draft: <platform>, review of <date>
- Review (short summary, no personal data): <...>
- Type: positive | neutral | negative (fair) | negative (facts wrong) | possibly not a customer
- Draft reply:
  > <text>
- Facts to confirm before posting: <list, or "none">
- Promises in this reply: <list, checked against the profile, or "none">
- Escalation: no | yes, see note
- Posted by: the user, on <platform>
```

## Step 4: Set up brand-mention watching (free)

Use only free tools and each platform's own search and notifications. Do not scrape sites in ways their terms forbid, and do not create fake accounts to see private groups.

1. **Google Alerts.** Google's help page says: "You can get emails when new results for a topic show up in Google Search." ([Google Search Help, create an alert](https://support.google.com/websearch/answer/4815696)) The steps there: go to google.com/alerts, enter a topic, click "Show options" to choose how often, which types of sites, language and region, then "Create Alert". Suggest one alert each for:
   - the business name in quotes, e.g. `"Bluebell Bakery"`;
   - the name with the town, if the name is common;
   - each main product or service name;
   - common misspellings of the name;
   - the website domain, e.g. `"bluebell-bakery.example"`;
   - the owner's name, only if the owner is the public face of the business and agrees.
2. **Review platforms.** In each platform the user listed, check whether its business account can notify them of new reviews, and help them switch it on using the platform's own help page.
3. **Social networks and forums.** For each place the user listed, write down the search to run each week (the name, the misspellings, the product names). Use the platform's own search box and saved searches where it offers them.
4. **A watch log.** One row per mention. A spreadsheet or a CSV file is enough:

```csv
date_found,where,link,summary,sentiment,needs_reply,escalate,status
2026-01-12,Google review,<link>,Late delivery complaint,negative,yes,no,draft ready
```

Tell the user plainly that no free setup catches every mention: alerts miss some pages and private groups are invisible. The weekly routine covers the gaps that matter most.

## Step 5: The weekly routine

Agree one fixed slot each week with the user. Each week, in this order:

1. **Reviews.** Open each review platform and list every new review since last week.
2. **Mentions.** Read the alert emails and platform notifications; run the saved searches from step 4.
3. **Log.** Add each item to the watch log.
4. **Escalate** anything that matches step 6 first, before other replies.
5. **Draft** replies with step 3. The user approves and posts them.
6. **Spot patterns.** If the same complaint appears more than once, note it for whoever can fix the cause. Replies calm one reader; fixes stop the next review.
7. **Ask for reviews fairly** (step 7), the same way for every customer.
8. **Summarise** for the user:

```markdown
## Reputation week of YYYY-MM-DD
- New reviews: <count per platform, as counted in the log>
- Replies drafted: <n>; posted by the user: <n, as the user reports>
- Mentions logged: <n>; needing action: <list>
- Escalated: <items, or "none">
- Repeated themes: <theme, how often, suggested fix owner>
- Next week: <one or two actions>
```

Counts come from the log only. Never estimate them.

## Step 6: Escalation (a human decides)

Stop. Do not draft a normal public reply, and bring these straight to the escalation contact in the profile:

- **Legal:** a threat to sue, a lawyer's letter, a claim of defamation, contact from a regulator or the police, a demand for money to remove a review.
- **Safety:** an injury, an illness, an allergic reaction, a dangerous product, a threat of violence, any mention of self-harm.
- **Privacy and security:** a claim that personal data leaked or an account was hacked, or a review that exposes someone's private details.
- **Serious allegations:** discrimination, harassment, fraud, or an accusation against a named staff member.
- **Crisis signs:** a journalist asks for comment, many similar posts appear quickly, or a post spreads widely.
- **Anything the user cannot check** and that would hurt someone if it were wrong.

What you prepare for the human:
1. A short fact sheet: what was said, where, when, the link, and what is known and not known. No guesses about causes.
2. A reminder to keep evidence: screenshots with the date and link. Delete nothing.
3. If the human wants something public before they have the facts, at most a short holding reply for them to approve word for word:

```
Thank you for raising this. We take it seriously and are looking into it now. Please contact us at <private contact route> so we can follow up with you directly.
```

In a crisis, one person speaks for the business, every public word states only confirmed facts, and nobody speculates. For legal or safety matters, the human talks to a qualified professional before saying more.

## Step 7: Fair reviews (what this skill will not do)

If the user asks for any of the following, refuse that part, say why in one or two sentences with the source, and offer the fair alternative.

| The request | Why the skill refuses | The fair alternative |
|---|---|---|
| Write reviews for the business, including "AI reviews" for real or invented customers, or reviews posted by staff as if they were customers | The FTC's final rule bans fake reviews, naming "AI-generated fake reviews", and undisclosed reviews by company insiders ([FTC, final rule](https://www.ftc.gov/news-events/news/press-releases/2024/08/federal-trade-commission-announces-final-rule-banning-fake-reviews-testimonials)). In the UK, submitting or commissioning "a fake consumer review" is a banned practice ([DMCC Act 2024, Sch. 20 para 13](https://www.legislation.gov.uk/ukpga/2024/13/schedule/20); [CMA guidance](https://www.gov.uk/government/publications/unfair-commercial-practices-cma207/unfair-commercial-practices)). The EU's Your Europe portal says traders "are also prohibited from paying people to write fake reviews or make endorsements" ([Your Europe](https://europa.eu/youreurope/citizens/consumers/unfair-treatment/unfair-commercial-practices/index_en.htm)) | Ask real customers, the same way for all (template below) |
| Review gating: ask only happy customers, or send unhappy ones to a private form and happy ones to the review site | Google prohibits businesses that "selectively solicit positive reviews from customers" ([Google Maps content policy](https://support.google.com/contributionpolicy/answer/7400114)). The FTC's guide says: "Don't ask for reviews only from customers you think will leave positive ones." ([FTC guide](https://www.ftc.gov/business-guidance/resources/soliciting-paying-online-reviews-guide-marketers)) Trustpilot asks businesses to invite "everyone in the same way" ([Trustpilot](https://corporate.trustpilot.com/legal/for-businesses/guidelines-for-businesses)) | Invite every customer at the same point, with neutral wording |
| Offer a discount, gift, entry to a draw or payment for a review | Google prohibits incentives "in exchange for posting any review" ([Google Maps content policy](https://support.google.com/contributionpolicy/answer/7400114)). Yelp: "Don't offer freebies, discounts, or payment in exchange for reviews" ([Yelp](https://biz.yelp.com/support-center/Reviews/Best_Practices/Don-t-Ask-for-Reviews/en-US)). Trustpilot: "We don't allow incentivized reviews on Trustpilot." ([Trustpilot](https://corporate.trustpilot.com/legal/for-businesses/guidelines-for-businesses)). The FTC rule bans incentives "conditioned on the writing of consumer reviews expressing a particular sentiment" ([FTC, final rule](https://www.ftc.gov/news-events/news/press-releases/2024/08/federal-trade-commission-announces-final-rule-banning-fake-reviews-testimonials)) | Ask without any reward (this skill's default). Never on Google, Yelp or Trustpilot: they ban incentives for reviews. Elsewhere, only if that platform's current rules allow it: the same reward goes to everyone whatever they write, and the business makes sure every review makes the reward apparent. The FTC says: "But remember that failing to disclose incentives could be a violation of the FTC Act." ([FTC Q&A](https://www.ftc.gov/business-guidance/resources/consumer-reviews-testimonials-rule-questions-answers)). In the UK, submitting or commissioning "a consumer review that conceals the fact it has been incentivised" is a banned practice, and "“commissioning” includes incentivising by any means", so the duty sits with the business that offers the reward ([DMCC Act 2024, Sch. 20 para 13(1)(b), (5)(c), (5)(g)](https://www.legislation.gov.uk/ukpga/2024/13/schedule/20)). EU rules on incentivised reviews: UNVERIFIED, not checked by this skill ([rules and sources](references/rules-and-sources.md)) |
| Ask for reviews on Yelp | Yelp: "Don't ask anyone to review your business, be it customers, mailing list subscribers, friends, family, etc." ([Yelp](https://biz.yelp.com/support-center/Reviews/Best_Practices/Don-t-Ask-for-Reviews/en-US)) | Do not ask for Yelp reviews; reply well to the ones that come |
| Pressure a reviewer to change or delete a review (threats, legal threats without grounds, public accusations, offers) | The FTC rule covers "unfounded or groundless legal threats, physical threats, intimidation, or certain false public accusations" used to stop or remove negative reviews ([FTC, final rule](https://www.ftc.gov/news-events/news/press-releases/2024/08/federal-trade-commission-announces-final-rule-banning-fake-reviews-testimonials)) | Reply calmly (step 3), fix the problem privately, report reviews that truly break the platform's rules |
| Ask staff, friends or family for reviews without saying who they are | The FTC guide says not to ask staff or family and friends for reviews unless they disclose the connection ([FTC guide](https://www.ftc.gov/business-guidance/resources/soliciting-paying-online-reviews-guide-marketers)); Google bans content "based on a conflict of interest" | Leave reviews to customers |
| Write reviews of competitors, or pose as someone else | That is a fake review and impersonation | None. Compete on the work |

Say the reason plainly, for example: "I can't write reviews for your business. A review has to come from a real customer's own experience, and fake reviews are banned by the FTC, Google and other platforms. I can draft a review request you send to every customer instead."

Outside the US, UK and EU, tell the user their country has its own rules and that this skill does not list them; their national consumer-protection authority is the place to check.

### Fair review request template

Google allows businesses to "share a review request link or QR code" ([Google Business Profile, manage reviews](https://support.google.com/business/answer/3474050)). Send the same request to every customer at the same point (for example, a few days after delivery), whether you expect praise or criticism. Do not use this on Yelp.

```
Hi <first name>, thank you for choosing <business>. If you have a minute, we'd value an honest review of your experience, good or bad: <platform review link>. It helps other customers decide, and it helps us improve. <Sign-off>
```

No reward, no "if you were happy", no "if not, contact us first".

## Step 8: Final check before you hand over

Go through this list for every batch of drafts. Fix anything that fails before you show the drafts.

- [ ] Every fact in a reply was confirmed by the user, or is listed under "Facts to confirm".
- [ ] No private details (names beyond a first name the reviewer shows publicly, order numbers, health or case details, contact details of the reviewer).
- [ ] Confidential-work businesses: no reply confirms that the reviewer is a client.
- [ ] Every promise matches the reputation profile.
- [ ] No argument, sarcasm, blame or legal language; two to five sentences; signed as the profile says.
- [ ] No discount, offer or link to a sales page in a reply.
- [ ] Nothing offered in exchange for changing or removing a review.
- [ ] Every escalation trigger went to step 6, not to a normal reply.
- [ ] No fake review, gated request or banned incentive was drafted; any refusal gave the reason and a source.
- [ ] Counts in the weekly summary come from the watch log, not estimates.
- [ ] The user knows they post every reply themselves, and that the rules above are general information, not legal advice.
