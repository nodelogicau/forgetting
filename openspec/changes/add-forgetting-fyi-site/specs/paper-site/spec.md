## ADDED Requirements

### Requirement: The site is one static file with no build and no external request
The site SHALL consist of a single hand-written `docs/index.html`, served by GitHub Pages from `docs/` on `main`. The file SHALL contain no `<script>` element and SHALL reference no resource on any other origin: no external stylesheet, font, image, or `@import`. All diagrams SHALL be inline SVG.

#### Scenario: The page is loaded
- **WHEN** `index.html` is opened in a browser with the network inspector recording
- **THEN** exactly one request is made, for the document itself, and no script executes

#### Scenario: A reviewer checks the source
- **WHEN** the file is searched for `<script`, `<link rel="stylesheet"`, `src="http`, `href="http` inside `<link>`, and `@import`
- **THEN** none is found

### Requirement: The custom domain is declared in the repository
`docs/CNAME` SHALL contain exactly `forgetting.fyi`, and `docs/README.md` SHALL record the Pages settings and the DNS records needed to serve it.

#### Scenario: Pages is configured from the repository
- **WHEN** Pages is set to deploy `main` from `/docs`
- **THEN** GitHub reads the custom domain from `docs/CNAME` without it being typed into settings

### Requirement: The page renders in both colour schemes
Colours SHALL be defined as CSS custom properties on `:root`, redefined under `prefers-color-scheme: dark`, and every SVG SHALL take its fills and strokes from those properties.

#### Scenario: The system theme changes
- **WHEN** the operating system switches between light and dark
- **THEN** the page, including the figure and the draft notes, re-renders legibly with no hard-coded colour remaining from the other scheme

### Requirement: The page is the only copy of the whitepaper
`docs/index.html` SHALL carry the full text of the whitepaper, from the Summary through the References, and SHALL be where the paper is edited. `whitepaper.md` SHALL be a stub stating that the paper has moved to https://forgetting.fyi and SHALL NOT carry any of the paper's argument. No script or build step SHALL generate the page from another source.

#### Scenario: A reader opens the old file
- **WHEN** `whitepaper.md` is opened on GitHub
- **THEN** it links to https://forgetting.fyi and contains no section of the paper

#### Scenario: The port is checked
- **WHEN** each paragraph of the page's paper body is read against `whitepaper.md` at the last commit before it became a stub
- **THEN** the wording, section order, quotations and references agree, apart from the paper's title block, which becomes the page's title block

### Requirement: The source keeps prose diffs small
The paper's prose in `docs/index.html` SHALL be one block element per paragraph, wrapped at about 78 columns, with no inline `style` attributes. `docs/README.md` SHALL record this convention.

#### Scenario: A one-word fix is committed
- **WHEN** a single word in a paragraph is changed
- **THEN** the diff touches no more than the wrapped lines of that paragraph

### Requirement: The page opens with a paper's title block
The page SHALL open with a title block, not a product hero: the series name "Forgetting", the title "Remember forward.", the paper's subtitle, an epigraph quoting "It's a poor sort of memory that only works backwards" and crediting the White Queen in Lewis Carroll's *Through the Looking-Glass*, and a status paragraph stating that the paper is a draft, that nothing in it is normative, and linking to https://particulars.fyi and https://intentions.fyi. The References SHALL list *Through the Looking-Glass*. The title block SHALL contain no buttons or calls to action, and no heading on the page SHALL name a writer.

#### Scenario: A reader arrives
- **WHEN** the page loads at the top on a desktop viewport
- **THEN** the title, subtitle, epigraph and status paragraph are visible without scrolling, and the paper's text follows the figure and contents without anything in between

#### Scenario: The epigraph is traced
- **WHEN** the epigraph's credit is read against the References
- **THEN** *Through the Looking-Glass* is listed there

#### Scenario: A reader follows a sibling link
- **WHEN** the particulars.fyi or intentions.fyi link in the status paragraph is activated
- **THEN** the browser lands on that format's site

### Requirement: The typography serves reading, not promotion
The page SHALL be set as a paper: a serif system font stack, one left-aligned text column of about 40rem, links in the text colour and underlined, and no accent colour. Colour SHALL be limited to the text, muted-text, rule and background tokens. Draft notes, tables and the figure SHALL be distinguished by rules, italics and weight, not by fills or hues.

#### Scenario: A reviewer checks the palette
- **WHEN** the `:root` custom properties are read
- **THEN** each one is a neutral (background, text, muted text, or rule) in both schemes, and no element uses a colour outside them

### Requirement: The figure shows the kinds of memory over the provenance spine
The title block's figure SHALL show four kinds of memory: semantic, labelled particulars, and prospective, labelled intentions, drawn as specified; episodic and procedural drawn as not yet specified, in a visibly different style. It SHALL show provenance as a band beneath all four. The particulars and intentions elements SHALL link to their sites. The SVG SHALL carry a `<title>` and `<desc>`.

#### Scenario: The diagram is read
- **WHEN** the figure is read
- **THEN** two kinds appear as specified formats, two appear as gaps, and provenance spans all four

#### Scenario: The diagram is read against the paper
- **WHEN** each label is compared with §2, §4 and §8
- **THEN** no label says something those sections do not

### Requirement: The paper has a contents list and stable section ids
A contents list SHALL link to the Summary, every numbered section, and the References. Each of these SHALL carry a hand-chosen `id` that does not change when its heading's wording changes. `docs/README.md` SHALL list the ids as the page's deep-linking interface.

#### Scenario: A sibling deep-links
- **WHEN** a URL of the form `https://forgetting.fyi/#provenance` is opened
- **THEN** the browser scrolls to the provenance section

#### Scenario: A heading is reworded
- **WHEN** a section heading's text is edited
- **THEN** its `id` is unchanged and every id in `docs/README.md` still resolves

### Requirement: Draft notes stay visible and marked as open
Every *Draft note* in the paper SHALL be rendered as a distinct element, labelled "Draft note" and styled so that it reads as unsettled, apart from the surrounding argument, in both colour schemes.

#### Scenario: The draft notes are counted
- **WHEN** the page's draft-note elements are counted
- **THEN** their number equals the number of *Draft note* blockquotes in `whitepaper.md` at the last commit before it became a stub

### Requirement: Claims about a format agree with its README
Nothing the page states about what particulars or intentions does SHALL contradict that format's README on `main` at the time of publication. The page MAY argue for why a format is as it is.

#### Scenario: The format sections are checked
- **WHEN** §5, §6 and §7 are read against the particulars and intentions READMEs
- **THEN** no sentence asserts a behaviour the relevant README contradicts

### Requirement: The footer's licence statement agrees with the repository
The footer SHALL state that the whitepaper is released under CC0 1.0 Universal, and this SHALL match the `LICENSE` file and the README's License section.

#### Scenario: The licences are compared
- **WHEN** the footer, `LICENSE`, and the README License section are read together
- **THEN** all three agree

### Requirement: The README points at the site
`README.md` SHALL link to https://forgetting.fyi as the place to read the whitepaper and SHALL NOT link to `whitepaper.md` as the paper.

#### Scenario: A reader opens the README
- **WHEN** the first screen of the README is read
- **THEN** the link to forgetting.fyi is visible
