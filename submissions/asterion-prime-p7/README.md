# Asterion Prime P7

[Replay console](https://asterion-p7-console.vercel.app) · [System source](https://github.com/uukuguy/asterion) · [Reproduction guide](https://github.com/uukuguy/asterion/blob/main/docs/guides/prime-p7-community-reproduction.md) · [Result record](https://github.com/uukuguy/asterion/blob/main/docs/results/arc-agi-3/README.md) · [Competition scorecard](https://arcprize.org/scorecards/60c10b53-9b8d-4af9-aae7-85f81543198a)

## Submission details

| Field | Value |
|---|---|
| Name | Asterion Prime P7 |
| Author | [Jiangwen Su](https://github.com/uukuguy) · [Hugging Face](https://huggingface.co/uukuguy) |
| Benchmark / set | ARC-AGI-3 · public |
| Competition score | **100.00** — normally closed official scorecard |
| Completion | **25/25 games · 183/183 levels** |
| Online actions | **6,781** |
| Model / seed | `gpt-6.1-sol` / `0` |
| Version / date | `P7-2026-10-07` / `2026-10-07` (UTC+8) |
| Code | [uukuguy/asterion](https://github.com/uukuguy/asterion) |
| Scorecard | [60c10b53-9b8d-4af9-aae7-85f81543198a](https://arcprize.org/scorecards/60c10b53-9b8d-4af9-aae7-85f81543198a) |
| Cost | Not reported; see accounting scope below |

The YAML records all required fields, the author's public profiles, a software
citation, and the exact research model. The ARC-AGI-3 score is supplied through
the scorecard URL. The method and result links above point to the public
producing system and checked evidence.

## Method

Prime P7 is Asterion's ARC-AGI-3 application. Its general method connects
language hypotheses, persistent program models, real counterexamples, and
cross-attempt experience in a versioned research loop. The public repository
includes the producing workspace, tool bridge, controlled action broker, and
evidence validation code.

P7 turns observations into a revisable WorldMap of candidate rules, action
meanings, goals, competing hypotheses, and unresolved questions. The LLM uses
this map to choose a useful computation or discriminating experiment; it can
act with a partial model before every rule is settled.

In persistent IPython, the LLM writes state projections, transition and goal
candidates, and search programs—for example, `project(frame)`,
`step(state, action)`, `goal(state)`, and `search(state)`. These are programs
created during research, not a supplied table of game answers. It compares
alternative explanations and routes using its own models.

The LLM tests predictions against recorded observations and submits short
plans with explicit expected outcomes. Host-side checks return matches or
concrete expected/actual counterexamples. When reality contradicts a
prediction, the LLM revises its WorldMap or program and recomputes the next
plan. The host checks evidence; the LLM interprets and revises the hypotheses.

Later attempts selectively reuse earlier WorldMaps, corrections, unknowns,
counterexamples, artifacts, and program cells—including material from failed
attempts. The LLM revises and reruns useful programs against current evidence.
This research reuse is distinct from restoring an independently checked
successful action prefix in a new local game.

At save time, candidate routes are independently replayed against the local
SDK and checked for source identity and achieved progress. Certificates bind
these checks to the saved actions and game assets; official submission reads
this authority before dispatching real online actions.

## Evaluation and accounting scope

The linked record accumulated iterative research on public games, with retained
same-game experience, validated prefix reuse, generic infrastructure repairs
between attempts, and operator-controlled retries and selected cognition
resets. P7's LLM research produced the WorldMaps, programs, and discovered
routes. The Competition submission reexecutes the certified routes online
without new model inference. The scorecard has normally closed with 25/25 games and 183/183 levels
completed in 6781 actions; its final server score and every selected route
were checked against the closed receipt. The YAML supplies the
scorecard link without a numeric score or an estimated cost.

P7 records input/output token usage, but the inspected accounting surface does
not establish cumulative USD spend or the cache/pricing detail needed to
calculate it. The last online route execution made no new model calls; that
does not measure the preceding research cost. The optional YAML `cost` field
is therefore omitted. No accompanying paper or project social-post URL is supplied in this entry;
the repository documentation and software citation describe the work.

## Reproduction

Reproduction of the system requires the external ARC SDK/game assets, a
configured Pi/backend profile for live research, and Competition credentials
for online submission. The source checkout alone does not include the operator's
private run history or certified saved-route roster. Operators can run the
public system and accumulate their own experience and certified routes using
the reproduction guide.
