# Days 25 & 26: MCP Client Integration

## 1. Detailed Theory

Building the Server is only half the battle. How does an AI Application actually *use* the server? By implementing an **MCP Client**.

### Client Responsibilities
1. **Connection:** Establish a connection to the server (via `stdio` for local scripts, or `SSE` for remote servers).
2. **Discovery:** Call `listTools()`, `listResources()`, and `listPrompts()` to find out what the server can do.
3. **Execution Routing:**
   - The user asks: "What are my top tasks today?"
   - The Client passes the User Prompt + The Discovered Tools to the LLM.
   - The LLM responds with a Function Call: `get_jira_tickets`.
   - The Client intercepts this, calls the MCP Server's `callTool("get_jira_tickets")`.
   - The Server returns the JSON of the tickets.
   - The Client passes the JSON back to the LLM.
   - The LLM generates the final response.

## 2. Recommended YouTube Tutorials

- [Using MCP in your AI Apps (Vercel)](https://www.youtube.com/watch?v=yP5Wz_oOktc)
- [How to Connect Claude Desktop to Local DBs via MCP](https://www.youtube.com/watch?v=1bEj1kQZkDU)

## 3. Real-Time Project GitHub Links

- [Claude Desktop Config](https://github.com/modelcontextprotocol/servers) - See how Claude Desktop is configured as an MCP client.
- [Vercel AI SDK MCP Example](https://github.com/vercel/ai/tree/main/examples/mcp) - Code demonstrating how to hook up an MCP client to a React frontend using the Vercel AI SDK.
