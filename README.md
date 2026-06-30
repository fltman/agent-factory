# Agent Factory

[![Support me on Patreon](https://img.shields.io/badge/Patreon-Support%20my%20work-FF424D?style=flat&logo=patreon&logoColor=white)](https://www.patreon.com/AndersBjarby)

Ett självorganiserande agent-team för Claude Code som bygger sig självt. Du startar med två kärnagenter – en CEO och en HR – som tillsammans intervjuar dig, identifierar vilka roller projektet behöver och rekryterar nya agenter efter hand.

## Hur det fungerar

1. **CEO** intervjuar dig om projektet och identifierar vilka kompetenser som behövs.
2. **HR** designar tre kandidatvarianter för varje roll (specialist, generalist, innovatör).
3. Du intervjuar kandidaterna och väljer vinnaren, som sparas i `.claude/agents/`.
4. Alla agenter kan själva begära nya kollegor via HR – teamet växer organiskt.

Människan är alltid med i loopen och godkänner varje rekrytering.

## Kommandon

| Kommando | Beskrivning |
|----------|-------------|
| `/start` | Starta nytt projekt – CEO intervjuar dig |
| `/recruit` | Rekrytera en ny agent till teamet |
| `/team` | Visa nuvarande team och roller |

## Användning

Öppna projektet i Claude Code och kör `/start`. Kärnagenterna ligger i `.claude/agents/` (`ceo.md`, `hr.md`) och kommandona i `.claude/commands/`. Nya agenter kräver en omstart eller `/agents`-refresh för att laddas.

## Tech

Claude Code (Markdown-agenter och slash-kommandon under `.claude/`).
