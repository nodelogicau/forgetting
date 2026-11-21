## Why

episodes now has its own site, https://episodes.fyi, but the paper still introduces the family as two specified formats and draws episodic memory as a gap. One sentence in §7 also contradicts the episodes README: it says an episode can name the intention it was the occasion of, while the README says "An episode does not name the intention it realised, and intentions does not cite episodes." The paper-site spec lets this happen, because its README-agreement requirement covers only particulars and intentions.

## What Changes

- The status paragraph in the title block, the footer, *The formats* in the References, the `<meta name="description">` and the HTML comment at the top of `docs/index.html` name episodes beside particulars and intentions, link episodes.fyi where the others link their sites, and mark episodes as a draft.
- §7's *The return path* is corrected. The episode names nothing. A claim cites the episode as its evidence (through `source.document.ref`) and cites the intention it bears on, and the self-understanding cites that claim.
- Figure 1: episodic moves across the divider into *the formats*. It is drawn as a solid box labelled episodes, linked to episodes.fyi, with a small *draft* tag. Procedural is the only gap. The `<title>`, `<desc>` and caption say three formats, one of them a draft, and one gap. The Summary's account of the family agrees.
- §8's draft note ("check this section against its README when it reaches `episodes/0.1`") stays, because nothing in episodes is declared yet.

## Capabilities

### New Capabilities

None.

### Modified Capabilities

- `paper-site`:
  - *The page opens with a paper's title block*: the status paragraph also links https://episodes.fyi and says that episodes is a draft.
  - *The figure shows the kinds of memory over the provenance spine*: three kinds are drawn as formats, with episodes marked draft and linked, and procedural is drawn as the one gap.
  - *Claims about a format agree with its README*: extends to episodes, so §7, §8 and §9 are read against the episodes README.

## Impact

- `docs/index.html`: the title block (status paragraph, Figure 1), the Summary, §7, the References, the footer, and the head (meta description and source comment).
- `docs/README.md`: one line. "Unlike particulars.fyi and intentions.fyi" also names episodes.fyi. The agreement rule already names episodes.
- `openspec/specs/paper-site/spec.md`: three requirements, applied when the change is archived.
- Working tree: `docs/index.html` already has an uncommitted rewrite of the Kierkegaard paragraph in §8. It agrees with the episodes README. Commit it on its own before this change, so this change's diff stays readable.
- Out of scope, for a later change: what episodes adds to the argument, namely that a source being deleted is not a request to forget, redaction as the only deliberate forgetting, and `source_status` as a breakdown in §9's chain.
