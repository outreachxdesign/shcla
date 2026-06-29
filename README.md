# SHCLA Interactive Toolkit

Interactive data explorers and storytelling tools for the **Supportive Housing Community Land Alliance (SHCLA)**, prepared by **Outreach by Design**. Each tool is a self-contained HTML page that opens in any modern browser, no download or install required.

**Live site:** https://outreachxdesign.github.io/shcla/

The landing page (`index.html`) links to every tool. The links below point to the live pages once GitHub Pages is enabled (see *Hosting* at the bottom).

---

## Tools

### The Model — how the SHCLA model works
| Tool | Live link | Source file shared |
| --- | --- | --- |
| The Common System vs the SHCLA Model | `/model/system-comparison/` | TOC_Model_Interactive.html |
| Marcus's Path | `/model/marcus-path/` | TOC_Model_Game.html |

### The Population — who SHCLA serves
| Tool | Live link | Source file shared |
| --- | --- | --- |
| Behind Every Number, a Person Without a Home | `/population/behind-every-number/` | Behind_Every_Number.html |
| CHIS Data Explorer | `/population/chis-explorer/` | CHIS_Explorer.html |
| HMIS Data Explorer | `/population/hmis-explorer/` | HMIS_Explorer.html |
| Adults in the Homelessness System | `/population/hmis-analysis/` | HMIS_Analysis.html |

### The Neighborhood — the place and its geography
| Tool | Live link | Source file shared |
| --- | --- | --- |
| A Neighborhood Worth Choosing | `/neighborhood/neighborhood-choice/` | Full_Story.html |
| Oakland Community Need Map | `/neighborhood/community-need-map/` | Oakland_Blockgroups.html |
| Oakland Block Groups Explorer | `/neighborhood/block-groups/` | Oakland_neighborhood_comparison.html |

> Note: `Neighborhood_Choice.html` was identical to `Full_Story.html`, so only one copy is included. A stray `SHCLA_TOC_Model_Interactive.html` duplicated `TOC_Model_Interactive.html` and was not included.

---

## Folder structure

Each tool lives in its own folder as `index.html`, so its URL is the clean folder path (the trailing slash serves `index.html` automatically). This means a tool can be updated by replacing the file inside its folder **without changing the link** already placed in the toolkit.

```
/
├── index.html                         landing page (links every tool)
├── README.md                          this file
├── model/
│   ├── system-comparison/index.html
│   └── marcus-path/index.html
├── population/
│   ├── behind-every-number/index.html
│   ├── chis-explorer/index.html
│   ├── hmis-explorer/index.html
│   └── hmis-analysis/index.html
└── neighborhood/
    ├── neighborhood-choice/index.html
    ├── community-need-map/index.html
    └── block-groups/index.html
```

## Updating a tool

Replace the `index.html` inside the relevant folder with the new version (same filename). The live link stays the same. Changes appear within about a minute of committing.

---

## A few things to know

**Internet connection required.** Every tool loads its fonts from Google Fonts. A few load mapping or charting libraries from public CDNs (Leaflet for the maps, D3 for the homelessness-system flow diagram). The pages will not look right offline.

**Some maps pull live public data at view time.** *A Neighborhood Worth Choosing* and *Oakland Community Need Map* query free OpenStreetMap services (Overpass and Nominatim) when they load. They work without any key, but if a map is slow or a layer is briefly missing, that is the public service rate-limiting, not the page. For a guaranteed-fast version, the queried data could be saved into the file instead of fetched live as a future enhancement.

**Data is aggregate and de-identified.** The CHIS tools use published survey indicators. The HMIS tools use aggregate counts of distinct individuals from a UC Berkeley data request (adults 18–59, Jan 2023–Apr 2026); no person-level records are embedded.

**Brand pass pending.** The landing page uses a palette drawn from the existing tools as a neutral starting point. SHCLA may update brand colors, logos, and typography in a future revision.

---

*Prepared by Outreach by Design for SHCLA.*

## Hosting (GitHub Pages)

After the files are committed, enable Pages once:

1. Repository **Settings → Pages**
2. **Source:** Deploy from a branch
3. **Branch:** `main`, folder `/ (root)` → **Save**

The site goes live at `https://outreachxdesign.github.io/shcla/` within a minute or two. The repository must be **Public** for free GitHub Pages.
