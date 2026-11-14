# Junction 2026 – Handoff (Stand: Sa 14.11.2026, 02:00)

Kontext für die KI: Ich (Handan) bin beim Hackathon Junction 2026 in Espoo (Hype Arena). Das hier ist die Zusammenfassung aus einem früheren Chat. Bitte antworte kurz, einfach und auf Deutsch.

## Event & Fristen
- Finale Abgabe: **So 15.11. 10:00**. Danach ist das Formular zu, verspätete Abgaben gibt es nicht. Vorher von DRAFT auf FINAL stellen, Bearbeiten bleibt bis 10:00 möglich.
- Abgabe in der Junction-App: Menü → **Project Submission**. Das macht **nur eine Person pro Team**.
- Peer Review: **So 10:30–13:00**. Das ganze Team muss vor Ort sein, sonst kein Hauptpreis.
- Top 5 pitchen um 14:15 (3 Min Pitch + 3 Min Fragen). Hauptpreis 10.000 €.
- Bewertung für den Hauptpreis: Innovation, Wirkung (Impact), Umsetzung. Die Top 5 werden von den Teilnehmern gewählt.

## Regeln
- Kein Code, der vor dem Event geschrieben wurde
- Team: 1–4 Personen
- Pitch-Video max. 2 Minuten (YouTube/Loom, öffentlich)
- Quellcode-Link Pflicht, Lizenz MIT (Open Source)
- Abgabe braucht: Name, Punchline, Beschreibung, Challenge, Tech-Stack, Video, Demo- und Code-Links, Pitch-Deck (PDF), Telefonnummern, Discord-Namen

## Unsere Challenge: „Make Blueprints Talk“ (Stoa)
- Ein Programm, das Fragen in normaler Sprache zu Bauzeichnungen und Gebäudemodellen beantwortet, **richtig und überprüfbar**
- Bewertung je 25 %: **Genauigkeit**, **Begründung sichtbar machen** (zeigen, wo in der Zeichnung die Antwort steht), **Kreativität**, **niedrige Kosten pro Anfrage**
- Gewünscht sind hybride Lösungen (großes Modell + Bilderkennung/Geometrie + kleine Modelle), die nicht vom nächsten großen KI-Modell überholt werden
- Preise: 1.000 € + Work Trial bei Stoa / 750 € / 250 €
- Datensatz: Preview (0,5 GB) und Full (10 GB), Links auf der Challenge-Seite in der Junction-App

## Projekt: DrawingSense (Arbeitstitel)
- Fragen stellen → Antwort + **markierte Stelle in der Zeichnung** + Sicherheit (Confidence)
- **Routing:** Einfache Fragen gehen an ein kleines, günstiges Modell (Gemma), schwere an Gemini
- **Wow-Idee für den Hauptpreis:** Widersprüche zwischen Plänen automatisch finden, plus Kostenanzeige pro Antwort

## Tech Challenges (nur die, die passen)
| Challenge | Preis | Einsatz im Projekt |
|---|---|---|
| Gemini API | 4.000 € + Cloud-Credits | Zeichnungen lesen (Bilderkennung) |
| Modal | 2.000 $ + 3.000 $ Credits | Gemma auf GPU hosten, öffentliche Demo-URL |
| Gemma | 1.000 € | Kleines, günstiges Modell für einfache Fragen |
| Codex | 10.000 $ Credits | Codex beim Entwickeln nutzen und das dokumentieren |
| Nemotron | RTX 5080 | Zweites Bildmodell zur Gegenprüfung |
| CRACI | LEGO pro Person | GitHub Actions mit `runs-on: craci` |
| Aiven | 1.000 € | Datenbank für den Index der Zeichnungen |

Nicht passende Tech Challenges wieder abwählen.

## Team (4 Personen)
- Software Engineer: Pipeline (Einlesen → Index → Routing)
- Vibe-Coder 1: Demo-Oberfläche (Zeichnung anzeigen, Stelle markieren)
- Vibe-Coder 2 (Business/Pharma): Testfragen aus dem Datensatz, Pitch-Deck, Video
- Ich: Architektur, Zusammenführen (Merge), Anforderungen der Tech Challenges

**Problem:** Bisher entwickelt jeder für sich. Ziel: **ein** gemeinsames Repo, jeder arbeitet in einem eigenen Branch, gemergt wird in `main`.

## Setup-To-dos
- [ ] GitHub-Organization + Repo anlegen, Team einladen
- [ ] Mac und Arbeitslaptop: Repo klonen (`gh auth login`, dann `gh repo clone ORG/REPO`)
- [ ] `.env` für API-Keys anlegen und in `.gitignore` eintragen. Keys nie auf GitHub oder im Discord!
- [ ] Credits einlösen (pro Person). Junction-App → **Developer Tools and Assets** → Kachel öffnen:
  - Gemini (Key über aistudio.google.com), Modal 100 $, Verda 200 € (Console + Formular), OpenAI Codex 100 $, Claude 20 $, Aiven 50 $
  - CRACI: Invite-Code im Discord-Kanal #craci (nur eine Person pro Team)
  - Oxylabs auslassen (braucht Kreditkarte)
- [ ] Discord im Browser öffnen: #announcements, #craci, Stoa-Kanal

## Zeitplan
- Sa 9:00 – Team-Meeting (30 Min) mit diesem Plan
- Sa 12:00 – Finale Abgaben sind ab jetzt möglich
- Sa 22:00 – Feature-Stopp, ab dann nur noch Fehler beheben
- So 07:00 – Video aufnehmen
- So 09:30 – Abgabe auf FINAL stellen

## Infos vor Ort
- WLAN: Junction2026 / pushtheboundaries
- Workshops heute: Cala 11:00, Intel 12:00, Modal 13:30, Exa 16:30 (Loft im 4. Stock bzw. Hardware Lab im 5. Stock)
- Info Desk im 2. Stock
