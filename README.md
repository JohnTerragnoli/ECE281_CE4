ECE281_CE4
==========


#Overview
The purpose of this computer exercise was to learn how to use some of the basic functions of PRISM, which is assembly code.  This involved storing numbers, adding numbers, doubling numbers, reading values in from locations/inputs, outputing values, and using loops.  This was all done using a virtual simulator. The functionality for this lab was in parts A, B, and C, which are shown and explained below. 




#Part A
The full assembly code for Part A can be seen here: [Part_A](https://raw.githubusercontent.com/JohnTerragnoli/ECE281_CE4/master/Part%20A%20Code.psm)

The important part of the code is listed below: 

```
		   00	   7	LDAI		N	1	Y //9	puts 9 into the accumulator
		   01	   9				  Y	0	N
		   02	   D	STA	B0	N	2	Y //stores the value in the accumulator, 9, at the position B0	
		   03	   0			  	Y	0	N
		   04	   B				  Y	0	N
		   05	   7	LDAI		N	1	Y //8	puts 8 into the accumulator
		   06	   8			  	Y	0	N
		   07	   D	STA	C4	N	2	Y //stores the value in the accumulator, 8,into the location C4
		   08	   4				  Y	0	N
		   09	   C				  Y	0	N
		   0A	   7	LDAI		N	1	Y //B	puts the hex value B into the Accumulator
		   0B	   B			  	Y	0	N
		   0C	   D	STA	CB  N	2	Y //stores the value in the accumulator, hex B,into the location CB
		   0D	   B			  	Y	0	N
		   0E	   C				  Y	0	N
0F	   0F	   9	JMP	0F	N	2	Y
		   10	   F				  Y	0	N
		   11	   0				  Y	0	N

```

#Part B
The full assembly code for Part B can be seen here: [Part_B](https://raw.githubusercontent.com/JohnTerragnoli/ECE281_CE4/master/Part%20B%20Code.psm)

#Part C
The full assembly code for Part C can be seen here: [Part_C](https://raw.githubusercontent.com/JohnTerragnoli/ECE281_CE4/master/Part%20C%20Code.psm)






#Suggestions
1. Ask "are you sure you want to quit" when you hit the red x beofre the program actually closes, so you don't lose everything on accident. 
2. Reset the inputs when the reset button is hit.  


#Documentation
C3C Spence helped explain to me that we're supposed to label the locations in the RAM and the Programming Wizard by the same name so that that they can interact if necessary.  
