# VLSI-LAB-EXP-4
# SIMULATION AND IMPLEMENTATION OF SEQUENTIAL LOGIC CIRCUITS

# AIM: 
 To simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using Xilinx ISE.

# APPARATUS REQUIRED:

Xilinx 14.7
Spartan6 FPGA

# **LOGIC DIAGRAM**

# SR FLIPFLOP

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/77fb7f38-5649-4778-a987-8468df9ea3c3)


# JK FLIPFLOP

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/1510e030-4ddc-42b1-88ce-d00f6f0dc7e6)

# T FLIPFLOP

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/7a020379-efb1-4104-85ee-439d660baa08)


# D FLIPFLOP

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/dda843c5-f0a0-4b51-93a2-eaa4b7fa8aa0)


# COUNTER

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/a1fc5f68-aafb-49a1-93d2-779529f525fa)


  
# PROCEDURE:
```
STEP:1  Start  the Xilinx navigator, Select and Name the New project.
STEP:2  Select the device family, device, package and speed.       
STEP:3  Select new source in the New Project and select Verilog Module as the Source type.                       
STEP:4  Type the File Name and Click Next and then finish button. Type the code and save it.
STEP:5  Select the Behavioral Simulation in the Source Window and click the check syntax.                       
STEP:6  Click the simulation to simulate the program and  give the inputs and verify the outputs as per the truth table.               
STEP:7  Select the Implementation in the Sources Window and select the required file in the Processes Window.
STEP:8  Select Check Syntax from the Synthesize  XST Process. Double Click in the  FloorplanArea/IO/Logic-Post Synthesis process in the User Constraints process group. UCF(User constraint File) is obtained. 
STEP:9  In the Design Object List Window, enter the pin location for each pin in the Loc column Select save from the File menu.
STEP:10 Double click on the Implement Design and double click on the Generate Programming File to create a bitstream of the design.(.v) file is converted into .bit file here.
STEP:11  On the board, by giving required input, the LEDs starts to glow light, indicating the output.
```
# VERILOG CODE:
# SR FLIPFLOP:
```
module srff(s,r,clk,reset,q);
input s,r,clk,reset;
output reg q;
always@(posedge clk)
begin
if(reset==1)
q =1'b0;
else 
begin
case({s,r})
 2'b00: q = q;
 2'b01: q = 1'b0;
 2'b10: q = 1'b1;
 2'b11: q = 1'bx;
 default:q = ~q;
endcase
end 
end
endmodule
```
# JK FLIPFLOP:
```
module jk_ff(j,k,clk,reset,q);
input j,k,clk,reset;
output reg q;
always@(posedge clk)
begin
if(reset==1)
q =1'b0;
else 
begin
case({j,k})
 2'b00: q = q;
 2'b01: q = 1'b0;
 2'b10: q = 1'b1;
 2'b11: q = ~q;
 default:q =1'b0;
endcase
end 
end
endmodule
```
# T FLIPFLOP:
```
module tff(clk,rst,j,q);
input clk,rst,j;
output reg q;
always@(posedge clk)
begin
case(t)
1'b0:q=q;
1'b1:q=~q;
default=q=1'b0;
endcase
end
endmodule
```
# D FLIPFLOP:
```
module dff(clk,rst,d,q);
input clk,rst,d;
output reg q;
always@(posedge clk)
begin
if(rst==1)
q=1'b0;
else
q=d;
end
endmodule
```
# OUTPUT WAVEFORM:

# SR FLIPFLOP:
![WhatsApp Image 2024-04-21 at 14 12 36_28147a26](https://github.com/Afsar1276/VLSI-LAB-EXP-4/assets/161407741/6862bfd4-e55e-4dfa-8a0e-ecc45f24a73a)

# JK FLIPFLOP:
![WhatsApp Image 2024-04-21 at 14 11 40_7d6df3ee](https://github.com/Afsar1276/VLSI-LAB-EXP-4/assets/161407741/3e68b7f0-b719-4c89-a4db-bc65d8e52c95)

# T FLIPFLOP:
![WhatsApp Image 2024-04-21 at 14 11 46_a798cc19](https://github.com/Afsar1276/VLSI-LAB-EXP-4/assets/161407741/2e7464b0-7e77-474a-9e00-3c6d7c93d2a6)

# D FLIPFLOP:
![WhatsApp Image 2024-04-21 at 14 11 52_55b5eb33](https://github.com/Afsar1276/VLSI-LAB-EXP-4/assets/161407741/9d91daa4-c884-4aa2-b9d1-2060b9668e04)


# RESULT:
Hence thus given To simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using vivado
