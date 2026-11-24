# CheckChinaTransit MCP for OpenClaw

CheckChinaTransit connects OpenClaw agents to deterministic calculators, decision advisors, and compatibility probes via a remote Streamable-HTTP MCP server.

- Website: https://checkchinatransit.com
- Remote MCP endpoint: https://checkchinatransit.com/api/mcp
- Source: https://github.com/AbigailDavised/checkchinatransit-mcp

The bundle declares a `streamable-http` MCP connection. After enabling it in OpenClaw, verify connectivity by invoking only the read-only `check_china_twov_nationality_eligibility` tool.
