# Agent Factory 🏭

> Ett självorganiserande agent-team som bygger sig självt.

## Koncept

Detta projekt använder en meta-approach till agenter: **Agenter som rekryterar agenter**.

Istället för att manuellt skapa agenter, startar du med två kärnagenter (CEO + HR) som sedan bygger upp ditt team baserat på projektbehov.

## Hur det fungerar

```
┌─────────────────────────────────────────────────────────────┐
│  1. PROJEKTSTART                                            │
│     /start → CEO intervjuar dig om projektet                │
│                                                             │
│  2. TEAMANALYS                                              │
│     CEO identifierar vilka roller som behövs                │
│                                                             │
│  3. REKRYTERING                                             │
│     CEO → Rekryteringsorder → HR                            │
│     HR skapar 3 kandidatvarianter                           │
│                                                             │
│  4. INTERVJU                                                │
│     CEO + HR intervjuar kandidater                          │
│     Du väljer vinnaren                                      │
│                                                             │
│  5. EXPANSION                                               │
│     Alla agenter kan begära nya kollegor via HR             │
│     Teamet växer organiskt efter behov                      │
└─────────────────────────────────────────────────────────────┘
```

## Kommandon

| Kommando | Beskrivning |
|----------|-------------|
| `/start` | Starta nytt projekt - CEO intervjuar dig |
| `/recruit` | Rekrytera ny agent till teamet |
| `/team` | Visa nuvarande team och roller |

## Kärnagenter

### 🎯 CEO
- **Roll**: Projektledare och visionär
- **Ansvar**: Förstå projektet, identifiera behov, delegera
- **Trigger**: Projektstart, strategiska beslut

### 👔 HR  
- **Roll**: Agent-arkitekt och rekryterare
- **Ansvar**: Designa agenter, skapa kandidater, genomföra intervjuer
- **Trigger**: När någon behöver en ny kollega

## Rekryteringsprocessen

1. **Order**: CEO (eller annan agent) skickar rekryteringsorder till HR
2. **Design**: HR skapar 3 kandidatvarianter:
   - 🅰️ **Specialist** - Smal och djup
   - 🅱️ **Generalist** - Bred och flexibel  
   - 🅲 **Innovator** - Oväntad approach
3. **Intervju**: Kandidater testas med scenariofrågor
4. **Val**: Du väljer vinnaren
5. **Installation**: Vinnaren sparas i `.claude/agents/`

## Projektstruktur

```
.claude/
├── agents/
│   ├── ceo.md              # Projektledare
│   ├── hr.md               # Agent-arkitekt
│   ├── candidates/         # Temporära kandidater under rekrytering
│   └── [dynamiska agenter...]
├── commands/
│   ├── start.md            # Projektstart
│   ├── recruit.md          # Rekryteringsprocess
│   └── team.md             # Teamöversikt
└── settings.json
```

## Snabbstart

```bash
# 1. Starta projektet
/start

# 2. Svara på CEOs frågor om vad du vill bygga

# 3. CEO identifierar roller och startar rekrytering

# 4. Delta i intervjuer och välj dina agenter

# 5. Börja bygga med ditt nya team!
```

## Tips

- **Var specifik** med CEO om vad du vill bygga
- **Tänk i roller** - vilka kompetenser behövs?
- **Iterera** - du kan alltid rekrytera fler agenter senare
- **Alla kan rekrytera** - agenter kan be HR om kollegor

## Designprinciper

1. **Progressive Team Building** - Börja smått, väx efter behov
2. **Human in the Loop** - Du godkänner alla rekryteringar
3. **Specialisering** - Varje agent har ett tydligt fokus
4. **Självorganisering** - Agenter kan identifiera egna behov och rekrytera kollegor

## 🔄 Självorganiserande team

**Alla agenter kan begära nya kollegor via HR!**

Detta är kärnan i Agent Factory. När en agent jobbar och inser att den behöver hjälp:

```
┌─────────────────────────────────────────────────────────────┐
│  Frontend-dev: "Jag behöver hjälp med API-integration..."   │
│         │                                                    │
│         ▼                                                    │
│  Frontend-dev → Rekryteringsorder → HR                      │
│         │                                                    │
│         ▼                                                    │
│  HR skapar 3 kandidater för "API-specialist"                │
│         │                                                    │
│         ▼                                                    │
│  Frontend-dev + CEO intervjuar → Användaren väljer          │
│         │                                                    │
│         ▼                                                    │
│  Ny kollega: api-specialist.md installeras                  │
└─────────────────────────────────────────────────────────────┘
```

Rekryteringsorderformat (alla agenter har detta i sin prompt):
```
REKRYTERINGSORDER
================
Roll: [titel]
Syfte: [varför behövs denna roll]
Kärnkompetenser: [vad måste agenten kunna]
Verktyg: [vilka tools behöver agenten]
Samarbetar med: [andra agenter]
Prioritet: [hög/medium/låg]
```

## Tekniska noter

- Agenter laddas vid sessionstart
- Nya agenter kräver omstart ELLER `/agents` refresh
- Kandidater sparas temporärt i `candidates/`
- CLI-flaggan `--agents` kan användas för att testa kandidater live
