# ASIC Design Class
<details>
  
<summary>Lab 1: Compiling a small C program with gcc compiler and RISCV gcc compiler </summary>

## Lab 1A: Compiling a C program with gcc compiler, execute it and generate the output.

Write the C code in a file using any text editor and save it as sum1ton.c (source code).

Next, compile the source code using gcc compiler, this will generate the executable code.

Now, run the executable code to see the output.

Following image includes the source code and three commands to execute in terminal in sequence as shown, to generate the output.

![4-final](https://github.com/user-attachments/assets/aee6f573-d616-460f-8f7b-94fd9fad46fd)

## Lab 1B: Compiling a C program with RISCV gcc compiler, execute it, generate the output and compare with the output of Lab 1B.

The next task is to compile the sum1ton.c using RISCV gcc compiler using the command in following image, also to see the assembly code for C program, use the next command.

![1b-obj-dump1](https://github.com/user-attachments/assets/53cb974a-bced-4388-ab5f-b62bd0a68919)


Observe that object code dump generates the following, main function is present at location 10184 and 15 instructions are present in assembly code.

![1b-obj-dump](https://github.com/user-attachments/assets/1266eeb0-1246-483b-802b-da78ad867e37)

Next, try 0fast of RISCV compiler for same C code and observe the object code dump, now the main function is located at 100b0 and number of instructions present is 12.

![1b-obj-dump2-command](https://github.com/user-attachments/assets/6f62164f-66f3-4e5a-8249-0b21a8bd5a2c)

![1b-obj-dump2](https://github.com/user-attachments/assets/7c33319c-1092-4b76-924d-84d49bf7e8b3)

</details>

<details> 
  <summary>Lab 2: Simulating and degbugging c program with Spike RISC-V ISA Simulator </summary>

  ## Lab 2
</details>

<details>
  <summary>Lab 3: Write a C program for Gaussian elimination algorithm and run it on gcc and RISCV gcc </summary>

  ## Lab 3

  ![gauss](https://github.com/user-attachments/assets/fe01afaf-3f2b-4456-a40d-395f784dec01)

  ![gauss1](https://github.com/user-attachments/assets/d5ecafc7-a5fa-4429-aeff-b8996770a61a)

</details>

<details>
  <summary>Lab 4: TL Verilog, Makerchip IDE, Build a 5 stage pipelined RISCV processor </summary>

  ## Lab 4

Implementing a combinational circuit in TLV : Four function calculator using multiplexer

![Calculator](https://github.com/user-attachments/assets/eb6fe03f-6ede-40d0-8891-e71654a95171)

RISCV Block diagram - To be implemented in TLV, blockwise

![riscv-Block_diagram](https://github.com/user-attachments/assets/75ec57fe-8ce8-44a6-9420-d7f8b1a4d36a)

Program Counter

![programcounter](https://github.com/user-attachments/assets/6d40c0d7-7ff1-4188-b3d4-351ad8ad5e39)

Instruction Fetch

![instruction fetch](https://github.com/user-attachments/assets/3b64fcbd-14fe-4529-9671-5f107e60235f)

Instruction Decode

![instruction decode1](https://github.com/user-attachments/assets/c70d0629-28ea-468e-a498-a3183eabe908)

ALU

![alu](https://github.com/user-attachments/assets/c887fa03-efd4-4b3b-a0fb-8199e8871718)


Register Read

![reg_rd](https://github.com/user-attachments/assets/36c042aa-1a80-4095-92b2-2a25dfa68ee5)

Register Write

![reg_wr](https://github.com/user-attachments/assets/be815086-96ed-4599-81e1-173bb7b51b36)

Branching

![branching](https://github.com/user-attachments/assets/d77ccf7a-192a-4b76-ba59-4891b0931dd6)

RISCV implementation, combined cpu using above blocks.

![Diagram](https://github.com/user-attachments/assets/194d1d52-96ab-4a7f-8bd3-7a158e1406f1)

Following shows the clock and reset signals in waveform.

![clk](https://github.com/user-attachments/assets/cf192530-3d34-401d-b0a8-3cb1ffa9853f)

![reset_signal](https://github.com/user-attachments/assets/c21dba93-e09d-4419-bd75-595a3cc0562e)

The final sum getting accumulated with each cycle can be seen as following.

![final sum accumulation](https://github.com/user-attachments/assets/2d354c34-2718-49ac-a8df-572f430dd3ae)










</details>


