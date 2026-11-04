---
name: aim-higher
description: "Raises the ceiling on a task before work starts, using the four kinds of ambition (speed, altitude, depth, range) from Felix Rieseberg's 13 October 2026 essay on being more ambitious with models. Use whenever someone commissions substantial work and the ask is pitched at the literal task rather than the outcome behind it: a tracker, report, letter, analysis, reconciliation, listing, plan, build or fix. Also use it on aim higher, be more ambitious, think bigger, what would an expert do, go deeper, am I asking for the right thing, or /aim-higher. Use it before a multi-session build, a forensic or financial analysis, or anything producing a recurring deliverable. Use it on correspondence and filings too: an email, letter, demand, motion or opposition is a decision document, not creative work. Do NOT use it on fiction or voice work, on a one-step factual answer, or on a task already scoped with instructions to execute as written."
---

# Aim Higher

Felix Rieseberg's claim is that the model is no longer the limit, the size of the ask is. He sorts ambition into four kinds and skips the first, because everyone already does it.

| Kind | The move | Status here |
|---|---|---|
| **Speed** | Same work, less time | Already the default. Needs no skill. |
| **Altitude** | Work the outcome, not the task | Lever 1 |
| **Depth** | Work the way the best in the field work | Lever 2 |
| **Range** | Bring in other fields and their instruments | Lever 3 |

This is not a prompt pack. A pasted prompt is a one-off. What changes results is that the three questions get asked before work starts, every time, and answered against what is actually there rather than what is assumed.

## The guardrail that comes first

Rieseberg's depth technique "pick unreasonable goals and tell the model they're very reasonable" is sound, and it is also the one way this skill can cause real harm.

**An unreasonable TARGET is fine. An unreasonable CLAIM is a lie.** Asking for 200ms when the page takes 5s is good practice. Reporting 200ms because it was the target is a false statement. The same holds for every number: a recall figure, a reconciliation total, a word count, a deadline.

So raising a target changes what gets attempted and changes nothing about what gets asserted. Every claim keeps its provenance, every computed number comes from a tool run in that session, and a search that found nothing is a statement about where you looked, not about what exists. If ambition and verification pull against each other, verification wins and the gap gets stated: "the target was X, the measured result is Y."

Close every piece of work this skill touches with four lines:

```
Target aimed at: <the raised target>
Measured result: <what the tool returned, with the tool named>
Gap:             <the difference, stated plainly>
Judged by:       <the outside check that settled it>
Not verified:    <anything still open, named>
```

## Lever 1, Altitude: what is the goal beyond the goal

Rieseberg's test: ask what should happen next, and keep asking until the answer stops being a document. He notes altitude helps most when the work feeds a meeting or a decision, and least on creative work.

Produce three rungs. Pick one and name the rung below it as the fallback, rather than presenting a menu:

1. **The literal ask, done well.** State it in a line so there is a floor.
2. **The decision it serves.** Give the model the raw material and ask what changed, why, and what to do. Then name the two or three decisions that are genuinely urgent, each with the case for and against.
3. **The thing that replaces the ask.** Design something better than the deliverable, test that design against the project's own history, and propose running it beside the current way for one cycle.

Worked shape: someone asks for a permit tracker. Rung 1 is the tracker. Rung 2 is which three permits are most likely to slip and what moves each. Rung 3 is a process that flags a slip before the counterparty does, validated against the permits that already slipped.

**The part people skip.** Rieseberg had to change his own workflow before altitude was possible: he made crash reports fetchable, mapped app versions to commits, and gave the model machines to reproduce on. The analogue is almost always access to the raw source rather than a summary of it. Name the missing access explicitly, because without it rung 3 is theatre. Typical gaps: the portal rather than the exported report, the console rather than the screenshot, the accounting file rather than the statement PDF, transaction data rather than a monthly total.

**Skip this lever on fiction and voice work.** A letter, an email and a filing are decision documents and altitude applies fully; a novel is not.

## Lever 2, Depth: work the way the best in the field work

Open with Rieseberg's framing: a deeper version of the task, not a bigger one. More pages is not depth.

