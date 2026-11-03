# KissMyPost for Claude

KissMyPost answers questions about Reddit audiences with real numbers instead of guesses. Ask Claude which subreddits fit a product or topic, how big a community is and how fast it grows, when its members are active, which communities share the same people, what Reddit talks about around a topic, or how often a brand or phrase comes up month by month. Every answer links to the full report on kissmypost.com.

## Install

From the Claude directory, add **KissMyPost** in claude.ai, Claude Desktop, Cowork or Claude Code. To install it straight from this repository in Claude Code:

```
/plugin install kissmypost --marketplace krutytskyi/kissmypost-claude-plugin
```

## What is inside

- **MCP server** `kissmypost` at `https://kissmypost.com/api/mcp` (remote, read-only tools). Nothing runs on your machine.
- **Skill** `reddit-audience-research`: tells Claude which KissMyPost tool to call for each kind of question and how to present the numbers.

## Sign-in

The server needs a free KissMyPost account. In claude.ai, Claude Desktop and Cowork, connect the KissMyPost connector and sign in when Claude asks. In Claude Code, run `/mcp`, pick `plugin:kissmypost:kissmypost` and choose **Authenticate**; a browser window opens for sign-in.

Prefer an API key in Claude Code? Create one at https://kissmypost.com/mcp and add the server yourself instead of using the plugin's entry:

```bash
claude mcp add --transport http kissmypost https://kissmypost.com/api/mcp --header "Authorization: Bearer YOUR_KEY"
```

## What it sends and where

The plugin talks to one destination only: `https://kissmypost.com/api/mcp`. When Claude calls a tool, it sends the tool name and its arguments, such as a subreddit name, a topic, a brand domain or a search phrase, plus your sign-in token. The plugin has no hooks, scripts or local commands, and it does not read your files, chat history or environment. The tools never post, vote or message anyone on Reddit.

## Privacy and support

- Privacy policy: https://kissmypost.com/privacy (see "ChatGPT and other AI assistants (MCP)" for what the server logs and for how long).
- Terms: https://kissmypost.com/terms
- Support: https://kissmypost.com/contact
