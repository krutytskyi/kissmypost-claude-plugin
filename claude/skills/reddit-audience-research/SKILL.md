---
name: reddit-audience-research
description: Research a Reddit audience with KissMyPost data. Use when the user asks who is on Reddit for a product, niche or topic, how big, active or fast-growing a subreddit is, who its members are (age, gender, countries, other interests), which communities share its audience, how two subreddits compare, or for Reddit-wide statistics. Works through the KissMyPost connector.
---

# Reddit audience research with KissMyPost

Answer with numbers from the KissMyPost tools, never from memory. If no KissMyPost tools are available in this conversation, say so and point the user to https://kissmypost.com/mcp to connect KissMyPost (in claude.ai it is listed in the Claude Directory). Do not invent subscriber counts, growth or demographics while it is missing.

## Steps

1. **Shortlist communities.** For a topic, product or niche, call `find_subreddits_by_topic` with one or two words (it matches names and descriptions). Use `search_subreddits` when the user gives part of a subreddit name, and `top_subreddits` for "biggest" or "fastest growing" questions, optionally with a topic.
2. **Size up the best 2-3.** Call `subreddit_overview` for each. Compare members, 12-month growth, monthly posts and active authors. An active mid-size community often fits better than a huge quiet one; say why you rank them the way you do.
3. **Who the people are.** `subreddit_audience` gives demographics, gender, age and the other subreddits its people spend time in.
4. **Neighbours.** `similar_subreddits` lists communities with similar topics and with a shared audience. Use it to widen a shortlist that is too small.
5. **Side by side.** For "A vs B" questions call `compare_subreddits` once with both sides instead of two overviews.
6. **Topic map.** `explore_topics` shows where a subject sits among Reddit topics and which subreddits lead that area.
7. **Reddit as a whole.** `reddit_statistics` gives the headline monthly figures (active people, posts and comments per day, who Redditors are). `search_research` finds KissMyPost studies on a subject.

## Answer rules

- Quote the figures the tools return together with the month they refer to, and keep each tool's report link so the user can check it.
- Label anything that did not come from a KissMyPost tool as your own knowledge, so sources stay apart.
- Some tools need a signed-in or paid KissMyPost account and answer with an access message otherwise. Tell the user plainly what could not be answered, continue with the other tools, and do not push an upgrade.
- There is a daily limit on distinct items. Ask only for the subreddits, topics and phrases the user needs; repeating a call with the same argument returns the same answer.
- The tools are read-only: nothing is posted, voted or sent on Reddit. NSFW subreddits are never returned.
