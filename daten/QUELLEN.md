# Datenquellen Reanimations-Co-Pilot

Für diesen Use Case gibt es keinen passenden offenen Datensatz: Reale Reanimationsprotokolle sind Patientendaten. Gearbeitet wird deshalb mit selbst geschriebenen, frei erfundenen Fällen.

## Im Repo
| Datei | Inhalt | Herkunft |
|---|---|---|
| `simulierter_fall_01.md` | Übungsfall als Ereignisliste mit Zeiten | frei erfunden für den Hackathon, medizinisch nicht geprüft |

## Fachliche Grundlagen (nur verlinkt, nicht kopiert)
| Quelle | Wofür | Hinweis |
|---|---|---|
| [Leitlinien des European Resuscitation Council](https://www.cprguidelines.eu/) | Ablauf, Zeitabstände, Begriffe | Urheberrechtlich geschützt. Poster und Algorithmen nicht ins Repo kopieren, nur verlinken. |
| [Deutscher Rat für Wiederbelebung (GRC)](https://www.grc-org.de/) | Deutsche Fassungen der Leitlinien | Wie oben. |
| Utstein-Schema | Welche Angaben ein Reanimationsprotokoll enthalten sollte | In der Fachliteratur frei nachlesbar. |

## Empfehlung für den Hackathon
- Zeitabstände und Hinweistexte trägt das Medizin-Team selbst in `spec.md` ein, mit Angabe der Leitlinienstelle.
- Zwei bis drei Fälle reichen: einer zum Entwickeln, einer als Blind-Fall, einer für die Demo.
- Eigene Fälle im selben Format wie `simulierter_fall_01.md` schreiben.
