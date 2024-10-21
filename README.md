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

<details> 
  <summary>Lab 5: TL Verilog to Verilog conversion using Sandpiper and testing the converted Verilog based riscvcore </summary>

  ## Lab 5

In Lab 4, in makerchip, riscvcore is built using TL Verilog, it generates tlv file. The tlv file generated in Lab4 is given to Sandpiper converter to generate verilog code.
In Lab 5, task is to match the output waveforms generated on makerchip and those generated by gtkwave after running testbench.

Following image shows the verilog generated by Sandpiper being compiled by iverilog and output waveform can be seen in next image on gtkwave.
  
![verilog2gtk](https://github.com/user-attachments/assets/d543c283-870b-439a-b0de-f03c10e96ba4)

Clock name is clk_bhu(makechip) and clk_bhu1(gtkwave) and sum can be seen in out which matches the output of makerchip in lab 4 which was generated by TL Verilog riscvcore.
1. Makerchip waveforms - click on image to open in new tab for clear view of waveforms.

Clock signal - clk_bhu

![clk](https://github.com/user-attachments/assets/cf192530-3d34-401d-b0a8-3cb1ffa9853f)

Reset signal

![reset_signal](https://github.com/user-attachments/assets/c21dba93-e09d-4419-bd75-595a3cc0562e)


Final sum
![final sum accumulation](https://github.com/user-attachments/assets/2d354c34-2718-49ac-a8df-572f430dd3ae)

2. gtkwave waveforms - clk_bhu1, out sum
   
!![gtkwave](https://github.com/user-attachments/assets/82550bb5-2acb-463a-af06-02e595b4503d)

</details>

<details> 
  <summary>Lab 6: Simulating Riscv-core with PLL and DAC, Yosys installation. </summary>

  ## Lab 6

  In Lab 5, riscv core was compiled in iverilog and program to sum 1 to 9 was shown working with output seen in gtkwave.
  In lab 6, with riscv core, DAC and PLL are added and the output of sum of numbers can be seen with its analog equivalent.

![asic_update](https://github.com/user-attachments/assets/8fdc4563-2ad2-4c29-8ec1-5ad71f925b72)


Yosys installation for next lab.
![yosys](https://github.com/user-attachments/assets/f2cab8b4-cb77-4668-823a-aac0e0ba37d3)

</details>

<details>
<summary>Lab 7: RTL design using Verilog with SKY130 Technology </summary>
  
## Lab 7
1 - Introduction to Verilog RTL design and Synthesis

![0 Screenshot from 2024-10-21 16-18-21](https://github.com/user-attachments/assets/096a7ff9-d3ef-4fed-9622-7244788a47e4)

In above figure, the central block is design, which consists of verilog code written as per specification for desired functionality.

To test whether the desired fuctionality is achieved, we need testbench which contains verilog code to generate set of stimulus and for given stimulus corresponding code for observer. Testbench also contains timing information related to running of simulation.

To perform above tasks, we use iverilog compiler and gtkwave waveform viewer as shown in following figure
![1 Screenshot from 2024-10-21 16-18-47](https://github.com/user-attachments/assets/6da79ef2-ee32-4cb6-b229-3e5516dabfae)

Following example shows a simple design of mux and corresponding testbench.
To run the verilog code in iverilog, and view waveforms in gtkwave, run the following three commands sequentially,
![image](https://github.com/user-attachments/assets/bda941fb-c0c7-43ed-81b9-ee77f735da20)

Mux module
```
module good_mux (input i0 , input i1 , input sel , output reg y);
always @ (*)
begin
	if(sel)
		y <= i1;
	else 
		y <= i0;
end
endmodule
```
Testbench for mux module
```
`timescale 1ns / 1ps
module tb_good_mux;
// Inputs
reg i0,i1,sel;
// Outputs
wire y;
// Instantiate the Unit Under Test (UUT), name based instantiation
	good_mux uut (.sel(sel),.i0(i0),.i1(i1),.y(y));
	//good_mux uut (sel,i0,i1,y);  //order based instantiation
initial begin
	$dumpfile("tb_good_mux.vcd");
	$dumpvars(0,tb_good_mux);
	// Initialize Inputs
	sel = 0;
	i0 = 0;
	i1 = 0;
	#300 $finish;
end
always #75 sel = ~sel;
always #10 i0 = ~i0;
always #55 i1 = ~i1;
endmodule
```
## Yosys and Logic synthesis

Yosys is a logic/RTL synthesis software suite which converts verilog, represented by Design block into netlist as shown in following diagram.

The block shown as .lib contains standard library cells which are present in pdk.

To perform synthesis, yosys needs commands as read_verilog, read_verilog, write_verilog.

![image](https://github.com/user-attachments/assets/8c0ea0b6-4835-4fb0-a8fd-c838036a9eed)

Once netlist is generated, it needs to be verified, for that it is run through iverilog, output vcd file is generated, which is run through gtkwave.

![image](https://github.com/user-attachments/assets/91c62c0e-883b-4425-97e4-eb01ff193e46)

Following command loads the liberty file containing standard cells, as shown, 418 cells types are imported,
![image](https://github.com/user-attachments/assets/00e054c8-5378-4c0a-878c-ce58171e8a5b)

Next, using read_verilog, we generated RTL for given design,
![image](https://github.com/user-attachments/assets/ecc37670-2191-42eb-b4a1-87842a62bcf1)

Following command is used for synthesis of top module
![image](https://github.com/user-attachments/assets/23e97d6d-b672-484d-9112-7e9d7189faa8)

Following command generates the netlist,
![image](https://github.com/user-attachments/assets/86e6ce95-0521-45ed-8d04-2383d48ed888)

![image](https://github.com/user-attachments/assets/c30129e8-3b96-4d4a-8747-fb0437b63fab)

Showing RTL design
![image](https://github.com/user-attachments/assets/def3ddaf-b6a2-47cd-886e-e9317c68ae47)

Next write netlist which can be used for simulation,
![image](https://github.com/user-attachments/assets/61bb5247-3b37-4d8f-b155-e428b1e471b9)

The generated netlist is as follows
![image](https://github.com/user-attachments/assets/d6b86354-2694-4d00-9b88-bbe2ed12bfe1)


2 - Timing libs, hierarchical vs flat synthesis and efficient flop coding styles

3 - Combinational and sequential optmizations

4 - Gate level synthesis, blocking vs non-blocking statements and Synthesis-Simulation mismatch

</details>
