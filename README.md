# RISC-V Talent Development Program, powered by Samsung Semiconductor India Research (SSIR) along with VLSI System Design (VSD)
The program is designed to empower participants with cutting-edge knowledge and skills, catering to the rapidly growing semiconductor industry. It is an initiative by Samsung Semiconductor India Research in collaboration with VLSI System Design (VSD).

## Basic Details
**Name:** Vishnupriya V  
**College:** RV Institute of Technology and Management  
**E-mail:** rvit22bec050.rvitm@rvei.edu.in  
**Linkedln Profile:** https://www.linkedin.com/in/vishnupriya-v-213b282a5/  
**GitHub Profile:** https://github.com/Vishnupriya280104

### Task 1
Task is to install the RISC-V toolchain using the VDI link and perform C based lab and RISC-V based lab
### Task 2
Task is to Compile the C program using RISC-V GCC/SPIKE and observe the performance under the -O1 and -Ofast compiler optimization flags, and to generate and collect the RISC-V object dump for both -O1 and -Ofast.
### Task 3
Decoding RISC-V Instructions: A Visual Guide
#### Instruction Types
**R-type:** Register type
**I-type:** Immediate type
**S-type:** Store type
**B-type:** Branch type
**U-type:** Upper immediate type
**J-type:** Jump type
#### Machine code for lui a0, 0x21
!![objdump_1](https://github.com/user-attachments/assets/b8af8978-1824-4cbd-aa05-1075defec872)

**Type:** U-type
**Breakdown:**
**Immediate** (imm[31:12]): 0x21 → Binary: 0000000000100001.
**Destination Register** (rd): a0 = x10 → Binary: 01010.
**Opcode**: lui → Binary: 0110111.

