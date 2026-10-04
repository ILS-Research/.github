# ILS – Institut für Landes- und Stadtentwicklungsforschung

[English](https://github.com/ILS-Research/.github/blob/main/profile/README.md) · **Deutsch**

## Wer wir sind

Das ILS (Institut für Landes- und Stadtentwicklungsforschung gGmbH) in Dortmund betreibt raumwissenschaftliche
Stadtforschung. Die Urbanisierung des frühen 21. Jahrhunderts ist enorm dynamisch: Urbane Räume entstehen, wachsen und
verändern sich, ihr Wandel verläuft zunehmend diskontinuierlich und disparat. Wir untersuchen die Dimensionen des
urbanen Wandels auf unterschiedlichen Maßstabsebenen und international vergleichend und gewinnen im aktiven Dialog mit
Praxis, Politik und Gesellschaft Erkenntnisse für eine nachhaltige Transformation und Gestaltung urbaner Räume.

Webseite: https://www.ils-forschung.de/ · GitLab: https://gitlab.com/ils-research

Auf GitHub teilen wir Software, die in unserer Forschung und im Arbeitsalltag entsteht, soweit sie anderen nützt.

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
| [**Semantic Scholar Bridge**](https://github.com/ILS-Research/semantic-scholar-api-key-bridge-for-semantic-zotero) | Teilt einen Semantic-Scholar-API-Schlüssel mit einer Gruppe (Institut, Labor, Kurs), damit Werkzeuge wie Semantic Zotero oder MCP-Server funktionieren, ohne dass jede Person einen eigenen Schlüssel beantragt. |

SeekChat, SeekBook und ZotSeek arbeiten zusammen: SeekChat nutzt ZotSeek und SeekBook als Suchquellen, wenn sie
installiert sind, und findet die Literaturliste eines Dokuments über Find Online References.

### Forks mit unseren Ergänzungen

Diese Plugins stammen von anderen; unsere Forks ergänzen, was wir brauchten. Urheberschaft und Lizenzen bleiben bei den
ursprünglichen Autor*innen.

| Fork | Original | Was wir geändert haben |
|---|---|---|
| [**ZotSeek**](https://github.com/ILS-Research/ZotSeek) | [introfini/ZotSeek](https://github.com/introfini/ZotSeek) (José Fernandes, MIT) | Embeddings von einem ausdrücklich freigegebenen Server im eigenen Netz (z. B. GPU-Rechner), optional Buchtreffer aus SeekBook. |
| [**Find Online References**](https://github.com/ILS-Research/zotero-find-online-references) | [MuiseDestiny/zotero-reference](https://github.com/MuiseDestiny/zotero-reference) (AGPL-3.0) | Läuft mit Zotero 7 bis 10 und bietet eine Schnittstelle für andere Plugins (SeekChat liest darüber Literaturlisten und importiert Quellen). Experimentell, nicht zu 100 % verlässlich. |
| [**Semantic Zotero**](https://github.com/ILS-Research/semantic-zotero) | [AgiNetz/semantic-zotero](https://github.com/AgiNetz/semantic-zotero) (MIT) | Branch zur Nutzung mit der Semantic Scholar Bridge. |

## Daten des öffentlichen Verkehrs

| Werkzeug | Was es macht |
|---|---|
| [**delfi-dataset-fixer**](https://github.com/ILS-Research/delfi-dataset-fixer) | Jupyter-Notebook, das den bundesweiten Fahrplandatensatz (DELFI, GTFS) so repariert, dass Routing-Software wie OpenTripPlanner ihn laden kann: Es löscht Haltestellen ohne ID, setzt Haltezeiten auf die übergeordnete Station, wenn eine Haltestelle den falschen Typ hat, entfernt Umstiege zu nicht vorhandenen Haltestellen und schreibt eine bereinigte GTFS-Zip. Das Notebook steht unter MIT-Lizenz, der DELFI-Datensatz hat eine eigene Lizenz. |

## Mitwirken

Rückmeldungen und Fehlermeldungen bitte als Issue im jeweiligen Repository.
