module pisca;
	reg clok;
	input led;
	
	assign led = clok;

	always #2 clok = ~clok;

	initial begin
		$dumpvars(0, clok, led);
    			clok <= 0;
    			#500;
    		$finish;
	end	
endmodule
