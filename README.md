# Example MCP-Server

## Usage

In your mcp.json file in vscode, under `.vscode/mcp.json`, add the following configuration:

### MacOS / Linux

```json
{
    "inputs": [
        {
            "type": "promptString",
            "id": "example-token",
            "description": "The token for the MCP server",
            "password": true
        }
    ],
    "mcpServers": {
        "example-mcp-server": {
            "type": "stdio",
            "command": "npx",
            "args": ["-y", "github:Username/example-mcp-server"],
            "env": {
                "EXAMPLE_TOKEN": "${input:example-token}"
            }
        }
    }
}
```

### Windows

```json
{
    "mcpServers": {
        "example-mcp-server": {
            "command": "cmd",
            "args": ["/c", "npx", "-y", "github:Username/example-mcp-server"],
            "env": {
                "EXAMPLE_TOKEN": "${input:example-token}"
            }
        }
    }
}
```
