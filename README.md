# Graiphic Whitepaper Series

Welcome to the **Graiphic Whitepaper Collection**, a public series of technical papers documenting our work on **graph computing**, **AI orchestration**, and **hardware integration**.

Graiphic develops the world’s first system unifying **AI + Logic + Hardware + Energy** under a **single ONNX-based graph** — fully editable, executable, and measurable through **LabVIEW** and our in-house toolkits.

---

## 🧭 Philosophy of the Series

At Graiphic, everything begins with the **graph**.

We use **ONNX** not only as a model format, but as the **universal file system** describing the logic, dataflow, and hardware orchestration of an entire application.  
Our LabVIEW-based IDE and toolkits act as the graphical editors and compilers for these ONNX graphs.

Execution follows two complementary paradigms:

1. **IR-last (current)** — **ONNX Runtime** with optimized **Execution Providers** (CUDA, TensorRT, OpenVINO, ROCm, Xilinx, Qualcomm...).  
2. **IR-first (next)** — **MLIR** compilers (IREE, OpenXLA, oneAPI...) for ahead-of-time specialization and deterministic deployment.

This dual IR strategy keeps ONNX as the single source of truth while giving us runtime breadth today and compiler-grade control tomorrow.

---

### 🧩 Graph Execution Philosophy

<p align="center">
  <img src="./img/IR.png" alt="Dual IR Strategy Diagram" width="720"/>
</p>

- **ONNX = File system & abstraction layer**  
- **LabVIEW = Visual IDE & orchestration cockpit**  
- **Graiphic Toolkits = ONNX authoring + editing + execution bridges**  
- **IR-first / IR-last = compilation vs runtime orchestration**

---

### 🚀 Positioning in the AI Stack

<p align="center">
  <img src="./img/Orvillechart.png" alt="Disruptive Zone Chart" width="700"/>
</p>

Graiphic operates in the **disruptive zone** — where AI becomes deployable, autonomous, and hardware-independent.

---

## 📚 Whitepapers

### **1. GO HW — From Models to Systems (v1.3)**
**Theme:** Unified hardware orchestration in ONNX  
**Summary:** GO HW extends ONNX beyond inference to real-time control of physical systems. It introduces GPIO, DMA, ADC/DAC, timers, and energy-aware monitoring as ONNX nodes, enabling deterministic, low-latency execution on SoCs.

<p align="center">
  <img src="./img/GO-HW_Whitepaper.PNG" alt="GO HW Cover" width="600"/>
</p>

**File:** [`GO-HW_Whitepaper_1.3.pdf`](./GO%20HW%20%E2%80%94%20From%20Models%20to%20Systems/GO-HW_Whitepaper_1.3.pdf)

---

### **2. Benchmarking the Future: Comparing LabVIEW GPU Toolkits — CuLab, G²CPU, and the Graiphic Accelerator (v1.0)**
**Theme:** Performance comparison of LabVIEW GPU acceleration frameworks  
**Summary:**  
This study evaluates the **Graiphic Accelerator Toolkit** against **CuLab** and **G²CPU**, measuring computational throughput, memory efficiency, and runtime determinism under identical LabVIEW test environments.  
The benchmark covers **four workloads** — **GEMM**, **Arithmetic**, **Complex Number Computation**, and **Signal Processing** — and highlights Graiphic’s **compiled ONNX graph execution** advantage versus DLL-based frameworks.

<p align="center">
  <img src="./img/Benchmarking_Whitepaper.PNG" alt="Benchmarking Whitepaper Cover" width="600"/>
</p>

**File:** [`Benchmarking_the_Future_1.0.pdf`](./Benchmarking%20LabVIEW%20GPU%20Toolkits%20CuLab%2C%20G2CPU%2C%20and%20the%20Graiphic%20Accelerator/Benchmarking%20the%20Future%20Comparing%20LabVIEW%20GPU%20Toolkits%20CuLab%2C%20G2CPU%2C%20and%20the%20Graiphic%20Accelerator.1.0.pdf)

