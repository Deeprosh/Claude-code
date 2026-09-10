# Model Context Protocol  
Using MCP we will allow LLM,to access the internal or the external tools which LLM's alone cant do it alone.  
Just install the MCP server client in the calude.Instead of installing all the different API's for different tool we can just use MCP server to interact with the claude.  
~~~
claude mcp add --transport stdio postgres -- npx -y @modelcontextprotocol/server-postgres "postgresql://localhost/mydb"
~~~

~~~
claude mcp add --transport http github https://api.githubcopilot.com/mcp/
~~~
