# Career Site Jobs — MCP Server

Get every open job straight from companies' official career boards — Greenhouse, Lever, Ashby, Workable, SmartRecruiters, Recruitee, Personio and Breezy — from your AI agent or MCP client. Salary, remote flag, and full description as structured records, with an only-new mode for daily monitoring of fresh openings.

This repo is the MCP listing for the [Career Site Jobs](https://apify.com/magnova/career-site-jobs) Actor by Magnova on Apify. The server is hosted by Apify at the pinned endpoint below — there is nothing to install or run from this repository; you just point your MCP client at the URL.

## Tools

The pinned connection loads a focused tool set:

- **magnova--career-site-jobs** — Fetch open jobs from official career boards on Greenhouse, Lever, Ashby, Workable and more, with an optional only-new monitoring mode. Returns structured records: title, company, location, salary where listed, remote flag, full description, and apply URL.
- **fetch-actor-details** — Fetch the Actor's full input schema, pricing, and documentation, so an agent can check parameters and cost before running it.
- **get-actor-run / get-dataset-items** — Run and storage helpers, loaded automatically, used to fetch the results a run produced.

## Connect

Pinned endpoint (Streamable HTTP):

```
https://mcp.apify.com?tools=fetch-actor-details,magnova/career-site-jobs
```

On first connect, your client will ask you to sign in with your Apify account (OAuth). If your client cannot do OAuth, pass your Apify API token as an `Authorization: Bearer <YOUR_APIFY_TOKEN>` header instead.

### Cursor / VS Code / other Streamable HTTP clients

```json
{
  "mcpServers": {
    "career-site-jobs": {
      "url": "https://mcp.apify.com?tools=fetch-actor-details,magnova/career-site-jobs"
    }
  }
}
```

### Claude Desktop

Claude Desktop's config file only runs local commands, so use the `mcp-remote` bridge:

```json
{
  "mcpServers": {
    "career-site-jobs": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.apify.com?tools=fetch-actor-details,magnova/career-site-jobs"
      ]
    }
  }
}
```

The same pinned URL also lives in this repo's `.mcp.json`, and `server.json` is the listing for the Official MCP Registry, published as `io.github.memeanalyst/career-site-jobs-mcp`.

## Pricing

Pay per event, billed to your own Apify account: **$0.002 per job returned — $2 per 1,000 jobs**. No start fee, no subscription, and you are only charged for records actually delivered.

## Links

- Actor on Apify Store: https://apify.com/magnova/career-site-jobs
- MCP endpoint: https://mcp.apify.com?tools=fetch-actor-details,magnova/career-site-jobs

*Job records come from companies' official career boards.*
