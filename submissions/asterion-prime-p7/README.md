# Asterion Prime P7

[System source](https://github.com/uukuguy/asterion) · [Reproduction guide](https://github.com/uukuguy/asterion/blob/main/docs/guides/prime-p7-community-reproduction.md) · [Result record](https://github.com/uukuguy/asterion/blob/main/docs/results/arc-agi-3/README.md) · [Competition scorecard](https://arcprize.org/scorecards/60c10b53-9b8d-4af9-aae7-85f81543198a)

Prime P7 is Asterion's ARC-AGI-3 application. An LLM maintains a semantic
WorldMap and revisable mechanics hypotheses, writes executable models and
searches short plans in persistent IPython, and chooses active experiments
whose predictions are compared with real feedback. The workspace records
corrections and reusable experience for subsequent attempts. The public
repository includes the reasoning workspace, tool bridge, controlled action
broker, and evidence validation code.

At save time, candidate routes are independently replayed against the local
SDK and checked for source identity and achieved progress. Certificates bind
these checks to the saved actions and game assets; official submission reads
this authority before dispatching real online actions.

The linked record accumulated iterative research on public games, with retained
same-game experience, validated prefix reuse, generic infrastructure repairs
between attempts, and operator-controlled retries and selected cognition
resets. P7's LLM research produced the WorldMaps, programs, and discovered
routes. The Competition submission reexecutes the certified routes online
without new model inference. Its scorecard is currently in progress; the final
server score is confirmed by a checked closed receipt. The YAML supplies the
scorecard link without a numeric score or an estimated cost.

Reproduction of the system requires the external ARC SDK/game assets, a
configured Pi/backend profile for live research, and Competition credentials
for online submission. The source checkout alone does not include the operator's
private run history or certified saved-route roster. Operators can run the
public system and accumulate their own experience and certified routes using
the reproduction guide.
