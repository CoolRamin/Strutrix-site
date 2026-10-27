# Strutrix Studio Website

Public source for the product website of **Strutrix Studio**, a Windows desktop program by RamisoftSolutions for the
structural analysis and design of three-dimensional frames: buildings, industrial structures, pipe racks, towers,
trusses, portal frames and transmission poles. It analyses every load combination to first order or by the AISC 360-22
direct analysis method, designs every steel member to AISC 360-22 by LRFD or ASD, generates the ASCE 7-22 load
combinations, audits every result's equilibrium, and hands its support reactions to FoundaTrix Studio and PileAxis.

This repository's **Issues** are also the public place to report a bug in the program or ask for a feature: see
[Reporting bugs and requesting features](#reporting-bugs-and-requesting-features).

## Scope of this repository

This repository contains **only the static website** (`src/`): HTML, CSS, a small script and SVG artwork, plus the
GitHub configuration that makes its Issues usable as a public support channel.

**It does not contain, and will never contain, any Strutrix Studio application source code.** The desktop program, its
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
| `/` | `src/index.html` | Home: what the program does, the frames it generates, the free analysis and design, Pro, the structure link, your AI assistant, plans, download, support |
| `/features/` | `src/features/index.html` | The engineering in detail: the model, loads, combinations, analysis, results, steel design, tapered tubes, line loading, data, cloud, the link, limits, validation, references |
| `/pricing/` | `src/pricing/index.html` | Free, signed in, and Pro, with a comparison table and questions |
| `/support/` | `src/support/index.html` | Where to report a bug, ask for a feature or write privately |
| `/privacy/` | `src/privacy/index.html` | Privacy policy |
| `/terms/` | `src/terms/index.html` | Terms of use, including the engineering disclaimer |
| (any 404) | `src/404.html` | Not-found page |

`styles.css` and `site.js` are the family's shared files, the same as FoundaTrix Studio's site (www.foundatrix.com) and
PileAxis's (www.pileaxis.com), so the three product sites read as one family; Strutrix Studio's few additions sit at the
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
  Strutrix Studio and its length is a server setting.
- The emphasis is on what the program computes, end to end, and on its engineering accuracy.
- No connection details of the AI-assistant connector (no address, no client id) anywhere.
- Fictional project, client and site names only in any picture or example.

## Pictures

There are **no screenshots of Strutrix Studio yet**: every product picture is an SVG illustration drawn in the
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

Not screenshots to replace: `src/images/screens/structure-link.svg` (a diagram of the link: a frame's reactions read by
FoundaTrix Studio and PileAxis) and `src/images/assistant-frame.svg` (a generic assistant conversation, deliberately not
any one assistant's interface, creating a building frame through the connector with the tool names the endpoint really
exposes, in the fictional job "Sample Distribution Centre").

When replacing one: a fictional project and client only (never a real one), a dark-theme window of about 1500 x 1000,
cropped below the caption row, saved as WebP at quality 84 to 86 in `src/images/screens/`; then update the `<img>`
`src`, `width`, `height` and `alt`.

Artwork: `src/images/strutrix-mark.svg` (the nav and footer mark) and `src/favicon.svg` (the small mark) are drawn in the
family's style, the navy plate, the isometric lavender faces and the teal ground grid of the FoundaTrix Studio and
PileAxis marks: a one-bay steel frame braced on its front face, a lateral load on its corner. The program's own mark
arrives with its Store package; when it does, convert its `Logo.xaml` and `Logo.Small.xaml` into these two files, as
the sister sites did. `src/images/hero-frame.svg` (the hero) and `src/images/types/*.svg` (the six frames the Generate
menu builds) are illustrations.

## Values still to settle

| What | Where | Now |
|---|---|---|
| Microsoft Store link | `src/index.html`, `#download`; every "Coming soon" button goes to `/#download` | Not listed yet. The panel shows a "Coming soon" badge and the Store button as a non-link (`.store-btn--soon`). When the listing is live: make the button an `<a class="store-btn" href="https://apps.microsoft.com/detail/<Store ID>">` (as the sister sites do), change the badge and the buttons' "Coming soon" to "Download free", and the announce bar to the listing |
| The Pro split | Home `#pro`, `#plans`; `/pricing/` | Stated as the program's premium catalogue has it: tapered tubes (with the Pole and H-Frame generators), IFC and Revit export, the firm on the report, search by a structure's inputs, and the structure link; everything else free |
| The structure link and the assistant connector | Home `#link`, `#connect`; Features `#link`, `#connect` | Advertised as the program's manual describes them; check they are open to customers in all three programs on launch day |
| Hosting and domain | `.github/workflows/deploy.yml`, canonical links, `robots.txt`, `sitemap.xml` | Written for **Azure Static Web Apps** and `https://www.strutrix.com`. The workflow deploys nothing until the repository secret `AZURE_STATIC_WEB_APPS_API_TOKEN` is set |

The privacy policy and terms of use follow the sister programs' (www.foundatrix.com/privacy, www.pileaxis.com/privacy),
adapted to what Strutrix Studio does (effective October 26, 2026). When the program's Store folder gains its own
`PrivacyPolicy.md` and `TermsOfUse.md`, keep them and these pages one text.

## Local preview

There is no build step. Because the links are root-absolute, serve `src/` with any static file server rather than
opening the files directly, for example:

```bash
python -m http.server 8080 --directory src
```

then open `http://localhost:8080/`.

## Deployment

The site is meant for **Azure Static Web Apps** (Free plan), as its sister sites are. Every push to `main` runs
`.github/workflows/deploy.yml`, which publishes `src/` once the repository secret `AZURE_STATIC_WEB_APPS_API_TOKEN` (the
app's deployment token) is set, and reports that it deployed nothing until then. Pull requests are not deployed.
`src/staticwebapp.config.json` sets trailing slashes, the 404 page and the security headers, including a content
security policy.

The canonical address is `https://www.strutrix.com`: the canonical links, `og:url`, `robots.txt` and `sitemap.xml` all
name it. To go live: create the Static Web App, set the secret, add `www.strutrix.com` (CNAME) and the apex (TXT
validation, then an A record to the app's stable inbound IP) as custom domains, and make `www` the default.

## Contributing

Typo fixes and copy improvements are welcome by pull request; see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT for the website's source and content (see [LICENSE](LICENSE)). The Strutrix Studio program itself is separate,
closed-source software under its own terms. "Strutrix Studio" and its mark are not licensed for reuse by the MIT
license.
