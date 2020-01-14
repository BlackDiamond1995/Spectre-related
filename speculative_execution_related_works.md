### Context-Sensitive Fencing
alplos 2019  
Context-Sensitive Fencing: Securing Speculative
Execution via Microcode Customization
* a mechanism that leverages a dynamic decoding architecture to inject fences between control flow and loads, without
recompilation or binary translation
* a simple dynamic mechanism that eliminates redundant (per basic block) fences
* a decode-level branch predictor isolation technique that mitigates branch mis-training
variants of Spectre
***

### SpectreGuard
DAC 2019  
SpectreGuard: An Efficient Data-centric Defense Mechanism against Spectre Attacks
* a novel data-centric defense approach
* focusing on secret data, rather than code
* on gem5 full system simulator and Linux kernel
* a table of known speculative execution attacks
***

### DAWG
MICRO 2018  
DAWG: A Defense Against Cache Timing Attacks in Speculative Execution Processors
* demonstrating that the replacement policy can leak information in a way-partitioned cache
* a cache way partitioning scheme, DAWG, with strong isolation properties that blocks attacks based on the cache state exfiltration channel
* illustrate the limitations of cache partitioning for isolation
***

### InvisiSpec
MICRO 2018  
InvisiSpec: Making Speculative Execution Invisible in the Cache Hierarchy
* a generalization of speculative execution attacks where any speculative load may pose a threat
* Under TSO, using fences to defend against Spectre attacks slows down execution by 74% relative to a conventional, insecure processor; InvisiSpec reduces the execution slowdown to only 21%
* Using fences to defend against futuristic attacks slows down execution by 208%; InvisiSpec reduces the slowdown to 72%
***

### Efficient Invisible Speculative Execution through Selective Delay and Value Prediction
ISCA 2019  
Efficient Invisible Speculative Execution through Selective Delay and Value Prediction
* delay speculative loads until they are non-speculative, preventing any speculative side-effects from happening
* limit the eager delay solution only to loads that miss in the L1 cache
* Value Predicting Delayed Loads: We augment the delayon-miss solution with a value predictor (VP), enabling L1 misses to execute using a predicted value.
***

### CleanupSpec
MICRO 2019
CleanupSpec: An “Undo” Approach to Safe Speculation
* Rollback changes to L1 efficiently.
* Invalidate changes to the Randomized L2/LLC.
* Randomize replacement policy for L1.
* Delay changes to coherence state in remote cache.
***

### MI6
MICRO 2019  
MI6: Secure Enclaves in a Speculative Out-of-Order Processor
* there are many subtle side channels associated
with queues and associated arbitration required to handle
multiple outstanding memory requests in the memory hierarchy
* describe how to enforce strong isolation in such systems
* by using a new purge instruction, the complexity of the out-of-order processor core can be completely decoupled from the complexity of a modern memory hierarchy
* optimizations based on indistinguishability to software in our purge implementation
* key modifications to the security monitor to maintain strong isolation in a speculative processor
* an optimization relating to access permissions checking
* security comes at the cost of approximately 16.4% average slowdown for protected programs
***

### NDA
MICRO 2019  
NDA: Preventing Speculative Execution Attacks at Their Source
* introduce a speculative-execution-attack taxonomy based on how attacks induce wrong-path execution
* NDA, a new technique to control speculative data propagation in out-of-order processors to defeat speculative execution attacks
* multiple variants with differing security/performance tradeoffs
***

### Speculative Taint Tracking
MICRO 2019  
Speculative Taint Tracking (STT): A Comprehensive Protection
for Speculatively Accessed Data
* open source https://github.com/cwfletcher/stt
* provide a comprehensive study of covert channels on
speculative microarchitectures
* propose a general framework for preventing speculatively accessed data from leaking over any covert channel
* propose a novel scheme to quickly disable protection on
flows of data, once the data’s producer access instruction(s)
becomes non-speculative
* it adds only 8.5%/14.5% overhead
***

### SPECCFI
SP 2020  
SPECCFI: Mitigating Spectre Attacks using CFI Informed Speculation
* present a new defense against Spectre variants that rely on polluting the BTB and RSB, by embedding CFI principles into the branch prediction decisions
* it leads to little overhead
***

### SpecShield
PACT 2019  
SpecShield: Shielding Speculative Data from Microarchitectural Covert Channels
* Proposes a microarchitectural framework for eliminating transient execution attacks which grant access to arbitrary memory
* the first general solution addressing speculative data-flow within the pipeline
***

### 
DAC2019 SafeSpec
SafeSpec: Banishing the Spectre of a Meltdown with Leakage-Free Speculation
* separating speculative state into separate structures
* identify a new class of speculative attacks (Transient Speculation Attacks)

<!-- ### Foreshadow
USENIX‘18  
Foreshadow: Extracting the Keys to the Intel SGX Kingdom with Transient Out-of-Order Execution
***

### SgxPectre Attacks
arXiv’18  
SgxPectre Attacks: Stealing Intel Secrets from SGX Enclaves via Speculative Execution
***

### A Systematic Evaluation of Transient Execution Attacks and Defenses
USENIX‘19  
A Systematic Evaluation of Transient Execution Attacks and Defenses
* We systematize Spectre- and Meltdown-type attacks, advancing attack surface understanding, highlighting misclassifications, and revealing new attacks. 
* We provide a clear distinction between Meltdown/Spectre, required for designing effective countermeasures. 
* We provide a classification of gadgets and discuss their prevalence in real-world software.
* We categorize defenses and show that most, including deployed ones, cannot fully mitigate all attack variants.
* We describe new branch mistraining strategies, highlighting the difficulty of eradicating Spectre-type attacks
***

### NetSpectre
ESORICS 2019  
NetSpectre: Read Arbitrary Memory over Network
* the first fully remote Spectre attack
* We present the first access-driven remote cache attack (Evict+Reload) and the first remote Spectre attack.
* We demonstrate the first Spectre attack which does not use the cache but a new and fast AVX-based covert channel.
* We use simpler Spectre gadgets in remote ASLR breaks.
***

### BranchScope
ASPLOS'18  
BranchScope: A New Side-Channel Attack on Directional Branch Predictor
* the first fine-grained attack on the directional branch predictor
* BranchScope is not affected by defenses against BTB-based attacks.
* BranchScope works reliably and efficiently from user space across three generations of Intel processors in the presence of system noise.
* Providing branch prediction units that are secure to side channel attacks. -->