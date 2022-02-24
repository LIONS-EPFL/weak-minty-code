# Weak Minty code

This code accompanies the paper titled [_Escaping limit cycles: Global convergence for constrained nonconvex-nonconcave minimax problems_](https://infoscience.epfl.ch/record/291889/files/escaping_limit_cycles_global_c.pdf) at ICLR 2022.

## Overview

- [`Lowerbounds.nb`](/Lowerbounds.nb) verifies the steps for the proof of Theorem 3.4.
- [`PolarGame.nb`](/PolarGame.nb) verifies the steps in Appendix C.2.
- [`Forsaken.nb`](/Forsaken.nb) verifies the steps in Appendix C.3.
- [`GlobalForsaken.nb`](/GlobalForsaken.nb) verifies the steps in Appendix C.4.
- [`Experiments.nb`](/Experiments.nb) contains all deterministic experiments.
- [`StocExperiments.nb`](/StocExperiments.nb) contains all stochastic experiments.

## Hyperparameter recommendations

We recommend the following parameters for CurvatureEG+:

- ν = 0.99 such that that initial guess is close to ||JF(z)||².
- τ = 0.5 such that we do not incur too many backtracking calls. Setting it even smaller will reduce the number of backtracks further. However, there is a tradeoff since decreasing τ leads to a smaller extrapolation stepsize which might prevent convergence.
