### Foreshadow
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