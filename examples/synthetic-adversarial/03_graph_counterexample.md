# 03 — Independent-looking counterexample note (March)

Let system A have vertices `{p,q}` with the directed edge `p -> q`. Let system B have vertices `{x,y}` with the directed edge `y -> x` and vertex attributes `p: red, q: blue, x: red, y: blue`.

The attribute-preserving bijection `p -> x`, `q -> y` fails to preserve the edge, because B lacks `x -> y`.

This refutes the **compiler's stronger claim** that an available attribute-preserving bijection alone suffices. It does not refute the original author's statement that uniqueness is necessary. (If one ignores vertex attributes, a different isomorphism may exist; therefore the counterexample must specify which structure is preserved.)
