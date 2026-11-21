## MODIFIED Requirements

### Requirement: The page opens with a paper's title block
The page SHALL open with a title block, not a product hero: the series name "Forgetting", the title "Remember forward.", the paper's subtitle, an epigraph quoting "It's a poor sort of memory that only works backwards" and crediting the White Queen in Lewis Carroll's *Through the Looking-Glass*, and a status paragraph stating that the paper is a draft, that nothing in it is normative, and linking to https://particulars.fyi, https://intentions.fyi and https://episodes.fyi. The status paragraph SHALL say that episodes is itself a draft for as long as its README declares nothing. The References SHALL list *Through the Looking-Glass*. The title block SHALL contain no buttons or calls to action, and no heading on the page SHALL name a writer.

#### Scenario: A reader arrives
- **WHEN** the page loads at the top on a desktop viewport
- **THEN** the title, subtitle, epigraph and status paragraph are visible without scrolling, and the paper's text follows the figure and contents without anything in between

#### Scenario: The epigraph is traced
- **WHEN** the epigraph's credit is read against the References
- **THEN** *Through the Looking-Glass* is listed there

#### Scenario: A reader follows a sibling link
- **WHEN** the particulars.fyi, intentions.fyi or episodes.fyi link in the status paragraph is activated
- **THEN** the browser lands on that format's site

#### Scenario: The status of episodes is read
- **WHEN** the status paragraph is read while the episodes README opens with "Nothing in this document is declared"
- **THEN** the paragraph says that episodes is a draft

### Requirement: The figure shows the kinds of memory over the provenance spine
The title block's figure SHALL show four kinds of memory. Three SHALL be drawn as formats in the solid style: semantic, labelled particulars; prospective, labelled intentions; and episodic, labelled episodes. One SHALL be drawn as a gap, in a visibly different style: procedural. While the episodes README declares nothing, the episodes element SHALL carry a visible *draft* tag inside its box. The figure SHALL show provenance as a band beneath all four. The particulars, intentions and episodes elements SHALL link to their sites. The SVG SHALL carry a `<title>` and `<desc>`, and the `<desc>` and the caption SHALL agree with the drawing about which kinds are formats, which is a draft, and which is the gap.

#### Scenario: The diagram is read
- **WHEN** the figure is read
- **THEN** three kinds appear as formats, episodes among them tagged as a draft, one appears as a gap, and provenance spans all four

#### Scenario: The diagram is read against the paper
- **WHEN** each label is compared with §2, §4 and §8
- **THEN** no label says something those sections do not

#### Scenario: A reader follows a format in the figure
- **WHEN** the particulars, intentions or episodes label in the figure is activated
- **THEN** the browser lands on that format's site

### Requirement: Claims about a format agree with its README
Nothing the page states about what particulars, intentions or episodes does SHALL contradict that format's README on `main` at the time of publication. The page MAY argue for why a format is as it is.

#### Scenario: The format sections are checked
- **WHEN** §5, §6 and §7 are read against the particulars and intentions READMEs
- **THEN** no sentence asserts a behaviour the relevant README contradicts

#### Scenario: The episodic passages are checked
- **WHEN** §7, §8 and §9, and Figure 2's description and caption, are read against the episodes README
- **THEN** no sentence asserts a behaviour that README contradicts, and in particular none says that an episode names or cites an intention
