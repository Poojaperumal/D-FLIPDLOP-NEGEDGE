# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

/* write all the steps invloved */

**PROGRAM**

 
 Developed by: POOJA.P  RegisterNumber: 212224100041
```
module Ex8(d, clk, rst, q, qbar);
    input d;
    input clk;
    input rst;
    output q;
    output qbar;
     reg q;
     reg qbar;
       always @ (posedge(clk) or posedge(rst)) begin
       if (rst==1'b1)
     begin
     q=1'b0;
     qbar=1'b1;
     end
      else if (d==1'b0)
     begin
     q=1'b0;
     qbar=1'b1;
     end
      else
     begin
     q=1'b1;
     qbar=1'b0;
     end      end    endmodule

```
     

**RTL LOGIC FOR FLIPFLOPS**


![Screenshot 2025-05-12 090517](https://github.com/user-attachments/assets/fc60e295-9fc9-4083-8529-4904389cf935)


**TIMING DIGRAMS FOR FLIP FLOPS**



![Screenshot 2025-05-12 090639](https://github.com/user-attachments/assets/eedc9bba-7baa-48b9-ab01-d98098b7df9b)


**RESULTS**


Thus the D flipflop using verilog and validating their functionality using their functional tables is verified
