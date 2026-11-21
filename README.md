# Lomen MCP server

Ask your AI assistant about your website traffic.

We make [Lomen](https://lomenanalytics.com/?utm_source=github&utm_medium=directory&utm_campaign=mcp-directories), website analytics with a tracking script that sets no cookies. This repository holds the listing files for our remote MCP server. It contains no application code: the server is a hosted service, and its source is private.

## Connect

- Endpoint: `https://lomenanalytics.com/mcp`
- Transport: Streamable HTTP
- Auth: OAuth 2.1 through Supabase Auth, with dynamic client registration. A request without a token returns 401 with `resource_metadata` pointing to `https://lomenanalytics.com/.well-known/oauth-protected-resource`.

Add the endpoint as a remote MCP server (a custom connector) in your MCP client, then sign in with your Lomen account when the OAuth window opens. You need a Lomen account with our script on your site.

```json
{ "mcpServers": { "lomen": { "url": "https://lomenanalytics.com/mcp" } } }
```

## Tools

All five tools are read-only. None of them can change a setting, add or remove a site, or touch revenue connections.

| Tool | What it returns |
|---|---|
| `list_sites` | The websites tracked in your Lomen account |
| `get_website_overview` | The last 30 days: pageviews, unique visitors, visits, the daily series, top pages, entry and exit pages, sources, referring hosts, countries, devices, browsers, operating systems, screen sizes, UTM campaigns and how many visitors are on the site right now |
| `investigate_traffic_day` | One day compared with the same weekday in earlier weeks: which sources, landing pages and campaigns account for the change, and when the data cannot attribute it |
| `generate_ai_insight` | A short written summary of the last 30 days. Each one uses one of the account's AI insights |
| `get_subscription` | Your Lomen plan and billing interval |

## About Lomen

Lomen is in public beta and free during the beta. Paid plans are planned, and the pricing is not final. Lomen does not do custom events or funnels.

- Registry name: `io.github.MrBananKaka123/lomen` in the [official MCP Registry](https://registry.modelcontextprotocol.io/v0.1/servers?search=io.github.MrBananKaka123/lomen)
- Docs: https://lomenanalytics.com/docs?utm_source=github&utm_medium=directory&utm_campaign=mcp-directories#connections
- Contact: gustav@lomenanalytics.com
