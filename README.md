# StruTrix Studio

**StruTrix Studio** is professional Windows software by RamisoftSolutions for the structural analysis and design of
three-dimensional frames: buildings, industrial structures, pipe racks, towers, trusses, portal frames and transmission
poles. It analyses every load combination to first order or by the AISC 360-22 direct analysis method, designs every steel
member to AISC 360-22 by LRFD or ASD, analyses structures built in stages, designs seismic force-resisting systems to
ANSI/AISC 341-22, and audits every result's equilibrium. The analysis and the steel design are free, with no limit on model
size or time and no account required.

**Latest version: 1.105 (November 7, 2026).** [Website](https://www.strutrix.com/) ·
[Features](https://www.strutrix.com/features/) · [Verification](https://www.strutrix.com/verification/) · [What's new](https://www.strutrix.com/whats-new/) ·
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

## How its results are checked

StruTrix Studio's results are held to answers it did not write. Measured on the code of version 1.105, and repeated by automated
tests with every build; [every comparison is on the website](https://www.strutrix.com/verification/).

| Published source | What was compared | Result |
|---|---|---|
| AISC Design Examples | 46 strengths, by LRFD and ASD: tension, compression, flexure, shear, torsion and combined forces | All within 1.35%, 43 of them within 1% |
| AISC 360-22 Commentary, Figures C-C2.2 and C-C2.3 | The two second-order benchmark problems, moment and deflection at each axial load | All within 0.37%; the Commentary asks for 3% and 5% |
| Beam-column closed forms | Second-order moment and deflection, axial loads from 100 to 900 kips | Within 0.00001% |

Every design check names its clause, every line of a member's working is computed again from its own inputs, and a separate
calculation audits every combination's equilibrium. More than 1,700 automated tests cover the analysis, the steel checks, the
load combinations and the program. These are RamisoftSolutions' own comparisons; AISC and ASCE have not reviewed or endorsed the
program.

## New in version 1.105

- Staged construction analysis in the Microsoft Store: an addition to an existing structure, or any number of stages.
- Seismic design by AISC 341-22, with ASCE 7-22's equivalent lateral force, story drift and stability.
- Rigid diaphragms.
- The support reactions read by FoundaTrix Studio and PileTrix Studio.
- The User's Manual rearranged, with pictured tutorials of a staged construction analysis and a seismic design.

Every release's notes are in [CHANGELOG.md](CHANGELOG.md) and on the website's
[What's new](https://www.strutrix.com/whats-new/) page.

## Coming soon

These are not available yet, and what each will do may change before it ships. Everything above describes the program as
it is today.

- **Connection design** (Pro, in development): a steel frame's connections designed down to every plate, bolt and weld by
  AISC 360-22 Chapter J. A connection is chosen from a library and assigned to the member ends it suits, fitted to the true
  sections it joins, and each limit state is checked by the clause it cites, under every design combination of the
  analysis, by LRFD or ASD.
  - **The library**: single plates, double angles, shear end plates, seats, single angles, tees, shear splices and bracket
    plates; flange-plated, directly welded and end-plate moment connections; with bracing connections, column splices and
    base plates to follow.
  - **Prequalified moment connections** of ANSI/AISC 358-22 (reduced beam section, bolted end plates, bolted flange plate,
    and welded unreinforced flange-welded web), designed for the moment and shear the seismic design works at the column's
    face.
  - **A 3D connection editor**: every plate, bolt and weld drawn to size and clickable; change a diameter or a thickness in
    its properties and the design follows at once, each part coloured by how hard it is working.
  - **On the model**: connections assigned end by end or automatically by what carries each beam, and shown by coloured
    symbols.
  - **The working**: every check worked out equation by equation with its clause, and printed in a report of the connection
    with its drawing.
  - **Your own library**: your connections kept in the cloud, ready for your other projects. A model holding connections is
    saved to the cloud.
- **Also on the way**: multi-storey buildings modelled from typical floors (free with an account), and the seismic
  assessment of steel buildings by pushover to ASCE 41-23 (Pro).

## Common questions

- **Can it be used for real steel design?** Yes, within its scope: three-dimensional frames of linearly elastic members under
  static loads, analysed to first order or by the AISC 360-22 direct analysis method, with every steel member designed by LRFD or
  ASD. It is professional software for practising engineers, not a student or educational program. As with any program, the
  engineer stays responsible for the model, the loads and the results.
- **Are its AISC 360-22 checks verified?** They are held to the answers AISC published:
  [46 strengths from the AISC Design Examples within 1.35%, and the Commentary's second-order benchmarks within 0.37%](https://www.strutrix.com/verification/).
- **Does it generate load combinations?** Yes: the ASCE 7-22 combination generator writes the strength, allowable stress and
  service combinations, with notional loads.
- **Does it produce calculation reports?** Yes, free and with no watermark: a typeset PDF of the basis, the model, the loads, the
  combinations, the equilibrium, the reactions and every member's checks clause by clause; and a member detail that works every
  check equation by equation with its clause, in a window or as a PDF.
- **Does it work with BIM tools?** It exports to IFC 4.3 with true steel profiles and to Revit 2025, 2026 and 2027 as native
  structural columns and framing (Pro).
- **Which design codes does it cover?** United States standards: AISC 360-22, ANSI/AISC 341-22, the member side of ANSI/AISC
  358-22, ASCE 7-22, ASCE/SEI 48-19, ASCE MOP 74 and 113, and the NESC. Eurocode, AS/NZS and other national steel codes are not
  offered.
- **How long has it been available?** It is new: in the Microsoft Store since November 1, 2026. Its frame analysis engine and
  steel checks also ship in FoundaTrix Studio.
- **Does StruTrix Studio do staged construction analysis?** Yes, since version 1.105 in the Microsoft Store, as a Pro
  feature: an addition to an existing structure, or a structure built in any number of construction stages, each stage
  analysed on the structure standing then, first-order or by the direct analysis method.
- **Does it design for seismic loads?** Yes: seismic force-resisting systems are designed to ANSI/AISC 341-22 with
  ASCE 7-22's equivalent lateral force, drift and stability (Pro). It does not run a modal response spectrum or
  time-history analysis.
- **Does it design connections?** Not yet. Today it designs the members, and a seismic design reports the connections'
  required strengths. Connection design is in development as a Pro feature, down to every plate, bolt and weld by
  AISC 360-22 Chapter J and ANSI/AISC 358-22: see [Coming soon](#coming-soon).
- **Is it free?** The modelling, the loads, the combinations, the analysis, the AISC 360-22 steel design and the
  calculation report are free, with no limit on model size or time, no watermark and no account. It is professional
  software for real projects, not a student or evaluation edition. The Pro features are a separate set, free to try.
- **What does it not do?** Plates, walls and solids, dynamics, material nonlinearity, concrete, wood and cold-formed
  steel design, and, until connection design ships, the design of connections' plates, bolts and welds. The website's
  features page lists every limit.

## Reporting bugs and requesting features

- **Bug reports and feature requests (public):** open an [issue](../../issues/new/choose) and pick the template that
  fits.
- **Private matters** (confidential project data, licensing, security): email `admin@ramisoftsolutions.com`. Please do
  not attach a client's model to a public issue.
- **Version details:** in the program, **Help > About > Copy details** copies the version, the build and how the
  program was installed. Paste them into the issue.

## About this repository

This repository is the public source of the website, www.strutrix.com, and its **Issues** are the public place to report a bug or
ask for a feature. **It holds no application source**: the desktop program, its engine and its cloud service are developed in a
separate, private repository. Notes for whoever maintains the website are in [MAINTAINING.md](MAINTAINING.md).

## Contributing

Typo fixes and copy improvements are welcome by pull request; see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT for the website's source and content (see [LICENSE](LICENSE)). The StruTrix Studio program itself is separate,
closed-source software under its own terms. "StruTrix Studio" and its mark are not licensed for reuse by the MIT
license.
