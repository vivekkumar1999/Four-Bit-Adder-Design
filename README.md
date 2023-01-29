# Four-Bit-Adder-Design
Four bit adder using Half and Full Adder's.



module four_bit_adder(clr,a,b,z);
input clr;
input [3:0]a,b;
output [4:0]z;
wire [2:0]w;
half_adder ha1(.clr(clr),.a(a[0]),.b(b[0]),.sum(z[0]),.carry(w[0]));
full_adder fa1(.Clr(clr),.A(a[1]),.B(b[1]),.Cin(w[0]),.Sum(z[1]),.Carry(w[1]));
full_adder fa2(.Clr(clr),.A(a[2]),.B(b[2]),.Cin(w[1]),.Sum(z[2]),.Carry(w[2]));
full_adder fa3(.Clr(clr),.A(a[3]),.B(b[3]),.Cin(w[2]),.Sum(z[3]),.Carry(z[4]));
  
endmodule



