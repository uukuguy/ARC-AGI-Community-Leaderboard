# Asterion Prime P7

[System source](https://github.com/uukuguy/asterion) · [P7 operating guide](https://github.com/uukuguy/asterion/blob/main/docs/guides/prime-p7-games-and-official-results.md) · [Competition scorecard](https://arcprize.org/scorecards/60c10b53-9b8d-4af9-aae7-85f81543198a)

Prime P7 is Asterion's ARC-AGI-3 application. An LLM maintains a semantic
WorldMap and revisable mechanics hypotheses, writes executable models and
searches short plans in persistent IPython, then compares predictions with
observed feedback. The workspace records corrections and reusable experience
for subsequent attempts. The public repository includes the reasoning
workspace, tool bridge, controlled action broker, and evidence validation code.

The evaluation linked here used known public games and multiple finite research
attempts. Later attempts could restore validated action prefixes and reuse
earlier same-game observations, hypotheses, and experience. Candidate routes
were independently replayed against the local SDK and checked for source
identity and achieved progress before becoming saved submission inputs.

The final Competition submission executes these previously discovered native
action routes online. That saved-route submission path performs no new model
inference. Its scorecard validates execution through the Competition service;
the full research process precedes that replay. This evaluation does not establish
cold-start solving, held-out generalization, or ARC Prize Verified status.
The YAML supplies the scorecard link without a numeric score or an estimated
cost.

Reproduction of the system requires the external ARC SDK/game assets, a
configured Pi/backend profile for live research, and Competition credentials
for online submission. The source checkout alone does not include the operator's
private run history or certified saved-route roster. See the operating guide for
the distinction between fresh research, retained-evidence continuation, and
saved-route submission.
