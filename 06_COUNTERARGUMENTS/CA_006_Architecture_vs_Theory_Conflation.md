# CA_006: Architecture vs Theory Conflation

**Status:** Active — standing concern
**Date:** 2026-06-11

## The Challenge

The framework risks conflating theoretical primitives with architectural objects. These are different things serving different purposes:

- **Theoretical primitives** (Goal, Policy, Interpretation) explain *why behavior happens*
- **Architectural objects** (Working Theory, Evidence, Decision, Outcome, Uncertainty) structure *how reasoning should be stored and retrieved*

The danger: treating architectural convenience as theoretical truth. Just because "Working Theory" is a useful entity to store and retrieve doesn't mean it's a fundamental component of optimizer behavior. And just because "Claim" is a theoretical atomic unit doesn't mean it's the right entity for a database schema.

## Evidence of Conflation

1. **Goal** appears as both an optimizer primitive (Theory) and a reasoning object (Architecture)
2. **Policy** appears in Theory, Architecture, and Topography Engineering
3. The reduction exercise (Claim → Decision → Outcome) mixed theoretical reduction with implementation design
4. The reasoning architecture was initially presented alongside optimizer primitives as if they occupied the same conceptual space

## Why This Matters

If the layers aren't kept separate:
- Theoretical debates get resolved by implementation convenience ("let's just use Working Theory because it's easier to store")
- Architectural decisions get constrained by theoretical purity ("we can't use Working Theory because it's not a primitive")
- Implementation choices leak into theory ("the decision journal works, therefore Claim-Decision-Outcome is the correct theoretical model")

Each layer should evolve on its own terms, under its own validation criteria.

## Standing Instruction

When proposing any new entity or concept, explicitly identify which layer it belongs to:
- Is this a theoretical claim about how optimizers work?
- Is this an engineering dimension of information environments?
- Is this an architectural object for organizational reasoning systems?
- Is this an implementation mechanism?

If it appears in more than one layer, explain why — or flag it as a potential conflation.

## Cross-References
- FL_010 (Layer Separation — the fault line this counterargument protects)
- CA_005 (Unfalsifiability — conflation makes the framework harder to falsify)
- FL_009 (Optimizer Architecture — Theory layer)
