# 📊 Benchmarking the Future: Comparing LabVIEW GPU Toolkits  
**CuLab, G2CPU, and the Graiphic Accelerator**

Welcome to the **Graiphic Benchmarking Whitepaper Repository**, where we share the **methods, results, and LabVIEW sources** used to compare the main GPU acceleration toolkits for **LabVIEW**.

This repository accompanies the official whitepaper:  
👉 [**Benchmarking the Future: Comparing LabVIEW GPU Toolkits CuLab, G2CPU, and the Graiphic Accelerator (v1.0)**](./Benchmarking%20the%20Future%20Comparing%20LabVIEW%20GPU%20Toolkits%20CuLab%2C%20G2CPU%2C%20and%20the%20Graiphic%20Accelerator.1.0.pdf)

---

## 🧩 Overview

This benchmark measures and compares the **performance**, **integration**, and **determinism** of several LabVIEW GPU toolkits — all tested in the same LabVIEW environment.

### Toolkits Compared
- **Graiphic Accelerator Toolkit**
- **CuLab GPU Toolkit** (Ngene)
- **G2CPU Toolkit** (Natan Biesmans)
- **Native LabVIEW CPU execution**

The objective is to provide a **real-world comparison** and understand the trade-offs between speed, scalability, and ease of integration.

---

## ⚙️ Test Environment

| Component | Specification |
|------------|---------------|
| **OS** | Windows 11 |
| **CPU** | Intel® Core™ i9-10850K @ 3.60 GHz |
| **GPU** | NVIDIA GeForce RTX 3060 |
| **LabVIEW** | 2025 Q3 |
| **CUDA** | 12.9 |
| **TensorRT** | 10.13.3.9 |
| **Date** | October 15, 2025 |

This setup represents a balanced workstation configuration for reproducible LabVIEW GPU benchmarks.

---

## 📚 Benchmarks Included

1. **GEMM Processing**  
   Matrix multiplication followed by arithmetic post-processing.  
2. **Arithmetic Operations**  
   Iterative Add / Neg / Mul / Div loops for element-wise operations.  
3. **Complex Number Computation**  
   Handling of real + imaginary tensors using ONNX custom nodes.  
4. **Signal Processing Application**  
   FFT + arithmetic operations on **real NI-like signal data (~32 k samples)**.  
   ➤ This test was designed to reflect realistic, small-scale sensor workloads — not synthetic stress tests.

---

## 🧠 Key Findings

- **Graiphic Accelerator (TensorRT)** achieves the **highest performance**, up to:  
  - ⚡ **5× faster than CuLab**  
  - ⚡ **40× faster than G2CPU**  

- **Compiled-graph execution (ONNX Runtime)** significantly reduces overhead versus **per-node DLL execution**.

- **Complex-number support** is functional via custom ONNX nodes — an open research topic for future native integration.

- For **small data blocks**, CPU execution remains competitive; GPU benefits grow with workload size.  
  ➤ The goal is *understanding performance behavior*, not claiming absolute superiority.

---

## 🧪 Source Files

All LabVIEW VIs used to generate the benchmark results are available in the  
[`/Source`](./Source) directory.

| Benchmark | Folder | Description |
|------------|---------|-------------|
| **GEMM** | [Source/GEMM](./Source/GEMM) | Matrix-multiplication tests |
| **Arithmetic** | [Source/Not Complex](./Source/Not%20Complex) | Scalar & vector operations |
| **Complex** | [Source/Complex](./Source/Complex) | Custom complex-number computation |
| **Signal Processing** | [Source/Signal Processing Without Indicator And Warmup](./Source/Signal%20Processing%20Without%20Indicator%20And%20Warmup) | FFT-based signal test |

> **Note:** Two additional large files are required for full signal-processing reproduction:  
> - `G2CPU Read RF BIN quick record_2020 Bench all exec without indicator.vi` (14 MB)  
>   🔗 [Download here](http://download2.graiphic.io/_Bench/G2CPU%20Read%20RF%20BIN%20quick%20record_2020%20Bench%20all%20exec%20without%20indicator.vi)  
> - `TEMP.BIN` (2 GB, test data file)  
>   🔗 [Download here](http://download2.graiphic.io/_Bench/TEMP.BIN)

---

## 🔬 Replication & Discussion

This benchmark was built for **transparency, reproducibility, and community collaboration**.  
All materials (VIs, datasets, configurations) are public — anyone can rerun or extend the tests.

We strongly encourage:
- 🔁 Independent replication using different GPUs, CPUs, or LabVIEW versions  
- 📈 Comparative submissions via pull requests or GitHub issues  
- 🧩 Proposals for new test cases (e.g., deep learning workloads, larger FFTs, etc.)  
- 🧠 Constructive discussion on methodology and interpretation  

> **Benchmarking is not competition — it’s collaboration.**  
> Our goal is to build shared understanding, not to declare winners.

📢 **Discussion board:** Use [GitHub Issues](https://github.com/Graiphic/whitepapers/issues) to post replication results, observations, or suggestions.  
📁 **Repository:** [https://github.com/Graiphic/whitepapers](https://github.com/Graiphic/whitepapers)

---

## 🚀 About Graiphic

**Graiphic** develops the first ecosystem unifying **AI + Logic + Hardware + Energy** inside a single **ONNX graph**.  
Our technology, **GO HW (Graph Orchestration Hardware)**, enables a universal, hardware-agnostic execution layer bridging **ONNX Runtime**, **MLIR**, and **LabVIEW**.

### 📬 Get in Touch
- 💡 Funding & Partnerships → [funding@graiphic.io](mailto:funding@graiphic.io)  
- 🌐 Website → [www.graiphic.io](https://www.graiphic.io)

---

## 🗓️ Versioning

| Version | Date | Author | Description |
|----------|------|--------|-------------|
| **1.0** | 2025-10-15 | Youssef Menjour (Graiphic) | First release of benchmarking whitepaper and LabVIEW sources |

