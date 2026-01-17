---
name: team
description: Visa nuvarande agent-team och deras roller
---

# 👥 Team Översikt

Visa en översikt av alla agenter i projektet.

## Instruktioner

1. **Lista alla agenter** i `.claude/agents/`:
   ```bash
   ls -la .claude/agents/*.md 2>/dev/null | grep -v candidates
   ```

2. **För varje agent, extrahera**:
   - Namn (från `name:` i frontmatter)
   - Roll/Description (från `description:`)
   - Verktyg (från `tools:`)
   - Modell (från `model:`)

3. **Presentera i tabellformat**:
   ```
   ┌────────────────────────────────────────────────────────────┐
   │                    🏢 PROJEKT-TEAM                         │
   ├────────────────────────────────────────────────────────────┤
   │ AGENT          │ ROLL              │ VERKTYG    │ MODELL   │
   ├────────────────────────────────────────────────────────────┤
   │ ceo            │ Projektledare     │ Read,Task  │ sonnet   │
   │ hr             │ Agent-arkitekt    │ Read,Write │ sonnet   │
   │ [fler...]      │                   │            │          │
   └────────────────────────────────────────────────────────────┘
   ```

4. **Visa också**:
   - Antal agenter totalt
   - Eventuella kandidater under rekrytering
   - Senast rekryterad agent

## Om inga agenter finns

```
⚠️ Teamet är tomt!

Kör /recruit eller prata med CEO för att börja bygga ditt team.
```

## Teamdynamik

Om användaren vill, analysera också:
- Vilka kompetenser som finns
- Eventuella gap i teamet
- Förslag på nästa rekrytering
