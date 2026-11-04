# Paste-ready wording

Written to be used as-is rather than adapted. Each block is for a person to paste into any chat, or for the model to run against the task in front of it without being asked.

Contents: the depth prompt (generic, then six domain variants) · the altitude escalation · the range opener · the closing report.

---

## The depth prompt, generic

```
I want a deeper version of this task, not a bigger one.

Before you do anything, answer four things.
1. What would the best person in this field do that I have not asked for?
2. What is the rawest source material they would start from? Name the actual
   documents, not a summary of them.
3. What specific methods and tools would they use? If the honest answer is a
   database or a statistical test, say so and do not hand me a table instead.
4. What, other than you or me, would show the result is right? Name a check
   that can actually be run.

Then rewrite my request to ask for exactly that, and show me the rewrite
before you start.
```

---

## Forensic accounting and bank reconciliation

```
I want a deeper version of this, not a bigger one.

Answer these before touching the numbers.
1. What would a forensic accountant preparing for deposition do on this file
   that I have not asked for?
2. Name the rawest sources: which statements, which months, which account, the
   actual filenames. If a month is absent, say which places you searched.
3. Would you do this in a queryable dataset rather than a spreadsheet? If yes,
   say so. A workbook whose totals are typed cannot disagree with its inputs.
4. What settles whether the result is right, other than you or me? Name the
   bank line, the recorded document or the counterparty record.

Then tell me which of my assumptions does not survive the raw data, before
you tell me anything that confirms it.
```

## Construction, permits and inspections

```
I want a deeper version of this, not a bigger one.

1. What would an owner's representative who has taken ten of these through
   this jurisdiction do that I have not asked for?
2. What is the rawest source: the portal record, the stamped set, the
   inspection history, the condition of approval itself? Name it.
3. What method would they use to know a permit is slipping before the agency
   says so?
4. What proves it, other than you or me? The portal status, the inspection
   record, the signed card.

Then tell me which items on my list look closed and are not.
```

## A filing or a contested document

```
Before drafting anything, write the list of elements or issues that must be
established, and show it to me. Nothing outside that list goes in, nothing on
it gets skipped.

Then answer: what would the best practitioner in this area do that I have not
asked for; what is the rawest source for each element, by document and date;
what authority carries each proposition, one per proposition; and what, other
than you or me, confirms the authority is good.

If this matter already has a record of determinations, read it first and
verify its entries against the documents. Do not start the analysis over.
```

## A manuscript, listing or submission

```
I want a deeper version of this, not a bigger one.

1. What would an acquiring editor at a house that publishes this genre do with
   this that I have not asked for?
2. What is the rawest material: the manuscript file itself, the word count
   measured from it, the comparable titles' live listings.
3. What method would they use to decide rather than to describe? Name the
   markers of a strong book in this genre and score against them.
4. What tells us it worked, other than you or me? A real reader's behaviour,
   a sample drop-off, a comparable title's rank.

Do not quote a word count from memory or from your notes. Count it from the
file and give me the number and the file hash.
```

## An app release or a growth question

```
I want a deeper version of this, not a bigger one.

1. What would a live-ops lead on a top-grossing app do here that I have not
   asked for?
2. What is the rawest source: the console export, the crash report, the build
   file, the actual dependency versions on the branch we are on.
3. What method separates signal from noise at this volume? If the volume
   cannot support a conclusion, say so instead of giving me one.
4. What proves the change worked, other than you or me? Name the metric, the
   baseline and the window.

Tell me first which of my beliefs about this product the data does not
support.
```

## A brand, a name or a storefront

```
Before any positioning, taglines or art, run the clearance checks and report
each one separately as NO CONFLICT FOUND with the source, query and date,
CONFLICT FOUND with the link, or NOT CHECKED with the reason.

Never tell me a name is cleared, clear, safe, protectable or available. Tell
me what each search found. A search result is a statement about your search.

Then, for the survivors only: what would a brand lead selling into this
category do that I have not asked for, what is the rawest source for the
category's real buying behaviour, and what outside signal would show the
positioning works.
```

---

## The altitude escalation

```
Do not answer the task yet. Give me three versions of the ask.

1. The literal thing I asked for, in one line, so there is a floor.
2. The decision this actually serves: what changed, why, and the two or three
   decisions that are genuinely urgent, each with the case for and against.
3. The thing that would replace what I asked for: design something better than
   this deliverable, test the design against this project's own history, and
   tell me what it would take to run it alongside the current way for one
   cycle.

Then tell me what access you are missing to make number three real, naming the
portal, console, file or account.

Pick one and name the rung below it as the fallback. Do not give me a menu.
```

---

## The range opener

```
Two things before you start.

First, restate this as a verb, not a noun. Not the document, the job the
document does.

Second, name the crew a strong team would have for this, including at least
one role from outside the obvious discipline, plus a red team whose job is to
find what is wrong with the result.

Then do the work each role would do. Do not write in their voice. I want the
analysis a short seller would produce, not prose that sounds like one.
```

---

## The closing report

Ambition and honesty are reported together, so a raised target never becomes a claim:

```
Target aimed at: <the raised target>
Measured result: <what the tool actually returned, with the tool named>
Gap:             <the difference, stated plainly>
Judged by:       <the outside check that settled it>
Not verified:    <anything still open, named>
```
