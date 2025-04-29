EX-21-POINTERS
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
    float number = 23.65;
    float *ptr = &number;

    printf("Original number: %.2f\n", *ptr);

    *ptr = 25.0;

    printf("Modified number: %.2f\n", *ptr);

    return 0;
}
```

## OUTPUT:
 	

![438643590-af9d2958-fe1d-4253-9401-f5ca5b753c07](https://github.com/user-attachments/assets/24d83231-28e5-4af0-9e2b-0e0cf88aec3d)










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

long long int product(int n) {
    
    if (n == 1) {
        return 1;
    }
    
    return n * product(n - 1);
}

int main() {
    int n = 12;

    long long int result = product(n);
    printf("The product of first %d natural numbers is: %lld\n", n, result);

    return 0;
}

```
## OUTPUT:

![438643839-200738f6-4911-47f0-81bc-924f0997a652](https://github.com/user-attachments/assets/9bf964c2-cc53-4a9e-bd99-92a510900224)


         		
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
    int m, n;

    printf("Enter the number of rows: ");
    scanf("%d", &m);
    printf("Enter the number of columns: ");
    scanf("%d", &n);

    int matrix[m][n];

    printf("Enter the elements of the matrix:\n");
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    for (int i = 0; i < m; i++) {
        int row_sum = 0;
        for (int j = 0; j < n; j++) {
            row_sum += matrix[i][j];
        }
        printf("Sum of row %d is: %d\n", i + 1, row_sum);
    }

    return 0;
}


```



## OUTPUT


 ![438643947-15439e7f-26fa-41ac-9a16-7b9e8d5c9c22](https://github.com/user-attachments/assets/6fcd4fe7-ac79-44a8-981b-e9c0f3c04d99)

 

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
    int rows;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    
    str[strcspn(str, "\n")] = '\0';

    printf("Enter number of rows: ");
    scanf("%d", &rows);

    int length = strlen(str);  
    for (int i = 1; i <= rows; i++) {
       
        for (int j = 1; j <= rows - i; j++) {
            printf(" ");
        }

        for (int j = 0; j < i; j++) {
            printf("%c ", str[j % length]);  
        }

        printf("\n");
    }

    return 0;
}
```

 ## OUTPUT


![438644052-0b950a5f-5829-4f4f-a2de-1b423685bbd7](https://github.com/user-attachments/assets/851f241e-9b87-4081-9813-bdd47e08ebd9)



## RESULT

Thus the C program to String process executed successfully
 

 





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
        scanf("%d", ptr + i);  
    }

    printf("The entered array elements are:\n");
    for (int i = 0; i < 6; i++) {
        printf("%d ", *(ptr + i));  
    }

    printf("\n");

    return 0;
}
```

## OUTPUT

 ![438644201-a456ac6e-5bba-4736-ba6f-78d981af5f76](https://github.com/user-attachments/assets/9736412b-f2a6-408e-a0a0-19384d338613)


## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


