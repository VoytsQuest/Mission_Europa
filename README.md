# Mission Europa – Das Geheimnis des verschwundenen Schatzes

HTML5-Escape-Game für die 5. Klasse (Gesellschaftslehre/Erdkunde), Teams aus zwei Kindern, ca. 25–35 Minuten.
© VoytsQuest – Lernspiele mit Köpfchen

## Ordnerstruktur

```
mission-europa/
├── index.html                    ← das komplette Spiel (HTML, CSS, JavaScript)
├── README.md
└── assets/
    ├── europakarte.pdf           ← Originalkarte der bpb (zum Ausdrucken)
    ├── europakarte.jpg           ← aus der PDF erzeugt (260 dpi), für die Kartenansicht im Spiel
    ├── professor.jpg             ← Bild von Professor Falkenstein (Urkunde)
    ├── brief_falkenstein.jpg     ← der gestaltete Brief des Professors (Startseite der Geschichte)
    ├── brief_falkenstein.mp3     ← der vorgelesene Brief (startet automatisch, Musik wird dabei leiser)
    ├── hintergrundmusik.mp3      ← eure Musik „Sanfte Morgenstimmung“ (MP3 für iPad/Safari)
    ├── hintergrundmusik.m4a      ← eure Originaldatei (Ersatzquelle)
    ├── fonts/                    ← Schrift „Lora“ (SIL Open Font License), lokal – keine Google-Server
    └── wappen/
        ├── 1_kompass.jpg … 8_schatztruhe.jpg   ← die acht Wappen, aus eurem Sammelbild ausgeschnitten
```

- **Bilder** liegen in `assets/` (Professor) bzw. `assets/wappen/` (Wappen).
- **Musik** liegt in `assets/hintergrundmusik.mp3`. Wer die Musik austauschen will, ersetzt diese Datei unter gleichem Namen. Fehlt sie, läuft das Spiel ohne Musik (der Button zeigt „Keine Musik“).
- Alle Verweise sind relativ – der Ordner kann so, wie er ist, hochgeladen werden.

## Lokal testen

Variante A (einfach): `index.html` doppelklicken. Alles funktioniert; die Lautstärke wird dann über den Browser geregelt.

Variante B (wie später online, empfohlen): Im Ordner `mission-europa` ein Terminal öffnen und
```
python3 -m http.server 8000
```
starten, dann im Browser `http://localhost:8000` öffnen. Für iPads im selben WLAN: `http://<IP-des-Rechners>:8000`.

## Veröffentlichen mit GitHub Pages

1. Auf github.com ein neues, öffentliches Repository anlegen, z. B. `mission-europa`.
2. „Add file → Upload files“: den **Inhalt** des Ordners hochladen (also `index.html` und den Ordner `assets` – nicht den Überordner selbst). „Commit changes“.
3. Repository → **Settings → Pages** → „Build and deployment“: Source „Deploy from a branch“, Branch `main`, Ordner `/ (root)` → Save.
4. Nach 1–2 Minuten ist das Spiel unter `https://<benutzername>.github.io/mission-europa/` erreichbar.
5. Auf dem iPad die Seite einmal komplett laden (Karte und Musik einmal öffnen). Solange der Tab geöffnet bleibt, läuft das Spiel auch ohne Internet weiter.

## Datenschutz

Keine Anmeldung, keine externen Server, keine Schriften/Skripte von Drittanbietern, keine Übertragung von Daten. Teamname, Spielstand und Bestenliste werden nur im `localStorage` des jeweiligen Geräts gespeichert. Die Bestenliste ist pro Gerät getrennt und kann über „Bestenliste löschen“ (zweimal tippen) geleert werden.

## Hinweise für die Lehrkraft (vor dem Unterricht lesen)

**Druck:** `assets/europakarte.pdf` im A4-Querformat bei **100 %** („Tatsächliche Größe“, nicht „An Seite anpassen“) drucken. Kontrolle: Die Maßstabsleiste von 0 bis 1.000 km muss genau 4 cm lang sein.

Die Lösungen und Messwerte stehen bewusst **nicht** in diesem öffentlichen Repository, sondern im separaten Lösungsheft (PDF) der Lehrkraft.

**Eingaben:** Groß-/Kleinschreibung egal; bei längeren Städtenamen wird ein einzelner Tippfehler toleriert. Planquadrate auch als „x 1“ oder „1x“. Zahlen auch mit „km“/„cm“ oder Tausenderpunkt. Leere oder ungültige Eingaben kosten keine Punkte.

## Punktesystem

| Abweichung vom Referenzwert | Punkte |
|---|---|
| 0–20 km | 150 |
| über 20 bis 40 km | 125 |
| über 40 bis 60 km | 100 |
| über 60 bis 80 km | 75 |
| über 80 bis 100 km | 50 |
| mehr als 100 km | 0 – erneut versuchen |

Normale Fragen (auch die Zentimeter-Messung): max. 100 Punkte. Jeder falsche Versuch −20, jeder Tipp −50 (einmalig) mögliche Punkte, nie unter 0. Maximal erreichbar: **2.600 Punkte**.

**Ablauf bei Entfernungen (zwei Schritte):**
1. *Messen:* Die Kinder tragen die gemessenen Zentimeter ein. Akzeptiert wird alles bis ±1 cm um den auf der Karte gemessenen Wert. Auch gerundete Werte werden angenommen.
2. *Umrechnen:* Die Frage nennt die eigene Messung („Ihr habt … cm gemessen“). Angenommen wird die richtige Rechnung (eigene cm × 250) **oder** jeder Wert bis ±100 km um die echte Luftlinie. Die Punkte richten sich wie bisher nach der Abweichung von der echten Luftlinie (Tabelle oben). Liegt die Rechnung richtig, die Messung aber mehr als 100 km daneben, gibt es 25 Punkte für die richtige Rechnung, damit kein Team festhängt.
Bestenliste: Punkte ↓, dann Zeit ↑, dann Tipps ↑.

## Hilfen im Spiel (kostenlos)

Oben in jeder Aufgabe: **🗺️ Europakarte** (zoombar), **🧭 Windrose** (alle acht Himmelsrichtungen mit Abkürzungen) und **📏 Maßstab-Hilfe**. Nur die 💡-Tipps kosten Punkte.

**Maßstabsprüfung:** drei Rechenfragen zum Maßstab.

## Zeitmessung

Die Zeit läuft erst ab **Level 1**. Brief und Maßstabsprüfung sind zeitfrei; die Punkte der Maßstabsprüfung zählen aber mit.

## Spielstand

Wird die Seite versehentlich neu geladen, bietet der Startbildschirm „Weiterspielen“ an – Punkte, Tipps und die bisherige Zeit bleiben erhalten.
