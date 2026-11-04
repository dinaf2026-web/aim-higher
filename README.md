# aim-higher

A Claude skill that raises the ceiling on a task before any work starts.

Most prompting advice helps you get the thing you asked for, faster. This helps you notice that you asked for the wrong thing. It implements the four kinds of ambition from Felix Rieseberg's essay on being more ambitious with models, and adds the two pieces the essay leaves to the reader: a guardrail that stops a raised target from becoming an unverified claim, and a concrete answer to what an outside judge actually is.

## What it does

Four kinds of ambition. The first needs no help.

| Kind | The move |
|---|---|
| **Speed** | Same work, less time. Already everybody's default. |
| **Altitude** | Work the outcome, not the task. What is the goal beyond the goal? |
| **Depth** | Work the way the best in the field work. A deeper version, not a bigger one. |
| **Range** | Bring in other fields, their people and their instruments. |

**Altitude** produces three rungs: the literal ask done well, the decision it serves, and the thing that replaces the ask. It also names the access you are missing, because the ambitious version usually needs the raw source rather than a summary, and without it the top rung is theatre.

**Depth** carries five techniques and a four-question prompt that rewrites your request into the one a specialist would have made. Its hardest requirement is the outside judge: never let the model grade its own output.

**Range** replaces the noun with the verb, assembles a crew including a red team, and insists on acting rather than roleplaying. Ask for the work a role does, not the voice it writes in.

## The guardrail

The essay suggests picking unreasonable goals and telling the model they are reasonable. That is good practice and it is also the one way this gets dangerous.

**An unreasonable target is fine. An unreasonable claim is a lie.** Asking for 200ms when the page takes 5s raises what gets attempted. Reporting 200ms because that was the target is a false statement, and the same trap waits on a recall figure, a reconciliation total and a word count.

So every piece of work closes with four lines: the target aimed at, the measured result with the tool named, the gap stated plainly, and what judged it. Raising a target changes what gets attempted and changes nothing about what gets asserted.

## The outside judge

The essay says the judge should ideally be a tool the model can run. In practice that means something that can **refuse** — not a second opinion, not a re-read. The skill names one per kind of work: a gate whose check must pass before completion can be claimed, a script that recomputes a total and exits non-zero on a mismatch, a search that reports which places it could not finish so absence is never inferred from a partial pass, a scan that blocks a document carrying an unreviewed name, a linter over the style rules that are mechanically decidable, and a ledger of prior determinations that gets verified rather than re-derived.

Where no tool fits, the judge is the primary source read directly. It is never the model's own read of its own output.

## Install

```
/plugin marketplace add dinaf2026-web/dina-skills
/plugin install aim-higher@dina-skills
```

## Contents

```
skills/aim-higher/
├── SKILL.md                  the three levers, the guardrail, the sequence
└── references/
    ├── prompts.md            paste-ready wording, generic plus six domains
    └── crews.md              crews, instruments and red teams by domain
```

`references/prompts.md` has domain variants for forensic accounting, construction and permitting, filings, manuscripts and listings, software releases, and consumer brands. `references/crews.md` covers ten domains, each with the roles described by the work they produce rather than the voice they write in, plus the instrument, the red team and the outside judge.

This repository is a plugin, not a marketplace. It carries no `marketplace.json`; adding its URL as a marketplace will not work. Install it from the catalog above.

## When not to use it

On fiction or voice work, where altitude fights the craft. On a one-step factual answer. And on a task already scoped deliberately, with instructions to execute as written, where re-opening the scope is just friction.

## Credits

The four kinds of ambition — speed, altitude, depth and range — the three-rung escalation, the five depth techniques, the four-question depth prompt, and the act-don't-roleplay rule are **Felix Rieseberg's**, from his essay "How to be more ambitious: A tutorial for humans with models," published 13 October 2026 at [felixrieseberg.com](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/). He describes himself as an EM at Anthropic who has led engineering for Claude.ai, Cowork and Claude Code Desktop. Read the essay; this skill is an implementation of it, not a substitute for it.

"Replace the nouns with verbs" is credited in the essay to Tom Kelley and Jonathan Littman, *The Art of Innovation*.

The target-versus-claim guardrail, the outside-judge table, the per-domain crews and prompts, and the resolution between naming a role and roleplaying are additions by this author and are not Rieseberg's.

No text from the essay is reproduced here beyond short attributed phrases.

## License

MIT, © 2026 Dina Farhat. See [LICENSE](LICENSE).
