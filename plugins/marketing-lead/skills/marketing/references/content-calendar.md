# Content calendar: columns, rhythm and review

Read this when you build a content calendar (Step 4 of `SKILL.md`).

## What a calendar is for

A calendar answers "what goes out, where, on which day, and has the owner approved it?" It is not a strategy: who the content is for and what it should achieve come from the campaign plan. If there is no plan, ask the five starred questions in `SKILL.md` first.

## The columns

Each column answers a question the user will actually ask. Do not add more unless the user asks.

| Column | What goes in it | Why |
|---|---|---|
| date | The day it goes out | The schedule itself |
| channel | One channel per row | The same topic on two channels is two rows, each written for its channel |
| topic | A few words | To spot repeats and gaps |
| campaign | The campaign plan it serves | A row with no campaign must justify itself |
| format | Post, image, short video, email, article | Lets the user batch similar work |
| drafted_by | "me" or "agent" | Shows what needs a careful read |
| approved_by | Only the user's name | Nothing goes out while this is empty |
| approved_on | The date of approval | Draft and approval on different days catch more mistakes |
| link_tagged | The destination with `utm_source`, `utm_medium`, `utm_campaign` | So the user can see which row brought visitors |
| disclosure | "no", or "yes:" plus the exact wording | So a paid, gifted or personal link never slips through |
| status | idea, drafted, approved, published, retired | The calendar at a glance |
| notes | Anything else | Kept short |

The agent may fill `drafted_by` and every column before it. Only the user fills `approved_by` and `approved_on`. If asked to fill them, refuse and explain that approval is the user's step.

## Example rows (placeholders)

```
date,channel,topic,campaign,format,drafted_by,approved_by,approved_on,link_tagged,disclosure,status,notes
[2027-03-02],[community group],[why a spring service saves a ruined commute],[spring-tune-up],post,agent,,,[https://example.com/book?utm_source=community&utm_medium=social&utm_campaign=spring-tune-up],no,drafted,
[2027-03-04],[email],[tune-up checklist and price],[spring-tune-up],email,agent,,,[https://example.com/book?utm_source=newsletter&utm_medium=email&utm_campaign=spring-tune-up],no,drafted,opted-in past customers only
[2027-03-31],[calendar],[keep, fix or retire pass],[all],review,me,,,,no,idea,monthly row
```

These rows are made up to show the format. Use `example.com` until the user gives the real address.

## A rhythm one person can keep

| When | What happens | Columns touched |
|---|---|---|
| One planning session a week | Draft next week's rows | date to drafted_by, link_tagged, disclosure |
| The next day | The user reads each draft fresh, then approves or fixes | approved_by, approved_on, status |
| On each date | The user publishes the approved row | status → published |
| A few minutes a day | The user answers replies and comments personally | none |
| One short slot a week | Look at what the tagged links brought | notes |

Two rules keep the rhythm alive:
- **Plan for the busiest week.** Use the number of pieces the user said they can keep up when work is heavy.
- **Separate drafting from approving.** Even alone, a gap of a day is where unprovable claims get caught.

## The monthly keep, fix or retire pass

Add a recurring row once a month. For everything already published:
- **Keep** if it is still true, still useful, and its link still works.
- **Fix** if a fact, price, link or screenshot changed. Change the "updated" date only after a real change.
- **Retire** if it is no longer true or belongs to a campaign that has ended and would mislead a new reader.

## People-first questions before approval

Google publishes questions for site owners to judge their own content (https://developers.google.com/search/docs/fundamentals/creating-helpful-content, last updated 2026-10-05, checked 2026-10-23). Two of them fit a calendar row well:
- "After reading your content, will someone leave feeling they've learned enough about a topic to help achieve their goal?"
- "Is the use of automation, including AI-generation, self-evident to visitors through disclosures or in other ways?"

Turn them into three checks for every row:
1. Who is this for, and what can they do after reading it?
2. Would the user publish it if search engines did not exist?
3. Would a reader ask how it was made? If an agent drafted it and the answer is yes, say so in the post.

## Volume is not a strategy

Do not fill a calendar with many near-identical pieces to cover more search terms. Google's spam policies describe scaled content abuse as "when many pages are generated for the primary purpose of manipulating search rankings" (https://developers.google.com/search/docs/essentials/spam-policies, last updated 2026-08-28, checked 2026-10-23). If the user asks for that, say no and propose fewer, more useful pieces.
