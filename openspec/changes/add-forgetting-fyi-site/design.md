## Context

particulars.fyi and intentions.fyi are each one hand-written `docs/index.html` with a `CNAME` and a `README.md` of deploy and DNS notes. Neither has a build, JavaScript, or any request to another origin. Both theme light and dark through CSS custom properties, and both are deliberately introductions: the specification README stays canonical on GitHub, and each page names no field so that a rename cannot falsify it.

This repository holds `whitepaper.md` (about 730 lines, ten numbered sections, Summary and References), a README that links to it, and a CC0 `LICENSE`. The paper is a draft with seven *Draft note* blockquotes and one Markdown table (§1, *The ready-to-hand*). It has no footnotes, code blocks, or internal anchor links. Its recent history is small wording commits. particulars' README links to the repository root, not to `whitepaper.md`.

## Goals / Non-Goals

**Goals:**
- The whitepaper readable as a typeset page at forgetting.fyi, recognisably a sibling of the two format sites.
- One copy of the paper, edited in place, with wording commits that stay as small and readable as they are in Markdown.
- Section ids stable enough for the format READMEs and sites to deep-link.
- Draft notes visible on the public page and distinguishable from settled argument.

**Non-Goals:**
- Keeping a Markdown copy in step, or generating the page from one.
- An introduction page that points at the paper elsewhere.
- Client-side behaviour, analytics, web fonts, or any asset served from elsewhere.
- Updating particulars' or intentions' READMEs or sites. That is a follow-up in those repositories.
- A GitHub Actions workflow. Deploy-from-branch needs none.

## Decisions

**The HTML is canonical and `whitepaper.md` becomes a stub.** The specifications stay on GitHub because implementers check compliance against them. Nobody checks anything against the whitepaper. Other options considered:
- *Hand-port and keep both in step.* Every wording fix would have to be made twice, and drift is near certain given the commit rate.
- *A stdlib script that regenerates the page body from the Markdown between markers*, as the proof figures are regenerated. Workable, but it keeps Markdown as the source of a document whose reading surface is the web, and it adds a converter to maintain.
- *Jekyll on Pages.* It generates the output, which breaks the siblings' hand-written single-file rule and makes their styling harder to match.

The stub keeps `blob/main/whitepaper.md` links from dead-ending. It is a title, one sentence pointing at https://forgetting.fyi, and a note that the history of the paper up to the move is in this file's git log.

**The paper's prose is ported once, faithfully.** The port is a change of medium, not an edit. Wording, section order, quotations and the References carry over unchanged. Markdown emphasis becomes `<em>`, bold becomes `<strong>`, straight quotes become typographic quotes, and the three tables become real `<table>`s. They get no `<caption>`, because a caption would be new wording; the sentence before each table already introduces it. Cross-references such as "section 8" become links to the section's id, which is markup, not wording. Any wording change waits for a later commit, so the port can be checked against `whitepaper.md` at the commit before the stub.

**Source formatting keeps diffs small.** One block element per paragraph, prose wrapped near 78 columns as the Markdown is, no inline styles, and a handful of classes. A one-word fix then diffs as one or two lines, as it does now. The convention is written in `docs/README.md`.

**Page structure.**
```
  header.title
    p.series      Forgetting
    h1            Remember forward.
    p.subtitle    the paper's own subtitle
    epigraph      "It's a poor sort of memory that only works backwards."
                  — the White Queen, Through the Looking-Glass
    p.status      the Draft blockquote's wording, with particulars.fyi and
                  intentions.fyi linked beside the format names
    figure        Figure 1: memory kinds over the provenance spine
  nav#contents    Summary, §1–§10, References
  main > article
    section#summary
    section#why-forget … section#open-questions   (h2, with h3 subsections)
    section#references
  footer          licence sentence
```
The paper's own title block (title, subtitle, the Draft blockquote) becomes the page's title block. "Forgetting" becomes the series line above the title, and the Draft blockquote becomes the status paragraph, unchanged except that the two sites are linked.

**A paper, not a pitch.** The first build reused the sibling landing pages' hero: uppercase accent eyebrow, centred display headline, pill buttons, a tinted plum palette, amber draft-note callouts and rules between sections. On a long essay that read as a product pitch and pulled attention away from the text, so it was dropped. The page is set as a paper instead:
- a serif system stack (Iowan Old Style, Palatino, Charter, Georgia), with no web font;
- one left-aligned column of about 40rem;
- no accent colour: the palette is background, text, muted text and rule, in both schemes;
- links in the text colour, underlined with a light rule;
- no buttons, and the sibling sites linked in running text;
- section breaks by spacing rather than rules.

