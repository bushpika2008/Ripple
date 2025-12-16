# Ripple
# 4-bit_ripple_counter
# AIM:
To implement 4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

# SOFTWARE REQUIRED:
Quartus prime

# THEORY
4 Bit Ripple Counter

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

<img width="950" height="408" alt="image" src="https://github.com/user-attachments/assets/ae5060ac-6b42-4b46-b38b-897afb05e048" />

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

<img width="592" height="491" alt="image" src="https://github.com/user-attachments/assets/75403bee-94dd-4e0c-b3c5-9c76fec931c4" />

<img width="510" height="376" alt="image" src="https://github.com/user-attachments/assets/cd3e29d4-ebf5-470f-a9f4-543c97902896" />
# Procedure
1.Increment count on each positive edge of the clock.

2.Reset count to zero when it reaches 15.

3.Generate clock signal (clk).

4.Instantiate the RippleCounter module.

5.Conduct functional testing by displaying the count at each clock cycle for 16 cycles. */

# PROGRAM
```
module bit_ripple_counter (
    input  wire clk,
    input  wire reset,
    output reg [3:0] q
);

    always @(posedge clk or posedge reset) begin
        if (reset)
            q <= 4'b0000;
        else
            q <= q + 1'b1;   
    end

endmodule
```
# Developed by: BUSHPIKA C
# RegisterNumber: 25007434
# RTL LOGIC FOR 4 Bit Ripple Counter

<img width="1086" height="573" alt="image" src="https://github.com/user-attachments/assets/592752f6-e8d7-4703-ab56-a7207979dae6" />

# TIMING DIGRAMS FOR 4 Bit Ripple Counter

<img width="1052" height="607" alt="image" src="https://github.com/user-attachments/assets/6d600736-029c-4139-8e72-9eba92a8195a" />

# RESULTS
Thus 4-BIT-RIPPLE-COUNTER is verified successfully.
