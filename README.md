ECE281_CE4
==========


#Overview
The purpose of this computer exercise was to learn how to use some of the basic functions of PRISM, which is assembly code.  This involved storing numbers, adding numbers, doubling numbers, reading values in from locations/inputs, outputing values, and using loops.  This was all done using a virtual simulator. The functionality for this lab was in parts A, B, and C, which are shown and explained below. 




#Part A
The full assembly code for Part A can be seen here: [Part_A](https://raw.githubusercontent.com/JohnTerragnoli/ECE281_CE4/master/Part%20A%20Code.psm)

The important part of the code is listed below: 

```
		   00	   7	LDAI	N	1	Y  	//puts 9 into the accumulator
		   01	   9			Y	0	N
		   02	   D	STA	B0	N	2	Y   //stores the value in the accumulator, 9, at the position B0	
		   03	   0			Y	0	N
		   04	   B			Y	0	N
		   05	   7	LDAI	N	1	Y   //8	puts 8 into the accumulator
		   06	   8		  	Y	0	N
		   07	   D	STA	C4	N	2	Y   //stores the value in the accumulator, 8,into the location C4
		   08	   4			Y	0	N
		   09	   C			Y	0	N
		   0A	   7	LDAI	N	1	Y 	//B	puts the hex value B into the Accumulator
		   0B	   B			Y	0	N
		   0C	   D	STA	CB  N	2	Y   //stores the value in the accumulator, hex B,into the location CB
		   0D	   B			Y	0	N
		   0E	   C			Y	0	N
	0F	   0F	   9	JMP	0F	N	2	Y
		   10	   F			Y	0	N
		   11	   0			Y	0	N

```

The purpose of this code was simple.  To put the value 9 into the accumulator, then store the value in the accumulator at the location B0.  Then, the program put 8 into the accumulator and stored this new value int he accumulator at the location C4.  Then, the program stored the hex value B in the accumulator.  the contents of the accumulator were then dumped into the location CB.  After all of this was finished, the program entered an infinte loop to end the program so that it would not crash.  

The rest of the code in Part A simply took up space, it just contained commands telling the computer to do nothing basically.  The computer never reached these commands anyway.  


// denotes comments.  


#Part B
The full assembly code for Part B can be seen here: [Part_B](https://raw.githubusercontent.com/JohnTerragnoli/ECE281_CE4/master/Part%20B%20Code.psm)

```
		   00	   F	LDAD	B0	N	2	N//puts the number from location B0 into the accumulator
		   01	   0				Y	0	N
		   02	   B				Y	0	N
		   03	   E	ADDD	B0	N	2	N//adds the number from B0 to the accumulator again
		   04	   0				Y	0	N
		   05	   B				Y	0	N
		   06	   6	ADDI	C	N	1	N	//adds 4's compliment in hex, just like subracting 4 from the accumulator
		   07	   C				Y	0	N
		   08	   4	OUT	2		N	1	N //outputs the value in the accumulator to the second output
		   09	   2				Y	0	N
loop	   0A	   9	JMP	loop	N	2	N
		   0B	   A				Y	0	N
		   0C	   0				Y	0	N

```

The purpose of this program was to take in a number at the memory location B0 and double it, subtract four, and then output the resulting value, which is in the accumulator, to output 2.  The computer then entered a never ending loop to end the program so that it doesn't crash.  The subtraction of 4 was done by adding C, which is the 2's compliment of 4 in hex.  This is basically subtracting four.  

The rest of the code in Part B simply took up space, it just contained commands telling the computer to do nothing basically.  The computer never reached these commands anyway.  


// denotes comments.  

#Part C
The full assembly code for Part C can be seen here: [Part_C](https://raw.githubusercontent.com/JohnTerragnoli/ECE281_CE4/master/Part%20C%20Code.psm)

The purpose of this program was to put the value of the input at input 3 into the first output, then subract one from that and put it in the second output, then subract one from the second output and put it in the third output.  Then, the program iterated to have the first output decriment by 1, and have the second and third outputs follow suit. This incrimentation was done by looping the progam back to the beginning, after putting the input value into the accumulator.  To decriment by 1, F was added, because F is the 2's compliment of 1 in hex.  

The rest of the code in Part C simply took up space, it just contained commands telling the computer to do nothing basically.  The computer never reached these commands anyway.  

The most important parts of the code for Part C are produced below: 






#Suggestions
1. Ask "are you sure you want to quit" when you hit the red x beofre the program actually closes, so you don't lose everything on accident. 
2. Reset the inputs when the reset button is hit.  


#Documentation
C3C Spence helped explain to me that we're supposed to label the locations in the RAM and the Programming Wizard by the same name so that that they can interact if necessary.  
