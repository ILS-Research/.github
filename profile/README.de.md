# ILS – Institut für Landes- und Stadtentwicklungsforschung

[English](https://github.com/ILS-Research/.github/blob/main/profile/README.md) · **Deutsch**

## Wer wir sind

Das ILS (Institut für Landes- und Stadtentwicklungsforschung gGmbH) in Dortmund betreibt raumwissenschaftliche
Stadtforschung. Die Urbanisierung des frühen 21. Jahrhunderts ist enorm dynamisch: Urbane Räume entstehen, wachsen und
verändern sich, ihr Wandel verläuft zunehmend diskontinuierlich und disparat. Wir untersuchen die Dimensionen des
urbanen Wandels auf unterschiedlichen Maßstabsebenen und international vergleichend und gewinnen im aktiven Dialog mit
Praxis, Politik und Gesellschaft Erkenntnisse für eine nachhaltige Transformation und Gestaltung urbaner Räume.

Webseite: https://www.ils-forschung.de/ · GitLab: https://gitlab.com/ils-research

**GitHub ist nicht alles, was wir veröffentlichen.** Hier findest du eine Auswahl, vor allem unsere Zotero-Plugins. Weiterer Code von uns liegt auf GitLab, in unserer Hauptgruppe: **https://gitlab.com/ils-research**.

## Zotero-Plugins

KI-Werkzeuge für [Zotero](https://www.zotero.org), bei denen die Daten in der eigenen Infrastruktur bleiben: Suche und
Sprachmodelle laufen auf deinem Rechner oder auf einem Server, den **du** selbst betreibst (zum Beispiel
[Ollama](https://ollama.com)). Nichts geht an einen Cloud-Dienst, solange du keinen Server ausdrücklich freigibst.
Alle laufen mit Zotero 7 bis 10 (empfohlen: 10).

### Eigene Plugins

| Plugin | Was es macht |
|---|---|
| [**SeekChat**](https://github.com/ILS-Research/seekchat-zotero) | Chat mit PDFs, Webseiten, EPUBs und Textdateien oder mit einer ganzen Sammlung. Antworten nennen ihre Quellen; jede Quellenangabe verlinkt auf die genaue Seite. Ein Werkzeug-Chat erledigt Dinge in Zotero: Referenzen aus eingefügtem Text importieren, die Bibliothek durchsuchen, Einträge in Sammlungen ablegen, die Literaturliste eines Papers zeigen und verlinken. Änderungen passieren erst, nachdem du eine Vorschau bestätigt hast. |
| [**SeekBook**](https://github.com/ILS-Research/seekbook-zotero) | Volltextindex für Bücher und lange Dokumente (ab 30 Seiten), durchsuchbar nach Bedeutung und Stichwort, mit Kapitel und gedruckter Seitenzahl für jede Stelle. Nutzbar über SeekChat und ZotSeek. |
| <a id="custom-cloud-modifier"></a>[**Zotero Custom Cloud Modifier**](https://gitlab.com/ils-research/zotero-plugins/zotero-custom-cloud-modifier) | Für alle, die einen eigenen Zotero-Server betreiben statt mit zotero.org zu synchronisieren: richtet Zotero auf deinen Server aus und lenkt Links, die sonst zu zotero.org führen (neue Gruppe, online ansehen, Konto anlegen), auf dein eigenes Portal. Du baust es einmal für deinen Server und gibst die XPI an deine Nutzer*innen weiter. Funktioniert mit unserem [zotero-selfhost](https://github.com/ILS-Research/zotero-selfhost). |

SeekChat, SeekBook und ZotSeek arbeiten zusammen: SeekChat nutzt ZotSeek und SeekBook als Suchquellen, wenn sie
installiert sind, und findet die Literaturliste eines Dokuments über Find Online References.

Die [**Semantic Scholar Bridge**](https://github.com/ILS-Research/semantic-scholar-api-key-bridge-for-semantic-zotero), die einen Semantic-Scholar-API-Schlüssel mit einer Gruppe teilt, damit Werkzeuge wie Semantic Zotero ohne persönliche Schlüssel funktionieren, ist eine Server-Komponente und steht unter [Selbst betreiben](#selbst-betreiben). Das Gleiche gilt für unseren Zotero-Server-Stack.

### Forks mit unseren Ergänzungen

Diese Plugins stammen von anderen; unsere Forks ergänzen, was wir brauchten. Urheberschaft und Lizenzen bleiben bei den
ursprünglichen Autor*innen.

| Fork | Original | Was wir geändert haben |
|---|---|---|
| [**ZotSeek**](https://github.com/ILS-Research/ZotSeek) | [introfini/ZotSeek](https://github.com/introfini/ZotSeek) (José Fernandes, MIT) | Embeddings von einem ausdrücklich freigegebenen Server im eigenen Netz (z. B. GPU-Rechner), optional Buchtreffer aus SeekBook. |
| [**Find Online References**](https://github.com/ILS-Research/zotero-find-online-references) | [MuiseDestiny/zotero-reference](https://github.com/MuiseDestiny/zotero-reference) (AGPL-3.0) | Läuft mit Zotero 7 bis 10 und bietet eine Schnittstelle für andere Plugins (SeekChat liest darüber Literaturlisten und importiert Quellen). Experimentell, nicht zu 100 % verlässlich. |
| [**Semantic Zotero**](https://github.com/ILS-Research/semantic-zotero) | [AgiNetz/semantic-zotero](https://github.com/AgiNetz/semantic-zotero) (MIT) | Branch zur Nutzung mit der Semantic Scholar Bridge. |

## Werkzeuge zur Raumanalyse

Liegen auf GitLab, in unserer Hauptgruppe.

| Werkzeug | Was es macht |
|---|---|
| [**dominant-mobility-classifier**](https://gitlab.com/ils-research/dominant-mobility-classifier) | QGIS-Plugin (experimentell), das Quartiere als fußgänger-, ÖPNV- oder autoabhängig einordnet, anhand von Erreichbarkeit von Einrichtungen, Nutzungsmischung, Grünanteil, Fußwegenetz und gut getaktetem ÖPNV. Nutzt OpenStreetMap, das OpenRouteService-Plugin und einen GTFS-Datensatz. |
| [**os-walk-eu**](https://gitlab.com/ils-research/os-walk-eu) | QGIS-Plugin OS-WALK-EU (Open Source Walkability Tool for European Union Member States), entwickelt mit Forschenden aus Irland, Portugal und Italien. Es berechnet die Walkability im Wohnumfeld (Standard: 500 m Wegedistanz) aus Einrichtungs- und Flächendaten von OpenStreetMap und fußläufigen Distanzen von OpenRouteService als Index von 0 bis 100. [StoryMap zu Nutzung, Interpretation und Grenzen](https://storymaps.arcgis.com/stories/abca15a2477843ca9e78fe1edd7ecab8). |
| [**flaechenampel_gfz_converter**](https://gitlab.com/ils-research/flaechenampel_gfz_converter) | Python-Modul, das mittlere Geschossflächenzahlen (GFZ) für Bebauungspläne aus einer XPlanung-Datenbank (PostgreSQL) berechnet. |

## Daten des öffentlichen Verkehrs

| Werkzeug | Was es macht |
|---|---|
| [**delfi-dataset-fixer**](https://github.com/ILS-Research/delfi-dataset-fixer) | Jupyter-Notebook, das den bundesweiten Fahrplandatensatz (DELFI, GTFS) so repariert, dass Routing-Software wie OpenTripPlanner ihn laden kann: Es löscht Haltestellen ohne ID, setzt Haltezeiten auf die übergeordnete Station, wenn eine Haltestelle den falschen Typ hat, entfernt Umstiege zu nicht vorhandenen Haltestellen und schreibt eine bereinigte GTFS-Zip. Das Notebook steht unter MIT-Lizenz, der DELFI-Datensatz hat eine eigene Lizenz. |

## Selbst betreiben

Server-Komponenten und Docker-Compose-Aufbauten, um Software auf der eigenen Infrastruktur zu betreiben.

| Projekt | Was es macht |
|---|---|
| [**zotero-selfhost**](https://github.com/ILS-Research/zotero-selfhost) | Ein selbst betriebener Zotero-Sync-Server ohne AWS-Abhängigkeit: Dataserver, Stream-Server, Web-Bibliothek, S3-kompatibler Dateispeicher und ein Portal mit Login (Passwort oder OpenID Connect) sowie Benutzer- und Gruppenverwaltung. Der offizielle Zotero-Desktop-Client synchronisiert nach Änderung von zwei Einstellungen damit. Passt zum [Zotero Custom Cloud Modifier](#custom-cloud-modifier) oben. Du suchst eine Lösung, die voraussichtlich dauerhaft gepflegt wird? Schau dir [altero](https://github.com/eseifert/altero) von Erich Seifert an, einen unabhängigen selbst betriebenen Sync-Server für den unveränderten Zotero-Client (AGPL-3.0, derzeit Beta). |
| [**Semantic Scholar Bridge**](https://github.com/ILS-Research/semantic-scholar-api-key-bridge-for-semantic-zotero) | Teilt einen Semantic-Scholar-API-Schlüssel mit einer Gruppe (Institut, Labor, Kurs), damit Werkzeuge wie Semantic Zotero oder MCP-Server funktionieren, ohne dass jede Person einen eigenen Schlüssel beantragt. |
| [**openqda-composestack**](https://github.com/ILS-Research/openqda-composestack) | Docker-Compose-Aufbau für [OpenQDA](https://github.com/openqda/openqda), ein Open-Source-Werkzeug zur qualitativen Datenanalyse, zusammen mit MySQL und Redis. Das Image wird aus dem Upstream-Repository in einer einstellbaren Git-Version gebaut; dieses Repository enthält nur die Betriebswerkzeuge. |

## Mitwirken

Rückmeldungen und Fehlermeldungen bitte als Issue im jeweiligen Repository.
