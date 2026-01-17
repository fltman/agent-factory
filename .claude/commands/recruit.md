---
name: recruit
description: Starta rekryteringsprocess för en ny agent till teamet
---

# 🎯 Rekryteringsprocess

Du ska nu facilitera en rekrytering av en ny agent till teamet.

## Instruktioner

### Om detta initieras av CEO eller annan agent:

1. **Ta emot rekryteringsorder** med följande information:
   - Roll som ska tillsättas
   - Syfte och kärnkompetenser
   - Verktyg som behövs
   - Prioritet

2. **Delegera till HR-agenten** med full rekryteringsorder:
   ```
   Använd HR-agenten för att skapa 3 kandidater för rollen [roll].
   
   Rekryteringsorder:
   [klistra in order från beställare]
   ```

3. **Koordinera intervjuprocessen**:
   - HR presenterar kandidater
   - Beställare (CEO/agent) + HR ställer frågor
   - Användaren fattar slutgiltigt beslut

4. **Slutför rekrytering**:
   - HR installerar vinnande kandidat
   - Bekräfta att agenten är tillgänglig
   - Uppdatera teamöversikt

### Om detta initieras direkt av användaren:

1. **Fråga vad för typ av agent som behövs**:
   "Vilken typ av agent vill du rekrytera? Beskriv:
   - Vad ska agenten göra?
   - Finns det specifika krav?
   - Vilka andra agenter ska den samarbeta med?"

2. **Skapa rekryteringsorder** baserat på svaren

3. **Delegera till HR** för kandidatskapande

4. **Genomför intervju** tillsammans med HR

5. **Låt användaren välja** vinnande kandidat

## Intervjufrågor (förslag)

Anpassa efter roll, men överväg:

1. **Scenariobaserad**: "Hur skulle du hantera [typisk situation för rollen]?"
2. **Problemlösning**: "Vad gör du om [vanligt problem]?"
3. **Samarbete**: "Hur kommunicerar du med [relaterad agent]?"
4. **Självkännedom**: "Vad är din största begränsning?"

## Efter rekrytering

- Verifiera att agenten fungerar: `ls -la .claude/agents/`
- Meddela teamet om ny kollega
- Föreslå första uppgift för nya agenten

## Kandidatmapp

Temporära kandidater sparas i:
```
.claude/agents/candidates/
```

Dessa rensas efter avslutad rekrytering.
