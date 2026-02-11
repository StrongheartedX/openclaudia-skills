# OpenClaudia is your marketing agent in the AGI era

I've been building something I want to share with this community — an open-source collection of 34 marketing skills that plug directly into coding agents like Claude Code and Codex.

It's called **OpenClaudia**, and the idea is simple: instead of paying for 5 different SaaS tools to handle SEO, email, content, and social, you run slash commands in your terminal and the AI agent does it end-to-end.

**What it can do right now:**

- `/seo-audit` — crawl your site, find issues, get a score and fixes
- `/write-blog` — generate a full SEO-optimized post with meta tags, sourcing images from Unsplash
- `/email-sequence` — create and actually send drip campaigns via Resend API
- `/keyword-research` — pull real data from SemRush, DataForSEO, SerpAPI
- `/competitor-analysis` — full breakdown of any competitor's SEO, ads, and content strategy
- `/social-content` — generate and post directly to Reddit, X, LinkedIn, Instagram via API
- `/brand-monitor` — track brand mentions and sentiment via Brand.dev

34 skills total across SEO, content writing, email, social media, ads, analytics, strategy, and growth.

**Why I built it:**

Most marketing tools are built for humans clicking through dashboards. But we're entering an era where AI agents can execute multi-step workflows autonomously. OpenClaudia gives these agents the playbooks they need — structured skills with real API integrations, not just prompt wrappers.

Everything runs locally in your terminal. Your content, API keys, and data never touch our servers. Fully open source under MIT.

**Get started:**

```
npx openclaudia install --all
```

Then open Claude Code and type `/write-blog "Why Your Product Beats the Competition"` — done.

GitHub: https://github.com/OpenClaudia/openclaudia-skills
Website: https://openclaudia.com

Would love feedback from this community. What marketing workflows would you want an AI agent to handle? What skills are missing?
