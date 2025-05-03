# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

Step 1: Open Quartus II in your laptop. 

Step 2: Write code to implement SR flipflop using verilog and validating their functionality using their functional tables. 

Step 3: Run compilation to check for errors. 

Step 4: Open waveform output and load input values. 

Step 5: Run simulation to get the output. 

Step 6: Open in RTL viewers to get RTL diagram output

**PROGRAM**

```
module EXP10(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
RTL LOGIC FOR SISO Shift Register
TIMING DIGRAMS FOR SISO Shift Register
RESULTS Thus the program to implement a SISO Shifter Register using verilog and
validating their functionality using their functional tables is successfully completed.
end
endmodule
```

/*
Developed by: Rithanya D
RegisterNumber: 212224050038
*/

**RTL LOGIC FOR SISO Shift Register**
![image](https://github.com/user-attachments/assets/2952dffb-60c1-4d73-a81e-f31d5e7ef85c)


**TIMING DIGRAMS FOR SISO Shift Register**
![image](https://github.com/user-attachments/assets/9b18ae77-64ae-4e7e-8098-c227e3c5ce6c)


**RESULTS**
Thus, the program to implement a SISO shift register using Verilog and to validate its functionality using its truth table was successfully completed.
