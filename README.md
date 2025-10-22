# Chip Fuzz

A collection of papers, tools and courses related to chip fuzzing. If there is any additional information that needs to be clarified, please feel free to PR or Issue!

Fuzz everything! Now let's fuzz chip!

---

## 2018
### ICCAD
- **RFUZZ: Coverage-Directed Fuzz Testing of RTL on FPGAs**  
  Paper: [ACM link](https://dl.acm.org/doi/10.1145/3240765.3240842) · Code: [ekiwi/rfuzz](https://github.com/ekiwi/rfuzz)

---

## 2020
### ICCAD
- **Hyperfuzzing for SoC security validation**  
  Paper: [ACM link](https://dl.acm.org/doi/10.1145/3400302.3415709) · Code: [skmuduli92/HyperFuzzer](https://github.com/skmuduli92/HyperFuzzer)

---

## 2021
### IEEE S&P
- **DifuzzRTL: Differential Fuzz Testing to Find CPU Bugs**  
  Paper: [IEEE link](https://ieeexplore.ieee.org/document/9519470) · Code: [compsec-snu/difuzz-rtl](https://github.com/compsec-snu/difuzz-rtl)


### MICRO
- **Effective Processor Verification with Logic Fuzzer Enhanced Co-simulation**    
  Paper: [ACM link](https://dl.acm.org/doi/10.1145/3466752.3480092) · Code: [chipsalliance/dromajo](https://github.com/chipsalliance/dromajo.git)


### DAC
- **DirectFuzz: Automated Test Generation for RTL Designs using Directed Graybox Fuzzing**   
  Paper: [IEEE link](https://ieeexplore.ieee.org/document/9586289/) · Code: _n/a_


### WOSET
- **RTLFuzzLab: Building A Modular Open-Source Hardware Fuzzing Framework**   
  Paper: [WOSET link](https://woset-workshop.github.io/PDFs/2021/a10.pdf) · Code: [ekiwi/rtl-fuzz-lab](https://github.com/ekiwi/rtl-fuzz-lab)

---

## 2022
### USENIX Security
- **TheHuzz: Instruction Fuzzing of Processors Using Golden-Reference Models for Finding Software-Exploitable Vulnerabilities**     
  Paper: [USENIX link](https://www.usenix.org/conference/usenixsecurity22/presentation/kande) · Code: _n/a_

- **Fuzzing Hardware Like Software**     
  Paper: [USENIX link](https://www.usenix.org/conference/usenixsecurity22/presentation/trippel) · Code: [googleinterns/hw-fuzzing](https://github.com/googleinterns/hw-fuzzing)
  亮点：AFL、总线语法（对tilelink总线系统也有一些工作）


### GLSVLSI
- **Efficient Cross-Level Processor Verification using Coverage-guided Fuzzing**      
  Paper: [ACM link](https://dl.acm.org/doi/10.1145/3526241.3530340) · Code: _n/a_


### DATE
- **Cross-Level Processor Verification via Endless Randomized Instruction Stream Generation with Coverage-guided Aging**      
  Paper: [IEEE link](https://ieeexplore.ieee.org/document/9774771) · Code: _n/a_

---

## 2023
### USENIX Security
- **MorFuzz: Fuzzing Processor via Runtime Instruction Morphing enhanced Synchronizable Co-simulation**   
  Paper: [USENIX link](https://www.usenix.org/conference/usenixsecurity23/presentation/xu-jinyan) · Code: [sycuricon/MorFuzz](https://github.com/sycuricon/MorFuzz)
  co-sim: 1.二阶段指令提交，先提交触发isa-emu记录下写回结果，再到延迟写回的数据准备好时再和记下的结果比较，以适配如rocket指令commit阶段延迟回写 2.可状态同步，再在遇到可missmatch的情况，允许将rtl的状态同步到sim中，以弥合一些isa中允许自由实现的差异
  ps.有点意思，但改进没啥意义
  morphing: 在IFU和IDU间插了个组件，即采用“运行时指令变形”技术，在处理器执行期间动态劫持并修改即将执行的指令，同时利用当前的运行时上下文信息（如寄存器状态和流水线情况）来生成具有有效格式和有意义语义的指令流
  ps.难绷，我认为不合适fuzz的形态

- **HyPFuzz: Formal-Assisted Processor Fuzzing**      
  Paper: [arXiv link](https://arxiv.org/pdf/2304.02485.pdf) · Code: _n/a_


### IEEE HOST
- **ProcessorFuzz: Processor Fuzzing with Control and Status Registers Guidance**     
  Paper: [IEEE link](https://ieeexplore.ieee.org/document/10133714) · Code: [bu-icsg/ProcessorFuzz](https://github.com/bu-icsg/ProcessorFuzz)


### ArXiv / Others

- **Achieving Last-Mile Functional Coverage in Testing Chip Design Software Implementations**     
  Paper: [IEEE link](https://ieeexplore.ieee.org/document/10172806) · Code: _n/a_

---

## 2024
### USENIX Security
- **WhisperFuzz: White-Box Fuzzing for Detecting and Locating Timing Vulnerabilities in Processors**     
  Paper: [USENIX link](https://www.usenix.org/conference/usenixsecurity24/presentation/borkar) · Artifact: [zenodo vulnerability artifact](https://zenodo.org/records/14166394)


### DAC
- **PathFuzz: Broadening Fuzzing Horizons with Footprint Memory for CPUs**   
  Paper: [DAC link](https://61dac.conference-program.com/presentation/?id=RESEARCH419&sess=sess136) · Code: [OpenXiangShan/xfuzz](https://github.com/OpenXiangShan/xfuzz)


### DATE
- **Beyond Random Inputs: A Novel ML-Based Hardware Fuzzing**  
  Paper: [arXiv link](https://arxiv.org/abs/2404.06856) · Code: _n/a_

- **MABFuzz: Multi-Armed Bandit Algorithms for Fuzzing Processors**  
  Paper: [IEEE link](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10546726) · Code: _n/a_

- **SSFuzz: Generating syntactic and semantic seeds for RISC-V processors**  
  Paper: [ACM link](https://dl.acm.org/doi/10.1145/3649476.3658712) · Code: _n/a_
  iie.

- **FormalFuzzer: Formal Verification Assisted Fuzz Testing for SoC Vulnerability Detection**   
  Paper: [IEEE link](https://ieeexplore.ieee.org/abstract/document/10473911) · Code: _n/a_


###  Others
- **The Emergence of Hardware Fuzzing: A Critical Review of its Significance**  
  Paper: [arXiv link](https://arxiv.org/abs/2403.12812) · Code: _n/a_

- **Fuzzerfly Effect: Hardware Fuzzing for Memory Safety**  
  Paper: [IEEE link](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10462151) · Code: _n/a_

---

## 2025
### USENIX
- **Encarsia: Evaluating CPU Fuzzers via Automatic Bug Injection**  
  Paper: [USENIX link](https://www.usenix.org/conference/usenixsecurity25/presentation/bolcskei) · Code: [comsec-group/encarsia](https://github.com/comsec-group/encarsia)


### ASPLOS
- **DejaVuzz: Disclosing Transient Execution Bugs with Dynamic Swappable Memory and Differential Information Flow Tracking assisted Processor Fuzzing**   
  Paper: [arXiv link](https://arxiv.org/abs/2504.20934) · Code: [sycuricon/DejaVuzz](https://github.com/sycuricon/DejaVuzz)

### MICRO
- **SymbFuzz: Symbolic Execution Guided Hardware Fuzzing**   
  Paper: [ACM link](https://dl.acm.org/doi/10.1145/3725843.3756131)· Code: _n/a_
  co-sim: 基于uvm，虽然和前面的不太一样，但没什么好说的
  driver: 用smt生成CFG树，也就是if分支判断树，去判断不同条件下变量的赋值情况，当生成的激励产生的变量值稳定后，如果还有CFG树分支没有执行过，就会顺着CFG树去找赋值情况，并提供激励来覆盖到。

### GLSVLSI
- **Bridging the Gap between Hardware Fuzzing and Industrial Verification**  
  Paper: [arXiv link](https://arxiv.org/abs/2506.00461) · Code: [magicYang1573/fast-hw-fuzz](https://github.com/magicYang1573/fast-hw-fuzz)
  基于verilator做了一个fuzz的性能优化：覆盖率是直接改verilator拿到的（代替与vcs进程通讯），Mutation是用简化的AFL（仅实现了这两个操作：havoc（随机修改字节值）和 splice（两个染色体交叉）），仿真并行化

- **Microarchitecture Evaluation Framework for Transient Execution Attack Vulnerability: Metrics, Fuzzing, and Sensitivity Analysis**
  Paper: [ACM Link](https://dl.acm.org/doi/10.1145/3716368.3735225) · Code: _n/a_

### Computers & Security
- **HScheduler: An execution history-based seed scheduling strategy for hardware fuzzing**  
  Paper: [Elsevier link](https://www.sciencedirect.com/science/article/abs/pii/S0167404825001671) · Code: _n/a_
  
### ICASSP
- **FeedbackFuzz: Fuzzing Processors via Intricate Program Generation with Feedback Engine**   
  Paper: [IEEE link](https://ieeexplore.ieee.org/document/10889404) · Code: _n/a_

### ???
- **FuSS: Coverage-Directed Hardware Fuzzing with Selective Symbolic Execution**
  Paper: [ACM link](https://dl.acm.org/doi/10.1145/3760529) · Code: _n/a_

---

## Related
- **Recent Papers Related To Fuzzing (repo)**   
  Repo: [wcventure/FuzzingPaper](https://github.com/wcventure/FuzzingPaper)

## Courses
|  Name   |  code   |
|-------|-------|
| [Design Verification](https://uobdv.github.io/Design-Verification/) | COMS30026 |
| [Secure Hardware Design](https://shd.mit.edu/2024/) | 6.5950/6.5951 (Previously [6.S983](csg.csail.mit.edu/6.S983/) and 6.888) |
| [One Student One Chip](https://ysyx.oscc.cc/docs/en/) | UCAS |

