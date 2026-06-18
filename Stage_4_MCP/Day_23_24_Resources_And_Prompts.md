# Days 23 & 24: Resources and Prompts in MCP

## 1. Detailed Theory

An MCP Server exposes three main primitives. We already covered **Tools** (actions the agent can take, like `create_file`). Now let's look at the other two.

### Resources
Resources are data that the AI agent can *read*, but usually not modify directly. They are exposed via URIs (like `file:///app/logs/error.log` or `postgres://db/schema`).
- **Why use them?** Instead of building a custom "read file" tool, the MCP server can just expose a directory of files as Resources. The MCP Client automatically knows how to fetch and read these URIs.
- **Example:** `getUsers`, `getCourses`.

### Prompts
Prompts are reusable prompt templates hosted on the server.
- **Why use them?** If you have a highly specialized prompt for reviewing Pull Requests, you don't want to hardcode it into the AI Client. You put it in the GitHub MCP Server. 
- **Example:** When the user clicks "Review PR" in Claude Desktop, the client fetches the `review_pr_template` prompt from the server, fills in the PR number, and sends it to the LLM.

## 2. Recommended YouTube Tutorials

- [Deep Dive into MCP Resources and Prompts](https://www.youtube.com/watch?v=0rsAFGg07Gg) *(Conceptually similar to tool extraction tutorials)*

## 3. Real-Time Project GitHub Links

- [MCP Typescript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - Look through the examples folder to see how `server.setRequestHandler(ListResourcesRequestSchema, ...)` is implemented.
