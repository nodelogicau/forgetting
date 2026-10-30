## Context

`paper-site` was written when the paper moved from `whitepaper.md` to `docs/index.html`. A count against the old file was a good check that the move dropped no notes. Now that the page is the only copy, it is the wrong check.

## Goals / Non-Goals

**Goals:** a scenario that holds for any number of notes and still catches a note that has lost its marking.

**Non-Goals:** changing how notes are styled, or which notes the paper carries.

## Decisions

**Check the pairing, not the number.** Every label is inside a note element, and every note element has the label. That catches the failure the requirement guards against: a note rendered as ordinary argument, or a styled box with no label. Pinning a number would break again on the next note anyone adds.

**Say what settling does.** A note that is settled is removed, and its answer goes into the prose, as particulars#42 did for section 9. Without this, "stay visible" could be read as "never removed".

## Risks / Trade-offs

- [The move-time check is lost] → The move happened in 2026-10-28-add-forgetting-fyi-site and passed then. Nothing now refers to `whitepaper.md`'s notes.
