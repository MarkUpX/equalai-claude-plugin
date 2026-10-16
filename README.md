# EqualAI for Claude

[EqualAI](https://www.equalai.io) tracks how AI assistants such as ChatGPT, Perplexity, Gemini, Google AI Overviews and Claude talk about your brand. This plugin lets you ask Claude about that data in plain language, in claude.ai, Cowork and Claude Code.

## What's included

- **EqualAI connector**: the EqualAI MCP server at `https://app.equalai.io/api/mcp`. It gives Claude read-only tools for your visibility summary, prompt performance, competitor mentions, cited domains and pages, stored AI answers, and search over your prompts, competitors, reports, recommendations and citations.
- **get-started skill**: confirms which projects are connected, shows a first 30-day visibility snapshot and explains how to change or revoke access.
- **ai-visibility-report skill**: builds a report covering visibility by AI model, weakest prompts, competitors and most cited sources, using only the numbers EqualAI returns.

## Requirements

An EqualAI account with an active subscription and at least one project with tracked prompts. [Start a free trial](https://app.equalai.io/signup).

## Use it

1. Install the plugin, then connect the EqualAI connector from the plugin's **Connectors** tab. In Claude Code, install it with the line below, then run `/mcp` and authenticate.

   ```
   /plugin install equalai --marketplace MarkUpX/equalai-claude-plugin
   ```
2. Sign in to EqualAI, tick the projects Claude may read and approve read-only access.
3. Ask, for example:
   - "How visible is my brand in AI answers over the last 30 days?"
   - "Which of my prompts have the lowest mention rate, and who gets mentioned instead?"
   - "Write an AI visibility report for my project for the last 90 days."

## Data

The plugin itself runs no code and stores nothing. Claude talks only to the EqualAI server at `app.equalai.io`, over HTTPS with OAuth. Claude sends tool inputs such as a project id, a number of days, a prompt id or a search query. EqualAI returns data from the projects you approved: visibility metrics, prompt text, competitor names, cited domains and URLs, report and recommendation titles, and short excerpts of stored AI answers. The connection cannot create, change or delete anything in EqualAI, and EqualAI does not receive your conversations with Claude. EqualAI logs the tool name, client, outcome and duration of each call.

Revoke access at any time under [AI Assistant Access](https://app.equalai.io/mcp/access) in EqualAI.

- Setup guide and tool list: https://www.equalai.io/mcp/
- Privacy policy: https://www.equalai.io/privacy/
- Terms: https://www.equalai.io/terms/
- Support: https://www.equalai.io/support/ or team@equalai.io

## License

The plugin files in this repository are released under the [MIT License](LICENSE). Use of the EqualAI service is governed by the [EqualAI Terms](https://www.equalai.io/terms/).
