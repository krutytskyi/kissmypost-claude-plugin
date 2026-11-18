---
name: find-subreddits
description: Find the right subreddits for a product, niche, topic or post idea with KissMyPost data. Use when the user asks which subreddits to post in, where their audience or customers are on Reddit, for subreddits like a given one, or for a list of communities about a topic, and wants them ranked by size, growth and activity. Works through the KissMyPost connector.
---

# Find subreddits with KissMyPost

Rank communities with KissMyPost numbers, not from memory. If no KissMyPost tools are available, say so and point the user to https://kissmypost.com/mcp to connect KissMyPost. Without it, you may name subreddits you know, but label them as unverified and give no figures.

## Steps

1. **Turn the request into short topics.** A product such as "a habit tracker for students" becomes topics like "productivity", "studying", "habits". One or two words per call work best.
2. **Collect candidates.**
   - `find_subreddits_by_topic` for each topic.
   - `search_subreddits` when the user names part of a subreddit.
   - `similar_subreddits` when the user gives a subreddit they already like ("subreddits like r/SaaS").
   - `top_subreddits` with a topic for "biggest" or "fastest growing".
3. **Check the top 3-5.** `subreddit_overview` for members, 12-month growth and monthly posts and authors. Drop communities that are large but nearly inactive, and say so.
4. **If the user has a concrete post or draft**, call `where_to_post` with it: it returns matching subreddits with timing per subreddit and seasonality in one call. It needs a paid KissMyPost account; if it is not available, continue with steps 2-3.
5. **Before recommending a community for promotion**, call `subreddit_posting_rules` when it is available to say what is allowed and how often posts are removed there.

## Answer format

- A short ranked list: subreddit, members, 12-month growth, monthly posts, and one line on why it fits. Include the month of the data and the report links.
- Separate "post here" from "read first": communities with strict rules or high removal rates go in the second group.
- Never suggest posting the same message to many subreddits. Suggest reading each community and adapting the post to it.
