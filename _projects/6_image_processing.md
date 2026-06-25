---
layout: page
title: image processing
description: Oct 2020 – 2022
img:
importance: 6
category: research
---

High-performance image-processing libraries on CPUs and embedded GPUs.

#### High-performance Image Processing on ARMv8 &middot; *2020 – 2021*

- Categorized image-processing algorithms into three types: **data-irrelevant**,
  **data-sharing**, and **irregular-memory-access** algorithms, and tailored an
  optimization strategy to each.
- Built the library using **ARM NEON intrinsics** for the low-level kernels and **OpenMP**
  for multi-threaded performance.
- Optimized algorithms, memory access, SIMD usage, and assembly instructions to
  substantially improve throughput.
- Achieved speedups of **1.2x** (cvtColor), **2x** (Resize), and **2x** (Filter) over the
  OpenCV library.

#### EgpuIP — Embedded GPU Accelerated Image Processing &middot; *HPCC 2022* &middot; [PDF](/assets/pdf/EgpuIP.pdf)

An embedded-GPU image-processing library built on **GLES (OpenGL ES)**, addressing the lack
of a general optimization guide for image processing on mobile GPUs.

- Proposed **performance optimization chains** that classify image-processing algorithms
  into three modes — **data-independent**, **data-sharing**, and **data-related** — by
  their memory-access and computation characteristics.
- Derived four optimization directions: (1) optimize off-chip memory access for
  memory-bound data-independent algorithms; (2) exploit data locality via shared memory and
  cache for data-sharing algorithms; (3) redesign algorithms to share computational results
  across threads for data-related algorithms; and (4) fully utilize compute resources across
  all three.
- Built the **EgpuIP** library and validated it on histogram equalization, Gaussian
  pyramid, and integral filter, achieving up to **19x**, **88x**, and **3x** speedups over
  OpenCV, respectively.
