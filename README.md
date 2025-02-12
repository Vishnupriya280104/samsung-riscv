# RISC-V Talent Development Program, powered by Samsung Semiconductor India Research (SSIR) along with VLSI System Design (VSD)
The program is designed to empower participants with cutting-edge knowledge and skills, catering to the rapidly growing semiconductor industry. It is an initiative by Samsung Semiconductor India Research in collaboration with VLSI System Design (VSD).

## Basic Details
**Name:** Vishnupriya V  
**College:** RV Institute of Technology and Management  
**E-mail:** rvit22bec050.rvitm@rvei.edu.in  
**Linkedln Profile:** https://www.linkedin.com/in/vishnupriya-v-213b282a5/  
**GitHub Profile:** https://github.com/Vishnupriya280104

### Task 1
<details>
  <summary>Task 1: Task is to install the RISC-V toolchain using the VDI link and perform C based lab and RISC-V based lab</summary>       
  
  **Ubuntu Installation**
  
![ubuntu_installation](https://github.com/user-attachments/assets/4751bdbc-7872-46a5-9b62-eb360a130b2e)
     
  **Compiling and running a RISC-V program using GCC**      
  
![riscv64](https://github.com/user-attachments/assets/8f58719c-4ba2-420e-8cdc-3a69251a0ca8)     
  
  **Analyzing the effect of -O1 optimization in RISC-V program**   
  
![riscv_O1](https://github.com/user-attachments/assets/c72ca528-2cee-48ae-a8e8-af1320e59d24)     
  
  **Analyzing the effect of -Ofast optimization in RISC-V program** 
  
![riscv_Ofast](https://github.com/user-attachments/assets/a5ef1181-6030-4d99-8b08-65ed5d3bdea9)     

  **Sum of numbers using C in leafpad file**
  
![sum_of_numbers_using_c](https://github.com/user-attachments/assets/b2c78484-7999-4f0f-b7b9-ded01512eb9e)       
</details>

### Task 2
<details>
  <summary>Task 2: Task is to Compile the C program using RISC-V GCC/SPIKE and observe the performance under the -O1 and -Ofast compiler optimization flags, and to generate and collect the RISC-V object dump for both -O1 and -Ofast.</summary>  
  
  **Sum of numbers using C in leafpad file**  
  
![sum_of_numbers_using_c](https://github.com/user-attachments/assets/fcd1d067-f886-4632-b827-cbbfbedd8f5d)  

  **Compiling and running a RISC-V program using Spike Simulator:**
  **Comparing O1 and Ofast**
  
![sum_spike_O1](https://github.com/user-attachments/assets/9c1838c9-88e8-4f4a-abec-37d756ac2060)

![sum_spike_Ofast](https://github.com/user-attachments/assets/e4cd1bc5-a73a-4430-8800-9b9ec07f1fe7)

  **Square of numbers using C in leafpad file**
  
![square_of number_using_c](https://github.com/user-attachments/assets/9e7a3c59-4c5e-41c7-a7b2-d56b3ed35748)

  **Compiling and running a RISC-V program using Spike Simulator:**
  **Comparing O1 and Ofast**
  
![square_spike_O1](https://github.com/user-attachments/assets/d77f9c18-116e-41a1-a886-1b9b3170a263)

![square_spike_Ofast](https://github.com/user-attachments/assets/fe6968df-0b17-4212-8023-d9f4a08ce54b)

</details>

### Task 3
<details>
  <summary>Task3: A Visual guide on decoding RISC-V instructions</summary>

### Instruction Types
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

</details>

### Task 4
<details>
  <summary>Task 4:  Task is to perform a functional simulation and observe the waveform</summary>

  **Functional simulatio of riscv**
  
![Functional simulatio of riscv](https://github.com/user-attachments/assets/b94c5472-d319-47ed-b37a-43b4cb8d90ea)

  **ADD**
  
![add](https://github.com/user-attachments/assets/aeaccfe3-d707-48aa-98bd-d1062a6d32d4)
  
  **ADDI**
  
![addi](https://github.com/user-attachments/assets/f69f7716-2856-404d-a7ab-84815296d307)

  **AND**
  
![and](https://github.com/user-attachments/assets/c2c3bec3-c57e-49b3-8f56-55fd40528e00)
  
  **BEQ**
  
![beq](https://github.com/user-attachments/assets/4d85e92c-de59-4c72-b1a3-b764ed2d03fe)
  
  **BNE**
  
![bne](https://github.com/user-attachments/assets/7530286a-9f5a-4687-91d9-9740aabe1eb9)
  
  **GTKwave** 
  
![GTKwave](https://github.com/user-attachments/assets/c28c23da-7dbd-4d86-8654-e1ef53a88b50)
  
  **OR**
  
![or](https://github.com/user-attachments/assets/7fdb5c0a-7379-4975-91ac-c8936efc2d76)
  
  **SLL**
  
![sll](https://github.com/user-attachments/assets/b8a279a0-a54a-40c1-822e-ed8778358bba)
  
  **SLT**
  
![slt](https://github.com/user-attachments/assets/aae6680a-897c-446f-bd9c-2340d6ac75b2)
  
  **SUB**
  
![sub](https://github.com/user-attachments/assets/252511c1-4ebd-40dd-a30e-90f1376054a3)
  
  **XOR**
  
![xor](https://github.com/user-attachments/assets/e9b909cf-6d23-4dee-8b59-949f75534931)

</details>

### Task 5
<details>
  <summary>Task 5: Task is to implement a project using VSDSquadron Mini and check whether the building and uploading of C program file on RISCV processor works. </summary>

  **Overview:**  
  The home safety system showcased here introduces an innovative solution utilizing a VSD Squadron Mini Developement Board, an IR sensor, a piezo buzzer and a Servo Motor. It essentially comprises of a smart door lock using a keypad and a servo motor, and a burglar detection system using an IR sensor and piezo buzzer.  

  *If the password entered by the user on the keypad is correct, the servo motor opens the door to allow entry into the house.  
  *If the password entered is incorrect, the user is denied entry into the house and the door remains closed.  
  +If the door is closed and movement is detected in the house using the IR sensor, the piezo buzzer alarms the home owner that there is a potential burglar who has brached into the house.  
  +If the password is entered correctly and the door is open, the IR sensor is switched off to avoid wrong detection.  

  **Components Required:**  
  -VSD Squadron Mini developement board with CH32V003F4U6 chip with 32-bit RISC-V core based on RV32EC instruction set  
  -IR sensor  
  -Keypad  
  -Servo motor  
  -Piezo buzzer  
  -Breadboard  
  -Jumper Wires  
  
</details>
 




