# Days 27 & 28: Building Real-World MCPs (GitHub & Jira)

## 1. Detailed Theory

Now that you know how the Client and Server communicate, it's time to build or implement production-ready servers.

### The GitHub MCP
To give an AI access to GitHub, you need an MCP server that wraps the GitHub API.
- **Tools needed:** `create_branch`, `create_pr`, `review_pr`, `search_code`.
- **Flow:** User asks AI to review a PR. AI uses `get_pr_diff` tool. Server fetches diff via GitHub API. AI reviews diff and uses `create_comment` tool.

### The Jira MCP
Enterprise AI requires project management access.
- **Tools needed:** `get_ticket`, `create_ticket`, `transition_issue`.
- **Flow:** User says "Move the login bug to in-progress". AI finds ticket via `search_ticket`, then calls `transition_issue`.

By running both the GitHub MCP and Jira MCP at the same time, your AI agent can read a Jira ticket and automatically open a GitHub PR to fix it.

## 2. Recommended YouTube Tutorials

- [Connecting AI to GitHub with MCP](https://www.youtube.com/watch?v=1bEj1kQZkDU)
- [Automating Jira with LLMs](https://www.youtube.com/watch?v=sPzc6hMg7So)

## 3. Real-Time Project GitHub Links

- [Official GitHub MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/github) - Review the source code for the official implementation.
- [Atlassian/Jira MCP Example](https://github.com/modelcontextprotocol/servers/tree/main/src/jira) - Review the source code for integrating with Jira.
