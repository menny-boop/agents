# GTM Agents

Cloud agents that run on a recurring schedule to support Menny's GTM workflow at Nilus.

All agents are managed via [claude.ai/code/routines](https://claude.ai/code/routines).

---

## Agents

| Agent | File | Schedule | What it does |
|-------|------|----------|--------------|
| [recapy](./recapy.md) | `recapy.md` | 8am, 11am, 2pm, 5pm, 8pm UTC | Scans Gong for new calls → generates follow-up email drafts → DMs to Slack |
| [coachy](./coachy.md) | `coachy.md` | Every 2 hours | Reviews Gong calls → scores against MEDDPICC → DMs brutal coaching feedback to Slack |
| [slacky](./slacky.md) | `slacky.md` | Every hour | Scans all Slack channels/DMs → distills last 60 min → DMs a crisp summary |

---

## How to update an agent

1. Edit the prompt in the agent's `.md` file in this repo
2. Go to [claude.ai/code/routines](https://claude.ai/code/routines) and update the prompt there too
   (or ask Claude Code to sync the change via the RemoteTrigger API)
