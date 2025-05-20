# Parallel Convex Hull Computation and Benchmarking

> High-performance CUDA implementations of classical and novel convex hull algorithms, benchmarked and compared for large-scale 2D point sets.

## Overview

This project implements and benchmarks various convex hull algorithms using CUDA C++, designed for parallel execution on GPUs.  
The goal is to evaluate and compare performance at scale, while proposing an efficient novel approach for optimized computation.

---

## Features

- CUDA implementations of:
  - **QuickHull**
  - **HeapHull**
  - **Asynchronous Incremental Approach**
  - **Parallel Graham's Scan**
  - **Hybrid SFQHull (The Novel Approach)**
- Synthetic data generation using Python (`input_gen.ipynb`)
- Batch execution script (`run_all.bat`)
  
---

## Project Structure

```plaintext
files/
│
├── heaphull.cu         # CUDA HeapHull
├── incremental.cu      # CUDA Asynchronous Incremental Approach
├── quickhull.cu        # CUDA QuickHull
├── Hybrid-sfqhull.cu   # Hybrid SFQHull Novel Approach
├── scan.cu             # CUDA Graham's Scan
│
├── input_gen.ipynb     # Jupyter Notebook to generate synthetic inputs
├── run_all.bat         # Batch script to compile & run all algorithms
│
├── results.txt         # Benchmark results (runtime comparisons)
       
```

---

## Getting Started

### Requirements

- CUDA Toolkit (v10.0 or higher recommended)
- NVIDIA GPU with compute capability 5.0+
- C++ Compiler
- Python 3.x (for input generation, if needed)
- `numpy` and `matplotlib` for `input_gen.ipynb`

---

### Build Instructions

You can compile individual `.cu` files using `nvcc`:

```bash
nvcc quickhull.cu -o quickhull
nvcc heaphull.cu -o heaphull
nvcc Hybrid-sfqhull.cu -o Hybrid-sfqhull
nvcc incremental.cu -o incremental
```

Or you can compile and run everything automatically using:

```bash
./run_all.bat
```

> ⚡ Make sure the `.bat` file paths match your local environment setup.

---

### Run Instructions

After building, just execute:

```bash
./quickhull
./heaphull
./Hybrid-sfqhull
./incremental
```

---

##  Results

Benchmark results are recorded in [`results.txt`](./results.txt).

---

## Contributing

Contributions are welcome!

---

## License

Distributed under the MIT License.  

---
