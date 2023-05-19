---
layout: default
---

<img class="profile-picture" src="assets/gasworks.jpg">

I'm a PhD student in [Statistics at Carnegie Mellon University](http://stat.cmu.edu/) where I am lucky to be advised by [Aaditya Ramdas](http://www.stat.cmu.edu/~aramdas/). My research is supported by an Amazon Graduate Research Fellowship.

Previously, I was an intern at [Microsoft Research](https://www.microsoft.com/en-us/research/lab/microsoft-research-new-york/), [Adobe Research](https://research.adobe.com/), and [SickKids](https://www.sickkids.ca/). Before that, I studied math at the University of Waterloo. More info can be found in my [CV](iws_cv.pdf).

I am broadly interested in statistical methods that make realistic nonparametric assumptions about data, often in adaptive, sequential settings. More specifically, I focus on
* Anytime-valid sequential inference,
* Nonparametric methods,
* Causal inference,
* Reinforcement learning, and
* Differential privacy.

---

## Selected papers

(Full list on [google scholar](https://scholar.google.com/citations?user=FnyNlFAAAAAJ&oi=ao).)

- **Anytime-valid off-policy inference for contextual bandits** \\
    I. Waudby-Smith, L. Wu, A. Ramdas, N. Karampatziakis, and P. Mineiro \\
    [arxiv](https://arxiv.org/abs/2210.10768) 

- **Time-uniform central limit theory and asymptotic confidence sequences** \\
    I. Waudby-Smith, D. Arbour, R. Sinha, E.H. Kennedy, and A. Ramdas \\
    [arxiv](https://arxiv.org/abs/2103.06476) 

- **A nonparametric extension of randomized response for private confidence sets** \\
    I. Waudby-Smith, Z.S. Wu, and A. Ramdas \\
    ICML, 2023 _(oral)_ · [arxiv](https://arxiv.org/abs/2202.08728) 

- **Estimating means of bounded random variables by betting** \\
	I. Waudby-Smith and A. Ramdas \\
    JRSSB, 2023 _(discussion paper)_ · [arxiv](https://arxiv.org/abs/2010.09686)

- **RiLACS: Risk-limiting audits via confidence sequences**\\
	I. Waudby-Smith, P.B. Stark, and A. Ramdas \\
    E-Vote-ID, 2021 _(Best paper award)_ ·
    [arxiv](https://arxiv.org/abs/2107.11323) ·
    [proceedings](https://link.springer.com/chapter/10.1007/978-3-030-86942-7_9)

- **Confidence sequences for sampling without replacement**\\
	I. Waudby-Smith and A. Ramdas \\
    NeurIPS, 2020 _(spotlight)_ ·
    [arxiv](https://arxiv.org/abs/2006.04347) ·
    [proceedings](https://proceedings.neurips.cc/paper/2020/hash/e96c7de8f6390b1e6c71556e4e0a4959-Abstract.html) 


--- 

## Software 

Below are some software packages that I either maintain or have contributed to. All of these packages should be easily installable (e.g. via `pip install pkg`) and fully documented but please open issues / submit PRs / email me if my code ever gives you a hard time.

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
*This Python package implements our nonparametric generalization of Warner's randomized response as well as methods for computing differentially private confidence intervals and sequences for means of bounded random variables as in [this paper](https://arxiv.org/abs/2202.08728).*
\\
[[`github`](https://github.com/WannabeSmith/nprr) · [`pypi`](https://pypi.org/project/nprr/)]

Methods that I have developed have also appeared in some other open-source projects (by people that write much better code than me) such as Microsoft's [VowpalWabbit](https://github.com/VowpalWabbit/vowpal_wabbit) (see [this commit](https://github.com/VowpalWabbit/vowpal_wabbit/commit/903d2aa35ad2c8017cc050b17602c3e49819176e)) or [GrowthBook](https://github.com/growthbook/growthbook)'s sequential testing implementation (see [this commit](https://github.com/growthbook/growthbook/pull/1155/commits/63ab0d0fc204f440e16984136a46a5922ab79931) or [the docs](https://docs.growthbook.io/statistics/sequential)) but I have not contributed to them directly.

---

## Connect 

* Email: [ianws@cmu.edu](mailto:ianws@cmu.edu)
* Github: [wannabesmith](https://github.com/wannabesmith)
* Twitter: [@iwaudbysmith](https://twitter.com/iwaudbysmith)

---

