# 19CS301Module-9
### EX: 9.1 MATRIX OPERATIONS
### Aim: 
To add two matrices of the same size (with user-specified rows and columns) and print the resulting matrix after performing the addition.
### Algorithm:
1. Accept the number of rows and columns for the matrices from the user.
2. Input the elements of the first matrix.
3. Input the elements of the second matrix.
4. Create a new matrix to store the result of the addition.
5. Perform the addition by adding corresponding elements of the two matrices.
6. Print the resulting matrix after the addition.


### Program:
```
rows = int(input())
cols = int(input())

matrix1 = []
for _ in range(rows):
    while True:
        row = list(map(int, input().split()))
        if len(row) == cols:
            matrix1.append(row)
            break

matrix2 = []
for _ in range(rows):
    while True:
        row = list(map(int, input().split()))
        if len(row) == cols:
            matrix2.append(row)
            break

add_matrix = []
for i in range(rows):
    row = []
    for j in range(cols):
        row.append(matrix1[i][j] + matrix2[i][j])
    add_matrix.append(row)

print("Addition of matrices:")
for row in add_matrix:
    print(row)

```
### Output:

![LAB9 DAY1](https://github.com/user-attachments/assets/c2ca07d5-3d8f-4317-a104-5408768f761e)

### Result: 
Thus, the given program is implemented and executed successfully .

### EX: 9.2 LIST COMPREHENSION
### Aim: 
To write a Python class program that generates all even numbers between 200 and 300 and stores them in a list using list comprehension.

### Algorithm:
1. Define a class with a method to generate even numbers between 200 and 300.
2. Use list comprehension to generate even numbers.
3. Store the even numbers in a list.
4. Return or print the list of even numbers.

### Program:
```
class EvenNumberGenerator:
    def generate_even_numbers(self):
        even_numbers = [num for num in range(200, 301) if num % 2 == 0]
        return even_numbers

generator = EvenNumberGenerator()
even_numbers_list = generator.generate_even_numbers()
print("Even numbers between 200 and 300:", even_numbers_list)
```
### Output:
![LAB9 DAY2](https://github.com/user-attachments/assets/f519e84d-3918-4d57-9b05-7ccb177c4750)

### Result: 
Thus, the given program is implemented and executed successfully .

### EX: 9.3 ADVANCED LIST PROCESSING
### Aim:
To write a Python program to find the transpose of a matrix using list comprehension.
### Algorithm:
1. Accept the number of rows and columns for the matrix from the user.
2. Input the elements of the matrix.
3. Use list comprehension to compute the transpose of the matrix.
       o The transpose of a matrix is obtained by swapping rows and columns.
4. Display the transpose matrix.

### Program:
```
rows = int(input("Enter the number of rows: "))
cols = int(input("Enter the number of columns: "))

print("Enter the elements of the matrix:")
matrix = []
for i in range(rows):
    row = list(map(int, input().split()))
    matrix.append(row)

transpose_matrix = [[matrix[i][j] for i in range(rows)] for j in range(cols)]

print("The transpose of the matrix is:")
for row in transpose_matrix:
    print(row)

```
### Output:
![image](https://github.com/user-attachments/assets/4e0eed13-2ce1-4bb6-bfd4-b36e7a91b1cf)

### Result: 
Thus, the given program is implemented and executed successfully .
 


### EX: 9.4       TOEPLITZ MATRIX
### Aim: 
To write a Python program to check whether the given matrix is a Toeplitz matrix.

### Algorithm:

1. Accept the number of rows and columns of the matrix from the user.
2. Input the elements of the matrix.
3. Check if the matrix is a Toeplitz matrix:
    - A matrix is Toeplitz if every descending diagonal from left to right is constant (i.e., all elements in each diagonal are the same).
4. Return True if the matrix is Toeplitz, otherwise return False.


### Program:
```
rows = int(input("Enter the number of rows: "))
cols = int(input("Enter the number of columns: "))

print("Enter the elements of the matrix:")
matrix = []
for i in range(rows):
    row = list(map(int, input().split()))
    matrix.append(row)

def is_toeplitz(matrix, rows, cols):
    for i in range(rows - 1):
        for j in range(cols - 1):
            if matrix[i][j] != matrix[i + 1][j + 1]:
                return False
    return True

if is_toeplitz(matrix, rows, cols):
    print("The matrix is a Toeplitz matrix.")
else:
    print("The matrix is not a Toeplitz matrix.")

```
### Output:

![image](https://github.com/user-attachments/assets/d1347beb-db9e-43f0-a854-803a0eaf8ced)


### Result: 
Thus, the given program is implemented and executed successfully.
 

