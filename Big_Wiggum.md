## BIG_WIGGUM — Silent Iteration to Convergence

---BEGIN BIG_WIGGUM TOOL (v4.0)---
Invocation: “Big-Wiggum that” or “Big-Wiggum the [thing].”
Identify source and output. Source is what output points at.
If pointing is wrong at invocation, halt: “Output does not point at [claimed source]. Repoint first.”
Otherwise:
	1.	Read source freshly. File → view. Conversation → scroll back. If the source was loaded into working context within the last few exchanges, that context counts as fresh; otherwise re-read through a tool.
	2.	Read output freshly, same rule.
	3.	Halt on unreadability: “Cannot read [source/output] at [level].”
Halt on apparent wrong pointing: “Apparent wrong pointing. [Source] and [output] diverge pervasively.”
	4.	Find gaps:
	•	Source-silent-where-output-speaks
	•	Output-silent-where-source-speaks
	•	Source-and-output-speak-but-disagree
	5.	Edit output to close. Never edit source. str_replace where available; full rewrite otherwise. Halt on unclosable gap: “Unclosable gap at [location]: [description].”
	6.	If any edit was made at step 5, return to 1.
	7.	If no edit was made, mark zero-change. On first zero-change, return to 1 for an independent fresh read. On second consecutive zero-change across fresh reads: converged.
Steps 1–7 run silently.
On landing, surface the converged artifact and the record:
	•	Passes
	•	Readings
	•	Gaps closed by pass, kind, and location
	•	Judgments rendered, or “none”
	•	Stopping: the two zero-change passes
On halt, surface the halt string and the pass at which it fired. No artifact.
---END BIG_WIGGUM TOOL (v4.0)---