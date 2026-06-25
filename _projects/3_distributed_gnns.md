---
layout: page
title: distributed GNNs
description: Dec 2024 – Present
img:
importance: 3
category: research
---

Plexus tames billion-edge graphs with a 3D parallel approach to full-graph GNN training,
distributing both graph data and computation across thousands of GPUs.

- Proposed a novel **3D parallel algorithm** that addresses the memory, communication,
  and load-balancing challenges of large-scale GNN training.
- Designed a **performance model** to automatically select optimal 3D virtual GPU grid
  configurations, and a **double-permutation scheme** to achieve near-perfect load
  balancing for sparse graph data.
- Achieved unprecedented scalability up to **2048 GPUs** on the Frontier and Perlmutter
  supercomputers, delivering up to a **54.2x speedup** over state-of-the-art frameworks.

Published at SC 2025. [PDF](/assets/pdf/plexus.pdf)

<p>
  <a href="/assets/paper_web/plexus/" class="btn btn-sm z-depth-0" role="button">Website</a>
</p>
