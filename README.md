# Design and simulate 3 bit synchronous counter using Verilog.

## THEORY
A 3-bit synchronous counter is a digital circuit that uses three flip-flops to count the number of clock pulses that have been applied to it. The outputs of the flip-flops are connected to a logic circuit that determines when the counter should increment. The counter increments its count value synchronously, which means that all three flip-flops change state at the same time.

The three flip-flops in the counter are T flip-flops. The T inputs of the flip-flops are connected to the outputs of the previous flip-flops, and the clock input is connected to all three flip-flops. The logic circuit that determines when the counter should increment is implemented using AND gates.

The operation of the 3-bit synchronous counter is as follows:

* The counter is initially reset to 000.
* When the clock pulse is applied, the T inputs of the flip-flops are set to 1, and the outputs of the flip-flops change state.
* The counter now has the value 001.
* The process repeats, and the counter increments its count value by 1 for each clock pulse that is applied.
* The counter can be used to perform a variety of tasks, such as counting the number of pulses in a signal, generating a timing sequence, or controlling the operation of other digital circuits.

Here are some of the advantages of using a 3-bit synchronous counter:

* It is more efficient than a ripple counter, because all three flip-flops change state at the same time.
* It can be used to generate a wider range of count values than a ripple counter.
* It is less susceptible to noise than a ripple counter.
Here are some of the disadvantages of using a 3-bit synchronous counter:

* It is more complex than a ripple counter.
* It requires more gates to implement.
* It is more expensive than a ripple counter.

# Logic Diagram
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20210518140350/SynchronousUpDownCounter-660x356.jpg">

# Netlist Diagram
![RTL_Viewer](https://github.com/Vineesh-AI-DS/Simulation-project--Digital-Electronics/assets/93427254/e64d28bb-c7ce-49a8-9ad6-7da71dc40923)

# Timing Diagram
![Waveform](https://github.com/Vineesh-AI-DS/Simulation-project--Digital-Electronics/assets/93427254/1f018205-2511-4530-8479-22fc957dece7)

# Truth Table
![TruthTable](https://github.com/Vineesh-AI-DS/Simulation-project--Digital-Electronics/assets/93427254/f27f0178-1e24-4f65-a44f-61aea2df86bd)

# Program
```verilog
module Skill_Ass (
  input clk,
  input reset,
  output reg [2:0] count
);

  always @(posedge clk) begin
    if (reset) begin
      count <= 3'b0;
    end else begin
      count <= count + 1;
    end
  end

endmodule
```
# Result
Thus, a 3 bit synchronous counter is designed and simulated using Verilog.
