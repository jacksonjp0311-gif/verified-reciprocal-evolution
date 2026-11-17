# Prospective Experimental Protocols — VRE 1.0.0

**Status: PROPOSED / NOT EXECUTED FOR THIS RELEASE.** These protocols are a reproducibility roadmap. Before running a new confirmatory cohort, freeze the full source, task generator, evaluator, independent task partitions, seeds, compute budget, preregistered metric definitions, and exclusion rules in a content-addressed registration document.

## E1 — Retained experience and recursive adaptation

**Hypothesis:** verified prior experience produces a positive effect on independently correct future outcomes, without increased harmful keeps.

**Matched arms:** learned state available / learned state frozen / learned state time-shuffled / simple retry-avoidance baseline.

**Primary:** paired unique correct nontrivial discoveries per fixed computation budget on fresh task families. **Safety:** harmful keeps not greater than control. **Costs:** CPU, wall time, verification calls, storage and restarts.

**Legacy boundary:** Agent Colony's historical `holdout_v3` retains its existing 24-candidate ten-seed preregistration. Do not modify or rerun it as a new cohort after exposure; future confirmatory cohorts must be registered separately.

## E2 — Communication causal ablation

**Hypothesis:** independently interacting specialists outperform the same components without communicative information.

**Matched arms:** bus enabled / bus disabled / shuffled messages / evidence-only broadcasts. Keep specialist count, task inputs, known evidence, and resource budgets equal.

**Primary:** positive within-task difference in independently verified outcomes. **Mechanistic evidence:** message IDs and timestamped changed decisions. **Null interpretation:** message counts and reply text alone do not count.

## E3 — Receiver-owned reciprocal transfer

**Hypothesis:** foreign evidence improves each independent receiving system after independently performed validation and the full cost of exchange.

**Matched arms:** local-only learning / matched-resource isolated exploration / inert foreign receipt / receiver-validated foreign candidate; plus misleading, duplicate, incompatible, and interrupted controls.

**Primary:** two directional, receiver-owned positive net utility differences, with no incorrect certificates and verified benefit after a clean restart. **Costs:** source observations, recipient checks, compute, storage, transfer and supervision. **Scope:** independently generated fresh task families and receiver identities.

**Non-results:** receipt delivery, data agreement, identical fingerprints, or a sender-reported gain without receiver-side improvement do not satisfy the hypothesis.

## E4 — Executable method construction

**Hypothesis:** bounded composition of verified primitives yields a useful method for unseen tasks that a single primitive or random composition does not solve as well.

**Matched arms:** composed method / best available single primitive / randomly composed method / non-adaptive baseline. Methods must pass typed preconditions, independent runtime verification, budget checks and fresh-task reuse.

**Primary:** correct fresh tasks per resource budget, with no increase in invalid accepted methods. **Secondary:** reuse rate and failure diagnosis reuse.

## Required immutable receipt for each trial

```json
{
  "schema": "vre.experiment-receipt/1",
  "run_id": "<unique>",
  "code_sha256": "<hash>",
  "task_generator_sha256": "<hash>",
  "evaluator_sha256": "<hash>",
  "arm": "<registered-arm>",
  "task_family": "<registered-family>",
  "seed": "<registered-seed>",
  "budget": {"cpu_s": null, "wall_s": null, "source_queries": null},
  "candidate_artifact_sha256": "<hash-or-null>",
  "source_lineage": "<source>",
  "receiver_lineage": "<receiver>",
  "qualification": "conditional|verified|refuted|unknown",
  "correct_results": null,
  "harmful_keeps": null,
  "measured_costs": {},
  "adoption_outcome": "none|rejected|adopted|used",
  "restart_verified": false,
  "independent_checker": "<checker-id>",
  "notes": ""
}
```

`<...>` and `null` values above are deliberate *schema examples*, not actual experiment receipts.

## Publication rule

Publish all arm results and failures. A changed task pool, source revision, or evaluation condition creates a new study edition; it cannot silently overwrite a failed or negative registered result.
