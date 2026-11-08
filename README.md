# StruTrix Studio

**StruTrix Studio** is professional Windows software by RamisoftSolutions for the structural analysis and design of
three-dimensional frames: buildings, industrial structures, pipe racks, towers, trusses, portal frames and transmission
poles. It analyses every load combination to first order or by the AISC 360-22 direct analysis method, designs every steel
member to AISC 360-22 by LRFD or ASD, analyses structures built in stages, designs seismic force-resisting systems to
ANSI/AISC 341-22, and audits every result's equilibrium. The analysis and the steel design are free, with no limit on model
size or time and no account required.

**Latest version: 1.105 (November 7, 2026).** [Website](https://www.strutrix.com/) ·
[Features](https://www.strutrix.com/features/) · [What's new](https://www.strutrix.com/whats-new/) ·
[Changelog](CHANGELOG.md) · [Microsoft Store](https://apps.microsoft.com/detail/9PM7B70ZXWRC)

> This README describes the program as of its latest version. The website, https://www.strutrix.com, is the complete and
> authoritative description of what the program does, with its limits stated plainly on the features page. This
> repository holds the website's source and the program's public issue tracker; the program's own source is private.

## What StruTrix Studio does

- **Any frame in 3D**, drawn member by member with drafting precision (work planes, set-out grid lines, object snaps,
  typed coordinates in feet and inches) or generated from a few dimensions: building frames, trusses, portal frames,
  circular grids, and (Pro) tapered transmission poles and H-frames.
- **Supports and connections**: supports fixed, pinned or on springs, one-way springs, imposed displacements, end releases
  and partial fixity, rigid end offsets and rigid links, tension-only and compression-only members, and rigid diaphragms.
- **Loads**: joint, member, projected, area and thermal loads and self-weight, in basic load cases by ASCE 7-22 category;
  the ASCE 7-22 combination generator for strength, allowable stress and service combinations, with notional loads.
- **Analysis**: first-order, or the AISC 360-22 direct analysis method (P-Delta and P-delta, reduced stiffness, notional
  loads) chosen per combination, on every core of the computer, with an independent equilibrium audit of every combination.
- **Staged construction analysis** (Pro): an addition to an existing structure, or a structure built in any number of
  construction stages, analysed the way it is built. Each stage's loads are carried by the structure standing then, every
  member carrying its axial force and deformed shape into the next stage, and new members fitted unstressed to where the
  structure stands. A conventional analysis of the structure built at once lets new members share loads the existing ones
  were carrying before they were there, which understates the forces in the existing members and misplaces the load
  distribution; in the User's Manual's own example it puts the existing columns' axial force 36% low.
- **AISC 360-22 steel design** by LRFD and ASD at points no more than six inches apart, unbraced lengths found from the
  structure, Optimise for the lightest section of each group that passes, net deflection checks, and a member detail that
  works every check equation by equation with its clause.
- **Seismic design by ANSI/AISC 341-22** (Pro), with the seismic requirements of ASCE 7-22: ordinary, intermediate and
  special moment frames, cantilever column systems, ordinary and special concentrically braced frames, eccentrically
  braced frames, buckling-restrained braced frames and dual systems; the equivalent lateral force, story drift and
  stability; the capacity-limited analyses; the member side of ANSI/AISC 358-22 prequalified moment connections; the
  required strengths of column bases, splices and connections; and what the construction documents must show, with the
  protected zones drawn on the model.
- **Transmission structures** (Pro): tapered round and polygonal tubes designed to ASCE/SEI 48-19, and transmission line
  design: line loading by the NESC, ASCE MOP 74 and MOP 113, conductors' sag and tension, insulator swing, NESC clearances,
  and line security and construction loads.
- **The structure link** (Pro): FoundaTrix Studio and PileTrix Studio read a saved structure's support reactions from the
  same cloud job, as footing loads or a pile's head loads.
- **Reports and exchange**: a typeset calculation report (free; the firm's name and logo on it Pro), export to IFC 4.3 and
  to Revit as native structural framing (Pro), and tables that take a paste from a spreadsheet and copy out.
- **Cloud and AI** (free account): cloud jobs shared with FoundaTrix Studio and PileTrix Studio, version history, and a
  connector through which your own AI assistant creates structures and runs what-if analyses that only you apply.

## New in version 1.105

- Staged construction analysis in the Microsoft Store: an addition to an existing structure, or any number of stages.
- Seismic design by AISC 341-22, with ASCE 7-22's equivalent lateral force, story drift and stability.
- Rigid diaphragms.
- The support reactions read by FoundaTrix Studio and PileTrix Studio.
- The User's Manual rearranged, with pictured tutorials of a staged construction analysis and a seismic design.

Every release's notes are in [CHANGELOG.md](CHANGELOG.md) and on the website's
[What's new](https://www.strutrix.com/whats-new/) page.

## Common questions

- **Does StruTrix Studio do staged construction analysis?** Yes, since version 1.105 in the Microsoft Store, as a Pro
  feature: an addition to an existing structure, or a structure built in any number of construction stages, each stage
  analysed on the structure standing then, first-order or by the direct analysis method.
- **Does it design for seismic loads?** Yes: seismic force-resisting systems are designed to ANSI/AISC 341-22 with
  ASCE 7-22's equivalent lateral force, drift and stability (Pro). It does not run a modal response spectrum or
  time-history analysis.
- **Is it free?** The modelling, the loads, the combinations, the analysis, the AISC 360-22 steel design and the
  calculation report are free, with no limit on model size or time, no watermark and no account. It is professional
  software for real projects, not a student or evaluation edition. The Pro features are a separate set, free to try.
- **What does it not do?** Plates, walls and solids, dynamics, material nonlinearity, concrete, wood and cold-formed
  steel design, and the design of connections' plates, bolts and welds. The website's features page lists every limit.

## About this repository

This repository is the public source for the product website of StruTrix Studio, www.strutrix.com. Its **Issues** are
also the public place to report a bug in the program or ask for a feature: see
[Reporting bugs and requesting features](#reporting-bugs-and-requesting-features).

**With every Store release**, update together: a new card on top of `src/whats-new/index.html`, the same notes on top of
[CHANGELOG.md](CHANGELOG.md), this README's "Latest version", "What StruTrix Studio does", "New in version" and "Common
questions", `src/llms.txt`, and the repository's GitHub description and topics where the headline features change. AI
search tools read this README as the program's description, so a feature missing here reads to them as a feature the
program lacks.

## Scope of this repository

This repository contains **only the static website** (`src/`): HTML, CSS, a small script and SVG artwork, plus the
GitHub configuration that makes its Issues usable as a public support channel.

**It does not contain, and will never contain, any StruTrix Studio application source code.** The desktop program, its
engine and its cloud service are developed in a separate, private repository. Nothing here requires or exposes that
source: no engine code, no model files, no cloud configuration, no build output of the program.

## Reporting bugs and requesting features

- **Bug reports and feature requests (public):** open an [issue](../../issues/new/choose) and pick the template that
  fits.
- **Private matters** (confidential project data, licensing, security): email `admin@ramisoftsolutions.com`. Please do
  not attach a client's model to a public issue.
- **Version details:** in the program, **Help > About > Copy details** copies the version, the build and how the
  program was installed. Paste them into the issue.

## Site map

| Path | File | What it is |
|---|---|---|
| `/` | `src/index.html` | Home: what the program does, the newest release's features (staged construction analysis `#staged`, seismic design `#seismic`), the frames it generates, the free analysis and design, Pro, the structure link (`#link`), what is coming soon (multi-storey buildings and the pushover), your AI assistant, plans, download, support |
| `/whats-new/` | `src/whats-new/index.html` | Every Store release, newest first: a new `article.release` card goes on top with each release (the newest marked `release--latest`), its lines from the release's Store "What's new" and the manual's version history |
| `/features/` | `src/features/index.html` | The engineering in detail: the model, loads, combinations, analysis, staged construction, results, steel design, seismic design, tapered tubes, line loading, data, cloud, the structure link, the AI assistant, limits, validation, references |
| `/pricing/` | `src/pricing/index.html` | Free, signed in, and Pro, with a comparison table and questions |
| `/support/` | `src/support/index.html` | Where to report a bug, ask for a feature or write privately |
| `/privacy/` | `src/privacy/index.html` | Privacy policy |
| `/terms/` | `src/terms/index.html` | Terms of use, including the engineering disclaimer |
| (any 404) | `src/404.html` | Not-found page |

`styles.css` and `site.js` are the family's shared files, the same as FoundaTrix Studio's site (www.foundatrix.com) and
PileTrix Studio's (www.piletrix.com), so the three product sites read as one family; StruTrix Studio's few additions sit at the
end of `styles.css` under their own heading. A change to a shared rule belongs in all three sites. The pages are
hand-written HTML with no build step and no framework. The site uses no cookies, analytics, trackers or third-party
scripts, fonts or images: everything it loads comes from its own folder.

**Every `href` and `src` is root-absolute** (`/styles.css`, `/images/...`, `/pricing/`). The pages live in folders, so a
relative path that works from `/` breaks from `/pricing/`, and for a stylesheet it fails silently: the page still
renders, unstyled.

**No inline styles or scripts.** `staticwebapp.config.json` sends a content security policy with `style-src 'self'` and
`script-src 'self'`, so a `style=` attribute or a script body is ignored by the browser. The one `<script>` with a body is
the home page's JSON-LD block (`application/ld+json`), which is data and is not executed. The SVG artwork uses
presentation attributes only.

## Copy rules

- The company is **RamisoftSolutions**, one word.
- No other company's program is named; where a comparison is needed, the word is "reference".
- Features that are available to administrators only in the program are not advertised. Add them the day they open to
  customers.
- Pricing follows the program's words: free, signed in, Pro, free trial; Pro pricing "to be announced"; no promise of
  anything free for ever. The trial's length is not stated, because the program counts it from the first sign-in to
  StruTrix Studio and its length is a server setting.
- The emphasis is on what the program computes, end to end, and on its engineering accuracy.
- No connection details of the AI-assistant connector (no address, no client id) anywhere.
- Fictional project, client and site names only in any picture or example.

## Pictures

Since 2026-11-07 four pictures are **real captures**, taken from the User's Manual's own tutorial pictures
(`Strutrix/Strutrix.UI/ManualImages` in the program's repository, fictional models, the dark theme) and saved as WebP: `staged-axial-as-built.webp`
and `staged-axial-at-once.webp` (Home `#staged`, the manual's section 13.3 step 8 and 9, side by side), `staged-moment-final.webp`
(Home `#staged`) and `seismic-protected-zones.webp` (Home `#seismic`, section 13.4, cropped of its caption row, its empty command line
and its status line). Choose pictures of the model and of results drawn on it; a table of numbers says nothing to a visitor at a
glance (owner, 2026-11-07). The other product pictures are SVG illustrations drawn in the
program's dark theme from its real layout (the ribbon's tabs, the dock panes, the tables' columns), inside a `.shot`
frame whose bar stands in for the window's caption. Replace each with a real capture when one exists:

| Illustration | Used on | The real screenshot it stands for |
|---|---|---|
| `src/images/screens/studio-overview.svg` | Home (below the hero) | The Design tab on a braced building coloured by utilisation, a column selected, the Model Explorer, Properties and Command Line panes |
| `src/images/screens/modelling.svg` | Home `#features` | The Model tab: the drafting grid and set-out grid lines, a member being drawn to a snap, the Generate menu open |
| `src/images/screens/area-loads.svg` | Home `#features` | The Loads tab: a two-way area load drawn on its beams, and the Combinations table after Generate |
| `src/images/screens/direct-analysis.svg` | Home `#features` | The Results tab: a direct analysis combination on its deformed shape, coloured by moment |
| `src/images/screens/steel-design.svg` | Home `#features` | The Design tab: a frame coloured by utilisation above the Steel Design table |
| `src/images/screens/member-diagrams.svg` | Home `#features`, Features `#results` | Results > Diagram: the moment envelope on every member in the 2D view, and the Member Diagram pane |
| `src/images/screens/tapered-tubes.svg` | Home `#tubes`, Features `#tubes` | An H-frame of tapered tubes coloured by utilisation, beside the Steel Checks table filtered to one shaft |
| `src/images/screens/bim-export.svg` | Home `#pro` | The exported IFC in a BIM viewer (its branding cropped out), with the export's summary |
| `src/images/screens/calc-report.svg` | Features `#data` | Two pages of the calculation report on the app's background (never a PDF reader's window) |

`src/llms.txt` is a plain-text summary of the program for AI tools (the llms.txt convention), served at https://www.strutrix.com/llms.txt; keep it to what the pages say.

Not screenshots to replace: `src/images/screens/structure-link.svg` (a diagram of the link: a frame's reactions read by
FoundaTrix Studio and PileTrix Studio; unused while the link is in Coming soon, kept for its return to Home `#link`) and `src/images/assistant-frame.svg` (a generic assistant conversation, deliberately not
any one assistant's interface, creating a building frame through the connector with the tool names the endpoint really
exposes, in the fictional job "Sample Distribution Centre").

When replacing one: a fictional project and client only (never a real one), a dark-theme window of about 1500 x 1000,
cropped below the caption row, saved as WebP at quality 84 to 86 in `src/images/screens/`; then update the `<img>`
`src`, `width`, `height` and `alt`.

Artwork: `src/images/strutrix-mark.svg` (the nav and footer mark) and `src/favicon.svg` (the small mark) are drawn in the
family's style, the navy plate, the isometric lavender faces and the teal ground grid of the FoundaTrix Studio and
PileTrix Studio marks: a one-bay steel frame braced on its front face, a lateral load on its corner. The program's own mark
arrives with its Store package; when it does, convert its `Logo.xaml` and `Logo.Small.xaml` into these two files, as
the sister sites did. `src/images/hero-frame.svg` (the hero) and `src/images/types/*.svg` (the six frames the Generate
menu builds) are illustrations.

## Values still to settle

| What | Where | Now |
|---|---|---|
| Microsoft Store link | `src/index.html`, `#download`; every "Download free" button goes to `/#download` | Listed since 2026-11-01 (Store ID 9PM7B70ZXWRC): the panel's button and the pricing FAQ link to https://apps.microsoft.com/detail/9PM7B70ZXWRC (the announce bar announces the newest release and links `/whats-new/` since 2026-11-07); every "Download free" button goes to `/#download`. `.store-btn--soon` stays in the stylesheet unused; `.badge--soon` marks the Coming soon cards' state (Planned, Next release) |
| The Pro split | Home `#pro`, `#plans`; `/pricing/` | Stated as the program's premium catalogue has it: tapered tubes (with the Pole and H-Frame generators), IFC and Revit export, the firm on the report, search by a structure's inputs, and the structure link; everything else free |
| The structure link | Home `#link` (art `src/images/screens/structure-link.svg`), `#pro`, `#plans`; Features `#link`; `/pricing/` | Shipped: both readers went live in the Microsoft Store on 2026-11-07 (FoundaTrix Studio 1.168, PileTrix Studio 12.029), after the API redeploy and the structure migrations. The sections came back with issue 87's corrections (by category D, L, Lr, S, R, W and E; a combination with overstrength and a service combination offered to neither reader; the plane chosen in PileTrix Studio). `src/images/soon/structure-link.svg` is unused since, kept with the Coming soon art |
| Staged construction analysis and seismic design | Home `#staged` and `#seismic`, `#pro`, `#plans`; Features `#staged`, `#seismic`, `#limits`; `/pricing/`; `/whats-new/` | Shipped in StruTrix Studio 1.105 (in the Store as 1.1.5.0, 2026-11-07), both Pro. The staged comparison's numbers are the User's Manual's tutorial (section 13.3): 13.2 against 20.6 kip in the existing columns (36% low), 39.6 against 24.7 kip in the new column (60% high), the governing ratio 0.48 against 0.30, the beam's existing sag 49.9 kip-ft. Change them only with the tutorial. `src/images/soon/staged-construction.svg` is unused since |
| Multi-storey buildings from typical floors | Home `#soon` (its card is `#building`, art `src/images/soon/building-modeler.svg`), `#plans`; `/pricing/` (the Signed in plan and the comparison's Modelling and loads row) | In Coming soon since 2026-11-07 ("Planned", Free account): the plan is approved (LateralPile issue 90) and not started. A free feature for a signed-in engineer; a building still in the modeller is saved to the cloud only. When it ships, move it into the Features page and the Home features, and take "(coming soon)" off the Signed in plan and the comparison row |
| Free, with no limits, for real projects | Home: the announce bar (beside the newest release), the hero's assurances, `#free` (two tiles: No limit on model size, Made for real projects), the Free plan; `/pricing/`: the headline, the Free plan, three questions (model size, real projects, a catch); the descriptions of Home, Features and Pricing; `src/llms.txt`; the JSON-LD on Home and `/pricing/` | Stated on 2026-11-07 at the owner's word (AI search tools had read "free to start" as a limited or educational edition). Each claim was checked in the program: no cap on joints, members, cases or combinations (a generator makes up to 20,000 members a run and its preview draws up to 2,000; neither limits a model); no watermark (the report never draws one); the terms restrict no commercial use; developed and timed on the 9,723-member building of `tools/StrutrixPerf`. The Pro features are a separate set and stay named as such. The FAQ's JSON-LD is worked from the page's own questions: change a question, change the block. Never write "free to start" again |
| The assistant connector | Home `#connect`; Features `#connect` | Advertised as the program's manual describes it |

The privacy policy and terms of use follow the sister programs' (www.foundatrix.com/privacy, www.piletrix.com/privacy),
adapted to what StruTrix Studio does (effective October 26, 2026). When the program's Store folder gains its own
`PrivacyPolicy.md` and `TermsOfUse.md`, keep them and these pages one text.

## Local preview

There is no build step. Because the links are root-absolute, serve `src/` with any static file server rather than
opening the files directly, for example:

```bash
python -m http.server 8080 --directory src
```

then open `http://localhost:8080/`.

## Deployment

The site is hosted on **Azure Static Web Apps** (Free plan), as its sister sites are: the app `swa-strutrix-site` in the
resource group `rg-lateralpile`, region West US 2 (tags `product: StruTrix Studio`, `purpose: website`), default host
`black-pebble-0c68c441e.6.azurestaticapps.net`, stable inbound IP `20.29.155.69`. Every push to `main` publishes `src/`
through `.github/workflows/deploy.yml`, which authenticates with the repository secret `AZURE_STATIC_WEB_APPS_API_TOKEN`
(the app's deployment token, set 2026-10-26; without it the job deploys nothing and says so). Pull requests are not
deployed. `src/staticwebapp.config.json` sets trailing slashes, the 404 page and the security headers, including a content
security policy. If the deployment token is ever rotated in Azure, set the repository secret again.

| Address | DNS at GoDaddy | Role |
|---|---|---|
| `https://www.strutrix.com` | `CNAME www` to `black-pebble-0c68c441e.6.azurestaticapps.net` (validated by the CNAME itself) | Primary (canonical) address; Ready, its certificate issued, 2026-10-26 |
| `https://strutrix.com` | `TXT @` with the app's validation token, and `A @` to `20.29.155.69` (the domain's parked A record replaced) | Ready 2026-10-26; redirects to `www` (301, path kept) |
| `black-pebble-0c68c441e.6.azurestaticapps.net` | (Azure's own) | Redirects to `www` (301, path kept) |

`www` is the default domain, set in the Azure portal (the app's Custom domains page, "Set default", which has no CLI
command) on 2026-10-26. The portal keeps a hint "Add a CNAME, ALIAS or A record" beside the apex even with its A record in
place; the apex resolves to the app and redirects, so the hint needs nothing. The canonical links, `og:url`, `robots.txt` and `sitemap.xml` all name `https://www.strutrix.com`.

## Contributing

Typo fixes and copy improvements are welcome by pull request; see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT for the website's source and content (see [LICENSE](LICENSE)). The StruTrix Studio program itself is separate,
closed-source software under its own terms. "StruTrix Studio" and its mark are not licensed for reuse by the MIT
license.
