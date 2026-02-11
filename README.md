# Parity-Driven Quantum Mechanics

A new interpretive framework for quantum mechanics where binary parity (odd/even particle count) governs the transition between quantum and classical behavior.

**Author:** Karel John Murdoch (Independent Researcher)

## Papers

1. **[PARITY-THEORY.md](PARITY-THEORY.md)** -- Conceptual framework. Derives superposition, collapse, interference, entanglement, tunneling, the Zeno effect, and the quantum-gravity divide from a single principle: the Z2 parity of a universe's particle count.

2. **[PARITY-FORMALISM.md](PARITY-FORMALISM.md)** -- Mathematical formalism. Full Lagrangian (6 terms), equations of motion, exact solutions for N=1,2,3 particle systems, consistency checks (Lorentz invariance, energy conservation, Schrodinger equation recovery), and connection to BCS theory, Z2 lattice gauge theory, and Many-Interacting-Worlds.

## Core Claims

1. The total particle count in a universe is either odd or even -- a binary (Z2) property
2. Odd parity = quantum-active state; even parity = classical-dominant state
3. Particles transit between parallel universes primarily in pairs
4. Unpaired particles are not committed to any single universe (superposition)
5. Observation anchors a particle to the observer's universe, settling parity
6. Gravity couples only to anchored (paired, committed) matter

## Testable Predictions

- **Even/odd coherence oscillation:** Systems with even particle count maintain coherence longer than odd-count systems, with ratio exp(Delta_E / kT)
- **No gravitational decoherence for unpaired matter:** Contradicts Penrose objective reduction; testable by MAQRO-class satellite experiments at 10^-14 to 10^-12 kg
- **Sawtooth entangled group stability:** Entangled groups of even size are more stable than odd, producing a sawtooth pattern in decoherence rate vs group size

## Numerical Validation

Three simulation scripts verify the framework's internal consistency and compare it against Penrose's objective reduction model:

```bash
# Install dependencies
python -m venv .venv && source .venv/bin/activate
pip install numpy scipy matplotlib

# Run the formalism validation (10 parts, ~30 seconds)
python scripts/parity_formalism_validation.py

# Run the qualitative comparison against Penrose
python scripts/parity_vs_penrose.py

# Run the impartial comparison against 14 published experiments
python scripts/fair_fight.py
```

### Validation Results (parity_formalism_validation.py)

| Test | Result |
|------|--------|
| N=1 eigenvalues match analytic J +/- t1 | PASS |
| N=2 eigenvalues match 3x3 analytic solution | PASS |
| Even/odd spectral gap ratio follows exp(Delta_E/kT) | PASS |
| Ising phase diagram shows quantum-classical transition | PASS |
| Pair hopping dominates over single hopping | PASS |
| Gravitational mass = 0 for unpaired particles | PASS |
| Quantum Zeno effect reproduced | PASS |
| Schrodinger equation recovered at K=1000 (error < 10^-14) | PASS |
| Sawtooth entangled group stability confirmed | PASS |
| Penrose vs Parity divergence at 10^-14 to 10^-12 kg | PASS |

### Fair Fight Results (fair_fight.py)

Impartial comparison against 14 published experiments (1974-2019), with Penrose inheriting standard QM predictions:

| Category | Penrose | Parity |
|----------|---------|--------|
| Empirical match (14 experiments) | 13/14 | 3/14 |
| Numerical consistency | 4/5 | 5/5 |
| Theoretical merit | 14/16 | 9/16 |
| Unique testable predictions | 1 | 3 |

Models only diverge in the untested massive superposition regime (10^-14 to 10^-12 kg). The even/odd coherence test is the cheapest discriminating experiment.

## Requirements

- Python 3.10+
- NumPy, SciPy, Matplotlib

## References

Key references from the papers:

- Everett, H. (1957). Relative state formulation of quantum mechanics. *Rev. Mod. Phys.* 29, 454-462.
- Hall, M.J.W., Deckert, D.-A., Wiseman, H.M. (2014). Quantum phenomena modeled by interactions between many classical worlds. *Phys. Rev. X* 4, 041013.
- Penrose, R. (1996). On gravity's role in quantum state reduction. *Gen. Rel. Grav.* 28, 581-600.
- Wick, G.C., Wightman, A.S., Wigner, E.P. (1952). The intrinsic parity of elementary particles. *Phys. Rev.* 88, 101-105.

## License

MIT License. See [LICENSE](LICENSE).
