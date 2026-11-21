## Context

The paper was written when episodes was a gap, then a draft repository. Now it has a site (https://episodes.fyi) and a reference implementation (episodes-cli 0.2.0). The README still opens with "Draft. Nothing in this document is declared," and `episodes/0.1` has not been reached. So episodes sits between a specified format and a gap, and the paper has to show it as neither.

The page is constrained by the paper-site spec: one static file, a neutral palette, distinctions drawn with rules, italics and weight, not fills or hues, stable section ids, and prose wrapped one block per paragraph.

## Goals / Non-Goals

**Goals:**
- Every statement the paper makes about episodes agrees with the episodes README on `main`.
- A reader of the title block learns that there are three formats with sites, and that one of them is a draft.
- The spec requires both of these, so the drift can't come back unnoticed.

**Non-Goals:**
- New argument drawn from episodes: source deletion is not forgetting, redaction, `source_status`. That is a separate change.
- Renaming §8 *The gaps* or its id. The section still argues for the gap episodes fills, and ids don't change.
- Removing §8's draft note. It is settled at `episodes/0.1`, not by the site launch.

## Decisions

**Figure 1: episodic joins the formats, tagged draft.** The divider moves right, between episodic and procedural. The *the formats* label is centred over three boxes and *the gap* (singular) over one. The episodic box gets the solid `box` class and a solid edge to the spine. Its middle line is `episodes`, linked to https://episodes.fyi, in weight 600 like its siblings. A `small` italic `draft` tag sits inside the box, so that its status travels with it.
- *Alternative: keep it in gap style and link it.* That understates a format with a site and an implementation, and it leaves Figure 1 telling the reader two formats when the status line says three.
- *Alternative: a third, intermediate box style.* The palette rule leaves only stroke weight and dash for it, and a third dash pattern beside `box-gap` would be hard to read. A word is clearer than a stroke.

The episodic box moves from x = 425 to 410, so the three formats are evenly spaced (gaps of 15) and the wider gap of 30 falls at the divider (x = 605) before procedural. Procedural and the spine don't move. When the box was left at 425, the rendered figure showed the old gap between intentions and episodic and read as two groups.

**§7: the claim carries both citations.** Rewrite the last sentence of *The return path* to the README's direction of reference: a claim cites the episode as its evidence and cites the intention it bears on, and the self-understanding cites that claim. This is the same chain §9 describes, so the two sections now agree with each other as well as with the README.

**Status paragraph and footer wording.** The status paragraph names the three specifications and adds that episodes is a draft, for example: "…particulars (particulars.fyi), intentions (intentions.fyi), and episodes (episodes.fyi), which is still a draft." The footer's "the reasoning behind particulars and intentions" names all three, and only the status paragraph carries the draft qualifier. *The formats* in the References adds an episodes.fyi link and keeps "(draft)".

**Spec: extend, not fork, the agreement requirement.** *Claims about a format agree with its README* names episodes, and its scenario adds §8 and §9 (and §7 for the return path) against the episodes README. No separate requirement for episodes, because the rule is the same for every format.

## Risks / Trade-offs

- [Figure 1 says "three formats" while episodes is undeclared] → The *draft* tag in the box and the status line both qualify it. §8's draft note stays as the trigger for re-checking.
- [The episodes README changes before 0.1, and the paper drifts again] → The extended agreement requirement makes it a spec failure. The §8 draft note names the checkpoint.
- [The fetched README was partly summarised in exploration] → Each sentence changed in §7 and the status line is checked against the README's verbatim text before commit.
