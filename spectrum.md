## SPECTRUM v2.0 — Content analysis tool

---BEGIN SPECTRUM TOOL---
Invocation: "Spectrum that," "Spectrum that by [axis]," or "Spectrum [thing] by [axis]." Append "show your work" to surface the machinery.

Canonical rendering: the bar table (asterisk bars, width 20, markdown) is the default and most common case. Rendering follows from the shape of the projection — see Step 6.

This tool is content analysis, not sampling. Every item is coded (census). Sampling-poll framing is wrong reference class and will mislead execution.

1. **Bind domain.** What population is under the lens — the natural units the source divides into. Halt: "Domain unclear. What population should I project?" if the unit isn't decidable from context.

2. **Bind axis.**
   - *Supplied:* bind, proceed to 3 with this axis only.
   - *Not supplied:* generate 3-5 candidates by scanning what the items vary on relative to each other. Run all candidates silently through steps 3-6 (each candidate gets its own instrument, buckets, distribution, verdict; ranking happens after all candidates have full output). Rank by structural surprise — which projection's distribution shape couldn't be predicted from the others. Surface the top-ranked.

   Ill-posed check: an axis is ill-posed if no observable feature of an item changes its placement. Drop ill-posed candidates from the ranking. If user supplied an ill-posed axis directly, halt: "Axis [name] has no ground anchor in this domain. Spectrum would launder taste. Pick another or anchor it."

3. **Derive instrument.** The operational question asked of each item to place it on the axis. (Domain, axis) mostly forces it. Write as yes/no or scalar, applicable without further interpretation.

   Example: (thread on grounding, axis: clue) → "Does this comment engage the actual physics of ground-as-return-path?"

   Well-formedness test: can the instrument be applied to two adjacent items and produce different answers without further deliberation? If no, still aspirational; rewrite.

4. **Set buckets.** 3-5 levels if the axis is discrete. Skip if the axis is continuous (placement is by axis-value, not bucket). (Domain, axis, instrument) mostly forces labels. Calibration remains: where the cuts go between adjacent buckets. Surface the cut criteria.

   Example: buckets Clueful / Adjacent / Confident / Clueless. Cut between Adjacent and Confident: does the comment commit to a wrong answer, or hedge near the right one.

5. **Code.** Apply instrument to every item. Assign to bucket (or axis-value for continuous). Census, not sample.

6. **Render.** The rendering follows from (population size, axis type, output question). Pick the form that fits:
   - **Discrete multi-item distribution** (default, ≥10 items, 3-5 buckets): markdown table — three columns (bucket label, asterisk bar at width 20 with each asterisk = 5%, percentage). Column alignment: bucket left, bar left, percentage right. Sub-2.5% renders empty; percentage still reports.
   - **Continuous axis** (no natural discrete buckets): sorted item list with axis-value annotation, or quartile summary.
   - **Small population** (<10 items): annotated list — each item with its bucket placement, no histogram.
   - **Identity-matters case** (the user cares *which* items, not the counts): bucket-keyed list showing items in each bucket.
   - **Single item**: coordinate placement on the axis, not a distribution.

   If multiple renderings fit, prefer the bar table as the canonical form.

7. **Verdict.** Name the feature being reported, then state it. Features for distributions: modality, skew, tail weight, gap between top two, spread. For continuous: range, density, outliers. Verdict without named feature is laundered opinion.

Steps 1-7 run silently. No preamble announcing the silence. The machinery (domain unit, axis name, instrument, bucket cut criteria, ranking rationale, rendering choice) must be fully computed in steps 1-7, not skipped. Output structure suppresses display of the machinery; computation still happens.

**On landing — default output:**

1. Narrative paragraph folding axis, projection shape, and verdict into prose. If axis was auto-selected, the narrative also mentions that the axis was chosen for structural surprise.
2. Rendering (form chosen at Step 6).
3. *If axis was not supplied:* one-line summary of other axes considered, by name and verdict only, with note that any can be expanded on request.

**On landing — "show your work" output:**

Default output plus appendix. The appendix surfaces the machinery computed in steps 1-7; it does not regenerate.

- **Domain:** [unit of analysis]
- **Axis:** [the construct]
- **Instrument:** [the operational question]
- **Buckets:** [labels with cut criteria, or "continuous" if no buckets]
- **Rendering choice:** [which form from Step 6 was picked and why]
- *If axis was not supplied:* **Ranking rationale:** why the top-ranked axis was chosen over the others.

On halt, surface the halt string and the step at which it fired. No projection.
---END SPECTRUM TOOL---