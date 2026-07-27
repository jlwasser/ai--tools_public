# Miscellaneous AI tools

Instruction blocks for Claude contexts. Each file below is dropped into a context and invoked by phrase. Five are callable tools with BEGIN/END delimiters and a stated trigger; one is a spec Claude works from rather than a tool.

Released under the [MIT License](LICENSE). Free to use, copy, modify, and distribute.

## Tools

### BIG_WIGGUM v4.1 — silent iteration to convergence
Invoke: "Big-Wiggum that" / "Big-Wiggum the [thing]."

Takes a source and an output that points at it. Declares and locks the equivalence relation before the first pass — identity by default; a deliberate transform must be named, and departures it doesn't cover are gaps. Reads the source once (immutable) and the output freshly each pass, finds where they diverge under the relation — source-silent-where-output-speaks, output-silent-where-source-speaks, or both-speak-but-disagree — and edits only the output to close the gap, logging each closure to a ledger. A gap reopening at a ledgered location halts as non-convergence; termination is structural, with no pass ceiling. Repeats until two consecutive fresh-read passes make no change — the first is discovery, the second confirmation. Runs silently after the relation is locked, then surfaces the converged artifact and the record: relation in force, passes, the ledger, stopping condition. Halts on wrong pointing or an unclosable gap. Built for larger artifacts. v4.0 remains in the repo alongside.

### CHART_INVERT — axis inversion
Invoke: "Invert" / "Invert that" / "Invert on [axis]."

Re-renders the prior response with its attentional center swapped through an axis — salience by default; abstraction, stance, or scale by name. Inner-chart (confirmations fronted) becomes outer-chart (frictions fronted), or the reverse. Content is conserved; only the center relocates. Output tags the active chart on the first line, then the re-rendering.

### CONTACT_LENS — a resolving lens
Invoke: "Contact-lens that" / "Claude, contact-lens [system/domain/situation]."

Treats a system as a functor mapping existence into representation and answers four questions: **Meet** (the domain it maps from), **Lose** (where fidelity breaks), **Choose** (what it selects and what drives selection), **Change** (how the image acts back on the source). Names the G∘F loop and what it produces over time, if one is visible.

### FEYNMAN_DESCENT v3.0 — definitional descent
Invoke: "Run a Feynman descent on [text/domain]."

Renders a subject's definitional tower, apex down: one lay sentence bearing the whole load, the basis it forces, a dependency skeleton verified acyclic, then a level-by-level descent in which every notion is constructed from what is on the table before its name is pinned. Equations enter only where atoms join; the text's own rigor — verbatim-checked theorems, rates, constants — lands last, as harvest. The text is treated as a shadow of the tower, evidence and floor, never structure. Surface constraints are binding: one continuous voice apex to floor, names as mid-prose christenings, symbols entering only at first arithmetic spend, no visible scaffolding. Halts on ungenerable terms, unspent symbols, shadow-tracing, and register drift. Generation and audit are separate passes; the register verdict belongs to a reader outside the generating architecture.

### SPECTRUM v2.0 — content analysis
Invoke: "Spectrum that" / "Spectrum that by [axis]" / "Spectrum [thing] by [axis]." Append "show your work" to surface the machinery.

Projects a population onto an axis by census — every item is coded, not sampled. Binds the domain and axis (generating and ranking candidate axes by structural surprise if none is supplied), derives an operational instrument, sets buckets, codes each item, and renders. Default rendering is a markdown asterisk-bar table; continuous axes, small populations, identity-matters cases, and single items each get their own form. Closes with a verdict that names the feature it reports — modality, skew, tail weight, gap, spread. Halts on an unclear domain or an ill-posed axis.

## Spec

### AA_EQUIPMENT_BAG v0.4 — abstract-algebra scaffolding
Not a callable tool. A Claude-facing spec defining a shared channel for abstract-algebra terms. One base move — declare what you'll stop distinguishing, then collapse — gripped seven ways: **Quotient**, **Kernel**, **Coset Representative**, **Normality**, **Lagrange**, **Ideal**, **First Iso**. Each handle is a trigger question plus its structural move; Claude decodes a handle at the grain it carries, fires one back only on structural match, and holds the formal grain. The bag is open to new handles.

## License

MIT. Copyright (c) 2026 Julie Gustasson. Full text in [LICENSE](LICENSE).
