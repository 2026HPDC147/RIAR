# HPDC 2026 — Paper ID #147 (Anonymous Repository)

This is the open-source repository for **HPDC 2026 paper ID #147**.  
This is currently an empty project without any code. If our paper is accepted, we will complete the code. This repository builds upon the open-source implementation from *Hans Kasan* (2022),  author of the baseline adaptive routing algorithm **DGB** used in this paper. We gratefully acknowledge the contribution of *Hans Kasan* to the research community.  




### ⚙️ Reproduction Instructions

1. Compile the simulator:

   ```bash
   cd RIAR/booksim/src
   make -j8
   ```

2. Run all synthetic workloads:

   ```bash
   cd ../results
   python allTest.py
   ```

   *Note:* This command launches multiple BookSim processes in parallel.  
   On a 96-thread AMD EPYC 2nd Gen CPU, this process takes about **4 hours**; on a personal computer, it may take up to **12 hours**.

3. Generate figures:

   ```bash
   python allFigures.py
   ```

4. After execution, the folder `RIAR/booksim/results` contains all experimental results presented in the paper.  
   In principle, after completing steps 2 and 3, the contents of `RIAR/booksim/results` and `RIAR/booksim/paperResults` should be identical.

---

### 📁 Implementation Notes

All algorithms presented in the paper are implemented in:  
- `RIAR/booksim/src/networks/dragonfly.cpp`  
- `RIAR/booksim/src/routers/iq_router.cpp`  

Due to time constraints, comments are limited at this stage.  
Comprehensive code documentation and additional explanations will be added after review results are announced.

