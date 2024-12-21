### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**
```
1.Type the program in the Quartus software.
2.compile and run the program.
3.geenerate the RTL schematic and save the logical diagram.
4.creat the node for the input and output to generate the timing diagram.
5.for the different input combination generate the timing diagram.
```

**PROGRAM**
```
/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:Shamrin.B
RegisterNumber:24900144
*/
```
```
module exp_11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @(posedge clk)
begin 
if(!rstn)
out<=0;
else 
out <= out+1;
end 
endmodule
```
**RTL LOGIC UP COUNTER**

![Screenshot (63)](https://github.com/user-attachments/assets/515ae72b-86d6-4160-b1d4-c5611a143118)


**TIMING DIAGRAM FOR IP COUNTER**

![Screenshot (65)](https://github.com/user-attachments/assets/9d5dc93e-bad1-41a0-bea4-85d7394a65d7)


**TRUTH TABLE**

![WhatsApp Image 2024-12-17 at 11 45 33_98391a4a](https://github.com/user-attachments/assets/33b1fe8e-9ac8-4854-b9c4-cd23708c051b)

**STATE TABLE**

![image](https://github.com/user-attachments/assets/b377c625-3359-41b9-9ae5-bbadf5db5bd5)


**RESULTS**:

4 bit synchronous up counter and validate functionality is studied and verified.
