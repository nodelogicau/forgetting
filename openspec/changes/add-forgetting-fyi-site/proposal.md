## Why

The whitepaper is the reasoning behind particulars and intentions, and both formats' READMEs point readers to it, but today it is a long Markdown file read in GitHub's file viewer. forgetting.fyi is now held. The two specifications stay on GitHub as their source of truth because implementers, human and AI, check compliance against them. The whitepaper is not checked against by anyone. It is an argument to be read, so its reading surface can be its source.

## What Changes

- A site at **forgetting.fyi**, served by GitHub Pages from `docs/` on `main`, built the same way as particulars.fyi and intentions.fyi: one hand-written `docs/index.html`, no build step, no JavaScript, no request to any other origin, inline SVG themed through CSS custom properties for light and dark.
- **The page is the whitepaper.** Unlike the sibling sites, it is not an introduction pointing elsewhere. The full text moves into `docs/index.html` and is edited there from then on. There is no second copy to keep in step.
- **BREAKING:** `whitepaper.md` is reduced to a stub saying the paper has moved to forgetting.fyi. Existing links to it still resolve to something useful.
- Hero: the eyebrow "Forgetting · the reasoning behind particulars and intentions", the headline **"Remember forward."**, a lead drawn from the Summary, a primary call to action into the paper, and secondary links to particulars.fyi and intentions.fyi. Beneath it is a diagram of the four kinds of memory over the provenance spine, then a muted credit to Lewis Carroll's White Queen ("It's a poor sort of memory that only works backwards"), who is now listed in the References.
- After the hero comes a contents list, then the paper from Summary to References, with stable section ids that other sites can deep-link to.
- *Draft notes* stay visible, styled as open questions so a reader can tell argument from unsettled argument.
- `docs/CNAME` carrying `forgetting.fyi`, and `docs/README.md` carrying the Pages settings, DNS records and editing conventions.
- `README.md` points at forgetting.fyi in place of `whitepaper.md`.
- Outside the repo: Pages settings and DNS at the registrar.

## Capabilities

### New Capabilities

- `paper-site`: what forgetting.fyi is built from and what it asserts. It covers a single static file with no build, script or external request, both colour schemes, the page being the sole copy of the whitepaper, the hero with its headline, credit and memory-kinds diagram, the contents list and stable section ids, visible draft notes, the rule that claims about a format agree with that format's README, a footer licence statement that agrees with the repository, and a README pointing at the site. It is named `paper-site` rather than the siblings' `landing-site` because the page is the document, not a way into one.

### Modified Capabilities

None. This repository has no specs yet.

## Impact

- New `docs/` directory with `index.html`, `CNAME` and `README.md`. `whitepaper.md` becomes a stub. `README.md` changes one link.
- Prose edits move from Markdown to HTML. Wording commits stay small and readable only if the source keeps one paragraph per `<p>` with wrapped lines. That convention is recorded in `docs/README.md` rather than left to habit.
- Section ids become a public interface once anything deep-links to them.
- Follow-up outside this repository, not part of this change: the two links in particulars' README (and optionally a link from each sibling site) can move from the GitHub repository to forgetting.fyi. Both already point at the repository root, so nothing breaks in the meantime.
