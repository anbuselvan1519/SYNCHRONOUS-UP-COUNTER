### SYNCHRONOUS-UP-COUNTER

## Name: Anbuselvan S
## Reg no: 212223240008

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

1.Initialize the shift register to a known state (e.g., all zeros).

2.Input a bit serially into the shift register.

3.Shift the contents of the register one position to the right (or left).

4.Output the shifted bit from the last stage of the register.

5.Repeat steps 2-4 for each bit you want to input and shift.

**PROGRAM**

Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by: Anbuselvan S

RegisterNumber: 212223240008

```
module exps(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule
```


**RTL LOGIC UP COUNTER**


![445438200-5fbff8d5-824e-49e6-9c55-325b6035b9eb](https://github.com/user-attachments/assets/63b31c90-1907-4aee-97dc-3fe9b1b9c92e)

**TIMING DIAGRAM FOR IP COUNTER**



![445438811-c2bf3767-28c2-4ae4-86df-357539650ba7](https://github.com/user-attachments/assets/8296cf0d-b503-4737-874e-e76305375f86)

**TRUTH TABLE**


![439865067-280aa944-e252-4e34-af14-847519bd4020](https://github.com/user-attachments/assets/c7580c4e-89d7-4372-9fd0-139f58765207)

**RESULTS**


Thus 4 bit synchronous up counter and validate functionality is successfully implemented.
