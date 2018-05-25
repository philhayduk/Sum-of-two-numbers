# Sum-of-two-numbers
This program will give you the sum of two numbers
;Phil Hayduk
;Irvine 32 project
;Sum two numbers

INCLUDE Irvine32.inc


 .data ; this is the data area
 sum db 0 ; create a variable named sum
 num1 db 0; first variable
 num2 db 0; second
 prompt1 db "Enter a number",0
 prompt2 db "Enter another number",0
 result db "The sum is ",0

 .code ; this is the code area
 main PROC
 mov edx, offset prompt1
 call writestring
 call readint ; cin>>Num1
 mov num1, al

 mov edx, offset prompt2
 call writestring
 call readint ; cin>>Num2
 mov num2, al ; al = al(num2) + num1

 add al, num1 
mov edx, offset result
 call writestring
 call writeint ; cout 


INVOKE ExitProcess,0 ; end the program
 main ENDP
 END main
