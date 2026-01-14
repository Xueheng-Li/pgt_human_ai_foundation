# Trust Game Attribution Analysis

## Key Finding

**The trust game uses SIGNAL-BASED attribution, not behavioral attribution.**

## Evidence

The attributed belief is:
```
\tilde{h}_H^{(2,A)} = \phi_H(\rho_A, x_A, \omega_H)
```

Arguments are all fixed parameters:
- ρ_A: AI prosociality (design parameter)
- x_A: Interface signal (experimental treatment)
- ω_H: Human anthropomorphism (individual trait)

**Does NOT depend on** AI strategy σ_A or transfer choice x.

## The Two "x" Variables

| Variable | Meaning | Role |
|----------|---------|------|
| x ∈ [0,E] | Monetary transfer | Strategic choice |
| x_A | Interface signal | Attribution input |

Remark (lines 31-33) explicitly clarifies this distinction.

## Why Referee Misread

The referee likely conflated monetary transfer x with interface signal x_A.

Quote: "the AI's sending decision x affects attributed expectations"

This would be true under **behavioral attribution**, but the paper uses **signal-based attribution** where x_A (interface) matters, not x (transfer).

## Behavioral Variant

A behavioral variant would be interesting:
```
\tilde{h}_H^{(2,A)} = \phi_H(\rho_A, x_A, \omega_H, x)
```

This creates strategic complementarity: AI generosity → higher attributed expectations → more guilt → higher returns.

**However**: This requires extending the equilibrium definition. The current paper avoids this by using signal-based attribution.

## Recommendation

1. Keep trust game as signal-based (current formulation is cleaner)
2. Extend existence theorem to cover behavioral attribution as robustness
3. Note in applications that signal-based attribution is used
4. Discuss behavioral attribution as extension for future work
