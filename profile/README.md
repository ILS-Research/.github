# ILS – Research Institute for Regional and Urban Development

**English** · [Deutsch](https://github.com/ILS-Research/.github/blob/main/profile/README.de.md)

## Who we are

The ILS (Institut für Landes- und Stadtentwicklungsforschung gGmbH) in Dortmund, Germany, does spatial urban research.
The urbanisation of the early 21st century is enormously dynamic: urban spaces emerge, grow and change, and their
transformation is increasingly discontinuous and disparate. We investigate the dimensions of urban change at different
scales and in international comparison, and in active dialogue with practitioners, policy-makers and society we turn
the findings into insights for the sustainable transformation and design of urban spaces.

Website: https://www.ils-forschung.de/en/ · GitLab: https://gitlab.com/ils-research

**GitHub is not everything we publish.** Here you find a selection, mainly our Zotero plugins. More of our code lives on GitLab, in our main group: **https://gitlab.com/ils-research**.

## Zotero plugins

AI tools for [Zotero](https://www.zotero.org) that keep your data in your own infrastructure: search and language
models run on your computer or on a server **you** operate (for example [Ollama](https://ollama.com)); nothing goes to a
cloud service unless you explicitly allow a server. All work with Zotero 7 to 10 (recommended: 10).

### Our own plugins

| Plugin | What it does |
|---|---|
| [**SeekChat**](https://github.com/ILS-Research/seekchat-zotero) | Chat with your PDFs, web pages, EPUBs and text files, or with a whole collection. Answers cite their sources; every citation links to the exact page. A tool chat does things in Zotero for you: import references from pasted text, search the library, save items to collections, show and link a paper's references. Changes are only made after you confirm a preview. |
| [**SeekBook**](https://github.com/ILS-Research/seekbook-zotero) | Full-text index for books and long documents (30+ pages), searchable by meaning and keyword, with chapter and printed page number for every passage. Used through SeekChat and ZotSeek. |
| [**Zotero Custom Cloud Modifier**](https://gitlab.com/ils-research/zotero-plugins/zotero-custom-cloud-modifier) | For people who run their own Zotero server instead of syncing with zotero.org: points Zotero at your server and sends links that would go to zotero.org (new group, view online, create account) to your own portal. You build it once for your server and hand the XPI to your users. Works with our [zotero-selfhost](https://github.com/ILS-Research/zotero-selfhost). |

SeekChat, SeekBook and ZotSeek work together: SeekChat uses ZotSeek and SeekBook as search sources when they are
installed, and finds a document's reference list through Find Online References.

The [**Semantic Scholar Bridge**](https://github.com/ILS-Research/semantic-scholar-api-key-bridge-for-semantic-zotero), which shares one Semantic Scholar API key with a group so that tools such as Semantic Zotero work without personal keys, is a server component and is listed under [Self-hosting](#self-hosting). The same goes for our Zotero server stack.

### Forks with our additions

These plugins are written by others; our forks add what we needed. Credit and licences stay with the original authors.

| Fork | Original | What we changed |
|---|---|---|
| [**ZotSeek**](https://github.com/ILS-Research/ZotSeek) | [introfini/ZotSeek](https://github.com/introfini/ZotSeek) (José Fernandes, MIT) | Embeddings from an explicitly allowed server in your network (e.g. a GPU machine), optional book results from SeekBook. |
| [**Find Online References**](https://github.com/ILS-Research/zotero-find-online-references) | [MuiseDestiny/zotero-reference](https://github.com/MuiseDestiny/zotero-reference) (AGPL-3.0) | Runs on Zotero 7 to 10 and offers an API other plugins can use (SeekChat reads reference lists and imports sources through it). Experimental, not 100 % reliable. |
| [**Semantic Zotero**](https://github.com/ILS-Research/semantic-zotero) | [AgiNetz/semantic-zotero](https://github.com/AgiNetz/semantic-zotero) (MIT) | Branch for use with the Semantic Scholar Bridge. |

## Spatial analysis tools

Hosted on GitLab, in our main group.

| Tool | What it does |
|---|---|
| [**dominant-mobility-classifier**](https://gitlab.com/ils-research/dominant-mobility-classifier) | QGIS plugin (experimental) that classifies neighbourhoods as walking, transit or car-dependent, based on proximity of facilities, land-use mix, green space, the pedestrian network and frequent public transport. Uses OpenStreetMap, the OpenRouteService plugin and a GTFS data set. |
| [**os-walk-eu**](https://gitlab.com/ils-research/os-walk-eu) | QGIS plugin OS-WALK-EU (Open Source Walkability Tool for European Union Member States), developed with researchers from Ireland, Portugal and Italy. It calculates the walkability of a residential neighbourhood (default 500 m walking distance) from facilities and land-use data of OpenStreetMap and walking distances from OpenRouteService, as an index from 0 to 100. [Story map with usage, interpretation and limits](https://storymaps.arcgis.com/stories/abca15a2477843ca9e78fe1edd7ecab8) (German). |
| [**flaechenampel_gfz_converter**](https://gitlab.com/ils-research/flaechenampel_gfz_converter) | Python module that calculates mean floor area ratios (GFZ) for development plans from an XPlanung database (PostgreSQL). |

## Public transport data

| Tool | What it does |
|---|---|
| [**delfi-dataset-fixer**](https://github.com/ILS-Research/delfi-dataset-fixer) | Jupyter notebook that repairs the nationwide German timetable data set (DELFI, GTFS format) so routing software such as OpenTripPlanner can load it: it drops stops without an ID, points stop times at the parent station where a stop has the wrong location type, removes transfers to stops that do not exist, and writes a fixed GTFS zip. The notebook is MIT-licensed; the DELFI data set has its own licence. |

## Self-hosting

Server components and Docker Compose setups for running software on your own infrastructure.

| Project | What it does |
|---|---|
| [**zotero-selfhost**](https://github.com/ILS-Research/zotero-selfhost) | A self-hosted Zotero sync server without AWS dependency: dataserver, stream server, web library, S3-compatible file storage and a portal with login (password or OpenID Connect) and user and group management. The official Zotero desktop client syncs against it after changing two settings. Pairs with the Zotero Custom Cloud Modifier above. Looking for a solution that is likely to be maintained long term? Take a look at [altero](https://github.com/eseifert/altero) by Erich Seifert, an independent self-hosted sync server for the unmodified Zotero client (AGPL-3.0, currently beta). |
| [**Semantic Scholar Bridge**](https://github.com/ILS-Research/semantic-scholar-api-key-bridge-for-semantic-zotero) | Shares one Semantic Scholar API key with a group (institute, lab, course), so tools such as Semantic Zotero or MCP servers work without everyone applying for a personal key. |
| [**openqda-composestack**](https://github.com/ILS-Research/openqda-composestack) | Docker Compose setup for [OpenQDA](https://github.com/openqda/openqda), an open-source tool for qualitative data analysis, together with MySQL and Redis. The image is built from the upstream repository at a configurable Git ref; this repository contains only the deployment tooling. |

## Contributing

Feedback and bug reports are welcome as issues in the respective repository.
