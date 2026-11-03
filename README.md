# KissMyPost for Claude and Cursor

KissMyPost is a Reddit analytics and audience research tool, and this plugin brings it into Claude. Use it as a subreddit finder for a product or topic, to size up a community (members, growth, activity), to plan Reddit marketing with the best time to post and each subreddit's posting rules, to see which communities share the same people, and to track Reddit brand mentions month by month. Claude answers with real numbers instead of guesses, and every answer links to the full report on kissmypost.com.

## Install

From the Claude directory, add **KissMyPost** in claude.ai, Claude Desktop, Cowork or Claude Code. To install it straight from this repository in Claude Code:

```
/plugin install kissmypost --marketplace krutytskyi/kissmypost-claude-plugin
```

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

## Skills without the plugin

The skills are plain `SKILL.md` files (instructions only, no scripts) and also work on their own, next to the KissMyPost connector:

- **claude.ai and Claude Desktop:** zip a skill folder (for example `find-subreddits/` with its `SKILL.md` inside), then Customize > Skills > + > Create skill > Upload a skill.
- **Claude Code:** copy a folder from `skills/` to `~/.claude/skills/`.
- **Other agents:** `npx skills add krutytskyi/kissmypost-claude-plugin`.

Without the connector the skills cannot fetch numbers; they ask you to connect KissMyPost at https://kissmypost.com/mcp.

## Sign-in

The server needs a free KissMyPost account. In claude.ai, Claude Desktop and Cowork, connect the KissMyPost connector and sign in when Claude asks. In Claude Code, run `/mcp`, pick `plugin:kissmypost:kissmypost` and choose **Authenticate**; a browser window opens for sign-in.

Prefer an API key in Claude Code? Create one at https://kissmypost.com/mcp and add the server yourself instead of using the plugin's entry:

```bash
claude mcp add --transport http kissmypost https://kissmypost.com/api/mcp --header "Authorization: Bearer YOUR_KEY"
```

## Cursor

Install **KissMyPost** from the Cursor Marketplace, then open Settings → Tools & MCP and click **Connect** next to KissMyPost to sign in (a free account works). The Cursor files are `.cursor-plugin/plugin.json`, `mcp.json` (OAuth with a public client, no secret) and `rules/kissmypost.mdc`; the skills are shared with Claude.

Prefer an API key? Use **Add to Cursor** at https://kissmypost.com/mcp instead.

Try: "How big is r/SaaS and is it growing?", "When should I post in r/startups?", "Where on Reddit do people talk about notion.so?"

## What it sends and where

The plugin talks to one destination only: `https://kissmypost.com/api/mcp`. When Claude calls a tool, it sends the tool name and its arguments, such as a subreddit name, a topic, a brand domain or a search phrase, plus your sign-in token. The plugin has no hooks, scripts or local commands, and it does not read your files, chat history or environment. The tools never post, vote or message anyone on Reddit.

## Privacy and support

- Privacy policy: https://kissmypost.com/privacy (see "ChatGPT and other AI assistants (MCP)" for what the server logs and for how long).
- Terms: https://kissmypost.com/terms
- Support: https://kissmypost.com/contact
