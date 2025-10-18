# 🧮 LabVIEW Open Benchmark Suite (LOBS)

**An open, reproducible, and community-driven benchmarking initiative for LabVIEW GPU and CPU acceleration.**

---

## 🎯 Purpose

The **LabVIEW Open Benchmark Suite (LOBS)** aims to establish a transparent and vendor-neutral standard for benchmarking computational performance in the **LabVIEW ecosystem**.

Inspired by **SPEC**, **MLPerf**, and the **Graiphic Benchmarking Series**, LOBS provides a shared framework where developers, researchers, and toolkit vendors can:
- run **reproducible test benches** on their own hardware,
- **compare results** under common conditions,
- and **contribute new workloads** to enrich the suite.

---

## ⚙️ Goals

- 🧩 **Unify performance evaluation** across GPU, CPU, FPGA, and hybrid backends.  
- 🔍 **Ensure reproducibility** via open-source VIs, datasets, and hardware specs.  
- 🤝 **Foster collaboration** between toolkit vendors, users, and NI partners.  
- 📈 **Promote transparency** — performance is beautiful when it’s explainable.  

---

## 🧠 Scope

LOBS will progressively cover the following categories:

| Category | Example Workloads | Typical Toolkits |
|-----------|-------------------|------------------|
| **Linear Algebra** | GEMM, Conv2D | Accelerator, CuLab, G²CPU |
| **Signal Processing** | FFT, Filtering, Cross-Correlation | Accelerator, NI Sound/Vision Modules |
| **Arithmetic & Logic** | Element-wise Add/Neg/Mul/Div | All GPU Toolkits |
| **AI & Inference** | ONNX Runtime models, CNNs, Transformers | Accelerator, OpenVINO, ONNX DNN |
| **Memory & IO** | Transfer latency, DMA throughput | G²CPU, custom SDKs |
| **Energy Profiling (future)** | Joule-per-operation metrics | GO HW integration |

---

## 🔬 Methodology Principles

Every benchmark included in LOBS must:
1. Be **open source**, reproducible by anyone with LabVIEW Professional or Community Edition.  
2. Include clear **hardware + driver configuration** documentation.  
3. Report **execution time (sec)** and **numerical correctness**.  
4. Be **independent** of vendor marketing — results speak through data.  

All submissions will be peer-reviewed through GitHub issues and merged once verified.

---

## 📘 Reference Benchmark

The **Graiphic Whitepaper “Benchmarking the Future”** serves as the **LOBS Reference 0** — the baseline set of tests for GEMM, Arithmetic, Complex, and Signal Processing workloads.  

📄 [Read the Whitepaper →](../Benchmarking%20the%20Future%20Comparing%20LabVIEW%20GPU%20Toolkits%20CuLab%2C%20G2CPU%2C%20and%20the%20Graiphic%20Accelerator.1.0.pdf)

---

## 🧩 How to Contribute

We welcome contributions from engineers, researchers, and toolkit developers.

### 🛠 Submit a New Test Case
1. Fork this repository.  
2. Add your test under `/LabVIEW Open Benchmark Suite/Benchmarks/<Category>/`.  
3. Include:
   - VI(s) and test data  
   - Hardware configuration (CPU, GPU, driver, OS)  
   - Expected results and performance metrics  
4. Submit a **Pull Request** with a short description.

### 🧾 Share Replication Results
Use GitHub **Issues** to post:
- screenshots,  
- execution logs,  
- or raw numeric results from your hardware.

All reproducible submissions will be cited in future versions of the benchmark report.

---

## 🧭 Roadmap

| Phase | Objective | Status |
|--------|------------|--------|
| **0** | Publish reference benchmark (Graiphic Whitepaper) | ✅ Done |
| **1** | Community replication & verification | 🟢 Ongoing |
| **2** | Add AI inference and deep learning test suite | ⏳ Planned |
| **3** | Energy & efficiency measurement (GO HW integration) | 🚧 In progress |
| **4** | Publish v1.0 Open Benchmark Specification | 📅 2026 |

---

## 🤝 Contributors & Partners

| Name | Organization | Role |
|------|---------------|------|
| **Graiphic** | France | Founder & Core Maintainer |
| **Open contributors** | – | Replication, validation, extensions |

If your organization wants to join as a co-maintainer or reviewer, please contact:  
📧 [benchmark@graiphic.io](mailto:contact@graiphic.io)

---

## 🧭 Motto

> “Benchmarking isn’t about who’s fastest —  
> it’s about understanding why.”  

---

## 📄 License

All contents of LOBS are released under the **MIT License** for maximum openness.

---

**© 2025 Graiphic — LabVIEW Open Benchmark Suite (LOBS)**  
Part of the Graiphic Open Science initiative.

