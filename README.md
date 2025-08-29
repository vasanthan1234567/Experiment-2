# Experiment-2
Write a program in Python language for Matrix multiplication fails. Introspect the causes for its failure and write down the possible reasons for its failure. 
### Name : VASANTHAN.N
### REG NO.: 212224240180
## Aim :
Write a python program for matrix multiplication and inspect for failures. 

## Algorithm :
1.	Start the program.
2. Create empty list formatrix1, matrix2 and result.
3. Get the rows and columns count from the user.
4. Get the values of two matrix.
5. Perform matrix multiplication and store the answer in result.
6. Stop the program. 

## Program :
```python

r1, c1 = input("Enter row and column count for matrix 1: ").split()
r2, c2 = input("Enter row and column count for matrix 2: ").split()


matrix1 = []
matrix2 = []
result = []


if r1.isnumeric() and c1.isnumeric() and r2.isnumeric() and c2.isnumeric():
    r1, c1, r2, c2 = map(int, (r1, c1, r2, c2))

    
    if c1 != r2:
        print("Matrix multiplication not possible")
    elif max(r1, c1, r2, c2) > 20 or min(r1, c1, r2, c2) == 0:
        print("Matrix multiplication not possible")
    else:
      
        print("Enter elements for matrix 1:")
        for i in range(r1):
            row = []
            for j in range(c1):
                row.append(int(input(f"Matrix 1[{i+1}][{j+1}]: ")))
            matrix1.append(row)

      
        print("Enter elements for matrix 2:")
        for i in range(r2):
            row = []
            for j in range(c2):
                row.append(int(input(f"Matrix 2[{i+1}][{j+1}]: ")))
            matrix2.append(row)

        for i in range(r1):
            row = []
            for j in range(c2):
                total = 0
                for k in range(c1):
                    total += matrix1[i][k] * matrix2[k][j]
                row.append(total)
            result.append(row)

     
        print("\nResultant Matrix:")
        for row in result:
            print(" ".join(map(str, row)))
else:
    print("Enter valid numbers")
```
## Output :

<img width="486" height="153" alt="Screenshot 2025-08-22 113325" src="https://github.com/user-attachments/assets/6efccf0c-522e-43c4-978d-c71902a50b32" />

<img width="507" height="152" alt="Screenshot 2025-08-22 113354" src="https://github.com/user-attachments/assets/88bde693-7a28-4508-8450-0307a128f60a" />

<img width="500" height="152" alt="Screenshot 2025-08-22 113426" src="https://github.com/user-attachments/assets/4238cd20-d9d3-4e5d-8fd7-156c793cb69a" />

<img width="502" height="140" alt="Screenshot 2025-08-22 113640" src="https://github.com/user-attachments/assets/71925cb5-99eb-44af-ba45-ee52da08669d" />

<img width="523" height="147" alt="Screenshot 2025-08-22 113729" src="https://github.com/user-attachments/assets/76f21955-e818-4806-800d-09faa0dd2ca7" />

## Result :
Thus, the python program for matrix multiplication is implemented and the causes for its failure is introspected successfully.
