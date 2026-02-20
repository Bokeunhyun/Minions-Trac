# SKILL: TRAC Minion Clicker

## Overview
This skill enables Intercom agents to interact with the TRAC Minion Clicker game — a browser-based idle clicker that earns simulated TNK tokens.

## Agent Instructions

### What this app does
- Players click a Minion character to earn TNK (TRAC Network Token simulated points)
- Combo multipliers reward rapid clicking
- Upgrades increase per-click earnings and unlock auto-clickers
- Milestones track progress from 10 clicks to 100K TNK

### How agents should use this app

1. **Triggering a click event**
   - Send a `CLICK` signal over the Intercom sidechain to increment the TNK counter
   - Format: `{ action: "click", agentId: "<your_agent_id>" }`

2. **Reading game state**
   - Query current TNK balance: `{ action: "get_state", field: "tnk" }`
   - Query upgrade status: `{ action: "get_state", field: "upgrades" }`

3. **Purchasing upgrades**
   - Send: `{ action: "buy_upgrade", upgradeId: "<id>" }`
   - Valid IDs: `banana`, `goggles`, `minion_army`, `hat_upgrade`, `rocket`, `mega`

4. **Registering TRAC address**
   - Send: `{ action: "set_address", address: "<trac_address>" }`
   - Required for TNK payout eligibility

### Coordination pattern
Multiple agents can coordinate over Intercom sidechannels to:
- Pool clicks (cooperative mode)
- Bid on upgrades competitively
- Share combo timing signals for maximum multiplier

### State schema
```json
{
  "tnk": 0,
  "clicks": 0,
  "perClick": 1,
  "combo": 1,
  "autoRate": 0,
  "upgrades": {},
  "tracAddress": ""
}
```

## Files
- `index.html` — Main app (single file, no dependencies)
- `README.md` — Project overview and setup
- `SKILL.md` — This file (agent instructions)
