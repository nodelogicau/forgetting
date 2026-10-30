## Why

The scenario under *Draft notes stay visible and marked as open* counts the page's draft notes against the number in `whitepaper.md` at the last commit before it became a stub. That was a migration check. The page has been the only copy since, and section 9 added three notes and particulars#42 settled one, so the count is now 7 and the scenario fails although every note is rendered as the requirement asks.

## What Changes

- Replace *The draft notes are counted* with a scenario that checks every note on the page as it stands: every "Draft note" label is inside a draft-note element, and every draft-note element carries the label.
- Add a scenario saying that a settled note is removed and its answer moves into the argument, so the number of notes is free to change.

## Capabilities

### New Capabilities

None.

### Modified Capabilities

- `paper-site`: *Draft notes stay visible and marked as open* gets two new scenarios in place of the migration count.

## Impact

- `openspec/specs/paper-site/spec.md`: one requirement.
- `docs/index.html`: no change. The page already has 7 labelled notes, each in its own element.
