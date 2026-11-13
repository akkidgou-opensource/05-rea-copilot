# Simulierter Fall 01 (frei erfunden)

**Achtung:** Dieser Fall ist für den Hackathon ausgedacht und medizinisch nicht geprüft. Er dient nur dazu, die App zu bedienen und das Protokoll zu testen. Das Medizin-Team darf und soll ihn korrigieren.

**Ausgangslage:** Schockraum, 14:02 Uhr. Übungspuppe, männlich, etwa 60 Jahre, kollabiert während der Aufnahme. Kein Puls tastbar.

**So wird der Fall benutzt:** Eine Person liest die Zeilen in Echtzeit vor, eine zweite tippt die Ereignisse in die App.

| Zeit seit Beginn | Ereignis |
|---|---|
| 00:00 | Kreislaufstillstand festgestellt, Reanimation beginnt, Thoraxkompressionen |
| 00:40 | Defibrillator angeschlossen |
| 01:10 | Rhythmusanalyse: Kammerflimmern |
| 01:20 | 1. Schock abgegeben, Kompressionen sofort weiter |
| 02:00 | Beutel-Masken-Beatmung, Sauerstoff angeschlossen |
| 03:20 | Rhythmusanalyse: Kammerflimmern |
| 03:30 | 2. Schock abgegeben |
| 04:10 | Venöser Zugang gelegt |
| 05:30 | Rhythmusanalyse: Kammerflimmern |
| 05:40 | 3. Schock abgegeben |
| 05:55 | Medikament 1 gegeben (laut Team-Spezifikation) |
| 06:10 | Medikament 2 gegeben (laut Team-Spezifikation) |
| 06:45 | Atemweg gesichert |
| 07:40 | Rhythmusanalyse: geordneter Rhythmus, Puls tastbar |
| 07:45 | Wiederkehr des Spontankreislaufs (ROSC) |
| 08:30 | 12-Kanal-EKG geschrieben |
| 09:00 | Übergabe an das weiterbehandelnde Team |

## Prüffragen für das Protokoll
- Stehen alle 17 Ereignisse mit der richtigen Zeit im Protokoll?
- Wie viele Schocks nennt das Protokoll? (erwartet: 3)
- Wie lange dauerte es bis ROSC? (erwartet: 7 Minuten 45 Sekunden)
- Steht irgendetwas im Protokoll, das nicht vorgelesen wurde?
