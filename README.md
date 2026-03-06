# zocdoc-doctor-finder

An agent skill for finding in-network doctors with real-time availability on Zocdoc.com using browser automation.

## What It Does

Enables an agent to search Zocdoc, extract structured provider data from the Redux store and GraphQL API, compare doctors by rating/distance/reviews, check appointment availability, and direct users to book. No authentication required — all data is on Zocdoc's public frontend.

**Requires browser access** (e.g., Claude computer use or similar browser automation).

## Install

### Via Vercel skills CLI

```bash
npx skills add Zocdoc/zocdoc-agent-skill
```

### Manual

```bash
git clone https://github.com/Zocdoc/zocdoc-agent-skill.git
cp -r zocdoc-agent-skill/zocdoc-doctor-finder ~/.claude/skills/
```

## Files

```
zocdoc-doctor-finder/
  SKILL.md                        # Main skill definition
  references/
    url-patterns.md               # Search URL params, specialty IDs, filters
    api-patterns.md               # Redux state structure, GraphQL availability API
```

## Example Prompts

**Find a provider:**
- "Find me a dermatologist in Chicago that takes Aetna"
- "I need a dentist near 10001, any availability this week"
- "Who can I see for back pain in Brooklyn?"

**Compare providers:**
- "Compare the top-rated primary care doctors within 5 miles of me"
- "Show me the highest-rated psychiatrists in San Francisco that take Blue Cross"

**Check a specific doctor:**
- "Does Dr. Smith take Blue Cross Blue Shield?"
- "What appointments does Dr. Gordon have available next week?"
- "Tell me about Dr. Kim — ratings, reviews, what she specializes in"

**Book an appointment:**
- "I want to book the 2:15 PM slot with Dr. Kim on Thursday"
- "Give me the booking link for the first doctor with the earliest availability"

See [SKILL.md](zocdoc-doctor-finder/SKILL.md#example-conversations) for full worked examples showing the complete search-to-book flow.
