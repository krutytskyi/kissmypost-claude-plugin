# KissMyPost for Claude

KissMyPost is a Reddit analytics and audience research tool, and this plugin brings it into Claude. Use it as a subreddit finder for a product or topic, to size up a community (members, growth, activity), to plan Reddit marketing with the best time to post and each subreddit's posting rules, to see which communities share the same people, and to track Reddit brand mentions month by month. Claude answers with real numbers instead of guesses, and every answer links to the full report on kissmypost.com.

## Install

Add **KissMyPost** from the Claude plugin directory in claude.ai, Claude Desktop, Cowork or Claude Code.

## What is inside

- **MCP server** `kissmypost` at `https://kissmypost.com/api/mcp` (remote, read-only tools). Nothing runs on your machine.
- **Five skills** that tell Claude which KissMyPost tool to call for each kind of question and how to present the numbers:

| Skill | Use it for |
|---|---|
| `reddit-audience-research` | Subreddit size, growth, demographics, shared audiences, comparisons, Reddit-wide statistics |
| `find-subreddits` | Which subreddits to post in for a product, niche, topic or draft |
| `reddit-best-time-to-post` | Best day and hour to post in a subreddit, in your time zone |
| `reddit-brand-mentions` | How often Reddit names or links to a brand or competitor, by month and subreddit |
| `reddit-marketing-plan` | A Reddit launch or promotion plan built on posting rules, removal rates, timing and threads to reply to |

The skills are plain instruction files with no scripts.

## Sign-in

The server needs a free KissMyPost account. In claude.ai, Claude Desktop and Cowork, sign in when Claude asks to connect KissMyPost. In Claude Code, run `/mcp`, pick the KissMyPost server and choose **Authenticate**; a browser window opens for sign-in. Other ways to connect are described at https://kissmypost.com/mcp.

Try:
- "Which subreddits should I post my SaaS launch in?"
- "When is the best time to post in r/startups?"
- "Who is the audience of r/homelab and what else do they read?"
- "Where is my brand mentioned on Reddit this month?"

## What it sends and where

The plugin talks to one destination only: `https://kissmypost.com/api/mcp`. When Claude calls a tool, it sends the tool name and its arguments, such as a subreddit name, a topic, a brand domain or a search phrase, plus your sign-in token. The plugin has no hooks, scripts or local commands, and it does not read your files, chat history or environment. The tools never post, vote or message anyone on Reddit.

## Privacy and support

- Privacy policy: https://kissmypost.com/privacy
- Terms: https://kissmypost.com/terms
- Support: https://kissmypost.com/contact
