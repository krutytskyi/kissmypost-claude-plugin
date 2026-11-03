---
name: reddit-audience-research
description: Research a Reddit audience with KissMyPost data. Use when the user asks which subreddits fit a product or topic, how big or active a subreddit is, when to post there, which communities share its audience, what Reddit talks about around a topic, or how often a brand or phrase is mentioned on Reddit.
---

# Reddit audience research with KissMyPost

Use the KissMyPost tools for numbers. Do not guess subscriber counts, growth, posting times or mention counts from memory. If the KissMyPost tools are not connected, say so and ask the user to connect KissMyPost before answering with numbers.

1. **Find communities.** For a topic or product, call `find_subreddits_by_topic` (it matches names and descriptions; short topics of one or two words work best). Use `search_subreddits` when the user gives part of a subreddit name. For "biggest" or "fastest growing" questions, call `top_subreddits`, optionally with a topic.
2. **Size up a subreddit.** Call `subreddit_overview` for the 2-3 most relevant results. Compare members, 12-month growth and monthly posts and authors: an active mid-size community often fits better than a huge quiet one.
3. **Timing.** Call `best_time_to_post` before suggesting when to post. Times are in UTC; convert them to the user's time zone if you know it. If the tool says timing matters little there, say so instead of picking a slot.
4. **Related communities.** `similar_subreddits` lists communities with similar topics and with a shared audience.
5. **Topics.** `explore_topics` shows where a topic sits on the map of Reddit topics and which subreddits lead that area.
6. **Brands and phrases.** For a company website, call `brand_mentions` with its domain (for example "notion.so"). For any word or phrase, `search_reddit_mentions` gives monthly post and comment counts and the subreddits that mention it most.
7. **Posting rules.** When `subreddit_posting_rules` is available, use it to say what a subreddit allows and how often posts there are removed.
8. **General Reddit numbers.** `reddit_statistics` gives the headline monthly figures for all of Reddit.

Rules for the answer:
- Quote the numbers the tools return, with the month or period they refer to, and keep each tool's report link so the user can check the source.
- Some tools may be unavailable for the user's account, and there is a daily limit on distinct items. If a tool returns an error or says it is unavailable, tell the user plainly what could not be answered and continue with the other tools. Ask only for the items the user needs and do not repeat calls for the same item.
- The tools are read-only: they do not post, vote or contact anyone on Reddit, and they do not return the text of posts or the names of authors. Do not offer those actions.
- Never suggest posting the same message to many subreddits. Recommend reading each community's rules first.
