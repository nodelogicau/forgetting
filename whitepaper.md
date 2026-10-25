# Forgetting

**Why we externalise memory, what kinds there are, and how particulars and
intentions fit together**

> **Draft.** Started 2026-10-25 from
> [particulars#35](https://github.com/nodelogicau/particulars/issues/35).
> Sections marked *Draft note* are where the argument is still thin or a
> decision is open. Nothing here is normative: the specifications are
> [particulars](https://github.com/nodelogicau/particulars) and
> [intentions](https://github.com/nodelogicau/intentions).

---

## Summary

People act best when their attention is on what is in front of them. What
they believe, what they want, and what they have promised compete with that
for as long as they're held in the head. This paper argues for a family of
open formats that hold those things outside the head, so that a person can
forget them and trust that they are kept.

Forgetting is only safe if the store remembers more than the head would have.
In particular it has to remember where each thing came from. That is the
property every format in the family shares, and the reason they keep
provenance when other memory systems don't.

The family models memory as several kinds rather than one store, because each
kind is externalised for a different reason, changes in a different way, and
needs the person's attention again for a different reason. particulars holds
semantic memory: what is believed about things in the world. intentions holds
prospective memory: what a person means to do, and why. Episodic and
procedural memory are not yet specified, and the paper ends with what each
would need.

---

## 1. Why forget

### The overthinker

Dostoevsky's underground man can't act. Every reason he finds for acting
draws another, more primary reason after it: "Where are my primary causes on
which I can rest? Where are my foundations?" The regress has no floor, and
the result of so much consciousness, he says, is inertia. The man of action,
by contrast, simply stops at the nearest cause and takes it for a foundation.
He is calm because he doesn't look closely.

Neither is a good model of a person living well. One examines everything and
does nothing. The other acts, but on foundations he never chose and couldn't
defend.

### Active forgetting

Nietzsche's answer is that forgetting is not a failure of memory but a power
in its own right: "there could be no happiness, no cheerfulness, no hope, no pride, no
present, without forgetfulness" (*Genealogy of Morals*, II §1, tr. Kaufmann).
In the earlier essay "On the Uses and Disadvantages of History for Life", the
herd grazing "unhistorically" is content, and a person who can't stop
carrying the past is paralysed by it. To act, something has to be let go of.

Nietzsche meant digestion: experience absorbed so completely it no longer
needs recalling. This paper borrows the phrase for something more literal.
A person can let a belief or a plan go *if it is kept somewhere else*. The
regress stops not because the person stopped looking, as the man of action
did, but because the foundations are written down, chosen, and open to
inspection whenever they're needed. Then they're not needed most of the time.

Nietzsche frees the present from the past. Camus asks the same of the
future: "Real generosity toward the future lies in giving all to the
present" (*The Rebel*, "Thought at the Meridian"). That can sound like a case
against planning, but it is the case for keeping plans somewhere else. A
person can give everything to the present only if the future they mean to
build is held for them, and comes back when it needs them.

### The ready-to-hand

Heidegger gives the shape of what forgetting buys. Equipment that works is
*ready-to-hand*: it withdraws into the activity, and you attend to the work,
not the hammer (*Being and Time*, §15). Only when it breaks down does it
become *present-at-hand*, an object to stare at and think about (§16).

Beliefs and intentions held in the head never fully withdraw. Unfinished goals
keep intruding on unrelated tasks until a plan has been made for them, at
which point the intrusion stops even though the goal is still unfinished
(Zeigarnik 1927; Masicampo and Baumeister 2011). Kept outside the head and
trusted, they can behave like equipment: absent while things go well, back in
view the moment something goes wrong.

Heidegger names three ways equipment comes back into view, and each has an
analogue here:

| Breakdown | Equipment | Externalised memory |
|---|---|---|
| Conspicuous | The tool is broken | A belief is contradicted |
| Obtrusive | The tool is missing | Recall finds nothing about something that matters |
| Obstinate | Something is in the way | A commitment clashes with what the person meant to do |

The design rule that follows is that the formats should be quiet until a
breakdown and loud at one. Most of the machinery in both specifications is
about knowing when that moment has come.

> *Draft note.* The table is a proposal. Check it against §16 and decide
> whether it earns its place or is too neat.

### Becoming who you are

Letting go of what you hold is half of it. The other half is that what you
hold can be examined. Frankfurt describes a person as someone who can want to
want something: who has desires about their desires and can ask whether the
wants that move them are ones they endorse (Frankfurt 1971). That is the
shape of "becoming a better self", and it needs the wants to be visible. You
can't easily examine a belief you can't see, or test a desire you have never
written down.

Nietzsche's subtitle to *Ecce Homo* is "how one becomes what one is". The
intentions format takes that literally. Every intention must say what it is
for, and the chain of reasons ends in a *terminus*: a standing
self-understanding, titled as a person rather than a task, such as *being
someone who follows through*. That is the format's answer to the underground
man: the regress ends at a foundation the person has chosen and written down.

### What this asks of the store

If a person is going to forget something on the strength of a store, the
store has to be trustworthy in a specific way. Clark and Chalmers, arguing
that a notebook can be part of a mind, set conditions for when an external
store counts: it is reliably available, readily used, trusted when it is
consulted, and was endorsed when it was written (Clark and Chalmers 1998).
Each reads as a requirement on a harness. The last is the one most agent
memory fails, because it doesn't record who wrote what. That is the subject
of section 4.

---

## 2. Memory, briefly

Psychology distinguishes kinds of memory that behave differently, and the
distinctions turn out to matter for design.

- **Retrospective and prospective.** Retrospective memory is of what has
  been. Prospective memory is remembering to do something in the future
  (Einstein and McDaniel 1990). Most memory research, and almost all agent
  memory, is retrospective.
- **Episodic and semantic.** Episodic memory is of events, located in time
  and place: *the certificate was renewed on Tuesday*. Semantic memory is of
  facts, detached from when they were learned: *the certificate expires in
  March* (Tulving 1972).
- **Declarative and procedural.** Episodic and semantic memory are both
  *knowing that*. Procedural memory is *knowing how*: skills and habits,
  exercised rather than recalled (Cohen and Squire 1980).
- **Source monitoring.** Remembering *where* something was learned is a
  separate process from remembering the thing, and it fails separately.
  People routinely retain a fact while losing its source, and misattribute
  sources in systematic ways (Johnson, Hashtroudi and Lindsay 1993). In its
  extreme form this is *source amnesia* (Schacter, Harbluk and McLachlan
  1984).

The point for design is that each kind changes differently:

| Memory | Lets the person stop holding… | Changes by | Needs attention when |
|---|---|---|---|
| Semantic | what they believe, and why | reconciliation | contradicted |
| Prospective | what they want and have committed to | resolution or retirement | due, blocked, or undermined by a changed belief |
| Episodic | what actually happened | accumulation only | reflecting: did I act as I meant to? |
| Procedural | how to do things | supersession and re-verification | it stops working |

You don't reconcile a past event, only beliefs about it. You don't contradict
a plan, you retire it. A store that treats all four the same will get at
least three of them wrong. That's why the family is several formats.

---

## 3. Why agents forget, and why it matters to the person

AI assistants are now where many people capture and reason over what they
know and mean to do. Their memory fails in three ways.

**It is siloed.** What one harness learns is invisible to another, and to the
person outside it. There is no equivalent of `.ics` for beliefs or plans.

**It has no provenance.** Agent memory typically stores the content and loses
the source: source amnesia, by design. A belief whose source is gone can only
be overwritten, not weighed. And because an assistant writes much of what it
remembers, the person can't tell which beliefs are theirs, which they were
told, and which the assistant inferred.

**It treats contradiction as overwrite.** When new information conflicts with
old, the old is replaced. The fact that a belief changed, why, and on whose
word, is lost, and with it the ability to notice that the source of the
change was wrong.

For the agent these are accuracy problems. For the person they are the
reason they can't let go. A store that might silently replace a belief, or
can't say where one came from, has to be checked, and a store that has to be
checked is present-at-hand all the time. It costs the attention it was meant
to free.

---

## 4. The provenance spine

Every format in the family shares a small set of conventions. Together they
are what make forgetting safe.

- **Every object says who wrote it.** A `source` names the person, the
  harness, and the model, as applicable. An agent acting alone is a valid
  source, and so is a person working without one; a source naming neither is
  malformed.
- **Authors are URIs.** The person who asserted something is a particular in
  their own right, and can be reasoned about: whether their claims tend to
  hold up, which other claims came from them.
- **Ids are prefixed UUIDv7.** Time-ordered, so a directory listing is a
  chronology, and typed by prefix, so an id says what it points at.
- **Files over databases.** YAML files in git. History, authorship and review
  come from git; an index is a cache of the files, never the reverse.
- **History is kept.** In particulars nothing is overwritten: a claim is
  retracted by appending a record, and belief changes only by synthesis. In
  intentions, objects are live state and are edited in place, but the events
  that happen to them are appended and never rewritten.

Provenance does two jobs. It lets an agent weigh conflicting information
instead of overwriting it, which is what particulars' dialectic is built on.
And it lets the person forget without abdicating: a belief can be put down
because it can always be picked up again with its reasons attached.

It matters most when an agent does the writing. intentions puts this sharply:
a harness may draft, but it may not make an intention firm, select a
placement, or accept a commitment without the person's act or a policy they
hold. Authorship is what distinguishes a person's own resolve from an
accumulation of other people's claims on their time. The same holds for
belief. A belief an assistant inferred shouldn't quietly become the person's.

> *Draft note.* intentions copies these conventions from particulars by
> agreement. Whether they should become a spec of their own is open
> (section 10).

---

## 5. Semantic memory: particulars

particulars, the Dialectical Knowledge Format (DKF), holds what is believed
about things in the world. Its objects are **particulars** (the things),
**claims** (assertions about them, each with a source and what backs it), and
**syntheses** (reconciliations of claims into a current belief, citing their
inputs).

Because claims keep their sources, a contradiction is evidence on both sides
rather than an error. The format takes its structure from dialectic: a claim
is met by a contrary claim, and a synthesis reconciles them, carrying the
reasoning. The synthesis becomes the new current belief, open to being
contradicted in turn.

What is computable without a model in the loop is what has *not* been
reconciled: claims newer than the current belief, and syntheses resting on
retracted inputs. That is exactly the conspicuous breakdown of section 1. A
well-behaved harness says nothing about a particular whose belief is settled,
and surfaces it when something new arrives that the current belief doesn't
account for.

particulars is the retrospective layer: what is known. It is deliberately
*not* a log of events, and not a store of procedures.

---

## 6. Prospective memory: intentions

intentions holds what a person means to do with their time. It replaces the
calendar's slot with a duration, a window, and a reason. It separates three
rungs that a calendar collapses:

- **Desire.** A want, expressed but not adopted. Desires may contradict each
  other freely and are checked against nothing. A passing remark goes here
  until the person adopts it or lets it go.
- **Intention.** A plan the person has adopted, which costs a why: it must
  serve something, and the chain of what it serves ends in a terminus, a
  self-understanding.
- **Commitment.** Where another party is involved, with a status per party
  that only that party can change.

This is the Belief–Desire–Intention structure of practical reasoning (Bratman
1987; Rao and Georgeff 1991), with particulars supplying the beliefs. It's
also Frankfurt's structure: desires that can be inspected, and adoption as
the act of endorsing one.

The format's design principles read as a theory of what to forget. "A plan
made is a plan the mind lets go of, whether or not it is done yet." A
settled plan spares a limited agent from deliberating again (Bratman 1987),
but only if it is held somewhere the person trusts, ends at a reason the
person has chosen to rest on, and comes back only when something actually
conflicts with it. Resolution ranks placements and never chooses. Clashes are
flags, never decisions. Both keep the person's acts the person's.

Implementation intentions, "when X, I will Y", are the strongest known form
of a decision closed in advance (Gollwitzer 1999), and intentions' policies
are where they live.

---

## 7. How they meet

The formats are coupled only through the URIs of the particulars they share.
A claim may cite an intention by id, and an intention may point at a claim,
but neither validates the other, and no reference is resolved across them.
Loose coupling is deliberate: each format can be adopted, implemented and
versioned alone.

Behaviour that spans both belongs in harness patterns, not in either
specification. Two are already clear.

**News for a plan.** An intention names a subject, parties and locations,
all particulars. A harness can recall what DKF believes about each, and any
belief newer than the intention's last edit is news the person may need. That
is the obstinate breakdown: something changed in the world that gets in the
way of the plan.

**The return path.** The intentions terminus *being someone who follows
through* references a DKF claim the person holds about themselves. That claim
is held because DKF records what they did. People infer who they are from
what they observe themselves doing (Bem 1972), so a self-understanding that
cites evidence is one the person can believe, and one that cites none is a
hope. This is where a record of episodes would make the loop work, and it is
the strongest argument for the gap in the next section.

> *Draft note.* Are there other harness patterns worth naming here? Candidates:
> a commitment imported from iCalendar that contradicts a DKF belief about a
> party; a desire whose stated reason is a belief that has since been retracted.

---

## 8. The gaps

### Episodic memory

Today a person who wants to record that *the certificate was renewed on
Tuesday* writes a DKF claim about the event. intentions says outright that a
retrospective account of what happened is not its job. So episodes are pushed
into a format built for reconciliation, where they don't belong: you don't
reconcile a past event, and an event log only accumulates.

That would be a small mismatch if episodes were peripheral. They are not.
Episodic memory is where the loop between intending and doing closes. Without
a record of what was done, there is nothing to compare against what was
meant, nothing for a self-understanding to cite, and no basis for asking
whether a person is becoming who they meant to be. Reflection, the fourth
row of the table in section 2, has nothing to work on.

> *Draft note.* Is this a third format or a DKF extension? Episodes need no
> dialectic, which points to a separate format. They take particulars as
> subjects and would be cited by claims constantly, which points to an
> extension.

### Procedural memory

Procedural memory exists in the ecosystem but outside any format: in skills
(`SKILL.md`), in prompts, and in a DKF workspace's `dkf.md` conventions
document, which addresses an agent without constraining anything.

Procedures change by supersession and need re-verification, and their
breakdown is the plainest of all: they stop working. Whether they need a
format, or whether skills already are one, is open.

---

## 9. Measuring it

Agent memory is commonly evaluated with LongMemEval, which tests information
extraction, multi-session reasoning, temporal reasoning, knowledge updates and
abstention over long chat histories (Wu et al. 2024). Most of its questions
are episodic: what was said, and when.

Read through the memory framing, the categories divide between the layers:

| Category | Owning layer | What DKF should be judged on |
|---|---|---|
| Knowledge update | Semantic | Reconciling, not overwriting; the current belief and why |
| Abstention | Semantic | Knowing what isn't known |
| Information extraction | Episodic, via ingestion | Whether ingestion captured it as a claim |
| Multi-session reasoning | Episodic and semantic | Synthesis across sources |
| Temporal reasoning | Episodic | Mostly out of scope until an episodic format exists |

DKF should be judged mainly on knowledge update, abstention and provenance,
and on ingestion for the rest. intentions-bench measures something
LongMemEval doesn't: whether a remark lands on the right rung, whether the
window is kept as the person said it, and whether the agent refrains from
acts that are the person's.

What no benchmark measures yet is the thing this paper is about: whether a
person can stop holding something. A proxy might be how often the store
needs checking, or how many surfaced items were genuine breakdowns rather
than noise.

> *Draft note.* Confirm the category mapping against particulars-bench's
> stratification and current results before publishing.

---

## 10. Open questions

- **Should the provenance spine be its own specification?** intentions copies
  DKF's id and author shape by agreement. A shared spec would make the family
  explicit, but is itself a form of coupling.
- **Is episodic memory a third format or a DKF extension?** See section 8.
- **Does the human purpose belong in the specifications?** Each
  specification's *Purpose* is about the format. Helping a person act with
  purpose may belong only here and on the landing pages, so the specs stay
  neutral about what they are used for.
- **When does upkeep become the breakdown?** A store the person has to tend
  is present-at-hand itself. The harness has to take on capture,
  reconciliation and surfacing so the person doesn't. How much can it take on
  before authorship is lost?
- **Agent or person?** The formats serve an agent's memory and a person's
  alike. The motivation is about the person; the benchmarks are about the
  agent. One reading is that the agent is the harness that keeps a person's
  externalised self.
- **Settled plans or radical freedom?** Sartre holds that no past choice
  binds: a person chooses again in every moment, and the anguish of that is
  the price of freedom. intentions sides with Bratman, holding that settled
  plans are what let a limited agent act at all. The paper should say why,
  and what the format does to keep a settled plan from becoming bad faith.

---

## References

**Philosophy.**
Fyodor Dostoevsky, *Notes from Underground* (1864), Part I §5.
Friedrich Nietzsche, "On the Uses and Disadvantages of History for Life"
(1874); *On the Genealogy of Morals* (1887), II §1; *Ecce Homo* (1888).
Martin Heidegger, *Being and Time* (1927), §§15–16.
Jean-Paul Sartre, *Being and Nothingness* (1943).
Albert Camus, *The Rebel* (1951), tr. Anthony Bower, "Thought at the
Meridian".
Harry Frankfurt, "Freedom of the will and the concept of a person",
*Journal of Philosophy* (1971).
Michael Bratman, *Intention, Plans, and Practical Reason* (1987).
Andy Clark and David Chalmers, "The extended mind", *Analysis* (1998).

**Psychology.**
Bluma Zeigarnik, "Das Behalten erledigter und unerledigter Handlungen",
*Psychologische Forschung* (1927).
Endel Tulving, "Episodic and semantic memory" (1972).
Daryl Bem, "Self-perception theory" (1972).
Neal Cohen and Larry Squire, "Preserved learning and retention of
pattern-analyzing skill in amnesia", *Science* (1980).
Daniel Schacter, Joan Harbluk and Donald McLachlan, "Retrieval without
recollection: an experimental analysis of source amnesia", *Journal of Verbal
Learning and Verbal Behavior* (1984).
Gilles Einstein and Mark McDaniel, "Normal aging and prospective memory",
*JEP: Learning, Memory, and Cognition* (1990).
Marcia Johnson, Shahin Hashtroudi and D. Stephen Lindsay, "Source
monitoring", *Psychological Bulletin* (1993).
Peter Gollwitzer, "Implementation intentions: strong effects of simple
plans", *American Psychologist* (1999).
E. J. Masicampo and Roy Baumeister, "Consider it done! Plan making can
eliminate the cognitive effects of unfulfilled goals", *JPSP* (2011).
Evan Risko and Sam Gilbert, "Cognitive offloading", *Trends in Cognitive
Sciences* (2016).

**Agents and evaluation.**
Anand Rao and Michael Georgeff, "Modeling rational agents within a
BDI-architecture", *KR* (1991).
Di Wu et al., "LongMemEval: benchmarking chat assistants on long-term
interactive memory" (2024).

**The formats.**
[particulars](https://github.com/nodelogicau/particulars) ·
[particulars-bench](https://github.com/nodelogicau/particulars-bench) ·
[intentions](https://github.com/nodelogicau/intentions) ·
[intentions-bench](https://github.com/nodelogicau/intentions-bench)
