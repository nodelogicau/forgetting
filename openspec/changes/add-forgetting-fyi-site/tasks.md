## 1. Settle what the page will assert

- [x] 1.1 Record the commit hash of `whitepaper.md` that the port is taken from
- [x] 1.2 Choose the accent hue (third sibling to particulars green and intentions indigo) and record the full palette for both schemes
- [x] 1.3 Fix the section ids (`summary`, `why-forget`, `memory`, `why-agents-forget`, `provenance`, `semantic`, `prospective`, `how-they-meet`, `gaps`, `measuring`, `open-questions`, `references`, plus chosen subsection ids)
- [x] 1.4 Decide whether to keep the hand-maintained "last revised" date

## 2. The page shell

- [x] 2.1 `docs/index.html` skeleton: head, title, description, inline SVG favicon, `:root` palette and dark override, type scale and SVG class vocabulary carried over from intentions, reading measure for long prose
- [x] 2.2 Hero: eyebrow, "Remember forward.", lead from the Summary, the calls to action to `#summary`, particulars.fyi and intentions.fyi
- [x] 2.3 Hero diagram: four memory kinds (two solid and linked, two dashed) over a provenance band, with `<title>` and `<desc>`
- [x] 2.4 Muted Carroll credit line and the draft / non-normative status line
- [x] 2.5 Contents nav linking every section id
- [x] 2.6 Styles for `aside.draft-note`, the §1 table, blockquoted quotations, and the References
- [x] 2.7 Footer with the CC0 licence sentence
- [x] 2.8 Top-of-file HTML comment stating that this file is the paper and how prose is formatted

## 3. Port the paper

- [x] 3.1 Summary and §1 *Why forget*, including the ready-to-hand table as a `<table>`
- [x] 3.2 §2–§4
- [x] 3.3 §5–§7
- [x] 3.4 §8–§10
- [x] 3.5 References, including the Carroll entry, with the format links
- [x] 3.6 Convert every *Draft note* blockquote to `aside.draft-note`

## 4. Supporting files

- [x] 4.1 `docs/CNAME` containing `forgetting.fyi`
- [x] 4.2 `docs/README.md`: purpose (the page is the paper), Pages settings, DNS records, `www` note, prose formatting convention, the list of stable section ids
- [x] 4.3 `whitepaper.md` reduced to a stub linking to https://forgetting.fyi and noting that its git history holds the paper up to the move
- [x] 4.4 `README.md`: replace the `whitepaper.md` link with forgetting.fyi

## 5. Verify

- [x] 5.1 No `<script`, no external stylesheet, font, image or `@import`; one request in the network inspector
- [x] 5.2 Both colour schemes: hero diagram, draft notes and table legible in each
- [x] 5.3 Phone width: no horizontal page scroll; the table and diagram scroll within their wrap
- [x] 5.4 Every link resolves: sibling sites, GitHub repositories, every `#id` in the contents and in `docs/README.md`
- [x] 5.5 Read the port paragraph by paragraph against `whitepaper.md` at the recorded commit; the draft-note count matches
- [x] 5.6 Read §5–§7 against the particulars and intentions READMEs on `main`
- [x] 5.7 Footer licence sentence agrees with `LICENSE` and the README License section
- [x] 5.8 A one-word test edit diffs as a single paragraph's lines (then revert)

## 6. Deploy and close out

- [x] 6.1 Commit `docs/`, the stub and the README edit together; push
- [ ] 6.2 Pages settings: deploy from `main`, folder `/docs`; confirm the `github.io` address serves the page
- [ ] 6.3 DNS: four apex `A` records (DNS-only) and `www` CNAME; wait for the certificate; enforce HTTPS
- [x] 6.4 Note the follow-up in particulars and intentions: point README links (and optionally each site) at forgetting.fyi
- [ ] 6.5 Archive the change with sync so `paper-site` lands in the main specs

## 7. Restyle as a paper

- [x] 7.1 Replace the hero (eyebrow, display headline, lead, pill CTAs) with a title block: series line, title, subtitle, Carroll epigraph, status paragraph linking the sibling sites
- [x] 7.2 Neutral palette only (background, text, muted, rule) in both schemes; links in text colour, underlined
- [x] 7.3 Serif system stack, one left-aligned ~40rem column, section breaks by spacing
- [x] 7.4 Figure 1 in thin monochrome lines; draft notes as muted text behind a thin rule; tables with booktabs-style rules
- [x] 7.5 Re-check: no script or external request, every anchor resolves, light, dark and phone widths render, figure fits the column
