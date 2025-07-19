# VS Code MCP Install Link Creator

A simple, elegant single-page application that generates VS Code install buttons for Model Context Protocol (MCP) servers.

## Features

- **Two Configuration Modes:**
  - **Simple**: Enter raw JSON configuration directly
  - **Enhanced**: Form-based configuration with validation for stdio and http/sse types

- **MCP Configuration Support:**
  - **stdio**: Configure command, arguments, and environment variables
  - **http/sse**: Configure server URL and headers

- **Badge Customization:**
  - Custom badge text
  - Color picker for badge and logo colors
  - Multiple style options (flat, flat-square, plastic, for-the-badge, social)
  - Uses Shields.io for badge generation

- **Output Formats:**
  - Markdown format for README files
  - HTML format for web pages

- **Live Preview:**
  - Real-time preview of the generated badge
  - Copy-to-clipboard functionality

## Usage

1. Open `index.html` in your web browser
2. Fill in your MCP server details:
   - Enter your MCP server name
   - Choose between simple JSON input or enhanced form
   - Configure your server settings (stdio or http/sse)
3. Customize your badge appearance:
   - Set badge text
   - Choose colors
   - Select style
4. Choose output format (Markdown or HTML)
5. Copy the generated code

## Example

For a Microsoft Docs MCP server, the app generates:

**Markdown:**

```markdown
[![Install in VS Code](https://img.shields.io/badge/VS_Code-Install_Microsoft_Docs_MCP-0098FF?style=flat-square&logo=visualstudiocode&logoColor=white)](https://vscode.dev/redirect/mcp/install?name=microsoft.docs.mcp&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Flearn.microsoft.com%2Fapi%2Fmcp%22%7D)
```

**HTML:**

```html
<a href="https://vscode.dev/redirect/mcp/install?name=microsoft.docs.mcp&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Flearn.microsoft.com%2Fapi%2Fmcp%22%7D"><img src="https://img.shields.io/badge/VS_Code-Install_Microsoft_Docs_MCP-0098FF?style=flat-square&logo=visualstudiocode&logoColor=white" alt="Install in VS Code"></a>
```

## MCP Configuration Format

The app supports the official VS Code MCP configuration format:

### stdio Configuration

```json
{
  "type": "stdio",
  "command": "npx",
  "args": ["-y", "mcp-server-name"],
  "env": {
    "API_KEY": "${input:api-key}"
  }
}
```

### http/sse Configuration

```json
{
  "type": "http",
  "url": "https://api.example.com/mcp",
  "headers": {
    "Authorization": "Bearer ${input:token}"
  }
}
```

## Badge Customization

Powered by [Shields.io](https://shields.io), the app supports:

- **Colors**: Hex, RGB, named CSS colors
- **Styles**: flat, flat-square, plastic, for-the-badge, social
- **Logo**: VS Code logo with customizable color
- **Text**: Fully customizable badge text

## Technologies Used

- Pure HTML, CSS, and JavaScript (no dependencies)
- Responsive design
- Modern CSS Grid and Flexbox layouts
- Shields.io for badge generation
- VS Code MCP install URL format

## License

See LICENSE file for details.
App to create VS Code install buttons for MCPs
