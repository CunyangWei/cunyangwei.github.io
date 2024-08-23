---
layout: archive
permalink: /projects/
title: "Research Projects"
author_profile: false
redirect_from: 
  - /projects
---

* _**Optimization of LLM Inference Framework on Mobile GPU**_

	07/2023 - 2024.01

    * Optimized the inference part of Llama 7B on Qualcomm Snapdragon 8gen2's Adreno 740 GPU, with a processing time of less than 2 seconds for the Step 0 phase with 32 token inputs and 8 tokens/s for the Step N phase.
    * Enhanced the performance of tall-and-skinny matrix multiplication, a computational hotspot in the step0 phase. It provides up to 4.0× speedups compared to CLBlast, by implementing a carefully planned tiling strategy for more efficient computation and on-chip memory optimization.
    * Improved the efficiency of GEMV, a key computational process in the stepN phase, reaching over 90% of peak bandwidth capability.

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
