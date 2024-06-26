# BOPIM
This repository houses the Python code for ``BOPIM: Bayesian optimization for influence maximization on temporal networks" by Eric Yanchenko, currently under review. Please cite the paper if you use these codes. Thanks!


Functions overview:

Single influence spread evaluation for SI model

sigma(E, S, lam, xxx=0)


Repeated influence spread evaluations for SI model

sigma_mc(E, S, lam, nsims=100, mc_cores=7)

Greedy algorithm with CELF step

greedy(E, k, lam, nsims=100, mc_cores=7)

Dynamic Degree algorithm from Murata and Koga (2018)

dyndeg(E, k, lam)

Find neighbors of nodes in set S

find_n(E0, S)

Compute Jaccard coefficient between two sets

jac(L1, L2)

Horseshoe prior Gibbs sampler

horseshoe_cov(y, X, Sigma, mc_burn=1000, mc_iters=5000, gamma=1)

Compute conditional mean and variance of GP regression model

mean_cov_func(Sstar, x, y, alpha, sigma2, gamma, Sigma, neighs)

Compute Expected improvement of new seed set

EI(Sstar, x, y, ystar, alpha, sigma2, gamma, Sigma, neighs)

BOPIM algorithm

bayesopt_new(E, kk=1, lam=0.01, N0=20, B=5, obj_sims=100, mc_burn=1000, mc_iters=5000, mc_cores=10)
