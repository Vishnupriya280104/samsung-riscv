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
![objdump_1](https://github.com/user-attachments/assets/b8af8978-1824-4cbd-aa05-1075defec872)
**Type:** U-type    
**Breakdown:**   
**Immediate** (imm[31:12]): 0x21 → Binary: 0000000000100001.  
**Destination Register** (rd): a0 = x10 → Binary: 01010.   
**Opcode**: lui → Binary: 0110111.   
**32-bit Binary Representation:** 0000000000100001 01010 0110111   
**Hexadecimal Representation:** 0x0021537  
#### Machine code for addi sp, sp, -16  
![objdump_2](https://github.com/user-attachments/assets/092e4a26-cd18-40a7-80e5-1fc6a9bf722e)  
**Type:** I-type  
**Breakdown:**   
**Immediate** (imm[11:0]): -16 → Two's complement: 111111110000.  
**Source Register** (rs1): sp = x2 → Binary: 00010.  
**Destination Register** (rd): sp = x2 → Binary: 00010.  
**Function Code** (funct3): addi → Binary: 000.   
**Opcode:** addi → Binary: 0010011.   
**32-bit Binary Representation:** 111111110000 00010 000 00010 0010011   
**Hexadecimal Representation:** 0xFF010113  
#### Machine code for li a2,100   
![objdump_3](https://github.com/user-attachments/assets/f474d41a-1c07-498c-9522-47b48a6737c0)   
**Expanded Form:** li is equivalent to addi a2, x0, 100.  
**Type:** I-type  
**Breakdown:**  
**Immediate** (imm[11:0]): 100 → Binary: 000001100100.   
**Source Register** (rs1): x0 → Binary: 00000.  
**Destination Register** (rd): a2 = x12 → Binary: 01100.  
**Function Code** (funct3): addi → Binary: 000.  
**Opcode:** addi → Binary: 0010011.  
**32-bit Binary Representation:** 000001100100 00000 000 01100 0010011  
**Hexadecimal Representation:** 0x06400613  
#### Machine code for li a1, 10  
![objdump_4](https://github.com/user-attachments/assets/d03bb739-3cac-422c-bd53-ef0c43b2ea28)  
**Expanded Form:** li is equivalent to addi a1, x0, 10.  
**Type:** I-type  
**Breakdown:**  
**Immediate** (imm[11:0]): 10 → Binary: 000000001010.  
**Source Register** (rs1): x0 → Binary: 00000.   
**Destination Register** (rd): a1 = x11 → Binary: 01011.   
**Function Code** (funct3): addi → Binary: 000.   
**Opcode:** addi → Binary: 0010011.   
**32-bit Binary Representation:** 000000001010 00000 000 01011 0010011   
**Hexadecimal Representation:** 0x00A00593   
#### Machine code for addi a0, a0, 384  
![objdump_5](https://github.com/user-attachments/assets/ccb6e763-18ce-4344-a372-1748ffd6045c)   
**Type:** I-type   
**Breakdown:**   
**Immediate** (imm[11:0]): 384 → Binary: 000110000000.  
**Source Register** (rs1): a0 = x10 → Binary: 01010.  
**Destination Register** (rd): a0 = x10 → Binary: 01010.   
**Function Code** (funct3): addi → Binary: 000.   
**Opcode:** addi → Binary: 0010011.   
**32-bit Binary Representation:** 000110000000 01010 000 01010 0010011   
**Hexadecimal Representation:** 0x18050513  
#### Machine code for sd ra, 8(sp)  
![objdump_6](https://github.com/user-attachments/assets/8a81df5e-07e1-41a0-8fbd-e7fd1bb865db)  
**Type:** S-type  
**Breakdown:**  
**Immediate** (imm[11:5|4:0]): 8 → Binary: 0000000001000.  
**Split**: imm[11:5] = 0000000, imm[4:0] = 01000.  
**Source Register** (rs2): ra = x1 → Binary: 00001.  
**Source Register** (rs1): sp = x2 → Binary: 00010.  
**Function Code** (funct3): sd → Binary: 011.  
**Opcode:** sd → Binary: 0100011.  
**32-bit Binary Representation:** 0000000 00001 00010 011 01000 0100011  
**Hexadecimal Representation:** 0x00113423    
#### Machine code for jal ra, 10408  
![objdump_7](https://github.com/user-attachments/assets/f73075a7-df1a-4115-b42f-4492d4e0ef56)  
**Type:** J-type  
**Breakdown:**  
**Immediate** (imm[20|10:1|11|19:12]):  
**Immediate value**: 10408 → Binary: 001010001000.  
**Break this into J-type fields**:  
imm[20]: 0  
imm[10:1]: 0100010000  
imm[11]: 0  
imm[19:12]: 00101000  
**Destination Register** (rd): ra = x1 → Binary: 00001.  
**Opcode:** jal → Binary: 1101111.  
**32-bit Binary Representation:** 0 0100010000 0 00101000 00001 1101111  
**Hexadecimal Representation:** 0x34000EF  
#### Machine code for ld ra, 8(sp)  
![objdump_8](https://github.com/user-attachments/assets/8cebe23e-3241-4956-9ed3-f6195887fceb)  
**Type:** I-type   
**Breakdown:**  
**Immediate** (imm[11:0]): 8 → Binary: 00000001000.  
**Source Register** (rs1): sp = x2 → Binary: 00010.  
**Destination Register** (rd): ra = x1 → Binary: 00001.  
**Function Code (funct3)**: ld → Binary: 011.  
**Opcode:** ld → Binary: 0000011.  
**32-bit Binary Representation:** 00000001000 00010 011 00001 0000011    
**Hexadecimal Representation:** 0x00813083  
#### Machine code for li a0, 0  
![objdump_9](https://github.com/user-attachments/assets/a6ad9f90-2f95-49b1-972a-9bc5c7155909)  
**Expanded Form:** li is equivalent to addi a0, x0, 0.  
**Type:** I-type  
**Breakdown:**   
**Immediate** (imm[11:0]): 0 → Binary: 000000000000.  
**Source Register** (rs1): x0 → Binary: 00000.  
**Destination Register** (rd): a0 = x10 → Binary: 01010.  
**Function Code** (funct3): addi → Binary: 000.  
**Opcode:** addi → Binary: 0010011.  
**32-bit Binary Representation:** 000000000000 00000 000 01010 0010011   
**Hexadecimal Representation:** 0x00000513   
#### Machine Code for addi sp, sp, 16  
![objdump_10](https://github.com/user-attachments/assets/9ab2a57b-ec5e-4c32-ad5b-4a02c57f5b2f)   
**Type:** I-type  
**Breakdown:**  
**Immediate** (imm[11:0]): 16 → Binary: 000000010000.  
**Source Register** (rs1): sp = x2 → Binary: 00010.  
**Destination Register** (rd): sp = x2 → Binary: 00010.  
**Function Code** (funct3): addi → Binary: 000.  
**Opcode:** addi → Binary: 0010011.  
**32-bit Binary Representation:** 000000010000 00010 000 00010 0010011  
**Hexadecimal Representation:** 0x01010113  
#### Machine code for ret  
![objdump_11](https://github.com/user-attachments/assets/2ee08002-3a0e-4d6f-9899-b14228b09206)   
**Expanded Form:** ret is equivalent to jalr x0, ra, 0.  
**Type:** I-type    
**Breakdown:**  
**Immediate** (imm[11:0]): 0 → Binary: 000000000000.  
**Source Register** (rs1): ra = x1 → Binary: 00001.  
**Destination Register** (rd): x0 → Binary: 00000.  
**Function Code** (funct3): jalr → Binary: 000.  
**Opcode:** jalr → Binary: 1100111.  
**32-bit Binary Representation:** 000000000000 00001 000 00000 1100111  
**Hexadecimal Representation:** 0x00008067  
#### Machine code for auipc a5, 0xfffff0  
![objdump_12](https://github.com/user-attachments/assets/77c47ad1-1614-4558-b4f0-8ea80ed3ef17)   
**Type:** U-type  
**Breakdown:**  
**Immediate** (imm[31:12]): 0xfffff0 → Binary: 111111111111111111110000.    
**Destination Register** (rd): a5 = x15 → Binary: 01111.     
**Opcode:** auipc → Binary: 0010111.   
**32-bit Binary Representation:** 111111111111111111110000 01111 0010111  
**Hexadecimal Representation:** 0xfffff097     
#### Machine code for addi a5, a5, -220  
![objdump_13](https://github.com/user-attachments/assets/d698b917-c88a-40ee-baf3-4cf69344f50d)  
**Type:** I-type  
**Breakdown:**   
**Immediate** (imm[11:0]): -220 → Two's complement: 111100110100.     
**Source Register** (rs1): a5 = x15 → Binary: 01111.  
**Destination Register** (rd): a5 = x15 → Binary: 01111.  
**Function Code** (funct3): addi → Binary: 000.  
**Opcode:** addi → Binary: 0010011.  
**32-bit Binary Representation:** 111100110100 01111 000 01111 0010011  
**Hexadecimal Representation:** 0xf2478793    
#### Machine code for beqz a5, 100f4 <register_fini+0x18>  
![objdump_14](https://github.com/user-attachments/assets/862a0530-cc68-4678-8997-4b840d36d244)  
**Expanded Form:** beqz is equivalent to beq a5, x0, offset.   
**Type:** B-type   
**Breakdown:**  
**Immediate** (imm[12|10:5|4:1|11]):   
**Offset to target:** 100f4 - 100dc = 0x18 → Binary: 00000000011000.   
**Fields:**   
imm[12]: 0   
imm[10:5]: 000000   
imm[4:1]: 1100  
imm[11]: 0  
**Source Registers:**  
rs1: a5 = x15 → Binary: 01111.  
rs2: x0 → Binary: 00000.    
**Function Code** (funct3): beq → Binary: 000.      
**Opcode:** beq → Binary: 1100011.   
**32-bit Binary Representation:** 0 000000 01100 01111 000 00000 1100011     
**Hexadecimal Representation:** 0x00007863  
#### Machine code for auipc a0, 0x0  
![objdump_15](https://github.com/user-attachments/assets/6bb7138e-3379-436f-97c4-2c2ce75c767a)  
**Type:** U-type  
**Breakdown:**   
**Immediate** (imm[31:12]): 0x0 → Binary: 000000000000.  
**Destination Register** (rd): a0 = x10 → Binary: 01010.  
**Opcode:** auipc → Binary: 0010111.     
**32-bit Binary Representation:** 000000000000 01010 0010111  
**Hexadecimal Representation:** 0x00000517  



