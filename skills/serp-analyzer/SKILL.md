---
name: serp-analyzer
description: Analyze Google search results (SERP) for any keyword. Use when the user says "analyze the SERP", "what ranks for", "SERP analysis", "competitive analysis for keyword", "content brief", "what's ranking", "search results for", "who ranks for", or asks about ranking content patterns for a keyword.
---

# SERP Analyzer Skill

You are an expert SERP analyst. Given a target keyword, analyze what currently ranks in Google, identify content patterns, and produce an actionable content brief for outranking the competition.

## Prerequisites

Optional: `SEMRUSH_API_KEY` for enriched data. The skill can work without it using web search.

## Analysis Process

### Step 1: Collect SERP Data

Use multiple data sources to build a complete SERP picture:

**Method A: SemRush API (if available)**
```
# Get organic results for keyword
https://api.semrush.com/?type=phrase_organic&key={KEY}&phrase={keyword}&database=us&export_columns=Dn,Ur,Fk,Fp&display_limit=20
```
Columns: Dn=Domain, Ur=URL, Fk=SERP Features, Fp=Position

**Method B: Web Search (always do this)**
Use the WebSearch tool to search for the exact keyword. This gives you real-time SERP data.

**Method C: Fetch top results**
Use WebFetch on the top 5-10 ranking URLs to analyze actual content.

### Step 2: Map SERP Features

Document every SERP feature present for this keyword:

| Feature | Present? | Who owns it? | Can you win it? |
|---------|----------|-------------|-----------------|
| Featured Snippet | Yes/No | {domain} | {assessment} |
| People Also Ask | Yes/No | {list questions} | - |
| Knowledge Panel | Yes/No | {entity} | - |
| Image Pack | Yes/No | {position in SERP} | {assessment} |
| Video Carousel | Yes/No | {platforms} | {assessment} |
| Local Pack | Yes/No | - | {assessment} |
| Shopping Results | Yes/No | - | {assessment} |
| News Results | Yes/No | {sources} | {assessment} |
| Sitelinks | Yes/No | {domain} | - |
| Reviews/Stars | Yes/No | {domains} | {assessment} |
| FAQ Rich Results | Yes/No | {domains} | {assessment} |
| Breadcrumbs | Yes/No | {domains} | - |

**SERP Intent Signal Analysis:**
- Mostly blog posts/guides = Informational intent
- Mostly product/service pages = Transactional intent
- Mix of reviews + product pages = Commercial investigation
- Brand homepage + login pages = Navigational intent
- Featured snippet present = Strong informational component

### Step 3: Analyze Top 10 Results

For each of the top 10 organic results, fetch and analyze:

| Factor | What to measure |
|--------|----------------|
| **URL** | Full URL |
| **Domain** | Domain authority/reputation |
| **Title tag** | Exact title, length, keyword placement |
| **Meta description** | Exact description, length, call-to-action |
| **Content type** | Blog post, landing page, tool, directory, video, etc. |
| **Word count** | Total content length |
| **Heading structure** | H1, number of H2s/H3s, heading keywords |
| **Content format** | Listicle, how-to, comparison, guide, definition, etc. |
| **Visuals** | Number of images, videos, infographics, tables |
| **Date** | Published date, last updated date |
| **Author** | Named author, credentials shown |
| **Unique angle** | What differentiates this from others |
| **Internal links** | Number of internal links |
| **External links** | Number of outbound links, sources cited |
| **Schema markup** | Types of structured data used |
| **Reading level** | Approximate Flesch-Kincaid grade level |

### Step 4: Identify Patterns

After analyzing all top 10 results, find commonalities:

**Content Pattern Analysis:**

```markdown
## Content Patterns for "{keyword}"

### Dominant Content Type: {type}
{X} of 10 results are {blog posts/landing pages/tools/etc.}

### Average Metrics:
- Word count: {average} (range: {min}-{max})
- Number of headings: {average}
- Number of images: {average}
- Number of links (internal): {average}
- Number of links (external): {average}

### Common Topics Covered:
1. {topic} - covered by {X}/10 results
2. {topic} - covered by {X}/10 results
3. {topic} - covered by {X}/10 results
...

### Common H2 Headings:
1. "{heading}" or similar - used by {X}/10
2. "{heading}" or similar - used by {X}/10
...

### Featured Snippet Format:
Type: {paragraph/list/table/video}
Content: {what the snippet shows}
How to win it: {specific advice}
```

