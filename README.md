# sequential-decision-making-reproduction# Dynamics of Sequential Decision Making — a reproduction

A reproduction of Rabinovich, Huerta and Afraimovich, *Dynamics of Sequential Decision
Making*, Phys. Rev. Lett. 97:188103 (2006), with Python simulations of the model's two
decision strategies.

Term project, *Neuroscience*, Sharif University of Technology, Winter 2024–2025.
Report in `report.pdf` (in Persian; code and figure labels in English).

## The model

Sequential decisions are modelled as transient dynamics in a Cognitive State Machine:
competing cognitive states `a_i` follow Lotka–Volterra-type dynamics,

    ȧ_i = a_i [ σ_i(I,t) − (a_i + Σ_{j≠i} ρ_ij a_j) ] + η_i(t),

and the decision sequence is realised as a stable heteroclinic sequence — a chain of
transitions between saddle points, each stable in every direction but one.

Two strategies are contrasted. **High-risk** decision making minimises the time spent
near each saddle by following the largest positive eigenvalue; **risk-aversion** picks
the saddle with the highest stability index instead.

## What is reproduced

- Time series of the cognitive states under high-risk dynamics, in a random and in a
  structured (repetitive) environment, with the corresponding phase-plane trajectories.
- The phase transition in high-risk decision making: median life length `L` and median
  number of nodes `C` against the number of choices `M`, for `N = 10, 25, 50`
  cognitive states. Longer sequences appear abruptly past a threshold in `M` for the
  larger systems, while `N = 10` stays flat.
- The sequence-length distribution `P(L)` under risk aversion for `N = 75`, which decays
  exponentially and is essentially independent of `M`.

## Authors

Mahdi Abolhasani and Alireza Habibzadeh. Course instructor: Dr. Saman Moghimi.

## Reference

M. I. Rabinovich, R. Huerta, V. Afraimovich, *Dynamics of sequential decision making*,
Phys. Rev. Lett. 97:188103, 2006.
