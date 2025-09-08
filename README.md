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
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />
#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
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
| 1200: 31                | 1204: 62                 |
| 1201: 12                | 1205: 24                 |
| 1202: 31                | 1206: 00                 |
| 1203: 12                | 1207: C4                 |
#### Manual Calculations
![add manual](https://github.com/user-attachments/assets/6c9db824-3c1b-4d85-a3eb-677a52b4715f)

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="653" height="438" alt="Screenshot 2025-09-08 160441" src="https://github.com/user-attachments/assets/997eca1d-c3d1-4347-b1d8-ebbcb9af0b17" />

<img width="640" height="405" alt="Screenshot 2025-09-08 160258" src="https://github.com/user-attachments/assets/b86845f6-094a-430b-ba8e-4df96723d31a" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
MOV AX,[SI]
MOV BX,[SI+02H]
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
|  1200: 31               |  1204:   00              |
|  1201: 12               |  1205:   00              |
|  1202: 31               |  1206:   00              |
|  1203: 12               |  1207:   C4              |
#### Manual Calculations
![sub manual](https://github.com/user-attachments/assets/c7113350-2236-4acf-9dab-0df74b6b0143)

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="641" height="405" alt="Screenshot 2025-09-08 162738" src="https://github.com/user-attachments/assets/ea9da608-b359-4931-b67d-a25a6ae36130" />

<img width="644" height="443" alt="Screenshot 2025-09-08 162631" src="https://github.com/user-attachments/assets/cfb7afca-f4b9-456b-b4ff-b094049a3e0c" />



## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
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
|  1200: 31               | 1204: 61                 |
|  1201: 12               | 1205: ED                 |
|  1202: 31               | 1206: 00                 |
|  1203: 12               | 1207: C4                 |
### Manual Calculations
![mul manual](https://github.com/user-attachments/assets/9ec17078-13f5-4cfb-a2a7-20e1633de80c)



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="633" height="402" alt="image" src="https://github.com/user-attachments/assets/77ffbc99-8c5b-4c6d-b045-7b96cacc25b3" />

<img width="647" height="433" alt="Screenshot 2025-09-08 163420" src="https://github.com/user-attachments/assets/3ec7aa7a-0d23-495b-9f49-541510f4b168" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
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
|  1200: 31               | 1204: 01                 |
|  1201: 12               | 1205: 00                 |
|  1202: 31               | 1206: 00                 |
|  1203: 12               | 1207: 00                 |

#### Manual Calculations
![div manual](https://github.com/user-attachments/assets/c9833800-f54b-4c16-8d02-be4460bc8991)



## OUTPUT FROM MASM SOFTWARE

<img width="647" height="444" alt="Screenshot 2025-09-08 164600" src="https://github.com/user-attachments/assets/e6058cd9-e95f-42f7-b97c-cb72beaf1979" />

<img width="642" height="427" alt="image" src="https://github.com/user-attachments/assets/99ab1143-8d75-4de0-968c-606b0e876a64" />






## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
