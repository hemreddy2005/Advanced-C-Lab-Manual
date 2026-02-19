# EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
# Aim:
To write a C program for passing structure as function and returning a structure from a function

# Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
# Program:

```
#include <stdio.h>
struct numbers
{
    int a;
    int b;
    int sum;
};
struct numbers add(struct numbers n);
int main()
{
    struct numbers n, result;
    printf("Enter value for a: ");
    scanf("%d", &n.a);
    printf("Enter value for b: ");
    scanf("%d", &n.b);
    result = add(n);
    printf("\nValue of a: %d", result.a);
    printf("\nValue of b: %d", result.b);
    printf("\nSum: %d", result.sum);
    return 0;
}
struct numbers add(struct numbers n)
{
    n.sum = n.a + n.b;
    return n;
}
```

# Output:

<img width="567" height="214" alt="image" src="https://github.com/user-attachments/assets/8afe7f73-ea36-4a06-a9da-1c47411401a8" />

# Result:

Thus, the program is verified successfully
