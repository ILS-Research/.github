# ILS – Research Institute for Regional and Urban Development

**English** · [Deutsch](README.de.md)

## Who we are

The ILS (Institut für Landes- und Stadtentwicklungsforschung gGmbH) in Dortmund, Germany, does spatial urban research.
The urbanisation of the early 21st century is enormously dynamic: urban spaces emerge, grow and change, and their
transformation is increasingly discontinuous and disparate. We investigate the dimensions of urban change at different
scales and in international comparison, and in active dialogue with practitioners, policy-makers and society we turn
the findings into insights for the sustainable transformation and design of urban spaces.

Website: https://www.ils-forschung.de/en/

On GitHub we share software we develop in our research and daily work, as far as it is useful to others.

## Zotero plugins

AI tools for [Zotero](https://www.zotero.org) that keep your data in your own infrastructure: search and language
models run on your computer or on a server **you** operate (for example [Ollama](https://ollama.com)); nothing goes to a
cloud service unless you explicitly allow a server. All work with Zotero 7 to 10 (recommended: 10).

### Our own plugins

| Plugin | What it does |
|---|---|
| [**SeekChat**](https://github.com/ILS-Research/seekchat-zotero) | Chat with your PDFs, web pages, EPUBs and text files, or with a whole collection. Answers cite their sources; every citation links to the exact page. A tool chat does things in Zotero for you: import references from pasted text, search the library, save items to collections, show and link a paper's references. Changes are only made after you confirm a preview. |
| [**SeekBook**](https://github.com/ILS-Research/seekbook-zotero) | Full-text index for books and long documents (30+ pages), searchable by meaning and keyword, with chapter and printed page number for every passage. Used through SeekChat and ZotSeek. |
| [**Semantic Scholar Bridge**](https://github.com/ILS-Research/semantic-scholar-api-key-bridge-for-semantic-zotero) | Shares one Semantic Scholar API key with a group (institute, lab, course), so tools such as Semantic Zotero or MCP servers work without everyone applying for a personal key. |

SeekChat, SeekBook and ZotSeek work together: SeekChat uses ZotSeek and SeekBook as search sources when they are
installed, and finds a document's reference list through Find Online References.

### Forks with our additions

These plugins are written by others; our forks add what we needed. Credit and licences stay with the original authors.

| Fork | Original | What we changed |
|---|---|---|
| [**ZotSeek**](https://github.com/ILS-Research/ZotSeek) | [introfini/ZotSeek](https://github.com/introfini/ZotSeek) (José Fernandes, MIT) | Embeddings from an explicitly allowed server in your network (e.g. a GPU machine), optional book results from SeekBook. |
| [**Find Online References**](https://github.com/ILS-Research/zotero-find-online-references) | [MuiseDestiny/zotero-reference](https://github.com/MuiseDestiny/zotero-reference) (AGPL-3.0) | Runs on Zotero 7 to 10 and offers an API other plugins can use (SeekChat reads reference lists and imports sources through it). Experimental, not 100 % reliable. |
| [**Semantic Zotero**](https://github.com/ILS-Research/semantic-zotero) | [AgiNetz/semantic-zotero](https://github.com/AgiNetz/semantic-zotero) (MIT) | Branch for use with the Semantic Scholar Bridge. |

## Public transport data

| Tool | What it does |
|---|---|
| [**delfi-dataset-fixer**](https://github.com/ILS-Research/delfi-dataset-fixer) | Jupyter notebook that repairs the nationwide German timetable data set (DELFI, GTFS format) so routing software such as OpenTripPlanner can load it: it drops stops without an ID, points stop times at the parent station where a stop has the wrong location type, removes transfers to stops that do not exist, and writes a fixed GTFS zip. The notebook is MIT-licensed; the DELFI data set has its own licence. |

## Contributing

Feedback and bug reports are welcome as issues in the respective repository.
