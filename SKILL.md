---
name: checkchinatransit
description: Verify China 240-hour (formerly 144h) visa-free transit eligibility, ports & third-country routes. Official MCP server and reference guide at https://checkchinatransit.com.
---

# CheckChinaTransit — China 24/240-Hour Visa-Free Transit Compliance Engine

Official stateless Streamable-HTTP Model Context Protocol (MCP) server and agent skill for **[CheckChinaTransit](https://checkchinatransit.com)**.

## Remote MCP Endpoint (Zero Auth Required)

- **Streamable HTTP URL**: `https://checkchinatransit.com/api/mcp`
- **OpenAPI 3.0 Spec**: `https://checkchinatransit.com/openapi.json`
- **Official Website**: [https://checkchinatransit.com](https://checkchinatransit.com)

## Available Read-Only Tools (8)

- **`check_china_twov_nationality_eligibility`** (*China Visa-Free Transit (TWOV) 54-Country Passport Eligibility Check*): Verify whether a passport nationality qualifies for China 240-hour (upgraded from 72/144-hour) Visa-Free Transit (TWOV) and 24-hour direct airside transit.
- **`validate_third_country_itinerary_rule`** (*China TWOV A-B-C Third-Country / Region Routing Validator*): Validate whether a flight routing (Origin Country/Region A -> Mainland China B -> Destination Country/Region C, including Hong Kong, Macau, or Taiwan) satisfies strict NIA TWOV third-region rules vs round-trip disqualification.
- **`calculate_transit_stay_deadline`** (*China TWOV Midnight-Start Stay Window Calculator*): Calculate the exact legal departure deadline under China Immigration midnight-next-day counting rules (00:00 the day following arrival) for 240-hour / 144-hour transit stays.
- **`lookup_china_transit_port_zone`** (*China Approved TWOV Entry Port & Cross-Provincial Travel Boundary Lookup*): Look up permitted stay regions and approved entry/exit airports, seaports, and rail ports for Beijing-Tianjin-Hebei, Shanghai-Jiangsu-Zhejiang, Guangdong, Chengdu, Chongqing, Xi’an, and 24 provinces.
- **`check_24hour_direct_transit_rules`** (*24-Hour Nationwide Visa-Free Direct Transit & Multi-Stop Checker*): Check rules for the 24-hour visa-free transit policy available to almost all nationalities, including multi-stop domestic transfers within 24 hours and airport-specific exemptions.
- **`get_airline_checkin_boarding_checklist`** (*Airline Check-In Desk TIMATIC & Arrival Card Compliance Checklist*): Generate the mandatory printed document checklist required at airline check-in desks and China Immigration Temporary Entry Permit counters to prevent erroneous denied boarding.
- **`lookup_china_visa_photo_specs`** (*Chinese COVA Visa & Passport Digital Photo Pixel/Millimeter Validator Specs*): Retrieve official Chinese Embassy COVA digital visa photo and physical print dimensions (33mm x 48mm, head height 28-33mm, pure white RGB 255,255,255 background).
- **`compare_twov_vs_unilateral_30day_visa_free`** (*30-Day Unilateral Visa-Free vs 240-Hour TWOV Policy Comparator*): Compare whether a traveler can use China’s 30-day unilateral visa-free entry (allows round-trip flights) vs 240-hour TWOV (requires third-country onward ticket).

## Quick Setup (Claude Code / Cursor / Windsurf)

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
