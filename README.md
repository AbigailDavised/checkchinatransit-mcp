

[![mcptry](https://mcptry.com/badge/com.checkchinatransit/mcp)](https://mcptry.com/servers/com.checkchinatransit/mcp)

[![Official Website](https://img.shields.io/badge/Website-checkchinatransit.com-blue)](https://checkchinatransit.com)
[![MCP Registry](https://img.shields.io/badge/MCP_Registry-com.checkchinatransit%2Fmcp-green)](https://www.mcptry.com/servers/com.checkchinatransit/mcp)
[![Glama Connector](https://img.shields.io/badge/Glama-Connector-purple)](https://glama.ai/mcp/connectors/com.checkchinatransit/mcp)

Verify China 240-hour (formerly 144h) visa-free transit eligibility, ports & third-country routes.

- **Official Workbench**: [https://checkchinatransit.com](https://checkchinatransit.com)
- **Remote MCP Endpoint**: `https://checkchinatransit.com/api/mcp` (`streamable-http`, read-only, no API key required)
- **Public OpenAPI 3.0**: [https://checkchinatransit.com/openapi.json](https://checkchinatransit.com/openapi.json)
- **LLM Context**: [https://checkchinatransit.com/llms.txt](https://checkchinatransit.com/llms.txt) · [https://checkchinatransit.com/llms-full.txt](https://checkchinatransit.com/llms-full.txt)

## Tools Provided (8 Read-Only Tools)

| Tool Name | Summary |
| :--- | :--- |
| `check_china_twov_nationality_eligibility` | Verify whether a passport nationality qualifies for China 240-hour (upgraded from 72/144-hour) Visa-Free Transit (TWOV) and 24-hour direct airside transit. |
| `validate_third_country_itinerary_rule` | Validate whether a flight routing (Origin Country/Region A -> Mainland China B -> Destination Country/Region C, including Hong Kong, Macau, or Taiwan) satisfies strict NIA TWOV third-region rules vs round-trip disqualification. |
| `calculate_transit_stay_deadline` | Calculate the exact legal departure deadline under China Immigration midnight-next-day counting rules (00:00 the day following arrival) for 240-hour / 144-hour transit stays. |
| `lookup_china_transit_port_zone` | Look up permitted stay regions and approved entry/exit airports, seaports, and rail ports for Beijing-Tianjin-Hebei, Shanghai-Jiangsu-Zhejiang, Guangdong, Chengdu, Chongqing, Xi’an, and 24 provinces. |
| `check_24hour_direct_transit_rules` | Check rules for the 24-hour visa-free transit policy available to almost all nationalities, including multi-stop domestic transfers within 24 hours and airport-specific exemptions. |
| `get_airline_checkin_boarding_checklist` | Generate the mandatory printed document checklist required at airline check-in desks and China Immigration Temporary Entry Permit counters to prevent erroneous denied boarding. |
| `lookup_china_visa_photo_specs` | Retrieve official Chinese Embassy COVA digital visa photo and physical print dimensions (33mm x 48mm, head height 28-33mm, pure white RGB 255,255,255 background). |
| `compare_twov_vs_unilateral_30day_visa_free` | Compare whether a traveler can use China’s 30-day unilateral visa-free entry (allows round-trip flights) vs 240-hour TWOV (requires third-country onward ticket). |

## Connect in 10 Seconds

### Claude Code
```bash
claude mcp add --transport http checkchinatransit https://checkchinatransit.com/api/mcp
```

### Cursor / Claude Desktop / Windsurf (`mcp.json`)
```json
{
  "mcpServers": {
    "checkchinatransit": {
      "type": "streamable-http",
      "url": "https://checkchinatransit.com/api/mcp"
    }
  }
}
```

### Agent Skill (`skills.sh`)
```bash
npx -y skills@latest add AbigailDavised/checkchinatransit-mcp -y
```

## License

MIT © [CheckChinaTransit](https://checkchinatransit.com)
