# Skill Field Note 40 — v7.8 Strong-Attractor Emergence Stress Test

Status: ACTUALLY EXECUTED LOCAL MATH/COMPUTER EXPERIMENT; candidate future GitHub Skill methodology, NOT a runnable `SKILL.md`. Case: V78-EMERGENCE-NO-GO. Related GL78-01..03, GL77-01..03, RA-H04; antecedent primary documents SRC-0104/0107 only previously bounded-audited, NO fresh original deep read in this iteration.

## Trigger

The user asked whether LuoShu is guaranteed or naturally likely in an exceptionally strong attractor. v7.7 designed the answer into a polynomial with 8 correct zeros, which proves existence, but cannot justify **emergence**. v7.8 deliberately withheld one or both diagonal rules in competing models and treated the LuoShu event as a held-out outcome.

## Actual Procedure (not proposed work)

1. Before run, froze `EXPERIMENT_PROTOCOL_v7.8.md`, SHA `1324a961e4674feb622a48bc51d1b6ea1a27a3e541f07ffa2c07472c6dbcc8a3`.
2. Enumerated all 9!=362,880 digit permutations; computed balance of 3 rows/3 columns, one held-out diagonal, both diagonals; made all policies explicit. Target 15 came from mass 45 divided by 3, not from a pretrained nine-grid template. **However the prior knowledge 'digits 1..9 on 3x3' and line-balance energies are already chosen by researcher.**
3. Enumerated 72 RC minima, forming exactly nine 8-element D4 orbits, one LuoShu orbit. Each center digit 1..9 occurs in one orbit. This ninefold orbit count is NOT a nine-step dynamics/cycle.
4. Evaluated exact finite Gibbs partition functions under temperature/gain parameter beta. Infinite beta RC selects uniformly from 72 minima so probability magic = 8/72 = 1/9, regardless how strongly equilibrium is concentrated; RC+one diagonal = 8/24 =1/3; FULL=8/8=1 by target-defining constraints. These are **conditional finite-state equilibrium results**, not universal claims about nonlinear attractors or physical self-organization.
5. Ran 128 independent fixed-start pair-swap steepest-descent trials per RC/FULL, 256 outcome rows; RC 75 zero-energy, only 5 LuoShu; FULL 102 zero-energy all LuoShu, but FULL explicitly contains both defining diagonal requirements. Greedy performance differs from Gibbs equilibrium and has local traps; no paired cost-normalized claim of superiority is valid.
6. Scoped 32/32 executable checks passed; inherited v7.7 31/31 and v7.6 17/17 targeted checks were rerun. v7.6 verifier initially failed because its default path was absent from the extracted archive; supplying the actual archived `EXPERIMENTS_V76` directory recovered 17/17. This is an input-path/configuration error, NOT a mathematics regression. Preserve the true route for future reproducibility. Full historical suite and independent source-hidden LLM evaluation NOT_RUN.

## Observed failure / counterexamples

- **Attraction vs specificity**: increasing gain/β concentrates mass on energy-minimum *set*; if that set contains 64 non-LuoShu options, no amount of β alone selects the LuoShu orbit. Finite-state conditional proof.
- **Nine vs nine**: nine D4 orbits occur in a static combinatorial classification, but no nine-period generator was derived. Do not equate to 九宮飛星.
- **Kinetic vs equilibrium**: finite local descent can stop at nonzero energy even where global minima exist; cold Gibbs equilibrium claims require stationary mixing not observed by gradient optimization.
- **Held-out target contamination**: the FULL positive control reaches magic more often because it includes both diagonal predicates, which define the desired output. It cannot demonstrate spontaneous discovery.
- **Stronger interpretation not licensed**: this task explicitly assumes a 3x3 lattice, 1..9 hard permutation prior, row/column global sums; not a bottom-up local interaction with truly unstructured initial state. It tests **insufficiency of these priors**, not natural emergence probability in Transformers, physical systems, or semantics.

## Repair rule usable in other research domains

`Target Emergence Claim -> list every assumption that already encodes the target -> remove one defining condition -> count all alternative minima -> compare exact/ordinary baselines -> measure target under held-out checks -> preserve negative result + conditional theorem -> design lower-prior generative task.`

For deterministic dynamics, distinguish basins and path-dependent selection; for Gibbs stationary ensembles, report energy degeneracy and mixing. Standard baselines are exact enumeration, finite Gibbs partition function, and ordinary greedy local search; no unique SMFT benefit shown.

## Generative residuals / next tests

- Can strictly local, translation/rotation-equivariant interactions on a lattice produce the exact nonlocal 3x3 sums without encoding the global solution? Specify actual finite-range energy, noise and observable protocol; compare ordinary constraint-solving.
- Can a *trained* Transformer with generic unsupervised objectives, no LuoShu examples/prompts/labels, develop a statistically significant held-out LuoShu-class geometry after representation-coordinate and multiple-testing controls? NOT_RUN.
- A nine-element **static orbit quotient** is not automatically a 9-cycle. To claim a nine-cycle, construct and observe a transition T with order 9, contrast affine AGL(2,3) no-order-9 theorem and carry coupling.
- Establish independent reconstruction Benchmark: sealed novel questions and matched budgets with genuinely separate executor/grader. NOT_RUN.

Evidence grade: exact computer-assisted finite enumeration + conditional Gibbs theorem + local synthetic optimization and 32/32 QA. No externally validated Semantic Attractor, no independent LLM study, no experimentally demonstrated semantic emergence.
