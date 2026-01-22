# AdventureWorks MCP Server

MCP server for AdventureWorksLT database built with **Azure Data API Builder 1.7+**. Connect your AI assistant directly to a SQL database - zero code required.

## 🧪 Try It Now

Test endpoint: `https://mcp.azure-api.net/adventureworks/mcp`

### Connect to Claude Desktop

Add to your Claude Desktop MCP settings:

```json
{
  "mcpServers": {
    "adventureworks": {
      "url": "https://mcp.azure-api.net/adventureworks/mcp"
    }
  }
}
```

## 🛠️ Available MCP Tools

The server exposes these database tables as MCP tools:

| Tool | Description |
|------|-------------|
| **Product** | Product catalog with pricing, colors, sizes |
| **ProductCategory** | Hierarchical product categories |
| **ProductModel** | Product model definitions |
| **Customer** | Customer information and contacts |
| **SalesOrderHeader** | Sales orders with dates and totals |
| **SalesOrderDetail** | Order line items with quantities and pricing |
| **Address** | Shipping and billing addresses |
| **CustomerAddress** | Customer-to-address mapping |
| **ProductDescription** | Multi-language product descriptions |

Each tool supports filtering, sorting, and relationship traversal through natural language queries.

## 💬 Example Queries

- "Show me the top 10 products by total sales revenue, including product name, total quantity   sold, and total revenue amount."
- "Analyze shipping patterns by showing the top 5 cities where orders are shipped, including the number of orders and total freight charges for each city."


## 🚀 Run Your Own

**Prerequisites:** Azure Data API Builder 1.7+, AdventureWorksLT database

```bash
# Install DAB CLI
dotnet tool install -g Microsoft.DataApiBuilder

# Set connection string
$env:MSSQL = "your-connection-string"

# Start server
dab start --config dab-config-mcp.json
```

The `dab-config-mcp.json` file contains the complete configuration - ready to use with any AdventureWorksLT database.

## 📚 Learn More

- [Azure Data API Builder](https://aka.ms/dab)
- [Model Context Protocol](https://modelcontextprotocol.io)

---

**Built with Azure Data API Builder 1.7+**
