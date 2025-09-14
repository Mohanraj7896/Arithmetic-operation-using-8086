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
<img width="707" height="707" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


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
|     1200 : 12           |      1204 : 24           |
1201 : 34  |  1205 : 68
1202 : 12   | 1206 : 00
1203 : 34    |1207 : C4

#### Manual Calculations
![WhatsApp Image 2025-09-14 at 14 03 30_bce4acec](https://github.com/user-attachments/assets/d26fd2e7-3128-49cc-9f15-b076e2e44ea9)


---

## OUTPUT IMAGE FROM MASM SOFTWARE

![WhatsApp Image 2025-09-14 at 14 05 21_d77ae7ba](https://github.com/user-attachments/assets/47650581-c23e-4881-8b8e-435aa9be3a03)

![WhatsApp Image 2025-09-14 at 14 05 22_875667eb](https://github.com/user-attachments/assets/e4560723-246a-4214-a7b6-321befb7a630)




## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="578" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
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
|               1200 : 12          |      1204 : 00                    |
1201 : 34 | 1205 : 00
1202 : 12 | 1206 : 00
1203 : 34 | 1207 : C4

#### Manual Calculations

![WhatsApp Image 2025-09-14 at 14 03 30_1f791b6b](https://github.com/user-attachments/assets/5564d0fd-ad2a-44b7-98b3-4db70a553198)



---


## OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-09-14 at 14 05 22_c5205835](https://github.com/user-attachments/assets/9d19eb02-6749-4005-afcc-d4d377e68f55)

![WhatsApp Image 2025-09-14 at 14 07 30_8914b19c](https://github.com/user-attachments/assets/51957d9a-87ae-4e5c-a1e6-454d923e3b51)


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="707" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



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
|         1200 : 12                |       1204 : 44                   |
1201 : 34 | 1205 : 51
1202 : 12 | 1206 : 97
1203 : 34 | 1207 : 0A

#### Manual Calculations

![WhatsApp Image 2025-09-14 at 14 03 29_c5543da4](https://github.com/user-attachments/assets/9e32e85d-be94-47b5-8d74-52d6a458159e)




---

## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-14 at 14 07 31_ac24efeb](https://github.com/user-attachments/assets/43eb0d10-1383-4c5b-90f3-52523aaeef46)

![WhatsApp Image 2025-09-14 at 14 07 31_5662e020](https://github.com/user-attachments/assets/b41a6435-e456-4580-9fbc-feb655f5a547)



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
|       1200 : 12                  |              1204 : 01            |
1201 : 34 | 1205 : 00
1202 : 12 | 1206 : 00
1203 : 34 | 1207 : 00

#### Manual Calculations

![WhatsApp Image 2025-09-14 at 14 03 29_0956bd48](https://github.com/user-attachments/assets/4b660fab-38fd-49ed-96d6-dd05cf341057)



---
## OUTPUT FROM MASM SOFTWARE

![WhatsApp Image 2025-09-14 at 14 07 31_07fd1776](https://github.com/user-attachments/assets/e8657091-6092-4c48-a797-a438523c6785)

![WhatsApp Image 2025-09-14 at 14 10 20_8783bf74](https://github.com/user-attachments/assets/a6604d9a-ac81-4538-ae4d-eb85999982ef)




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
