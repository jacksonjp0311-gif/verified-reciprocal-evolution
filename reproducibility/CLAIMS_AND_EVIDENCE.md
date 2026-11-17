# Claims and Evidence Register — VRE 1.0.0

**Scope:** this register separates demonstrated scoped mechanisms from unresolved hypotheses. It is not an independent re-execution of the source repositories. Repositories remain mutable; source commits below are the citation anchors.

| ID | Claim and evidence | Status | Primary artifact | Limitation |
|:--|:--|:--|:--|:--|
| C01 | Agent Colony has persistent roles, a communication bus, Oracle, Hive, self-change trials, and twin-control state | IMPLEMENTED | [Agent Colony source](https://github.com/jacksonjp0311-gif/agent-colony/tree/4304c25d78dab105f78cfbb9c97bf665e793bbf5) | Implementation ≠ demonstrated generalization |
| C02 | Treatment snapshot reports 1,325 cycles, 18 roles, 591 Oracle passes, 14 self-heal adopts | OBSERVED SNAPSHOT | [`CI_STATUS.json`](https://github.com/jacksonjp0311-gif/agent-colony/blob/4304c25d78dab105f78cfbb9c97bf665e793bbf5/society/CI_STATUS.json) | Cumulative; not equal-exposure causal comparison |
| C03 | Holdout v2: learning-on verified mean 4.0 versus 1.6 learning-off; harmful keeps 0.4 versus 0.2 | MIXED / CRITERION FAILED | [Holdout report](https://github.com/jacksonjp0311-gif/agent-colony/blob/4304c25d78dab105f78cfbb9c97bf665e793bbf5/evidence/2026-10-16-holdout-v2/README.md) | Five paired seeds, safety-constrained success rejected |
| C04 | Agent Colony cross-version holdout v2 showed no new capability | NO MEASURABLE GAIN | [Same holdout report](https://github.com/jacksonjp0311-gif/agent-colony/blob/4304c25d78dab105f78cfbb9c97bf665e793bbf5/evidence/2026-10-16-holdout-v2/README.md) | Restricted candidate family and budget |
| C05 | Agent Colony v3: 24 candidates, 10 paired seeds, preregistered | PROTOCOL READY / UNEXPOSED IN INSPECTED RECORD | [Preregistration](https://github.com/jacksonjp0311-gif/agent-colony/blob/4304c25d78dab105f78cfbb9c97bf665e793bbf5/evaluation/PREREGISTRATION.md) | Not a result; don't infer future success |
| C06 | 30 method cards formed, zero tested in learning report | NO METHOD-TRANSFER DEMONSTRATION | [`LEARNING.md`](https://github.com/jacksonjp0311-gif/agent-colony/blob/4304c25d78dab105f78cfbb9c97bf665e793bbf5/society/LEARNING.md) | No evidence of method reuse on new task families |
| C07 | One Mind is highly similar to the Agent Colony source substrate | REPO COMPARISON | [One Mind source](https://github.com/jacksonjp0311-gif/one-mind/tree/4cb56b27eacd7640e3c931f5625aadf9db4fd1f6) | 180/184 corresponding `.py` blob hashes in `colony/` and `hive/` identical at compared snapshots; not independent software evidence |
| C08 | SYMBIOTE fresh-input structural learning: 128 correct case/input predictions after restart | DEMONSTRATED BOUNDED LEARNING | [Registered result](https://github.com/jacksonjp0311-gif/SYMBIOTE/blob/482bf104c89721965ec006cc9f5b9f37237278bd/docs/ENGINE_EVOLUTION_002.md) | Isolated structural learner tied; no superior sample efficiency |
| C09 | SYMBIOTE rank policy cuts scoped GF(2) work from 28,439 to 713 units per case | DEMONSTRATED COMPONENT EFFICIENCY | [Registered result](https://github.com/jacksonjp0311-gif/SYMBIOTE/blob/482bf104c89721965ec006cc9f5b9f37237278bd/docs/ENGINE_EVOLUTION_002.md) | Same source query count; not full-engine speed advantage |
| C10 | Receiver-owned adoption and actual use demonstrated in one scoped SYMBIOTE scenario | BOUNDED MECHANISM | [Registered result](https://github.com/jacksonjp0311-gif/SYMBIOTE/blob/482bf104c89721965ec006cc9f5b9f37237278bd/docs/ENGINE_EVOLUTION_002.md) | No demonstrated economic bilateral benefit |
| H01 | Swarm communication improves unique verified results on new tasks | HYPOTHESIS | [Experiment E2](PROTOCOL.md) | Not causally established |
| H02 | Learning-on recursive policy improves fresh tasks with no increased harmful keeps | HYPOTHESIS | [Experiment E1](PROTOCOL.md) | Not yet shown under broad independent families |
| H03 | Receiver-verified foreign evidence yields positive bilateral net benefit | HYPOTHESIS | [Experiment E3](PROTOCOL.md) | Not yet established |
| H04 | The colony can autonomously compose and transfer executable methods | HYPOTHESIS | [Experiment E4](PROTOCOL.md) | Current method-card trials remain zero |

## Replication notes

- Source revisions are *evidence snapshots*, not certifications of all live behavior.
- For experimental reproduction, use each source repository's original frozen evaluator and registered task-family rules.
- If historical holdout labels were exposed, treat every rerun as a re-exposure and do not count it as an independent confirmatory success.
- The manuscript's mathematical notation is a proposed operational model. It is not cited as a newly proved theorem.
- This release has not been independently peer reviewed, nor does it claim a universal improvement over existing non-LLM algorithms.