1. **Use the instruments the best in the field use.** If the honest instrument is a database and a statistical test, do not hand back a markdown table. A spreadsheet whose totals are typed literals cannot disagree with its inputs, so it will never report an error.
2. **Pick an unreasonable goal and treat it as reasonable.** Subject to the guardrail above.
3. **Challenge what the user already believes.** Take the stated premise to the rawest source and test it adversarially rather than restating it. Say what in the premise does not survive the data, before saying what does.
4. **Produce new knowledge.** Once deep in the data, hunt the blind spot. Build the small simulation, then test its predictions against data it has not seen.
5. **Use an outside judge, never self-assessment.** Rieseberg says ideally a tool the model can run for immediate feedback.

### The outside judge is the lever that gets skipped

A judge is something that can **refuse**. Not a second opinion, not a checklist, not a re-read. Build or borrow one per kind of work:

| Kind of work | A judge that can refuse |
|---|---|
| Any multi-part build or audit | A gate file with a runnable check and an expected output, where the claim of completion fails unless the check passes |
| A figure or a total | A script that recomputes from inputs and exits non-zero on a mismatch, with the match count asserted in advance |
| "It is not there" | A search tool that reports which roots it could not finish, so absence is never inferred from a partial pass |
| A document leaving for someone else | A scan that blocks on an identifier or an unreviewed name |
| Prose against a style rule | A linter over the rules that are mechanically decidable, which refuses rather than advises |
| A prior conclusion | A ledger of determinations with sources and dates, verified rather than re-derived |

Where no tool fits, the judge is the primary source read directly. It is never the model's own read of its own output.

### The four-question depth prompt

Answer all four before starting, and show the rewritten ask:

1. What would the best person in this field do that has not been asked for?
2. What is the rawest source material they would start from? Name the actual documents, not a summary.
3. What specific methods and tools would they use?
4. What, other than the user or the model, would show the result is right? Name a check that can be run.

Then rewrite the request to ask for exactly that, and show the rewrite before building.

Paste-ready wording per domain is in `references/prompts.md`.

## Lever 3, Range: other fields, and their people

1. **Replace the noun with the verb.** The deliverable is a thing; the job is an action. A quarterly review is not a deck, it is getting busy people to believe a story about cause and effect and decide under uncertainty. A demand letter is making payment the counterparty's cheapest path. A listing page is a stranger deciding to risk money on an unknown author. Credited to Tom Kelley and Jonathan Littman, *The Art of Innovation*.
2. **Assemble the crew.** Name the roles a strong team would have, including from outside the obvious discipline, and a red team. Rieseberg's examples: an analyst, a journalist, an editor, a motion and audio designer when the work gets presented, and a short seller plus a forensic accountant as the red team. Per-domain crews are in `references/crews.md`.
3. **Act, do not roleplay.** Ask for the work the role does, not the voice it writes in. "Write like a forensic accountant" produces stranger prose and no better answer. "Tie every disclosed figure to a bank line and list what does not tie" produces the answer.

**On naming roles.** Much prompting advice says to assign a persona, and Rieseberg says avoid roleplay. Both are right about different things: name the role so its *standard* applies, then ask for its *output*, never its register.

## Sequence

1. Read whatever record of the project's current state exists. Without it, any higher target is guessed.
2. **Altitude.** Give the rungs and the access gap. Pick one, name the fallback.
3. **Depth.** Answer the four questions, name the judge, show the rewritten ask.
4. **Range.** Verb not noun, name the crew, assign work not voices.
5. Hand off to whatever review and completion discipline the project uses.
6. Report against the target, with the four closing lines.

Do not run all of this on a small task. One or two rungs and a named judge is the whole of it on a half-hour job. The full sequence earns its cost on a multi-session build, a forensic analysis, a recurring deliverable, or anything read by someone who can say no.

## What good looks like

A reply from this skill does not open with a menu. It opens with the raised target in one line, then the rung, then the judge that will settle whether it worked. If it reads like a framework being applied rather than a better answer being proposed, the skill has failed and the plain answer was right.
