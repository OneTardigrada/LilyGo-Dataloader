# LilyGo-Dataloader

Browser-basiertes Konfigurations- und Datenauslese-Tool für die ESM-Smartwatch (LilyGo T-Watch S3). Läuft komplett lokal im Browser, keine Installation nötig.

## Funktionen

- **Konfiguration erstellen & übertragen** — Fragebögen, Items, Zeitfenster und Benachrichtigungen per UI bearbeiten und auf die Uhr flashen.
- **Antworten auslesen** — Erhobene CSV-Daten von der Uhr herunterladen und lokal speichern.
- **Zeit synchronisieren** — RTC der Uhr mit der aktuellen Browserzeit abgleichen.
- **Self-Test** — Hardware-Diagnose der Uhr aus dem Browser anstoßen.

## Voraussetzungen

- **Chrome** oder **Edge** (Web Serial API; Firefox/Safari werden nicht unterstützt).
- USB-Kabel zur Uhr.
- Seite über `file://` oder `https://` öffnen (Web Serial funktioniert nicht über `http://`).

## Verwendung

1. `data_loader.html` im Browser öffnen (Doppelklick reicht).
2. Uhr per USB anschließen und einschalten.
3. **„Verbinden"** klicken → seriellen Port der Uhr auswählen → mit 115200 Baud verbunden.
4. Gewünschte Aktion wählen (Konfiguration laden, Antworten exportieren, Zeit setzen, …).

## Datei-Übersicht

| Datei | Zweck |
|---|---|
| `data_loader.html` | Hauptanwendung (alles in einer Datei: HTML/CSS/JS). |
| `index.html` | Einstiegsseite (leitet auf Data Loader weiter). |
| `sample_config.json` | Beispiel-Konfiguration als Vorlage. |

## Hinweise

- Es werden keinerlei Daten an Server gesendet — alles läuft im Browser.
- Bei Verbindungsabbrüchen die Uhr kurz aus- und wieder einstecken und erneut verbinden.
- Das Konfigurationsformat ist im Repo unter `docs/SPECIFICATION.md` beschrieben.
