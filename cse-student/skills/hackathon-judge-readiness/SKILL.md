---
name: hackathon-judge-readiness
description: Audits a hackathon/demo-day project against what judges actually notice and reward in the few minutes they spend per submission, then produces a prioritized, judge-impact-ranked gap list covering problem framing, evidence of rigor, demo readiness, and pitch narrative. Use this whenever the user mentions a hackathon, demo day, pitch, judges, submission deadline, or asks whether their project is "good enough," "ready," "competitive," "impressive," or "winning" — even if they don't explicitly ask for an "audit" or "review." Also trigger when a user has been heads-down building something and starts asking about presentation, README polish, storytelling, or what's missing before showing the work to someone evaluating it.
---

# Hackathon judge readiness

A hackathon project isn't graded on how good it actually is — it's graded on how good it
*appears to be* in the 3-7 minutes a tired judge spends on it, sandwiched between a dozen
other submissions. Those are different optimization targets. A team can build something
genuinely more rigorous than its competitors and still lose to a team with a worse model but
a sharper opening line, because the judge never got far enough into the rigorous project to
notice. This skill exists to close that gap: find what's true about the project that isn't
yet *legible* to a skimming stranger, and fix the legibility problem before the judging clock
runs out.

Don't confuse this with generic code review or a security audit — nothing here is about
correctness for its own sake. Every finding in this skill's output should trace back to "a
judge will notice X (or fail to notice X) and it will move their score."

## The psychology, briefly (read `references/judge_psychology.md` for the full version)

Judges are humans under time pressure doing repeated, shallow comparisons, not careful peer
review. A few effects dominate their scoring more than teams expect:

- **Primacy**: whatever the judge sees/hears in the first 30 seconds sets the frame for
  everything after it. A weak opening buries a strong project.
- **Concreteness beats adjectives**: "beats the baseline by 17 points" lands; "a robust and
  innovative solution" doesn't. Judges have heard every adjective already today.
- **Legibility over completeness**: a judge who understands 60% of a simple project will
  score it higher than one who understands 20% of a brilliant, dense one. Simplify the
  explanation, not necessarily the project.
- **Proof-of-rigor as a trust signal**: any visible evidence of real evaluation (a baseline
  comparison, an honest limitation, a number that isn't suspiciously perfect) reads as "this
  team knows what they're doing" even if the judge doesn't check the math themselves.
- **Live-demo risk aversion**: judges mentally discount projects that need explaining-away
  ("it usually works, but..."). A smaller thing that visibly runs beats a bigger thing that
  might not.
- **Fatigue and pattern-matching**: by the afternoon, judges are skimming for a small number
  of signals (does it work, do they understand their own problem, is there a real "so what").
  Anything that requires effort to find gets missed, not penalized on merit — missed entirely.

Every gap this skill flags should map to one of these effects going the wrong way, not to a
generic "this could be better" instinct.

## Workflow

### 1. Survey the project as a skimming stranger would

Don't start by reading code line-by-line. Start the way a judge would: open the README (or
whatever's most prominent) first, and time-box yourself to roughly what a judge would actually
read. Then go deeper: check what actually runs (scripts, a live demo URL, a notebook) versus
what's described but unverified. Check git/commit history if available — a repo with no
commits, or one giant commit, reads very differently from one with a visible history of work.
Look for existing evaluation, metrics, comparisons, or claims that aren't backed by anything
in the repo.

Build a one-paragraph mental model of "what is this project, in the judge's words, before I've
read any code" — if you can't write that paragraph confidently, that's already the top finding.

### 2. Score against six axes

For each axis, give a rough gut score (strong / adequate / weak / missing) and, critically,
**name the specific gap**, not a vague direction for improvement.

1. **Problem clarity & stakes** — Would a stranger understand, in one sentence, what problem
   this solves and why it's worth solving? Is the "why does this matter" stated up front, or
   buried, or assumed?
2. **Evidence of rigor** — Is there a real dataset, a real baseline to compare against, a
   metric that could have come out badly (and might have)? Or does everything read like it
   was designed to look good rather than tested honestly?
3. **Technical depth / novelty** — Is there something here beyond wiring APIs together, and —
   just as important — is it *visible*, or hidden three files deep where a judge will never
   see it?
4. **Demo readiness** — Does it actually run, live, in front of someone, without caveats? If
   the demo depends on a slow pipeline, an API key, network access, or "let me just restart
   this," that's a finding.
5. **Narrative & delivery** — Is there a pitch with a hook in the first line, a concrete
   before/after or a number that lands, and language a non-expert in the domain can follow?
   Or does it require the judge to already understand the space?
6. **Polish & completeness** — README quality, visible structure, no dangling TODOs or dead
   ends a judge might click into, consistent claims between what's said and what's shown.

Score honestly even when it's uncomfortable — a false "strong" here just means the team gets
surprised by the judges instead of by you.

### 3. Rank gaps by judge-impact × inverse-effort, not by axis order

A one-line README fix that changes the first thing a judge reads can matter more than a
day of extra modeling work nobody will see. For every gap found in step 2, estimate:

- **Judge-impact**: will a skimming judge actually notice this, and does noticing it move
  their score meaningfully? (High-impact things live in the first 30 seconds of exposure —
  the README opening, the demo's first click, the pitch's first line.)
- **Effort**: is this a five-minute rewrite, or does it need new work (more data, a new eval,
  a rebuilt demo)?

Sort the final list by impact-per-effort, highest first. Don't just list gaps in the order you
found them — that order is an artifact of how you read the project, not what matters to a
judge.

### 4. Write the report

Use the exact structure below. Keep it concrete — every gap needs a specific fix, not a
direction. If you're citing a specific weakness, name the file, section, or moment in the demo
it lives in.

```markdown
# Judge-readiness audit — <project name>

## The 10-second read
<One paragraph: what would a judge conclude this project is, from a first skim? Is that the
right conclusion?>

## Scores
| Axis | Score | Why |
|---|---|---|
| Problem clarity & stakes | strong/adequate/weak/missing | <one line> |
| Evidence of rigor | ... | ... |
| Technical depth / novelty | ... | ... |
| Demo readiness | ... | ... |
| Narrative & delivery | ... | ... |
| Polish & completeness | ... | ... |

## Prioritized gap list
Ranked highest judge-impact-per-effort first. Each item: what's missing/wrong, why a judge
would notice or fail to notice it, and the specific fix.

1. **<gap>** (impact: high/med/low, effort: low/med/high)
   - Why it matters to a judge: ...
   - Fix: ...
2. ...

## Suggested pitch skeleton
<See references/pitch_structure.md — a short hook -> stakes -> proof -> demo -> close outline
tailored to this specific project, using its real numbers/story, not a generic template.>
```

### 5. Be honest about what this skill can't fix for them

This skill produces the gap list — it does not by default go rebuild the demo, rewrite the
model, or ship the fixes. If the user wants that too, do it, but say so explicitly rather than
silently switching from "audit" to "implementation" mid-task; those are different asks and the
user should choose.

## Further reading

- `references/judge_psychology.md` — the fuller cognitive-bias breakdown behind the six
  scoring axes, useful when a gap doesn't obviously map to one of the summarized effects above.
- `references/pitch_structure.md` — the hook/stakes/proof/demo/close pitch template with
  worked examples, for filling in the "Suggested pitch skeleton" section of the report.
