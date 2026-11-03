---
name: reddit-brand-mentions
description: Measure how often Reddit mentions or links to a brand, product, competitor, website or phrase, month by month and by subreddit, with KissMyPost data. Use when the user asks how much Reddit talks about a company or product, compares brand buzz with competitors, monitors brand mentions on Reddit, or wants to read Reddit posts about a product. Works through the KissMyPost connector.
---

# Reddit brand mentions with KissMyPost

Use KissMyPost counts, never estimates from memory. If no KissMyPost tools are available, say so and point the user to https://kissmypost.com/mcp to connect KissMyPost.

## Pick the right measure

- **Links to a website** (for example "notion.so"): `brand_mentions` with the domain. It counts posts and comments that link to the site.
- **A name written in text** (a product, a person, a phrase such as "Cursor IDE"): `search_reddit_mentions`. It returns monthly post and comment counts for the last 24 months and the top subreddits. It needs a signed-in KissMyPost account.
- These are different questions: a brand can be named often but rarely linked. When the user says "mentions" without detail, use both and explain the difference in one line.

## Steps

1. Call the right tool for each brand or competitor the user names, one call per item.
2. **Comparisons:** put the brands in one table: total for the period, trend (rising, flat, falling) and the top 3 subreddits for each.
3. **Reading the posts:** when the user wants examples of what people say, `search_reddit_posts` returns up to 10 relevant posts with full text and links (paid accounts). Summarise them; quote only short pieces.
4. **Where to join the conversation:** the top subreddits from step 1 are a shortlist; `subreddit_overview` and `subreddit_posting_rules` (paid) tell the user whether those communities welcome brands.

## Answer rules

- Name the period and the month the data ends, and keep the report links.
- Ambiguous names (common words, people with the same name) inflate counts; say so when a name is ambiguous and suggest a more specific phrase.
- Read-only: nothing is posted or sent on Reddit.
