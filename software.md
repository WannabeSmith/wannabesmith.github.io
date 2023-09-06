---
layout: default
---

## Software 

Below are some software packages that I maintain. 

- **confseq: Confidence sequences and uniform boundaries**
\\
*This Python package (maintained by [Steve Howard](https://www.stevehoward.org) and me) implements several nonasymptotic confidence sequences, including those from [Howard et al. (2021)](https://arxiv.org/abs/1810.08240), [Howard & Ramdas (2022)](https://arxiv.org/abs/1906.09712), [Waudby-Smith & Ramdas (2020)](https://arxiv.org/abs/2006.04347) and [Waudby-Smith & Ramdas (2023)](https://arxiv.org/abs/2010.09686).*
\\
[[`github`](https://github.com/gostevehoward/confseq) · [`pypi`](https://pypi.org/project/confseq/)]

- **drconfseq: Doubly robust confidence sequences for sequential causal inference**
\\
*This R package implements the asymptotic confidence sequences of [Waudby-Smith et al.](https://arxiv.org/abs/2103.06476) and specifically confidence sequences for doubly robust treatment effect estimation in observational studies and randomized experiments.*
\\
[[`github`](https://github.com/WannabeSmith/drconfseq)]

- **RiLACS: Risk-limiting election audits via confidence sequences**
\\
*This Python package implements methods introduced in [Waudby-Smith, Stark, and Ramdas (2021)](https://arxiv.org/abs/2107.11323) for using confidence sequences and betting martingale-based tests to audit elections, and more specifically, any election that can be reduced to mean testing/estimation via [SHANGRLA (Stark, 2020)](https://arxiv.org/abs/1911.10035).*
\\
[[`github`](https://github.com/WannabeSmith/RiLACS) · [`pypi`](https://pypi.org/project/RiLACS/)]

- **NPRR: Nonparametric randomized response**
\\
*This Python package implements our nonparametric generalization of Warner's randomized response as well as methods for computing differentially private confidence intervals and sequences for means of bounded random variables as in [Waudby-Smith, Wu, and Ramdas (2023)](https://arxiv.org/abs/2202.08728).*
\\
[[`github`](https://github.com/WannabeSmith/nprr) · [`pypi`](https://pypi.org/project/nprr/)]

Methods that I have developed have also appeared in some other open-source projects (by people that write much better code than me) such as Microsoft's [VowpalWabbit](https://github.com/VowpalWabbit/vowpal_wabbit) (see [this commit](https://github.com/VowpalWabbit/vowpal_wabbit/commit/903d2aa35ad2c8017cc050b17602c3e49819176e)) or [GrowthBook](https://github.com/growthbook/growthbook)'s sequential testing implementation (see [this commit](https://github.com/growthbook/growthbook/pull/1155/commits/63ab0d0fc204f440e16984136a46a5922ab79931) or [the docs](https://docs.growthbook.io/statistics/sequential)) but I have not contributed to them directly.
