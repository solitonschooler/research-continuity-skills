# Worked summary — fictional quadratic notes

**Scope examined:** three short synthetic notes in full. This is a public teaching case, not a blind benchmark.

**Documented historical progression:** S1 asserted that *every* step in the negative-gradient direction for `f(x)=x^2` decreases the loss, without limiting step size. S2 constructed `x=1`, `h=-3`: although `h` opposes the gradient `f'(1)=2`, loss rises from `1` to `4`, refuting that universal assertion. S3 explicitly narrows the step to `x_new=(1-2*eta)*x`, and asserts strict decrease for `x != 0`, `0<eta<1`.

**Mathematical check:** `f(x_new)=(1-2*eta)^2*x^2 < x^2` for `x != 0` precisely when `|1-2*eta|<1`, equivalent to `0<eta<1`. This calculation supports the conditional quadratic claim, not all gradient algorithms.

**Value added:** historical error retained, counterexample linked, later author repair attributed correctly, and nonquadratic transfer recorded only as an open research question. No numerical experiment on an actual optimizer was executed.

**Handoff:** `worked_research_state.json` encodes the same state under the shared research JSON Schema. All evidence anchors refer to fictional files in this directory.
