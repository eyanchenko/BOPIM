# BOPIM
Bayesian optimization for influence maximization on temporal networks


This repository houses the code for ``BOPIM: Bayesian optimization for influence maximization on temporal networks" by Eric Yanchenko, currently under review. Please cite the paper if you use these codes. Thanks!


Functions overview:

Single influence spread evaluation for SI model

sigma(E, S, lam, xxx=0)


Repeated influence spread evaluations for SI model

sigma_mc(E, S, lam, nsims=100, mc_cores=7)


Horseshoe prior Gibbs sampler

horseshoe(y, X, mc_burn=1000, mc_iters=5000)


Dirichlet-Laplace Gibbs sampler

dirlap(y, X, mc_burn=1000, mc_iters=5000)


R2D2 Gibbs sampler

r2d2(y, X, mc_burn=1000, mc_iters=5000)


BOPIM algorithm

bayesopt(E, kk=1, lam=0.01, B=5, num_samps=20, obj_sims=100, prior="Horseshoe", mc_burn=1000, mc_iters=5000, mc_cores=7)
