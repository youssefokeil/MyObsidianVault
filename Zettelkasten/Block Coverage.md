Created on: 07-10-2025 12:22, note by Youssef Okeil
Status: #idea
Tags: #verification 
# Block Coverage
> is the percentage of basic blocks executed during simulation compared to total number of basic blocks. 


```verilog
module my_module(input clk, input sel, input [7:0] data, output reg [7:0] out);
    reg [7:0] internal_reg;
    always @(posedge clk) begin
        if(sel) begin
            internal_reg <= data;
        end else begin
            internal_reg <= internal_reg + 1;
        end
    end
    always @* begin
        case(internal_reg)
            8'h00: out = 8'h10;
            8'h01: out = 8'h20;
            8'h02: out = 8'h30;
            8'h03: out = 8'h40;
            default: out = 8'h50;
        endcase
    end
endmodule
```

In this example, the testbench should execute all the if/else conditions in the first block and all the cases in the second always block.

-----------------
# References
https://www.chipverify.com/verification/block-coverage