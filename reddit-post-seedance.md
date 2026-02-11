# How we use AI agents to handle all our marketing — 34 open-source skills you can install in one command

Most AI tools give you a chat box and call it a day. We wanted something that actually executes — not just suggests, but does the work end-to-end.

**OpenClaudia** is a set of 34 open-source marketing skills that plug into AI coding agents like Claude Code and Codex. You type a slash command in your terminal and the AI handles the rest: writing content, auditing your site, sending emails, posting to social media, pulling analytics data.

**What it looks like in practice:**

```
> /write-blog "How AI Is Changing Video Creation"
✓ 2,400-word article generated with meta tags and Unsplash images

> /seo-audit https://yoursite.com
✓ 47 pages analyzed — score: 82/100, 9 issues found

> /email-sequence --type product-launch
✓ 6-email drip sequence created and sent via Resend

> /social-content --platform reddit --topic "AI video tools"
✓ Posts generated for Reddit, X, and LinkedIn

> /competitor-analysis seedance.ai
✓ Full SEO, content, and positioning breakdown
```

**The full skill set covers:**

- SEO audits, keyword research, SERP analysis, backlink auditing
- Blog posts, landing pages, ad copy, email sequences
- Social media content creation and posting (Reddit, X, LinkedIn, Instagram)
- Google Analytics, Search Console, and Google Ads reporting
- Competitor analysis, pricing strategy, launch planning
- Brand monitoring, lead magnets, referral programs

All skills are powered by real APIs — SemRush, Ahrefs, SerpAPI, Resend, Unsplash, Reddit, Brand.dev, and Google services. But every API is optional; skills still work without them.

**Get started:**

```
npx openclaudia install --all
```

Open source under MIT. Runs locally. Your data stays on your machine.

GitHub: https://github.com/OpenClaudia/openclaudia-skills
Website: https://openclaudia.com

Would love to hear how others in this community are using AI agents for marketing. What's working?
