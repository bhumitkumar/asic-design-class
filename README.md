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


2 - (a) Timing libs, (b) hierarchical vs flat synthesis and (c) efficient flop coding styles

liberty file contains information about standard cells such as, timing, power, area parameters. Also, multiple forms of same logic cell are available in standard cell library with different characteristics.

Whenever there are multiple modules are present in design, the netlist can be synthesised in either hierarchical form or as flat form.



3 - Combinational and sequential optmizations

1. 2 input AND gate<br>
Run the following commands sequentially to generate netlist<br>
yosys<br>
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
read_verilog opt_check2.v<br>
synth -top opt_check2<br>
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
opt_clean -purge<br>
show
![image](https://github.com/user-attachments/assets/23db51d8-ac89-4925-8b71-5a082e05830c)

2. 2 input OR Gate<br>
Run the following commands sequentially to generate netlist<br>
yosys<br>
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
read_verilog opt_check.v<br>
synth -top opt_check2<br>
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
opt_clean -purge<br>
show
![image](https://github.com/user-attachments/assets/f652c88a-4772-4cd9-95bc-d8efb544dfbe)

3. 3 input AND gate<br>
Run the command in similar manner as above with opt_check3.v
![image](https://github.com/user-attachments/assets/28f71953-ce71-4eb3-b0ac-1f141eb5f224)

4. 2 input XNOR
Run the command in similar manner as above with opt_check4.v
![image](https://github.com/user-attachments/assets/f91b12e9-e4e8-4033-8449-c8d8b8c1e577)

In case of multiple modules, flatten command needs to be used before generating netlist, otherwise it will show following error.

![Multiple module error Screenshot from 2024-10-21 22-15-42](https://github.com/user-attachments/assets/86d20872-a2e3-4587-ba0d-acdd2840e36b)

5. D Flipflop with asynchronour reset - active low
yosys
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog dff_const1.v
synth -top dff_const1
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
show
![image](https://github.com/user-attachments/assets/94981cc0-46af-4e19-bec9-81d3a1b9af4a)

6. D Flipflop with asynchronour reset - active high<br>

yosys<br>
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
read_verilog dff_const2.v<br>
synth -top dff_const2<br>
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
show<br>
![image](https://github.com/user-attachments/assets/0c874f0b-1ca6-449c-8bc4-a2f99936a802)

7. D Flipflop with asynchronour reset Design 3<br>

yosys<br>
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
read_verilog dff_const3.v<br>
synth -top dff_const3<br>
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
show<br>
![image](https://github.com/user-attachments/assets/cb08e78d-b451-4f44-9cdb-0999691b03d4)

8. D Flipflop<br>
yosys<br>
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
read_verilog dff_const4.v<br>
synth -top dff_const4<br>
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
show<br>
![image](https://github.com/user-attachments/assets/dab1c857-bf01-458f-a603-677c68679d79)

9. D Flipflop<br>
yosys<br>
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
read_verilog dff_const5.v<br>
synth -top dff_const5<br>
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
show<br>
![image](https://github.com/user-attachments/assets/be1cdd24-f731-4c3f-adf0-15ea3d5896d6)

10. Counter optimisation

yosys<br>
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
read_verilog counter_opt.v<br>
synth -top counter_opt<br>
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
show<br>
![image](https://github.com/user-attachments/assets/72a7e3aa-4f1d-48d4-a7ed-b548f254bafb)

11. Counter optimisation 2

yosys<br>
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
read_verilog counter_opt2.v<br>
synth -top counter_opt2<br>
dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
show<br>
![image](https://github.com/user-attachments/assets/b4808391-5a6d-4634-8ed1-9bdf9100d3bf)




4 - Gate level synthesis, blocking vs non-blocking statements and Synthesis-Simulation mismatch

Previously, RTL synthesis is carried out where netlist is generated from verilog code, which uses standard cells of pdk.
Observe that synthesised netlist and RTL verilog code are logically same. This netlist will contain for example and gate with input and output.
In gate level synthesis, abstract gates in synthesised netlist are replaced with gate level verilog models which can be functional models or timing aware models.

Once netlist generated after gate level synthesis, we need to do functional verification to remove synthesis-simulation mismatch. 
Some of the reasons for synthesis-simulation mismatch are, missing sensity list, block-non blocking assignments or non standard verilog code.

![image](https://github.com/user-attachments/assets/16d8171f-273f-490c-b92c-bb88783c242b)

1. 2x1 mux using ternary operator<br>
Compilation in iverilog<br>
![image](https://github.com/user-attachments/assets/380ad93e-06aa-4a67-ba39-c2f8eed39150)

Output of synthesis<br>
yosys<br>
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
read_verilog ternary_operator_mux.v<br>
synth -top ternary_operator_mux<br>
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
opt_clean -purge<br>
write_verilog -noattr ternary_operator_mux_net.v<br>
show<br>

![image](https://github.com/user-attachments/assets/2bb7cfa8-8720-4695-913d-05d3d7915c23)

2. Bad 2x1 mux

Output of synthesis<br>
yosys<br>
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
read_verilog bad_mux.v<br>
synth -top bad_mux<br>
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
opt_clean -purge<br>
write_verilog -noattr bad_mux_net.v<br>
!gvim bad_mux_net.v<br>
show<br>


![image](https://github.com/user-attachments/assets/69887389-d366-4fa3-aa0b-7ed76212316e)

3. Related to blocking statement
yosys<br>
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
read_verilog blocking_caveat.v<br>
synth -top blocking_caveat<br>
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib<br>
opt_clean -purge<br>
write_verilog -noattr blocking_caveat_net.v<br>
show<br>
![image](https://github.com/user-attachments/assets/57d0657e-6a38-4acf-a458-6712ec1f8deb)


Synthesis-simulation mismatch example
1. missing sensitivity list
2. for blocking and non blocking statements
   
</details>

<details>
  
<summary>Lab 8: Synthesis of riscv core, pll and dac using SKY130 pdk </summary>

## Comparision of Functional simulation output and Synthesised output.

### Output waveforms of functional simulation
![Screenshot from 2024-10-23 20-31-0935](https://github.com/user-attachments/assets/1f40ad8d-6bf3-41e8-8c12-dbac400ea077)

### Output waveforms of Synthesised verilog file

![Screenshot from 2024-10-23 20-37-574](https://github.com/user-attachments/assets/5c811dda-a056-43e5-829f-1df6e26a7566)


## Yosys stats related to synthesis

![image](https://github.com/user-attachments/assets/b5cfe879-f47d-4e91-81c7-ba5e02c4196f)
![image](https://github.com/user-attachments/assets/74656874-f86f-43b7-bdfc-e39d30bf060f)
![image](https://github.com/user-attachments/assets/ec9c3bfd-e393-4672-b6eb-1617978a21cd)

## Standard cells usage

![image](https://github.com/user-attachments/assets/227196f6-8acf-4f77-a933-7df7027d4453)
![image](https://github.com/user-attachments/assets/d8b5f250-7491-4920-a2e9-bb479eb65144)

</details>


<details>
  
<summary>Lab 9: Static Timing Analysis of design using OpenSTA </summary>

Static Timing analysis involves checking of design in terms of whether timing requirements are met for each path within the design.
The input to static timing analysis tool is the synthesised netlist generated, clock definations and other constraints related to input and output, it is independent of logic inputs.

![image](https://github.com/user-attachments/assets/78a7b014-56c6-4971-9dd0-43fdef8eeb64)

source: https://www.vlsisystemdesign.com/static-timing-analysis-sta/

STA tool breaks down the whole design into different path and check whether the delay present in signal propogation is not creating issue in correct functioning of the design.

Two of the most common timing constraints in design are setup time and hold time constraints. When static timing analysis is performed, STA tool reports whether these timing constraints are met for everypath in design.

In this lab, OpenSTA is used to perform static timing analysis. 
![image](https://github.com/user-attachments/assets/baac721a-fb9b-4398-975f-ef2b37ec303a)

### Lab Task 
1) Clock period of 10.15ns. 
2) Setup uncertainty and clock transition will be 5% of clock - use set_clock_uncertainty with 10.15 * 0.05
3) Hold uncertainty and data transition will be 8% of clock - use set_clock_uncertainty with 10.15 * 0.08

1) Input to OpenSTA includes synthesised netlist, liberty file containg pdk and other clock related and path related definations.
Following clock is created with period of 10.15ns
![image](https://github.com/user-attachments/assets/c3062cec-fe5c-41a8-baba-15edb088efc9)

The report generated by OpenSTA is as follows,

for max delay in path
![image](https://github.com/user-attachments/assets/de296d6c-7c7f-4803-a5ca-2c1c938a4343)

For min delay in path
![image](https://github.com/user-attachments/assets/5fabd2f1-3095-4774-b759-086e5f0df076)

</details>

<details>
  
<summary>Lab 10: Static Timing Analysis of design using OpenSTA for process corners</summary>

Below is the snapshot of SDC
![image](https://github.com/user-attachments/assets/6509cba4-f24a-4a70-b65e-924e897efd52)

Table of various slack report

![image](https://github.com/user-attachments/assets/78d08671-c7b0-44b3-8b1a-fab8231eea71)


<img width="713" alt="wns" src="https://github.com/user-attachments/assets/74f8f222-58ea-4b27-bf25-b448f9cce736">

<img width="857" alt="avg worst slack" src="https://github.com/user-attachments/assets/e03eb76b-ee87-4968-b8b9-c54ac6361a3d">

<img width="857" alt="worstslack" src="https://github.com/user-attachments/assets/c5868ed1-13f2-448d-a0d7-581c424c3bc0">


</details>

<details>
<summary>Lab 11: Physical Design using OpenLANE and SkyWater130 PDK </summary>



# Physical Design using OpenLANE flow and SkyWater130 PDK

The main components of ASIC design includes following,

#### 1. RTL designs

Sources of RTL designs are librecores.org, opencores.org, github.commom
2. EDA Tools

Open source EDA tools are Qflow, OpenROAD, OpenLane
3. Process Design Kit(PDK) data

An example of opensource PDK is Skywater 130nm PDK

Following is a summary of simplified RTL to GDSII flow,

Synthesis - Design RTL is converted to circuits with componets form Standard cell library(SCL)

Floor/Poweplanning -
Chip floor planning - partition the chip die between different system building blocks and place IO pads

Macro Floor planning -  Dimensions, pin locations, rows definition
Powerplanning - Power network is created which includes, Power pads, Power straps, Power rings

Placement - Place the cells on the floorplan rows

Clock Tree Synthesis - Create a clock distribution network to deliver the clock to all sequential elements

Routing - Connecting cells together using available metal layers

Sign Off - Includes Physical verification through Design Rules Checking(DRC) and Layout vs Schematic(LVS) and Timing verification through Static Timing Analysis(STA).

![openlane flow](images/openlane.jpeg)


## Day 1 - Introduction to OpenLane

#### a. OpenLane working Directory
![workingdir](images/openlane_WD.png)
![workingdir](images/designpreprunsynth.png)

#### b. Design preparation steps

![workingdir](images/designprep.png)

#### c. Review files generated after design preparation and Synthesised
![workingdir](images/synth.png)
#### d. Steps to characterise Synthesis results

![workingdir](images/numberofcells.png)
![workingdir](images/dffnum.png)
Flop ratio calculations require, total number of cells synthesised and the number of flipflops among that,

```math
Flop\ ratio = \frac{number\ of\ flipflops}{total\ number\ of\ cells} = \frac{1613}{14876} = 0.10842968539

```
```math
Percentage\ of\ D-flipflops = 0.10842968539 * 100 = 10.842968539\ \%
```
## Day 2 - Floorplan and Introduction to library cells

#### a. Chip Floor planning considerations

1. Utilization factor and aspect ratio
2. Pre-placed cells
3. De-coupling capacitors
4. Power planning
5. Pin Placement and logical cell placement blockage
6. Floorplan in OpenLane and review layout in Magic
   
![workingdir](images/run_floorplan.png)
![workingdir](images/fpcomplete.png)
![workingdir](images/diearea.png)

<ins>Calculations of die area based on results generated from floorplan run</ins>

Floorplan run

![workingdir](images/flrplan_dir.png)

![workingdir](images/viewfloorplan.png)


tcl console for interaction

![workingdir](images/tclconsole.png)


![workingdir](images/floorplan.png)

Tapcells

![workingdir](images/tapcells.png)

IO pads

![workingdir](images/iopads.png)

Standard Cells
![workingdir](images/stancell1.png)
![workingdir](images/standardcells.png)

#### b. Library Binding and Placement

Need for libraries and characterisation

1. Netlist binding and initial place design
2. Optimise placement using estimated wire-length and capacitance
3. Final Placement optimisation
4. Congestion aware placement using Replace

Placement run

![workingdir](images/plmtrun.png)

Output of placement run

![workingdir](images/plmt_result.png)

Director after placement run

![workingdir](images/plmt_dir.png)

Placement of standard cell

![workingdir](images/plmn_stancell.png)


#### c. Cell design and characterization follows

1. Inputs for cell design follows
2. Circuit design Steps
3. Layout design steps
4. Typical characterization flow

#### d. General timing and characterization parameters

1. Timing threshold deifinitions
2. Propogation delay and transition time

## Day 3 - Design library cell using Magic layout and ngspice characterisation

#### a. CMOS inverter - Layout in Magic and spice simulation in ngspice

![workingdir](images/inverterrun.png)
![workingdir](images/inverterlayout.png)
![workingdir](images/layers1.png)
![workingdir](images/drcerror.png)



#### b. Layout and cmos fabrication processor

#### c. Sky130 tech files

## Day 4 - Pre-layout timing analysis and Clock tree synthesis

#### a. Timing modelling using delay tables

#### b. Timing analysis with ideal clocks using OpenSTA

#### c. Clock tree synthesis using TrintonCTS and signal integrity

#### d. Timing analysis with real clocks using OpenSTA


## Day 5 - Final steps for RTL2GDS using trintonRoute and OpenSTA

#### a. Routing and Design rule check(DRC)

#### b. Power distribution network and Routing

#### c. TrintonRoute features


</details>

