## 0. Before starting

- [x] 0.1 Commit the pending §8 Kierkegaard paragraph rewrite in `docs/index.html` on its own, so this change's diff is only this change.
- [x] 0.2 Re-read the episodes README on `main` verbatim: its status line, the passage on intentions ("An episode does not name the intention it realised…"), and the passage on how a claim cites an episode. Note the exact wording to check against.

## 1. Title block

- [x] 1.1 Status paragraph: name episodes (https://episodes.fyi) beside particulars and intentions as the specifications, and say that episodes is still a draft.
- [x] 1.2 Figure 1: move the divider between episodic and procedural, and centre *the formats* over the first three boxes and *the gap* over the last.
- [x] 1.3 Figure 1: give the episodic box the `box` class and a solid edge to the spine, make its middle line `episodes` linked to https://episodes.fyi (weight 600), and add a `small` italic *draft* tag inside the box.
- [x] 1.4 Figure 1: rewrite `<desc>` and the caption for three formats, one of them a draft, and one gap.
- [x] 1.5 Subtitle: "how particulars, intentions and episodes fit together".

## 2. Body

- [x] 2.1 Summary: describe the family as three formats, episodes a draft, with procedural memory unspecified. Check that nothing still implies two formats.
- [x] 2.2 §7 *The return path*: replace "an episode can name the intention it was the occasion of" with the README's direction. A claim cites the episode as its evidence and cites the intention it bears on, and the self-understanding cites that claim.
- [x] 2.3 Read §8, §9, and Figure 2's `<desc>` and caption against the episodes README. Fix any contradiction. Leave §8's `episodes/0.1` draft note in place.

## 3. Surround

- [x] 3.1 References, *The formats*: add an episodes.fyi link beside the GitHub link and keep "(draft)".
- [x] 3.2 Footer: "the reasoning behind particulars, intentions and episodes", with episodes linked to episodes.fyi.
- [x] 3.3 `<meta name="description">` and the source comment at the top of the file name episodes beside the other two.
- [x] 3.4 `docs/README.md`: "Unlike particulars.fyi and intentions.fyi" includes episodes.fyi.

## 4. Verify

- [x] 4.1 Check the static-file rules: no `<script>`, and no external stylesheet, font, image or `@import`. The new links are `<a>` only.
- [x] 4.2 Open the page in light and dark schemes. Figure 1's *draft* tag and the moved divider are legible, and nothing overflows at phone width.
- [x] 4.3 Prose diffs stay one block per paragraph, wrapped near 78 columns, with typographic quotes.
- [x] 4.4 Draft notes: every label sits in its own `aside.draft-note`, and the §8 note is still present.
- [x] 4.5 Run `openspec validate update-paper-for-episodes-site --strict`.
