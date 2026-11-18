---
name: reddit-best-time-to-post
description: Find the best day and hour to post in a specific subreddit with KissMyPost data, converted to the user's time zone. Use when the user asks when to post on Reddit, the best time to post in r/<name>, what time a subreddit is most active, or how to schedule Reddit posts. Works through the KissMyPost connector.
---

# Best time to post on Reddit with KissMyPost

Timing differs a lot between subreddits, so answer per subreddit with KissMyPost data. If no KissMyPost tools are available, say so and point the user to https://kissmypost.com/mcp to connect KissMyPost. Do not give a generic "best time to post on Reddit" from memory as if it were measured.

## Steps

1. **Get the subreddit.** If the user only has a topic, first find 1-3 subreddits with `find_subreddits_by_topic` and ask which one they mean, or take the most active one and say so.
2. **Call `best_time_to_post`** for each subreddit (one call per subreddit). It returns the best day and hour in UTC, how much timing matters there, the time zones of the active audience and how much data the answer rests on.
3. **Convert to the user's time zone** if you know it or they tell you. Show both: "Tuesday 14:00 UTC (16:00 in Madrid)".
4. **Say how much timing matters.** If the tool says timing matters little in that subreddit, tell the user that the post itself matters more than the hour, instead of presenting a slot as important.
5. **For a draft post**, `where_to_post` (paid accounts) returns matching subreddits with timing for each in one call.

## Answer rules

- Quote the day, hour, month of the data and the report link from the tool.
- If the answer rests on little data, say it is a weak signal.
- Do not schedule or publish anything; the tools are read-only.
