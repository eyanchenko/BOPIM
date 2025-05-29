# BOPIM
This repository houses the Python code for ``BOPIM: Bayesian optimization for influence maximization on temporal networks" by Eric Yanchenko, (accepted at Technometrics). Please cite the paper if you use these codes. Thanks!

@article{yanchenko2025bopim,

  title={BOPIM: Bayesian Optimization for influence maximization on temporal networks},
  
  author={Yanchenko, Eric},
  
  journal={Technometrics},
  
  number={just-accepted},
  
  pages={1--20},
  
  year={2025},
  
  publisher={Taylor \& Francis}
  
}


Functions overview:

Creates temporal snapshots from edge list

pre_process_times(E, grps = 10)

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

Compute the Jaccard correlation matrix

jac_kernel(neighs)

Compute the Hamming distance between two seed sets

hamming(x, y, kk)

Compute the Hamming correlation matrix

hamming_kernel(X, kk)

Compute the posterior distribution of the GP parameters

bayes_post(y, X, Sigma, mc_burn=1000, mc_iters=5000)


Compute conditional mean and variance of GP regression model

mean_cov_func(Sstar, x, y, kk, beta0, sigma2, Sigma, kernel, neighs)

Compute Expected improvement of new seed set

EI(Sstar, x, y, kk, ystar, beta0, sigma2, Sigma, kernel, neighs)

BOPIM algorithm

bayesopt(E, kk=1, kern="J", lam=0.01, N0=20, B=5, obj_sims=1000, mc_burn=1000, mc_iters=5000, mc_cores=7)
