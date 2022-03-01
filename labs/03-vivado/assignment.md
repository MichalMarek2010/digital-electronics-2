# Lab 3: YOUR_FIRSTNAME LASTNAME

### Two-bit wide 4-to-1 multiplexer

1. Listing of VHDL architecture from source file `mux_2bit_4to1.vhd`. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture Behavioral of mux_3bit_4to1 is
begin
    f_o <= a_i when (sel_i = "00") else
           b_i when (sel_i = "01") else
           c_i when (sel_i = "10") else
           d_i;
end architecture Behavioral;
```

2. Listing of VHDL stimulus process from testbench file (`tb_mux_2bit_4to1`) with asserts. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines. Verify at least four random input combinations:

```vhdl
     p_stimulus : process
    begin
       	s_d		<= "000";
        s_c 	<= "101"; 
        s_b 	<= "110"; 
        s_a 	<= "111";
        s_sel 	<= "00";
        wait for 100 ns;
        
        s_d		<= "010";
        s_c 	<= "111"; 
        s_b 	<= "010"; 
        s_a 	<= "101";
        s_sel 	<= "01";
        wait for 100 ns;
        
        s_d		<= "111";
        s_c 	<= "001"; 
        s_b 	<= "010"; 
        s_a 	<= "000";
        s_sel	<= "10";
        wait for 100 ns;
        
        s_d		<= "011";
        s_c 	<= "101"; 
        s_b 	<= "111"; 
        s_a 	<= "000";
        s_sel	<= "11";
        wait for 100 ns;
        wait;
    end process p_stimulus;
```

3. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![your figure]()
