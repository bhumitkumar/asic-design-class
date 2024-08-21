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
</details>
## Lab 2
<details>
  <summary>Lab 3: Write a C program for Gaussian elimination algorithm and run it on gcc and RISCV gcc </summary>
</details>
## Lab 3
<details>
  <summary>Lab 4: TL Verilog, Makerchip IDE, Build a 5 stage pipelined RISCV processor </summary>
</details>
## Lab 4
Implementing a combinational circuit in TLV : Four function calculator using multiplexer

![Calculator](https://github.com/user-attachments/assets/eb6fe03f-6ede-40d0-8891-e71654a95171)