#### 🧪 Source Materials and Reproducibility
All **LabVIEW source files** used to generate this whitepaper’s results are publicly available to ensure **transparency and reproducibility**.  
You can access them here:  
👉 [`/Benchmarking LabVIEW GPU Toolkits CuLab, G2CPU, and the Graiphic Accelerator/Source`](./Benchmarking%20LabVIEW%20GPU%20Toolkits%20CuLab%2C%20G2CPU%2C%20and%20the%20Graiphic%20Accelerator/Source)

This directory contains the **exact VIs and datasets** for the four benchmark cases described in the document:

| Benchmark | Folder | Description |
|------------|---------|-------------|
| 🧮 GEMM | [`Source/GEMM`](./Benchmarking%20LabVIEW%20GPU%20Toolkits%20CuLab%2C%20G2CPU%2C%20and%20the%20Graiphic%20Accelerator/Source/GEMM) | Matrix multiplication and memory throughput test |
| ➕ Arithmetic | [`Source/Not Complex`](./Benchmarking%20LabVIEW%20GPU%20Toolkits%20CuLab%2C%20G2CPU%2C%20and%20the%20Graiphic%20Accelerator/Source/Not%20Complex) | Scalar and vector arithmetic operations |
| 🔢 Complex | [`Source/Complex`](./Benchmarking%20LabVIEW%20GPU%20Toolkits%20CuLab%2C%20G2CPU%2C%20and%20the%20Graiphic%20Accelerator/Source/Complex) | Complex-number computation benchmark |
| 📈 Signal Processing | [`Source/Signal Processing Without Indicator And Warmup`](./Benchmarking%20LabVIEW%20GPU%20Toolkits%20CuLab%2C%20G2CPU%2C%20and%20the%20Graiphic%20Accelerator/Source/Signal%20Processing%20Without%20Indicator%20And%20Warmup) | FFT and arithmetic processing pipeline on sensor data |

Together, these resources make the whitepaper a **fully reproducible benchmark suite**, open to independent validation and community extensions.

---

### **3. GO GenAI — From Language to Logic Graphs (v1.0 – upcoming)**
Dynamic ONNX graphs for reasoning and agents, bridging GO HW with cognitive orchestration on sovereign hardware.

---

### **4. SOTA — The LabVIEW IDE for Graph Computing (v1.0 – upcoming)**
LabVIEW-native ONNX IDE for unified authoring, compilation, and orchestration.

---

### **5. Green AI — Energy-Aware Graphs (v1.0 – upcoming)**
Energy as a first-class metric: telemetry, ONNX annotations, multi-objective optimization (accuracy + joules).

---

## 🧩 Purpose

The **Graiphic Whitepaper Series** aims to:
- Document the architectural and technological foundations of our stack (SOTA, GO GenAI, GO HW).  
- Provide transparent benchmarks and reproducible data for the LabVIEW and ONNX communities.  
- Bridge AI compilation research and industrial system design.  
- Serve as a reference for collaborations with **NI**, **STMicroelectronics**, **Horizon Europe**, **DARPA**, and **all partners willing to work with us**.

---

## 🔗 Learn More & Follow Us

**Learn more and download SOTA:**  
👉 [https://www.graiphic.io](https://www.graiphic.io)

**Follow us on YouTube:**  
👉 [https://www.youtube.com/@graiphic](https://www.youtube.com/@graiphic)

**News & Insights:**  
👉 [https://graiphic.io/news-insights/](https://graiphic.io/news-insights/)

---

## ✉️ Contact

📧 **hello@graiphic.io**

---

## 💡 Support & Collaboration

If you like what we do, you can help us grow by **sharing our work**, **following our channels**, and **reaching out for collaboration**.  
Graiphic welcomes partnerships, industrial and academic exchanges, and all initiatives that push the boundaries of **graph-based AI, energy-aware computing, and sovereign technology**.

Together, we can accelerate the transition toward **open, explainable, and hardware-independent intelligence**.  
Graiphic turns opportunities into innovation — and innovation into impact.

---

## 🪪 License
All documents and images are released under **CC BY-NC-SA 4.0**.  
© 2025 Graiphic — [graiphic.io](https://www.graiphic.io)
