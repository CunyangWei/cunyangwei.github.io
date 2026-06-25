---
layout: page
title: LLM inference on mobile GPUs
description: Jul 2023 – Jan 2024
img:
importance: 4
category: research
---

Accelerated LLaMA-7B inference on mobile GPUs (Qualcomm Adreno 740) by co-designing
computation scheduling and memory-optimization strategies for the two inference phases.

- Optimized **tall-and-skinny matrix-multiplication** kernels for the prefill-phase
  computational bottleneck, achieving a **4.0x** improvement over the CLBlast baseline
  through sophisticated tiling algorithms and strategic on-chip memory utilization.
- Enhanced **GEMV** efficiency in the decode phase, reaching **>90% peak memory-bandwidth
  utilization** via targeted algorithmic and hardware-aware optimizations.

<video width="225" height="500" controls style="display: block; margin: auto;">
  <source src="https://dl.dropboxusercontent.com/scl/fi/s2qr78r1dkvly9akcjj52/perfxLLM.mp4?rlkey=hnvzdwixacug3mw4ro1nxcnoo&dl=1" type="video/mp4">
</video>
