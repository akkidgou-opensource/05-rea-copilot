# 05 · Reanimations-Co-Pilot

> Prototyp für den AKKI Hackathon 2026. Nur simulierte Fälle, kein Medizinprodukt, nicht für den Einsatz am Menschen.

**Bereich:** Rettungsstelle

**Idee:** Eine KI begleitet den Einsatz in der Rettungsstelle, von der digitalen Anamnese über die Dokumentation bis zur Unterstützung während der Reanimation.

**Vorschlag zur Eingrenzung:** Nur die Dokumentation. Ereignisse werden während einer simulierten Reanimation per Fingertipp mit Zeitstempel erfasst, ein Taktgeber läuft mit, und die KI schreibt daraus am Ende ein lesbares Protokoll.

## Warum
Anamnese, Dokumentation und Reanimationsablauf sind zeitkritisch und fehleranfällig, wenn sie parallel zur Versorgung von Hand erfolgen müssen.

## Was am Ende stehen soll
- Strukturierte Dokumentation von Ereignissen während des simulierten Einsatzes
- Ablaufunterstützung (z. B. Zeittakt)
- Ein lesbares Protokoll am Ende

**Erfolgskriterium:** Ein simulierter Fall läuft vollständig durch, mit lesbarem Ergebnis.

## So startet ihr
1. Oben auf **Code → Download ZIP** klicken und entpacken.
2. Im entpackten Ordner ein Terminal öffnen und `claude` eingeben (bei Codex: `codex`).
3. `SPICKZETTEL.md` öffnen und mit Block 1 beginnen.
4. Zwischenstände hochladen: siehe `GITHUB_ANLEITUNG.md`.

## Was in diesem Repo liegt
| Datei | Wofür |
|---|---|
| `SPICKZETTEL.md` | Umsetzungsplan für 8 Stunden, Block für Block |
| `CLAUDE.md`, `AGENTS.md` | Dieselben Regeln für den Coding-Agenten (Claude Code liest die erste, Codex die zweite Datei) |
| `GITHUB_ANLEITUNG.md` | Eure Arbeit auf GitHub bringen, ohne Git-Kenntnisse |
| `daten/QUELLEN.md` | Leitlinien und Hinweise zu Testdaten |
| `daten/simulierter_fall_01.md` | Ein frei erfundener Übungsfall als Ereignisliste |

## Stolpersteine
- Nur mit simulierten Daten arbeiten
- Auf **einen** Teilaspekt fokussieren: Dokumentation **oder** Anamnese **oder** Reanimationsablauf
- Die App gibt keine eigenen medizinischen Anweisungen. Zeitvorgaben und Hinweise stammen ausschließlich aus der Spezifikation des Teams

## Für Erfahrene
- Spracheingabe statt Fingertipp („Schock abgegeben“)
- Übergabetext nach einem festen Schema erzeugen
- Auswertung nach dem Fall: Zeitabstände zwischen den Ereignissen als Diagramm
