## Context

The paper argues from action and attention. This change adds the philosophy
of memory and of knowledge it leans on without citing, and the objections a
philosophical reader would raise first. It is constrained by the paper-site
spec: one static file, prose one block per paragraph near 78 columns, stable
ids, draft notes for anything unsettled, and agreement with each format’s
README.

## Goals / Non-Goals

**Goals:**
- Each addition does work in the argument it joins, rather than sitting in a
  survey. Each one either grounds a design rule, meets an objection, or
  settles an open question.
- Nothing said about particulars or episodes contradicts their READMEs. The
  redaction passage is checked against particulars’ *Redaction* section and
  the episodes README’s *Redaction* and `source_status`.
- Quotations stay short and are from works in the public domain or are a few
  words with a citation; everything else is paraphrase.

**Non-Goals:**
- A new numbered section. The paper’s structure holds; every addition is a
  subsection or a paragraph, so the contents list and existing ids don’t move.
- Stiegler, Derrida’s *Pharmacy*, and AGM belief revision. Each is relevant,
  but the *Phaedrus* and Harman already carry the argument, and the paper is
  long.
- `source_status` as a breakdown in §9.

## Decisions

**Ricoeur goes in §1, not §8.** Two kinds of forgetting is about the paper’s
title and its first argument, not about episodes. Placed after *Active
forgetting*, it qualifies Nietzsche at once: most of what the paper calls
forgetting is Ricoeur’s reserve forgetting, and erasure is the other kind.
The passage states what redaction is in both formats only at the level the
READMEs agree on: explicit, irreversible, never a side effect, not
cascading, and silent on git history.

**Harman is met head on, as a subsection of §4.** He is the objection, so he
gets his own heading and id. The answer is that both his premises are about
the cost to a limited mind of keeping reasons, and an external store moves
that cost off the mind. His principles of conservatism and clutter avoidance
are then shown to be design rules the formats already follow.

**Hegel with a caveat.** The thesis, antithesis and synthesis vocabulary is
Fichte’s and Chalybäus’s, not Hegel’s. The paper says so in one sentence
rather than let a reader catch it. What the format takes from Hegel is
*Aufhebung*: the synthesis cancels and keeps its inputs.

**Bad faith is answered in §6, and §11 keeps only the remainder.** The answer
belongs beside Bratman, where the format’s settled plans are introduced.
What stays open is whether a terminus titled as a person (*being someone
who…*) invites the *idem* reading the answer warns against. That is put as
the reduced open question.

**Narrative identity gets a draft note.** Whether a terminus presupposes that
a person narrates their life is a real question about the format, and the
paper’s answer (a terminus is a standing self-understanding, not a story) is
offered as provisional.

**A new requirement, not a check in tasks.** With some twenty new works cited,
a requirement that every cited work appears in the References is cheap to
check and keeps future edits honest.

## Risks / Trade-offs

- [The paper grows by about a fifth] → Each addition is kept to what the
  argument needs. Survey material is cut.
- [Readings of Ricoeur, Harman and Hegel are contestable] → Each is stated at
  the level of the standard reading, cited to a specific work, and any
  stronger use is marked as the paper’s own.
