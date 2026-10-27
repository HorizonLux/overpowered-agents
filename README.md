# Overpowered agents

Specialist agents and the skills they use, from [Get Overpowered](https://getoverpowered.ai/skills/). Browse them, read every file and copy a skill on [getoverpowered.ai/skills](https://getoverpowered.ai/skills/).

Every agent drafts. You approve, publish, send and pay. Read every file before you install it.

## Agents

### Marketing lead (`marketing-lead`)

A senior marketing role for one person or a small team. It sets your brand voice, plans campaigns, writes the posts and the launch email, briefs the pages Google should find, starts honest conversations with businesses that fit and answers your reviews. Every piece comes back as a draft for you to approve.

Skills: Branding (`branding`), Marketing (`marketing`), SEO (`seo`), Outreach (`outreach`), Reputation (`reputation`).

Planned, not written yet: Social calendar, Newsletter, Ads review, Results report, Landing page copy, Competitor watch.

### Product designer (`product-designer`)

A senior product design role. It maps how people move through your site or app, plans each page's layout and look, specifies every state of every screen and plans a test with five real people. It plans and reviews; you or your developer build.

Skills: Design (`design`), UI and UX (`ui-ux`).

Planned, not written yet: Accessibility audit, Onboarding flow, Design system starter, Test report.

### Sales and customer lead (`sales-lead`)

A sales and customer role for businesses that sell to other businesses or get reviewed online. It builds a lawful list of businesses that fit, writes short first emails and follow-ups with the rules for your region, and drafts calm replies to reviews with a weekly routine to keep up.

Skills: Outreach (`outreach`), Reputation (`reputation`).

Planned, not written yet: Proposal writer, Support replies, FAQ builder, Lost-deal review.

## Install

### Claude Code

```
/plugin marketplace add HorizonLux/overpowered-agents
/plugin install marketing-lead@getoverpowered
```

Swap `marketing-lead` for `product-designer` or `sales-lead`. Each plugin adds the agent and its skills.

### Codex

```
git clone https://github.com/HorizonLux/overpowered-agents
cp -r overpowered-agents/plugins/marketing-lead/skills/* ~/.agents/skills/
```

For the agent's role too, add the text of `plugins/<agent>/agents/<agent>.md` to your project's AGENTS.md.

### Other agent tools

```
npx skills add HorizonLux/overpowered-agents
```

It lists the skills; pick the ones you want.

### Claude web app

Turn on code execution, download a skill as a .zip from [getoverpowered.ai/skills](https://getoverpowered.ai/skills/), then upload it under Customize, Skills.

## Layout

```
.claude-plugin/marketplace.json     the marketplace (name: getoverpowered)
plugins/<agent>/.claude-plugin/     the plugin manifest
plugins/<agent>/agents/<agent>.md   the agent
plugins/<agent>/skills/<skill>/     SKILL.md and references/
```

A skill used by two agents is copied into both plugins, so each plugin installs on its own.

## Licence

MIT. Your AI tools' own plans and usage costs still apply.

Product names are used only to identify the tools they belong to and remain the property of their owners. Get Overpowered is an independent product and is not affiliated with, sponsored or endorsed by these companies.
