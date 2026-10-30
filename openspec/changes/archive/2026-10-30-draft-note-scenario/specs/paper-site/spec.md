## MODIFIED Requirements

### Requirement: Draft notes stay visible and marked as open
Every *Draft note* in the paper SHALL be rendered as a distinct element, labelled "Draft note" and styled so that it reads as unsettled, apart from the surrounding argument, in both colour schemes.

#### Scenario: Every note is marked
- **WHEN** the page's draft-note elements and its "Draft note" labels are listed
- **THEN** every label is inside a draft-note element, and every draft-note element carries exactly one label

#### Scenario: A settled note is removed
- **WHEN** the question a draft note raises is settled
- **THEN** the note is removed, its answer is carried in the surrounding argument, and the page still satisfies *Every note is marked*
