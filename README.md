# Hi, I'm Pubali Roy 👋 

I am a Computer Engineering Graduate Student at North Carolina State University and a former R&D FPGA Engineer. My expertise lies at the intersection of **ASIC/FPGA Design**, **Advanced Design Verification (DV)**, **Computer Architecture**, and **Hardware Acceleration for AI/ML Workloads**. 

I bring a blend of industry experience in high-speed digital datapath integration and deep academic specialization in cycle-accurate performance modeling and constraint-driven verification.

---

## Skills & Technologies

- **Design & Verification**: SystemVerilog, Verilog, RTL Design, Layered Testbenches (OVM/UVM concepts), SVA (SystemVerilog Assertions), Test Plan Generation
- **Protocols & Interfaces**: 10G Ethernet, MACsec, AXI4-Lite, AXI-Stream, I2C Multi-Bus Protocol, Wishbone Bus, SDRAM Burst Interfacing
- **Computer Architecture**: Out-of-Order (OoO) Superscalar Pipelines, Speculative Rename Injection, Stride Value Prediction, Cache Hierarchies (LRU, WBWA), Hardware Stream-Buffer Prefetching, Branch Prediction
- **AI / ML & Software**: Python, C++, Perl, Tcl, Bash Shell Scripting, GNU Makefiles, BERT Transformers, NLP Pipelines, Scikit-learn, Spacy
- **EDA & Hardware Tools**: Siemens QuestaSim / ModelSim, Xilinx Vivado, Cadence, Synopsys, GDB, Wireshark, Spirent Tester

---

## Featured Engineering Projects

### [CUDA Cache Simulator](https://github.com/PUBALI19/CUDA-Cache-Simulator)
*CUDA / GPU Computing / Computer Architecture
- Ported a cycle-accurate, multi-level cache simulator (LRU replacement, hardware stream-buffer prefetching) from a class-based C++ implementation to flat, GPU-compatible data structures with __host__ __device__ shared logic between CPU and GPU builds.
- Parallelized a cache-configuration design-space sweep in CUDA, using cudaMallocManaged and pointer-offset slicing to give each of up to 648 GPU threads private, independently-sized cache state.
- Diagnosed and fixed a GPU-specific floating-point precision bug (log2 divergence between host and device) that silently corrupted cache indexing, caught only through systematic line-by-line output verification against a CPU baseline across every configuration.
- Identified and resolved a single-block kernel launch bottleneck leaving 39 of 40 GPU streaming multiprocessors idle, and a unified-memory oversubscription issue that mimicked a hang at ~21.5GB on a 16GB GPU.
- Achieved a 3.6x speedup over the sequential CPU sweep at 648 threads, after determining that raw thread count alone did not reliably improve performance, isolating per-thread memory footprint and per-thread computational depth as the actual governing factors.

### [I2C Multi-Bus Controller (I2CMB) Layered Testbench](https://github.com/PUBALI19/Design-and-Verification-of-an-I2C-Multi-Bus-Controller)
*SystemVerilog | ASIC Verification | Test Plan Closure*
- Developed an object-oriented, layered verification environment using a custom base class library (`ncsu_pkg`) to thoroughly validate an open-source I2C IP core.
- Architected modular components including transaction generators, monitor pipelines (`wb_monitor`, `i2c_monitor`), active predictors, and a transaction-matching scoreboard.
- Linked over 20 distinct register and bus state conditions to functional `covergroups` and cross-coverage targets.
- Created a `bash` regression automation script (`regress.sh`) to run concurrent random-seed tests and merge `.ucdb` databases to achieve **99.2% functional coverage** and expose critical RTL bugs.

### [Hardware Value Predictor & Design Space Exploration](https://github.com/PUBALI19/Hardware-Value-Predictor-Design-Space-Exploration)
*C++ | Microarchitecture Modeling | Performance Analysis*
- Achieved a **2.04 IPC scaling speedup** on data-dependent SPEC benchmarks by architecting a cycle-accurate Stride Value Predictor (SVP).
- Integrated speculative rename injection and utilized Forward Probabilistic Counters (FPC) to enforce a strict 19.0 KB hardware storage budget while maintaining **>99.5% prediction accuracy**.

### [Out-of-Order Superscalar Processor Simulator](https://github.com/PUBALI19/Out-of-Order-Superscalar-Processor-Simulator)
*C++ | Processor Microarchitecture*
- Implemented a configurable, cycle-accurate Out-of-Order processor simulator modeling full pipeline execution stages: register renaming, wakeup/select, oldest-first issue logic, and in-order retirement.
- Benchmarked instructions-per-cycle (IPC) metrics across 40+ hardware configurations, optimizing the Issue Queue and Reorder Buffer (ROB) boundaries to achieve **7.4x performance scaling**.

### [Cache Simulator with Stream-Buffer Prefetching](https://github.com/PUBALI19/Cache-Simulator-with-Stream-Buffer-Prefetching)
*C++ | Performance Modeling | Memory Subsystems*
- Developed a parameterized multi-level cache simulator (L1 and L2) featuring True LRU replacement and nested Write-Back Write-Allocate (WBWA) cascading eviction policies.
- Integrated an optimized $N$-way circular hardware Stream-Buffer Prefetcher, **reducing L1 cache miss rates by 99.6%** across 55+ memory trace configurations.

### [AI-Powered Resume-to-Job Matching Engine](https://github.com/NCSU-NNDL-Spring26/NNDL_13)
*Python | Natural Language Processing | BERT Transformers*
- Awarded **"Best Technical Content"** at a selective engineering symposium.
- Developed a hybrid NLP engineering pipeline utilizing BERT Transformers for deep semantic embeddings paired with TF-IDF for keyword relevance tracking.
- Parsed a curated dataset of 9,400+ technical records with custom Spacy entity extraction algorithms to achieve a **94.9% profile matching accuracy**.

---

## Professional & Research Highlights
- **R&D FPGA Engineer (Tejas Networks - A Tata Group Company)**: Two years of experience integrating AMD MACsec security IP cores into a 10G Ethernet line datapath. Designed AXI4-Lite control planes, AXI-Stream data width converters, and multi-FIFO packet aggregators driven by round-robin FSM schedulers.
- **IEEE-Published Research**: Authored hardware/software hybrid systems including a GAN-based real-time speech recognizer, a CNN distress-detection asset for assistive healthcare, and a thermal fire detection system designed for space capsule safety environments.

---

**Connect with me:**
- [proy9@ncsu.edu](mailto:proy9@ncsu.edu)
- [linkedin.com/in/pubali-roy](https://linkedin.com/in/pubali-roy)
