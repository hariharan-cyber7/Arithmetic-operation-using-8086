# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="500" height="600" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200                    |    1204                  |
| 1201                    |    1205                  |
| 1202                    |                          |
| 1203                    |                          |


#### Manual Calculations

<img width="450" height="450" alt="image" src="https://github.com/user-attachments/assets/558f6d82-c5e1-4365-baba-6ec65ac65ac2" />




---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="500" height="500" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/dca386af-7cfc-4110-a008-5bd011cfc5bc" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS:CODE,DS:CODE
ORG 1000H
MOV SI,1200H
MOV AX,[SI]
MOV BX,[SI+02H]
MOV CL,00H
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END

```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|        1200             |                          |
|        1201             |           1204           |
|        1202             |           1205           |
|        1203             |                          |


#### Manual Calculations

<img width="450" height="450" alt="image" src="https://github.com/user-attachments/assets/dfbb39f1-9b82-495a-a7e9-28fc7860e010" />



---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="500" height="500" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/f395478e-78b8-49bd-b5e7-e7f3b5edb5fe" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200            |           1204           |
|         1201            |           1205           |
|         1202            |           1206           |
|         1203            |           1207           |


#### Manual Calculations

<img width="450" height="450" alt="image" src="https://github.com/user-attachments/assets/2cf2b7b8-ddc0-4aa6-9ef4-09504d0cad37" />



---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="500" height="500" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/d9dd91bf-2afa-4fab-80f9-cc24f6adde2b" />



## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200            |           1204           |
|         1201            |           1205           |
|         1202            |           1206           |
|         1203            |           1207           |


#### Manual Calculations

<img width="450" height="450" alt="image" src="https://github.com/user-attachments/assets/f9ce2e8e-70d9-4bd6-bcf2-58451e9a3b3f" />



---
## OUTPUT FROM MASM SOFTWARE
<img width="500" height="500" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/9eab7855-6a3a-4839-9941-ac1102841f05" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
