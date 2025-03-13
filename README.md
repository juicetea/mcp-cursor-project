# MCP Cursor Project

This project demonstrates the integration of Model Context Protocol (MCP) with Cursor IDE.

## Features

- GitHub MCP Server integration
- Custom MCP commands and tools
- Cursor IDE extensions

## Setup

1. Install dependencies:
```bash
npm install
```

2. Set up your GitHub Personal Access Token:
```bash
export GITHUB_PERSONAL_ACCESS_TOKEN=your_token_here
```

3. Start the MCP server:
```bash
npm start
```

## Configuration

The project uses the following configuration in `.cursor/mcp.json`:

```json
{
    "mcpServers": {
        "github": {
            "command": "npx",
            "args": [
                "-y",
                "cross-env",
                "GITHUB_PERSONAL_ACCESS_TOKEN=${your_token}",
                "npx",
                "-y",
                "@modelcontextprotocol/server-github"
            ]
        }
    }
}
```

## License

ISC