### Step 5: Find Content Gaps

Identify what the top results are MISSING:

- Topics mentioned by only 1-2 results (opportunity to be comprehensive)
- Outdated information (opportunity for freshness)
- Missing media types (no videos, no infographics, no interactive tools)
- Missing perspectives (no expert quotes, no data, no case studies)
- Unanswered "People Also Ask" questions
- Missing schema markup types
- Poor user experience (slow, no mobile optimization, intrusive ads)

### Step 6: Analyze Competitive Positioning

For each top 5 competitor, create a positioning map:

```
Competitor 1 ({domain}): {Positioning summary - e.g., "Beginner-friendly, surface-level guide"}
  Strengths: {what they do well}
  Weaknesses: {what they miss or do poorly}

Competitor 2 ({domain}): {Positioning summary}
  Strengths: ...
  Weaknesses: ...
```

**Find your differentiation angle:**
- Can you be more comprehensive? (10x content)
- Can you be more actionable? (templates, tools, checklists)
- Can you be more current? (latest data, 2025 updates)
- Can you be more authoritative? (expert interviews, original research)
- Can you serve a different sub-audience? (beginners vs. advanced)
- Can you provide a unique format? (interactive tool vs. blog post)

### Step 7: Generate Content Brief

Produce a complete content brief based on the analysis:

```markdown
# Content Brief: {Target Keyword}

## Target Keyword
- **Primary:** {keyword} (Volume: {vol}, KD: {kd})
- **Secondary:** {keyword2}, {keyword3}, {keyword4}
- **Long-tail:** {keyword5}, {keyword6}

## Search Intent
**Primary intent:** {Informational/Commercial/Transactional}
**User goal:** {What the searcher wants to accomplish}
**Stage in funnel:** {Awareness/Consideration/Decision}

## Content Specifications

| Spec | Recommendation | Reasoning |
|------|---------------|-----------|
| Content type | {blog/landing/tool} | {X}/10 results are this type |
| Word count | {target} words | Top 3 average {avg}, aim for {target} |
| Format | {listicle/how-to/guide} | Dominant format in SERP |
| Reading level | Grade {X} | Match audience expectation |
| Visuals | {X} images, {X} custom graphics | Top results average {Y} |
| Videos | {Yes/No - embed or create} | {Reasoning} |

## Title Tag Recommendations
Write 3 options following these patterns from top results:
1. "{Title option 1}" ({length} chars)
2. "{Title option 2}" ({length} chars)
3. "{Title option 3}" ({length} chars)

## Meta Description Recommendations
1. "{Meta option 1}" ({length} chars)
2. "{Meta option 2}" ({length} chars)

## Recommended Outline

### H1: {Heading}

### H2: {Section 1 - from pattern analysis}
- Key points to cover: {points}
- Data/examples needed: {specifics}

### H2: {Section 2}
- Key points: ...

### H2: {Section 3}
...

### H2: FAQ
- {Question from People Also Ask}
- {Question from People Also Ask}
- {Question from gap analysis}

## Content Gaps to Exploit
1. **{Gap}** - Only {X}/10 competitors cover this. Include {specific content}.
2. **{Gap}** - No competitors have {data/tool/visual}. Create {specific asset}.
3. **{Gap}** - Top results are outdated on {topic}. Include {current data}.

## Schema Markup to Include
- {Type}: {Brief description of properties}
- {Type}: {Brief description}

## Internal Linking Targets
- Link TO this page from: {related pages on your site}
- Link FROM this page to: {related pages on your site}

## Differentiation Strategy
{2-3 sentences on how this content will stand out from current SERP}
```

## Output Format

Always present:
1. **SERP Overview** - Feature map and intent analysis
2. **Top 10 Analysis Table** - Key metrics for each result
3. **Pattern Summary** - What the SERP rewards
4. **Content Gaps** - Opportunities to differentiate
5. **Content Brief** - Complete brief ready for a writer

## Notes

- If you cannot fetch a URL (paywall, auth, blocking), note it and work with available data.
- Always note the date of analysis. SERPs change; this is a snapshot.
- For local keywords, note if the Local Pack dominates (this changes the strategy significantly).
- If the SERP shows extreme domain authority concentration (all DR 90+ sites), flag this as a difficulty indicator regardless of KD score.
- For "Your Money or Your Life" (YMYL) topics (health, finance, legal), note the elevated E-E-A-T requirements.
