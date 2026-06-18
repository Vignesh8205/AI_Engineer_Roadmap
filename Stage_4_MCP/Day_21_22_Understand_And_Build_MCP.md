# Days 21 & 22: Understand and Build MCP

## 1. Detailed Theory

**MCP (Model Context Protocol)** is an open standard introduced by Anthropic. It aims to solve the biggest problem in Agent Engineering: **Tool Fragmentation**.

### The Problem Before MCP
If you build an AI app and want it to talk to GitHub, you have to write a custom GitHub integration. If someone else builds an AI app, they write their own GitHub integration. Every AI app has to reinvent the wheel.

### The MCP Solution
MCP creates a standard client-server architecture for tools.

1. **MCP Server:** A lightweight server you run locally or remotely. It exposes Tools, Resources, and Prompts in a standardized JSON-RPC format. (e.g., A "GitHub MCP Server" exposes `get_pr`, `create_issue`).
2. **MCP Client:** The AI Application (like Claude Desktop, or your custom agent). The client connects to the server and says, "What tools do you have?" 
3. **The Flow:** The AI Client automatically registers the tools provided by the Server. When the LLM decides to use a tool, the Client forwards the request to the Server, the Server executes it, and sends the result back.

**Day 22: Building your first server**
To build a server, you use the official MCP SDKs (TypeScript or Python). You define tools just like you did in Day 16, but wrap them in the MCP server initialization.

## 2. Recommended YouTube Tutorials

- [Introducing the Model Context Protocol (Anthropic Official)](https://www.youtube.com/watch?v=yP5Wz_oOktc)
- [How to Build an MCP Server in TypeScript (Fireship)](https://www.youtube.com/watch?v=1bEj1kQZkDU)

## 3. Real-Time Project GitHub Links

- [Model Context Protocol Specification](https://github.com/modelcontextprotocol/specification) - The official spec.
- [MCP Servers Reference](https://github.com/modelcontextprotocol/servers) - The official repository of reference servers (SQLite, GitHub, Google Drive).
