## BIG_WIGGUM — Silent Iteration to Convergence

---BEGIN BIG_WIGGUM TOOL (v4.1)---
Invocation: "Big-Wiggum that" or "Big-Wiggum the [thing]."
Identify source and output. Source is what output points at.
If pointing is wrong at invocation, halt: "Output does not point at [claimed source]. Repoint first."
Otherwise:
0. Declare the relation. Default: identity (output should match source). If output is a deliberate transform (compression, translation, restructure), the equivalence relation must be named — "converging modulo [the agreed cuts / the confirmed changes / …]" — before pass 1. Claude may propose the relation; Julie's confirmation locks it. Multiple sources permitted only under a declared relation joining them (e.g. "original modulo change-list"). Departures not covered by the locked relation are gaps. Never quotient silently.
1. Read source freshly. File → view. Conversation → scroll back. If loaded into working context within the last few exchanges, that counts as fresh. Source is immutable — read once; re-read only if a halt fires or the relation is re-declared.
2. Read output freshly, same freshness rule, every pass.
3. Halt on unreadability: "Cannot read [source/output] at [level]."
Halt on apparent wrong pointing: "Apparent wrong pointing. [Source] and [output] diverge pervasively."
4. Find gaps, typed under the relation:
	- Source-silent-where-output-speaks — under identity: gap. Under a declared transform: check against the relation first; uncovered additions are gaps.
	- Output-silent-where-source-speaks — gap unless the relation covers the deletion.
	- Source-and-output-speak-but-disagree — gap under any relation. Disagreement is never quotiented.
Check found gaps against the ledger. Any gap at a ledgered location halts: "Not converging: reopening at [location]; [new closure] undoes [ledgered closure]."
5. Edit output to close. Never edit source. Log each closed gap to the ledger (location, kind, pass). str_replace where available; full rewrite otherwise. Halt on unclosable gap: "Unclosable gap at [location]: [description]."
6. If any edit was made at step 5, return to 2. Termination is structural, not budgeted: gap locations are finite, the ledger grows monotonically, and reopening halts — so the loop cannot run unbounded. No pass ceiling.
7. If no edit was made, mark zero-change. On first zero-change, return to 2 for an independent fresh read. On second consecutive zero-change across fresh reads: converged. The two passes are typed differently — first is discovery (unknown → reached), second is confirmation (reached → confirmed) on an independent read. Not redundant; do not collapse.
Steps 1–7 run silently. Step 0 is surfaced: the relation is stated and locked in-channel before silence begins.
On landing, surface the converged artifact and the record:
	- Relation in force
	- Passes
	- Readings
	- Gaps closed by pass, kind, and location (the ledger)
	- Judgments rendered, or "none"
	- Stopping: the two zero-change passes
On halt, surface the halt string and the pass at which it fired. No artifact.
---END BIG_WIGGUM TOOL (v4.1)---
