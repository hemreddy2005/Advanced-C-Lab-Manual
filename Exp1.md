# EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

# Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

# Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
# Program:

```
#include <stdio.h>
struct eligible
{
    int age;
    char n[50];
};
int main()
{
    struct eligible e[10];
    int i, num;
    printf("Enter number of persons: ");
    scanf("%d", &num);
    for(i = 0; i < num; i++)
    {
        printf("\nEnter details for person %d\n", i + 1);
        printf("Enter Name: ");
        scanf("%s", e[i].n);
        printf("Enter Age: ");
        scanf("%d", &e[i].age);
    }
    printf("\n----- Vaccine Eligibility Details -----\n");
    for(i = 0; i < num; i++)
    {
        printf("\nName: %s", e[i].n);
        printf("\nAge: %d", e[i].age);
        if(e[i].age <= 6)
            printf("\nVaccine Eligibility: No\n");
        else
            printf("\nVaccine Eligibility: Yes\n");
    }
    return 0;
}
```

# Output:

<img width="873" height="491" alt="image" src="https://github.com/user-attachments/assets/8ccf4c8b-4fc0-493c-82c1-089fdf175d92" />

# Result:

Thus, the program is verified successfully.
