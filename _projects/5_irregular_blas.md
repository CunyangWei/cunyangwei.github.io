---
layout: page
title: irregular BLAS on CPUs
description: Oct 2021 – Apr 2023
img:
importance: 5
category: research
---

A line of work on high-performance irregular and batched BLAS for ARM and x86 CPUs,
spanning several frameworks.

#### IrGEMM — Irregular GEMM on ARM and x86 CPUs &middot; *TPDS 2024* &middot; [PDF](/assets/pdf/IrGEMM.pdf)

- Generated hundreds of highly optimized assembly kernels for diverse irregular GEMM
  types based on computing templates, instruction-mapping rules between templates and
  assembly code, and pipeline optimization strategies.
- Abstracted GEMM tiling into a boxing problem solved with dynamic programming to minimize
  memory access and maximize the compute-to-memory-access ratio.
- Built a load-balanced multithreaded scheduling framework for batch matrix multiplication
  on ARMv8 and Intel Cascade Lake architectures.
- Achieved single-threaded speedups of 2.3x / 2.7x / 2.5x and multi-threaded speedups of
  3.4x / 14.6x / 14.3x over Intel MKL, ARMPL, LIBXSMM, and BLIS.

<p>
  <a href="/assets/paper_web/irgemm/" class="btn btn-sm z-depth-0" role="button">Website</a>
</p>

#### IATF — Compact BLAS on ARMv8 &middot; *ICPP 2022* &middot; [PDF](/assets/pdf/IATF.pdf)

- Proposed computing-kernel templates for GEMM and TRSM based on a SIMD-friendly data
  layout, selecting the optimal kernel size and instruction selection from the
  compute-to-memory-access ratio.
- Designed data-packing kernels so the computing kernel's memory accesses are contiguous.
- Built an adaptive tuning framework that chooses the batch size from L1 cache and matrix
  size, and the optimal packing/computing kernels from input matrix properties.
- Achieved up to 4x (GEMM) and 5x (TRSM) speedup over ARMPL in double precision.

<p>
  <a href="/assets/paper_web/iatf/" class="btn btn-sm z-depth-0" role="button">Website</a>
</p>

#### LBBGEMM — Load-Balanced Batch GEMM on ARM CPUs &middot; *HPCC 2022* &middot; [PDF](/assets/pdf/LBBGEMM.pdf)

- Designed high-performance small-GEMM kernels without data packaging to greatly reduce
  memory-access overhead.
- Presented a load-balanced multi-thread task-scheduling strategy for batch GEMM.
- Achieved DGEMM_Batch speedups of 2.3x on a single thread and 4.2x on 48 threads over
  ARMPL.

<p>
  <a href="/assets/paper_web/lbbgemm/" class="btn btn-sm z-depth-0" role="button">Website</a>
</p>

#### SA_TRSM — Shape-Aware Auto-Tuning for Irregular TRSM &middot; *ICPADS 2023*

- A shape-aware auto-tuning framework for small-scale irregular-shaped TRSM, automatically
  selecting kernels and blocking strategies from the triangular-matrix shape to maximize
  performance.