What it shares with the siblings is the build discipline, not the look: one hand-written file, no script, no external request, light and dark through custom properties.

**The title and the epigraph.** "Remember forward." pairs with the series name: forgetting is what the person gets to do, and the title says what the remembering is for. The Carroll line stands as an epigraph under the subtitle, and Carroll is listed in the References (*Through the Looking-Glass*, 1871, ch. 5). No heading names a writer.

**Figure 1.** Four boxes, one per kind of memory from §2 and §8. *semantic → particulars* and *prospective → intentions* have solid outlines and link to their sites. *episodic* ("not yet specified") and *procedural* ("a way back to the reasons") are dashed. A band beneath all four is labelled *provenance*, from §4, because the paper argues it is the property the family shares. It is drawn in thin monochrome lines, like a figure in a paper. The box captions stay true to the paper's own words, and the figure carries a `<title>` and `<desc>` for screen readers.

**Stable section ids, chosen by hand.** These are short slugs of each heading's subject, not generated from heading text: `summary`, `why-forget`, `memory`, `why-agents-forget`, `provenance`, `semantic`, `prospective`, `how-they-meet`, `gaps`, `measuring`, `open-questions`, `references`. Every subsection gets an id too. Renaming a heading leaves its id alone. The list of ids is recorded in `docs/README.md` as the deep-linking interface.

**Draft notes are visible but quiet.** Each `> *Draft note.*` becomes `<aside class="draft-note">`, labelled "Draft note" in italics and set in muted text behind a thin left rule. Readers can see where the argument is thin, which is part of the paper's honesty about its status, and the note doesn't shout over the argument around it.

**Claims about a format defer to its README.** §5–§7 describe particulars and intentions. The page may argue for why they are as they are, but nothing it says about what a format does may contradict that format's README on `main`. This is the siblings' "says nothing the README does not" turned outward. The paper keeps its own line that nothing here is normative.

**Deploy from branch.** Repository settings, Pages, source "Deploy from a branch", `main`, `/docs`, custom domain `forgetting.fyi`, enforce HTTPS once the certificate is issued. DNS is the four GitHub Pages apex `A` records, DNS-only, and `www` as a `CNAME` to `nodelogicau.github.io`.

## Risks / Trade-offs

- [Editing prose inside HTML is less pleasant than Markdown] → One paragraph per element with wrapped lines keeps diffs small. The markup is limited to `p`, `em`, `strong`, `a`, `blockquote`, `aside`, `table`, `h2`/`h3`. Accepted as the cost of one copy.
- [GitHub no longer shows a readable paper] → The README's first screen and the stub both point at forgetting.fyi.
- [The port silently changes wording] → The port is checked paragraph by paragraph against `whitepaper.md` at the last commit before the stub, and no wording change rides along with it.
- [A section id changes and a deep link breaks] → Ids are hand-chosen, recorded in `docs/README.md`, and decoupled from heading text.
- [The paper drifts from a format's README as the formats evolve] → A verification task reads §5–§7 against both READMEs before launch. The existing practice of linking intentions and particulars issues from draft notes continues.
- [A draft is published under a permanent-looking domain] → The status line says "Draft" and the draft notes are visible. That is the honest state of the paper, and the site makes it plainer than the Markdown did.

## Migration Plan

1. Build `docs/` with the full paper while `whitepaper.md` is still the source, and review it at the `github.io` address.
2. In one commit, publish `docs/`, stub `whitepaper.md`, and repoint the README. From that commit on, prose edits go to `docs/index.html`.
3. Configure DNS and Pages, wait for the certificate, and enforce HTTPS.
4. Rollback: revert the commit. `whitepaper.md` returns with its full text, and the site can be unpublished in Pages settings.

## Settled during implementation

- **No accent hue.** A plum accent was tried first and removed with the rest of the landing-page styling; see *A paper, not a pitch*.
- **No "last revised" date.** A date maintained by hand goes stale, and the git log already records every revision. The status line carries the Draft blockquote's wording unchanged.
- **Port source:** `whitepaper.md` at `15b95da`, plus the Carroll entry added to the References in this change.
- **Subsection ids** go beyond the four named above: every `h3` in the body has one (`overthinker`, `becoming`, `what-the-store-needs`, `surfacing` as well). All are listed in `docs/README.md`.
