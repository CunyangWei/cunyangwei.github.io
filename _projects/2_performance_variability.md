---
layout: page
title: performance variability
description: Sep 2024 – Present
img:
importance: 2
category: research
---

Modern HPC systems are increasingly challenged by performance variability that
significantly impacts both scientific simulations and AI training — even minor delays on
a single node can cause widespread job slowdowns. This is exacerbated by heterogeneous
hardware, software jitter, and especially network contention, leading to inefficient
resource usage and higher operational costs.

- The first work to systematically investigate **network-induced** performance
  variability on modern GPU clusters, revealing that network delays are the dominant
  factor affecting overall system performance.
- Conducted a **longitudinal study** on production systems such as Perlmutter and
  Frontier, collecting extensive real-world data across both traditional MPI applications
  and distributed deep-learning workloads.
- Derived **actionable strategies** for mitigating network bottlenecks, advancing the
  efficiency of HPC and AI systems.

Published at IPDPS 2026. [PDF](/assets/pdf/2026-05-variability-ipdps.pdf) &middot;
Best Poster Award Nominee at SC 2025. [Poster](/assets/pdf/variability_poster.pdf)

<p>
  <a href="/assets/paper_web/variability/" class="btn btn-sm z-depth-0" role="button">Website</a>
</p>
