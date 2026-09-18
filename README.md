# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M5
## IAPR-5- Module 5 - FoC
## NAME : TAMIZHAN B
## DATE : 17/09/2026
### 9. Implementation of recursion.

### 10. Implementation of programs using pointer arithmetic.

---

# Ex.No:21

Aim:
To write a C program to check whether the number 1333 is even or odd using pointers.

Algorithm:

Step 1: Start

Step 2: Include the standard input-output library:
#include <stdio.h>

Step 3: Declare an integer variable num and an integer pointer ptr.

Step 4: Read the number from the user using scanf().

Step 5: Assign the address of num to the pointer ptr.

Step 6: Use the pointer to access the value of num.

Step 7: Check whether *ptr % 2 == 0.

If true, print 1333 is even.
Otherwise, print 1333 is odd.

Step 8: Stop.

Program:
```
#include <stdio.h>

int main()
{
    int num;
    int *ptr;

    scanf("%d", &num);

    ptr = &num;

    if (*ptr % 2 == 0)
        printf("%d is even.", *ptr);
    else
        printf("%d is odd.", *ptr);

    return 0;
}
```
## Output:

```
1333
1333 is odd.
533
533 is odd.
```

## Result:

Thus, the program was implemented and executed successfully, and the required output was obtained.

---

# Ex.No:22

Aim:
To write a C program to print the opposite diagonal elements of a 3 × 3 matrix.

Algorithm:

Step 1: Start

Step 2: Include the standard input-output library:
#include <stdio.h>

Step 3: Declare a 3 × 3 integer matrix.

Step 4: Read the number of rows and columns.

Step 5: Read the elements of the matrix using nested for loops.

Step 6: Print the opposite diagonal elements. For a 3 × 3 matrix, these are:

a[0][2]
a[1][1]
a[2][0]

Step 7: Stop.

Program:
```
#include <stdio.h>

int main()
{
    int a[3][3], rows, cols, i, j;

    scanf("%d%d", &rows, &cols);

    for (i = 0; i < rows; i++)
    {
        for (j = 0; j < cols; j++)
        {
            scanf("%d", &a[i][j]);
        }
    }

    printf("The Diagonal Elements of a Matrix = ");

    for (i = 0; i < rows; i++)
    {
        printf("%d ", a[i][cols - 1 - i]);
    }

    return 0;
}
```

## Output:

```
3 3
1 2 3
4 5 6
7 8 9
The Diagonal Elements of a Matrix = 3 5 7

```

## Result:

Thus, the program was implemented and executed successfully, and the required output was obtained.

---

# Ex.No:23
Aim:
To write a C program to read a month number and display the number of days in that month using a switch case statement.

Algorithm:

Step 1: Start

Step 2: Include the standard input-output library:
#include <stdio.h>

Step 3: Inside the main() function, declare an integer variable month.

Step 4: Read the month number from the user using scanf().

Step 5: Use a switch case statement:

Cases 1, 3, 5, 7, 8, 10, 12: Print 31 days.
Case 4, 6, 9, 11: Print 30 days.
Case 2: Print February -28 days. and in leap year The February month Have 29 days.
Default: Print invalid Month number. and Please try again ....

Step 6: Stop.

Program:
```
#include <stdio.h>

int main()
{
    int month;

    scanf("%d", &month);

    switch (month)
    {
        case 1:
        case 3:
        case 5:
        case 7:
        case 8:
        case 10:
        case 12:
            printf("31 days.");
            break;

        case 4:
        case 6:
        case 9:
        case 11:
            printf("30 days.");
            break;

        case 2:
            printf("February -28 days.\n");
            printf("in leap year The February month  Have 29 days.");
            break;

        default:
            printf("invalid Month number.\n");
            printf("Please try again ....");
    }

    return 0;
}
```

## Output:

```
10
31 days. 
2
February -28 days. 
in leap year The February month  Have 29 days.
11
30 days.
13
invalid Month number.
Please try again ....

```

## Result:

Thus, the program was implemented and executed successfully, and the required output was obtained.

---

# Ex.No:24

Aim:
To write a C program to check whether a given character is a digit or not without using any built-in function.

Algorithm:

Step 1: Start

Step 2: Include the standard input-output library:
#include <stdio.h>

Step 3: Declare a character variable ch.

Step 4: Read a character from the user using scanf().

Step 5: Check whether the character is between '0' and '9'.

If true, print the given character is digit: followed by the character.
Otherwise, print the given character is not digit: followed by the character.

Step 6: Stop.

Program:
```
#include <stdio.h>

int main()
{
    char ch;

    scanf("%c", &ch);

    if (ch >= '0' && ch <= '9')
        printf("the given character is digit: %c", ch);
    else
        printf("the given character is not digit: %c", ch);

    return 0;
}
```

## Output:

```	
5
the given character is digit: 5
h
the given character is not digit: h
```

## Result:

Thus, the program was implemented and executed successfully, and the required output was obtained.

---

# Ex.No:25
Aim:
To write a C program to print the even numbers in a given range using recursion.

Algorithm:

Step 1: Start

Step 2: Include the standard input-output library:
#include <stdio.h>

Step 3: Define a recursive function printEven(start, end).

Step 4: Check whether start is greater than end.

If true, return from the function.

Step 5: Check whether start is even using start % 2 == 0.

If true, print start.

Step 6: Call the function recursively with start + 1.

Step 7: In the main() function, read the starting and ending values.

Step 8: Call the recursive function.

Step 9: Stop.

Program:
```
#include <stdio.h>

void printEven(int start, int end)
{
    if (start > end)
        return;

    if (start % 2 == 0)
        printf("%d ", start);

    printEven(start + 1, end);
}

int main()
{
    int start, end;

    scanf("%d%d", &start, &end);

    printf("Even Numbers from %d to %d are: ", start, end);

    printEven(start, end);

    return 0;
}

```

## Output:

```
1 10
Even Numbers from 1 to 10 are: 2 4 6 8 10
2 20
Even Numbers from 2 to 20 are: 2 4 6 8 10 12 14 16 18 20
10 19
Even Numbers from 10 to 19 are: 10 12 14 16 18
```

## Result:

Thus, the program was implemented and executed successfully, and the required output was obtained.
