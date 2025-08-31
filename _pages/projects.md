---
layout: archive
permalink: /projects/
title: "Research Projects"
author_profile: false
redirect_from: 
  - /projects
---

* _**Unmasking Network-Induced Performance Variability in GPU-Accelerated Supercomputers**_
    
    09/2024 – Present

    * Modern HPC systems are increasingly challenged by performance variability that significantly impacts both scientific simulations and AI training, with even minor delays on a single node causing widespread job slowdowns. This issue is exacerbated by heterogeneous hardware, software jitter, and especially network contention, leading to inefficient resource usage and higher operational costs.
    * Our study is the first to systematically investigate network-induced performance variability on modern GPU clusters, revealing that network delays are the dominant factor affecting overall system performance.
    * We conducted a longitudinal study on production systems such as Perlmutter and Frontier, collecting extensive real-world data across both traditional MPI applications and distributed deep learning workloads. These novel insights provide actionable strategies for mitigating network bottlenecks, underscoring the originality and importance of our work in advancing HPC and AI system efficiency.

---

* _**Taming Billion-edge Graphs with 3D Parallel Full-graph GNN Training**_ 

    12/2024 – Present
    * Proposed a novel 3D parallel algorithm to address memory, communication, and load-balancing challenges in large-scale GNN training, enabling efficient distribution of graph data and computation across thousands of GPUs.
    * Designed a performance model to automatically select optimal 3D virtual GPU grid configurations and designed a double permutation scheme to achieve near-perfect load balancing for sparse graph data.
    * Achieved unprecedented scalability up to 2048 GPUs on the Frontier and Perlmutter supercomputers, delivering up to a 54.2x speedup over state-of-the-art frameworks.

---

* _**Optimization of LLM Inference Framework on Mobile GPU**_

	07/2023 - 2024.01

    * Accelerated LLaMA-7B inference on mobile GPUs (Qualcomm Adreno 740) by co-designing computation scheduling and memory optimization strategies.
    * Optimized tall-and-skinny matrix multiplication kernels for the prefill phase computational bottleneck, achieving 4.0× performance improvement over CLBlast baseline through sophisticated tiling algorithms and strategic on-chip memory utilization.
    * Enhanced GEMV operation efficiency in the decode phase, delivering >90% peak memory bandwidth utilization through targeted algorithmic improvements and hardware-aware optimization techniques.

<video width="225" height="500" controls style="display: block; margin: auto;">
  <source src="https://dl.dropboxusercontent.com/scl/fi/s2qr78r1dkvly9akcjj52/perfxLLM.mp4?rlkey=hnvzdwixacug3mw4ro1nxcnoo&dl=1" type="video/mp4">
</video>
---

* _**IrGEMM: An Input-Aware Tuning Framework for Irregular GEMM on ARM and X86 CPUs**_

	10/2022 - 04/2023

    * Generated hundreds of highly optimized assembly kernels for diverse irregular GEMM types based on computing templates, the instruction mapping rules between templates and assembly codes, and pipeline optimization strategies.
    * Abstracted tiling problems of GEMM into boxing problems that utilizes dynamic programming approach to minimum memory access of Irregular GEMM and maximum computational memory access ratio.
    * Built a load-balanced multithreaded scheduling framework for processing batch matrix multiplication to achieve the ultimate multi-threaded speedup.
    * Implemented a high-performance irregular matrix multiplication library for ARMv8 and Intel cascade Lake architectures. 
    * Increased the speed-up ratio of irregular DGEMM in a single-threaded environment to 2.3x, 2.7x, and 2.5x in comparison to Intel MKL, ARMPL, LIBXSMM, and BLIS; increased the speed-up ratio of irregular DGEMM in a multi-threaded environment to 3.4x, 14.6x, and 14.3x in comparison to Intel MKL, ARMPL, LIBXSMM, and BLIS.

---

* _**IATF: An Input-Aware Tuning Framework for Compact BLAS Based on ARMv8 CPUs**_

    10/2021 - 04/2022                         


    * Proposed computing kernel templates for GEMM and TRSM based on the SIMD-friendly data layout and analyzed the compute-to-memory-access ratio to find the optimal kernel size; and optimized instruction selection.  
    * Carefully designed the data packing kernel so that the memory accesses of the computing kernel are contiguous.  
    * Proposed an adaptive tuning framework to chooses an appropriate number of matrices for batch operation each time according to L1 cache size and matrix size, and chooses the optimal data packing kernel and computing kernel according to the input matrix properties.
    * Increased the speed-up ratio of GEMM and TRSM to 4x and 5x in comparison to ARMPL under double-precision floating-point operation.

---

* _**LBBGEMM: A Load-Balanced Batch GEMM Framework on ARM CPUs**_	

    05/2022 - 10/2022                                          


    * Designed high-performance small GEMM kernels without data packaging to greatly reduce the memory accessing overhead.                                                                                                      
    * Presented a load-balanced multi-thread task scheduling strategy for batch GEMM to improve multi-core performance dramatically.
    * Increased the speed-up ratio of DGEMM\_Batch to 2.3x for a single thread and 4.2x for 48 threads in comparison to ARMPL.   

---

* _**High-performance Image Processing Algorithms Optimization Based On ARMv8 CPUs**_,	

    10/2020 - 10/2021

    * Sorted image processing algorithms into three types (data irrelevant algorithm, data sharing algorithm and irregular memory access algorithm). 
    * Built a high-performance image processing algorithms library by writing the underlying code with Arm Neon Intrinsic and optimizing multi-threaded performance with OpenMP.
    * Presented optimized image processing algorithm library based on ARMv8 architecture and substantially improved the image processing performance by optimizing the algorithms, memory access, SIMD, and assembly instruction. 
    * Increased the speed-up ratio of cvtColor, Resize and Filter modules to 1.2x, 2x, and 2x in comparison to the OpenCV algorithms library.                                
