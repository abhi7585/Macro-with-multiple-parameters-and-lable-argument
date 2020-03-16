# Macro-with-multiple-parameters-and-lable-argument

Aim: Defining a macro with more positional arguments & label argument, expansion of macro &
generating expanded source code.

Instructions:
1) Write a ALP using few instructions & Macro calls with a label argument & multiple arguments.
2) Define domain/body of the Macro with arguments
3) Write a program which will replace each Macro call with its domain along with proper
arguments & performs expansion of the Macro.
4) Show the input source code with Macro call & output the expanded source code
5) Also output the following statistics:
- Number of instructions in input source code (excluding Macro calls)
- Number of Macro calls
- Number of instructions defined in the Macro call
- Actual argument during each Macro call
- Label argument during each Macro call
- Total number of instructions in the expanded source code.

Input 1: Input Source code with Macro calls
```
MOV R
STAR: ABHISHEK 30, 40, 50
DCR R
AND R
NEXT: ABHISHEK 33, 44, 55
MUL 88
HALT
```

Input 2: Macro definition
```
MACRO
&LAB ABHISHEK &ARG1, &ARG2, &ARG3
&LAB ADD &ARG1
SUB &ARG2
OR &ARG3
MEND
```

Output source code after Macro expansion:
```
MOV R
STAR: ADD 30
SUB 40
OR 50
DCR R
AND R
NEXT: ADD 33
SUB 44
OR 55
MUL 88
HALT
```
Statistical output:
```
Number of instructions in input source code (excluding Macro calls) = 5
Number of Macro calls = 2
Number of instructions defined in the Macro call = 3
Actual argument during first Macro call “ABHISHEK” = 30, 40, 50
Actual Label argument during first Macro call = STAR
Actual argument during second Macro call “ABHISHEK” = 33, 44, 55
Actual Label argument during second Macro call = NEXT
Total number of instructions in the expanded source code = 11
```
