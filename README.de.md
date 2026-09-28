# Where is my token

[简体中文](README.md) · [繁體中文](README.zh-TW.md) · [English](README.en.md) · [日本語](README.ja.md) · [Français](README.fr.md) · **Deutsch** · [한국어](README.ko.md)

[macOS-Beta herunterladen](https://github.com/xiu-hu404/where-is-my-token/releases/tag/v0.1.0-beta.4) · [Problem melden oder Verbesserung vorschlagen](https://github.com/xiu-hu404/where-is-my-token/issues)

**Token-Verbrauch und geschätzte Codex-Kosten auf dem Mac im Blick.**

Die Aufgabe läuft noch, aber der Token-Zähler steigt immer weiter. Wohin geht der Verbrauch? Where is my token zeigt dir die Token-Nutzung je Unterhaltung, die Cache-Trefferquote und die Kontextauslastung in einer kleinen Leiste. Eine geringe Cache-Nutzung oder stetig wachsende Protokolldateien geben dir Anhaltspunkte, um deine Arbeit mit Codex zu überprüfen.

![Beispiel einer Codex-Arbeitsfläche mit Token-Anzeige über der Unterhaltung](docs/images/codex-workflow-en.jpg)

Die Codex-Arbeitsfläche ist eine Illustration. Die Leiste stammt aus der tatsächlichen Oberfläche; Unterhaltung und Zahlen sind Beispieldaten. Die Abbildungen sind einheitlich auf Englisch.

## Was bringt dir das?

- **Verbrauch nachvollziehen.** Sieh die Gesamtmenge je Unterhaltung oder Projekt, ohne selbst Protokolle zu durchsuchen.
- **Ansatzpunkte finden.** Die Leiste weist auf anhaltend niedrige Cache-Trefferquoten und länger andauerndes Wachstum von Protokolldateien hin.
- **Kosten einordnen.** Lass den Verbrauch anhand bekannter API-Preise umrechnen und prüfe auf einem Beleg die Nutzung je Modell sowie die verbrauchsintensivsten Gesprächsrunden.
- **Selbst entscheiden.** Die Auswertung erfolgt lokal. Es gibt keine zusätzlichen Modellaufrufe, keine Nachrichten im Chat, keinen automatischen Modellwechsel und keine automatische Dateilöschung.

Du kannst eine Unterhaltung festlegen, nach Aktivierung des Folgemodus neu gesendeten Nutzernachrichten folgen oder die Summe des zugehörigen Projekts anzeigen. Der Monitor startet und stoppt mit den Codex-Fenstern. Er übernimmt die macOS-Sprache und unterstützt Deutsch, Englisch, vereinfachtes und traditionelles Chinesisch, Japanisch, Französisch und Koreanisch. ChatGPT, Codex und Modellnamen bleiben unverändert.

## Belege und Hinweise

![Verbrauchsbeleg mit Tokens, Dauer, API-Kostenschätzung und Gesprächsrunden](docs/images/receipt-showcase-en.jpg)

Erstelle einen Beleg, wenn du ihn brauchst. Wähle eine Unterhaltung oder ein Projekt, die N Runden mit dem höchsten Verbrauch oder alle Runden, 58 oder 80 mm Papierbreite und die Anzeige des API-Betrags. Drucken ist zunächst ausgeschaltet. Nach dem Aktivieren kannst du ein bereits gekoppeltes Gerät mit klassischem Bluetooth oder einen Systemdrucker wählen und den Druck im macOS-Druckdialog bestätigen.

![Oranger Statuspunkt bei niedriger Cache-Trefferquote mit zugehörigem Hinweistext](docs/images/advisory-showcase-en.jpg)

Der orange Statuspunkt macht auf eine zuletzt niedrige Cache-Trefferquote aufmerksam. Rechts steht der Text, der beim Bewegen des Zeigers auf den Punkt erscheint. Er gibt Anlass zum Nachsehen und ist kein Beweis für verschwendete Tokens.

## Installation und Deaktivierung

Aktuelle Version: **0.1.0-beta.4**. Erforderlich sind ein **Mac mit Apple Silicon und macOS 15 oder neuer**. Die Laufzeitumgebung ist enthalten; Python oder Xcode müssen nicht installiert werden. 

Wenn dir das Testpaket vorliegt:

1. Entpacke `Where-is-my-token-0.1.0-beta.4-macOS-arm64.zip`.
2. Öffne `Where is my token.app` und wähle die Installation mit anschließendem Start.
3. Führe zum Deaktivieren `Disable.command` aus. Einstellungen und Statistiken bleiben erhalten.

Wenn du das letzte reguläre Codex-Fenster schließt, stoppen Monitor und Datenerfassung. Beim Öffnen eines neuen Fensters starten sie wieder. Minimieren beendet die Erfassung nicht. Ein kleiner Hintergrundprozess wartet auf das nächste Fenster. Mit × klappst du die Leiste zu einer W·T-Schaltfläche zusammen; ein Klick darauf öffnet sie wieder.

Diese Beta hat noch keine Developer-ID-Signatur und ist nicht von Apple notarisiert. Sie ist ein lokales Begleitprogramm für Codex, kein ZIP zum Import in dessen Plugin-Verzeichnis. Codex-Hooks müssen nicht aktiviert werden.

## Datenschutz und aktuelle Grenzen

- Aus den lokal lesbaren Codex-Aufzeichnungen werden die nötigen Statistiken gespeichert. Vollständige Unterhaltungen werden nicht kopiert und Statistiken nicht hochgeladen. Die Daten liegen unter `~/Library/Application Support/Where is my token/`.
- Der Folgemodus orientiert sich an neu gesendeten Nachrichten, nicht an der gerade ausgewählten Unterhaltung oder ungesendeten Entwürfen.
- Die Cache-Trefferquote sagt nichts über die Richtigkeit der Antworten aus. Die Kontextauslastung zeigt nicht, ob Inhalte nötig sind; ein hoher Wert allein löst keinen Hinweis aus.
- Es zählen nur lokal erfasste Aufzeichnungen. Fehlende Mengen oder Preise erscheinen als „—“. Verbleibende Tokens werden nicht aus dem Abonnement abgeleitet.
- Der API-Betrag ist eine Umrechnung, keine tatsächliche Abbuchung. Abonnementkosten und ihre monatliche Aufteilung werden derzeit über Verwaltungsbefehle eingegeben; Belege in der Oberfläche zeigen vor allem API-Schätzungen.
- Protokollhinweise beruhen auf Dateigröße und Änderungszeit, nicht auf gemessenen physischen Schreibzugriffen. Hinweise zum passenden Zeitpunkt für Tests sind noch nicht in die Leiste eingebunden.
- Bluetooth-Druck setzt eine kompatible macOS-Druckwarteschlange voraus. Herstellerspezifische Protokolle und der Druck auf Papier sind noch nicht geprüft. Das Fensterverhalten wurde isoliert getestet; die Kompatibilität mit verschiedenen Codex-Versionen muss noch überprüft werden.

## Lizenz und Rückmeldungen

Kostenlose Software mit nicht öffentlichem Quellcode, **ausschließlich für nichtkommerzielle Zwecke**. Kostenloses Kopieren, Ändern, Neuverpacken und Weitergeben ist für nichtkommerzielle Zwecke gestattet. Weiterverkauf, kostenpflichtige Bündelangebote und der entgeltliche Zugang zu den Softwarefunktionen sind untersagt. Einzelheiten stehen in der [Lizenz](LICENSE).

[Problem melden oder Verbesserung vorschlagen](https://github.com/xiu-hu404/where-is-my-token/issues) · [Datenschutz](docs/privacy.md) · [Drittanbieterhinweise](THIRD_PARTY_NOTICES.md)
