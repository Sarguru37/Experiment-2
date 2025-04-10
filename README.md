## Name: SARGURU K
## Reg no: 212222230134
# Experiment-2

## Write a program in Python language for Matrix multiplication fails. Introspect the causes for its failure and write down the possible reasons for its failure. 
## Aim
Write a python program for matrix multiplication and inspect for failures. 

## Algorithm
1.	Start the program.
2. Create empty list formatrix1, matrix2 and result.
3. Get the rows and columns count from the user.
4. Get the values of two matrix.
5. Perform matrix multiplication and store the answer in result.
6. Stop the program. 

## Program
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


## Output

![image](https://github.com/user-attachments/assets/8c65ca21-8bba-41c3-b844-fbc16fd1ef6b)

![image](https://github.com/user-attachments/assets/c546635f-7e59-4e7a-8c92-260602ce92a4)

![image](https://github.com/user-attachments/assets/b38cd9d6-a173-4ea1-8e9f-815283b9db9e)

![image](https://github.com/user-attachments/assets/a7823a45-c3fb-40f1-b374-5f3cec7aa160)




## Result
Thus, the python program for matrix multiplication is implemented and the causes for its failure is 
introspected successfully. 
