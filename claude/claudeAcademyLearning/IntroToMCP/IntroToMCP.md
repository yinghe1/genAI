This one contains notes to the course: Introduction to model context Protocol https://anthropic.skilljar.com/introduction-to-model-context-protocol

- MCP main client server chart
![MCP main client server chart](img/MCPMainChart.png)

- MCP Git ToolList
![MCPGitToolList](img/MCPGitToolList.png)

- MCP To use Git tool sequence digram
![MCPSequenceDiagram](img/MCPSequenceDiagram.png)

- MCP to expose resources
![MCPResource](img/MCPResource.png)

- MCP direct vs templated resources
![DirectAndTemplatedResource](img/DirectAndTemplatedResource.png)

- MCP tools, resources, prompts who controls what
![MCPReviewToolResourcesPrompt](img/MCPReviewToolResourcesPrompt.png)

More notes:

Introduction to Model Context Protocol - MCP python sdk is useful to create mcp tools
Follow README.md of downloaded project
uv run main.py
mcp dev mcp_server.py to run the inspector
MCP review the last video is very important to explain when to use tool, resources and prompt for design purpose.

Other good resources:
- https://modelcontextprotocol.io/specification/2025-06-18/basic
- https://gofastmcp.com/tutorials/mcp this one has basic decorators and other useful info

```
@mcp.tool
@mcp.resource
@mcp.prompt
```

