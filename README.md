# OpenClaudia Skills

Open-source marketing skills for [Claude Code](https://docs.anthropic.com/en/docs/claude-code). The tool for marketers, like Claude Code is for programmers.

**Website:** [openclaudia.com](https://openclaudia.com)

## Quick Install

```bash
# Install all skills
npx skills add OpenClaudia/openclaudia-skills

# Install a specific skill
npx skills add OpenClaudia/openclaudia-skills --skill seo-audit
```

Or manually copy any skill directory into `~/.claude/skills/` (personal) or `.claude/skills/` (project).

## Skills

### SEO & Site Audit
| Skill | Description |
|-------|-------------|
| `seo-audit` | Full technical + on-page SEO audit with actionable fixes |
| `keyword-research` | Keyword research using SemRush API |
| `serp-analyzer` | Analyze SERP results and ranking factors |
| `backlink-audit` | Audit backlink profile and find opportunities |
| `schema-markup` | Generate and validate Schema.org structured data |
| `programmatic-seo` | Create SEO-optimized pages at scale |

### Content Writing
| Skill | Description |
|-------|-------------|
| `write-blog` | Generate SEO-optimized blog posts |
| `write-landing` | Create high-converting landing page copy |
| `copywriting` | Marketing copy for any page type |
| `copy-editing` | Line-by-line copy polish and improvement |
| `content-strategy` | Build content calendars and topic clusters |

### Email Marketing
| Skill | Description |
|-------|-------------|
| `email-sequence` | Create drip campaigns and nurture sequences |
| `email-subject-lines` | Generate and A/B test email subject lines |

### Social Media
| Skill | Description |
|-------|-------------|
| `social-content` | Create posts for Twitter/X, LinkedIn, Instagram |
| `thread-writer` | Write viral Twitter/X threads |
| `content-calendar` | Plan and schedule social media content |

### Ads & Conversion
| Skill | Description |
|-------|-------------|
| `google-ads` | Write Google Ads copy and campaigns |
| `facebook-ads` | Create Facebook/Meta ad campaigns |
| `page-cro` | Landing page conversion rate optimization |
| `ab-test-setup` | Design and implement A/B tests |

### Analytics & Research (API-Powered)
| Skill | Description | API Required |
|-------|-------------|--------------|
| `semrush-research` | SEO & competitive intelligence via SemRush | `SEMRUSH_API_KEY` |
| `brand-monitor` | Brand monitoring via Brand.dev | `BRANDDEV_API_KEY` |
| `google-analytics` | Pull GA4 reports and insights | Google OAuth |
| `search-console` | Google Search Console data & analysis | Google OAuth |
| `google-ads-report` | Google Ads performance reporting | Google OAuth |

### Strategy & Planning
| Skill | Description |
|-------|-------------|
| `marketing-ideas` | 139 proven marketing ideas by category |
| `marketing-psychology` | 70+ psychological principles for marketing |
| `competitor-analysis` | Full competitor strategy breakdown |
| `pricing-strategy` | Pricing page and strategy optimization |
| `launch-strategy` | Product launch planning and execution |
| `icp-builder` | Define ideal customer profiles |

### Growth & Automation
| Skill | Description |
|-------|-------------|
| `referral-program` | Design referral and viral loops |
| `lead-magnet` | Create lead magnets and gated content |
| `signup-flow-cro` | Optimize signup conversion funnels |
| `onboarding-cro` | Improve user onboarding flows |

## API Configuration

Some skills integrate with external APIs for live data. Set these in your `.env` or `~/.claude/.env.global`:

```bash
# Email sending (email-sequence, email-subject-lines)
RESEND_API_KEY=your_key_here

# SemRush (keyword-research, semrush-research, backlink-audit, competitor-analysis)
SEMRUSH_API_KEY=your_key_here

# Ahrefs (backlink-audit — alternative to SemRush)
AHREFS_API_KEY=your_key_here

# SerpAPI (serp-analyzer, keyword-research, competitor-analysis)
SERPAPI_API_KEY=your_key_here

# DataForSEO (serp-analyzer, keyword-research)
DATAFORSEO_LOGIN=your_login
DATAFORSEO_PASSWORD=your_password

# Brand.dev (brand-monitor)
BRANDDEV_API_KEY=your_key_here

# Google OAuth (google-analytics, search-console, google-ads-report)
GOOGLE_CLIENT_ID=your_client_id
GOOGLE_CLIENT_SECRET=your_client_secret

# Unsplash (write-blog, social-content — featured images)
UNSPLASH_CLIENT_ID=your_access_key

# Reddit (social-content — trending topics)
REDDIT_CLIENT_ID=your_client_id
REDDIT_CLIENT_SECRET=your_client_secret

# ScrapingBee (competitor-analysis — scraping protected pages)
SCRAPINGBEE_API_KEY=your_key_here
```

All API keys are optional. Skills work without them but provide richer data when keys are available. Each skill tells you which key is needed when invoked.

## Contributing

1. Fork this repository
2. Create a new skill directory under `skills/`
3. Add a `SKILL.md` with YAML frontmatter and instructions
4. Submit a pull request

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full guide.

## License

MIT - see [LICENSE](LICENSE)

## Created by

[Quanlai Li](https://quanl.ai) and the OpenClaudia community.
