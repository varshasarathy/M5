# EX-21-POINTERS

# AIM:
Write a C program to convert a 23.65 into 25 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (23.65).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 25.0.
4.	Print the modified value.

## PROGRAM:
```
#include <stdio.h>

int main() {
    float num = 23.65;
    float *ptr = &num;

    *ptr = 25.0;

    printf("Converted value: %.2f\n", num);

    return 0;
}
```
## OUTPUT:
 	
![437917689-012c6efa-a1b5-4d1c-b868-c948919055cf](https://github.com/user-attachments/assets/3a49f2fd-a754-42f7-be52-79b4651c8d06)


## RESULT:
Thus the program to convert a 23.65 into 25 using pointer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Product of first 12 natural numbers using Recursion

## ALGORITHM:

1.	Define a recursive function calculateProduct that takes an integer parameter n.
2.	Return n multiplied by the result of the calculateProduct function called with n - 1.
3.	Declare an integer variable n and an unsigned long long variable product.
4.	Initialize n with the value 12 (for the first 12 natural numbers).
5.	Call the calculateProduct function with n and store the result in the product variable.
6.	Print the result, indicating it is the product of the first 12 natural numbers.

## PROGRAM:
```
#include <stdio.h>

long long product(int n) {
    static long long result = 1;
    if (n > 0) {
        result *= n;
        product(n - 1);
    }
    return result;
}

int main() {
    int n = 12;
    printf("Product of first %d natural numbers is: %lld\n", n, product(n));
    return 0;
}
```
## OUTPUT:

![437918139-ca62a145-9450-4300-b956-819afaf79984](https://github.com/user-attachments/assets/9ad1078b-6bed-464e-a898-a74f6cdeb061)
        		
## RESULT:

Thus the program has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write C Program to find Sum of each row of a Matrix

## ALGORITHM:

1.	Declare and initialize the matrix with the desired values.
2.	Create a loop to iterate through each row of the matrix.
3.	Inside the loop, calculate the sum of the elements in each row.
4.	Print the sum for each row.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int rows, cols, i, j;
    printf("Enter the number of rows: ");
    scanf("%d", &rows);
    printf("Enter the number of columns: ");
    scanf("%d", &cols);

    int matrix[rows][cols];
    printf("Enter the elements of the matrix:\n");
    for (i = 0; i < rows; i++) {
        for (j = 0; j < cols; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }
    for (i = 0; i < rows; i++) {
        int sum = 0;
        for (j = 0; j < cols; j++) {
            sum += matrix[i][j];
        }
        printf("Sum of row %d is: %d\n", i + 1, sum);
    }

    return 0;
}
```


## OUTPUT

![437918746-6f8645a2-43c4-4687-bfaf-07c9d729c60a](https://github.com/user-attachments/assets/267e855b-aeae-406c-9f7e-448b4a4cf72d)

 ## RESULT
 


# EX-24-STRINGS

## AIM:

Write C program for the below pyramid string pattern. Enter a string: PROGRAM Enter number of rows: 5 P R O G R A M P R O G R A M P R O G R A M

## ALGORITHM:

1.	Input the number of rows for the pyramid (e.g., num_rows).
2.	Initialize variables:i for the row count (starting from 1),j for the character count (starting from 1)
3.	Start a loop for i from 1 to num_rows (for each row of the pyramid).
4.	Calculate the midpoint position as midpoint = (2 * num_rows - 1) / 2.
5.	End the program.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int rows, i, j, len;
    printf("Enter a string: ");
    scanf("%s", str);

    printf("Enter number of rows: ");
    scanf("%d", &rows);

    len = strlen(str);
    for (i = 1; i <= rows; i++) {
        for (j = 0; j < i; j++) {
            printf("%c ", str[j % len]); 
        }
        printf("\n");
    }

    return 0;
}
```
 ## OUTPUT
![437918997-82416810-0009-4cb7-9976-41b26f2d0302](https://github.com/user-attachments/assets/6a3c7d4a-e77e-4b08-ac06-90b25cee7fa8)

## RESULT

Thus the C program to String process executed successfully
 

 
.



# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to read and display an array of any 6 integer elements using pointer

## ALGORITHM
Step 1: Start the program.
Step 2: Declare the following:
•	Integer variable i for iteration.
•	Integer variable n to store the number of elements.
•	Integer array arr[10] to hold up to 10 elements.
•	Integer pointer parr and initialize it to point to the array arr.
Step 3: Read the value of n (number of elements) from the user.
Step 4: Loop from i = 0 to i < n:
•	Read an integer value and store it in the address parr + i using pointer arithmetic.
Step 5: Loop from i = 0 to i < n:
•	Print the element at *(parr + i) using pointer dereferencing.
Step 6: End the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int arr[6];
    int *ptr = arr;

    printf("Enter 6 integers:\n");
    for (int i = 0; i < 6; i++) {
        scanf("%d", (ptr + i));
    }

    printf("The entered elements are:\n");
    for (int i = 0; i < 6; i++) {
        printf("%d ", *(ptr + i));
    }

    printf("\n");

    return 0;
}
```
## OUTPUT

 ![437919418-5911289a-ef24-49ec-9025-4f86e7be6de9](https://github.com/user-attachments/assets/fbc12eaa-2aed-46cd-b7c8-0bcd0f2e7c02)

## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


