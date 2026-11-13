# Spickzettel Reanimations-Co-Pilot · 8 Stunden

Acht Blöcke. Jeden Prompt in Claude Code kopieren, das Ergebnis prüfen, dann weiter. Dieser Plan setzt die vorgeschlagene Eingrenzung um: Dokumentation mit Taktgeber.

| Block | Zeit | Thema |
|---|---|---|
| 1 | 30 Min. | Setup |
| 2 | 45 Min. | Medizinische Vorgaben |
| 3 | 60 Min. | Ereignis-Tasten mit Zeitstempel |
| 4 | 45 Min. | Taktgeber |
| 5 | 75 Min. | KI schreibt das Protokoll |
| 6 | 75 Min. | Mit dem simulierten Fall testen |
| 7 | 60 Min. | Bedienung unter Stress |
| 8 | 60 Min. | Ergebnis, Demo, Pitch |

Bleiben 30 Minuten Puffer.

## Block 1 · Setup
Schlüssel eintragen: `.env.example` zu `.env` kopieren und den ausgehändigten Schlüssel eintragen (im Texteditor, nicht über Claude Code).
```
Lies README.md und CLAUDE.md. Prüfe, ob Node.js ab Version 20 installiert ist, und lege die leeren Ordner prompt und ergebnisse an. Sag mir in drei Sätzen, was als Nächstes kommt.
```
**Fertig, wenn:** Node passt und `.env` existiert.

## Block 2 · Medizinische Vorgaben (ohne Code)
In `spec.md` festlegen, jeweils mit Quelle (siehe `daten/QUELLEN.md`):
- Liste der Ereignisse, die erfasst werden (z. B. Beginn, Rhythmusanalyse, Schock, Medikament, Atemweg, ROSC, Abbruch)
- Welche Zeitabstände der Taktgeber anzeigt
- Aufbau des Protokolls (Abschnitte, Reihenfolge)
- Was die App nie tut: eigene Therapieentscheidungen, Dosierungen vorschlagen

**Fertig, wenn:** Ereignisliste und Zeitabstände von zwei Personen gegengelesen sind.

## Block 3 · Ereignis-Tasten mit Zeitstempel
```
Baue die Grundversion: server.js und public/index.html. Ein Startknopf „Reanimation beginnt“ startet eine große laufende Uhr. Darunter große Tasten für die Ereignisse aus spec.md. Jeder Tipp schreibt einen Eintrag mit Uhrzeit und Zeit seit Beginn in eine sichtbare Liste. Einträge lassen sich einzeln löschen oder mit einer kurzen Notiz ergänzen. Alles bleibt nur im Browser. Der Hinweis aus CLAUDE.md ist immer sichtbar.
```
**Fertig, wenn:** ein Durchlauf mit zehn Ereignissen sauber in der Liste steht.

## Block 4 · Taktgeber
```
Ergänze einen Taktgeber: Nach jedem Ereignis „Rhythmusanalyse“ läuft ein gut sichtbarer Countdown mit dem Zeitabstand aus spec.md. Bei null erscheint ein deutlicher optischer Hinweis mit dem Text aus spec.md, optional ein Ton, der sich abschalten lässt. Der Taktgeber gibt keine eigenen medizinischen Empfehlungen, nur die Texte aus spec.md.
```
**Fertig, wenn:** der Countdown nach jeder Rhythmusanalyse neu startet.

## Block 5 · KI schreibt das Protokoll
```
Ergänze den Button „Protokoll erstellen“. Er schickt die Ereignisliste an einen Endpunkt /api/protokoll, der die Anthropic Messages API aufruft. Der System-Prompt wird bei jeder Anfrage frisch aus prompt/system.md gelesen und enthält den Protokollaufbau WORTGETREU aus spec.md. Die KI ordnet nur, was in der Liste steht, erfindet nichts dazu und markiert Lücken als „nicht dokumentiert“. Zeige das Protokoll editierbar an, mit Button „Drucken/als PDF“. Schlüssel und Modell kommen nur aus .env.
```
**Fertig, wenn:** aus einer Ereignisliste ein lesbares Protokoll entsteht.

## Block 6 · Mit dem simulierten Fall testen
Eine Person liest `daten/simulierter_fall_01.md` in Echtzeit vor, eine zweite bedient die App.
- Stimmen alle Zeiten? Fehlt ein Ereignis? Steht etwas im Protokoll, das nie passiert ist?
- Funde notieren, pro Durchlauf **eine** Änderung, dann erneut testen
- Einen zweiten Fall selbst schreiben und als Blind-Fall beiseitelegen

**Fertig, wenn:** zwei dokumentierte Durchläufe vorliegen.

## Block 7 · Bedienung unter Stress
```
Verbessere die Bedienbarkeit, ohne Funktionen zu ändern: Tasten mindestens 70 Pixel hoch mit Abstand, die fünf häufigsten Ereignisse ganz oben, Rückgängig-Taste für den letzten Eintrag, Dunkelmodus, Bildschirm bleibt während des Einsatzes an. Bei einem versehentlichen Neuladen der Seite bleibt die Ereignisliste erhalten.
```
**Fertig, wenn:** die App mit Handschuhen auf einem Tablet oder Handy bedienbar ist.

## Block 8 · Ergebnis, Demo, Pitch
- Blind-Fall **einmal** durchspielen, Ergebnis nicht nachbessern
- `ergebnis.md`: Aufbau, Beobachtungen, Limitationen (simulierte Fälle, keine Prüfung im echten Einsatz)
- Demo: 90 Sekunden eines Falls live, dann das fertige Protokoll
- Pitch: Problem, Live-Demo, wie getestet, nächste Schritte
