---
name: reddit-marketing-plan
description: Plan how to promote a product, launch or content on Reddit without getting removed, using KissMyPost data on subreddits, audiences, posting rules, removal rates, timing and threads worth replying to. Use when the user asks for a Reddit marketing strategy, how to launch or get first customers on Reddit, how to promote on Reddit without being banned, or which threads to reply to. Works through the KissMyPost connector.
---

# Reddit marketing plan with KissMyPost

Build the plan on KissMyPost numbers. If no KissMyPost tools are available, say so and point the user to https://kissmypost.com/mcp to connect KissMyPost; general advice without data must be labelled as such.

## Steps

1. **Understand the product** in one sentence and who buys it. Ask once if it is unclear.
2. **Find communities:** `find_subreddits_by_topic` for 2-4 short topics, then `subreddit_overview` and `subreddit_audience` for the best 3-5. Prefer active communities where the product's buyers are, not the biggest ones.
3. **Check what is allowed:** `subreddit_posting_rules` (paid accounts) for each shortlisted subreddit: allowed post types, karma or account-age gates and how often posts are removed. Communities that remove most promotional posts become "reply only".
4. **Pick the format per community:**
   - a useful post (a lesson, data, a story) where self-posts survive;
   - replies to existing threads where promotion is removed. `reply_radar` (paid) returns fresh threads worth replying to and replies that did well on similar threads.
5. **If the user has a draft**, `where_to_post` (paid) returns matching subreddits with timing and seasonality for it.
6. **Timing:** `best_time_to_post` for each subreddit you recommend posting in, converted to the user's time zone.

## Plan format

A table with one row per subreddit: why it fits, members and activity, what is allowed, format (post or replies), best time, and the report link. Then 3-5 next steps for the first two weeks.

## Rules

- Never suggest posting the same message to many subreddits, using several accounts, or asking for votes. Recommend that the user takes part in each community before promoting.
- Disclose affiliation: tell the user to say they built the product when they mention it.
- Quote figures with their month and report link. The tools are read-only and never post for the user.
