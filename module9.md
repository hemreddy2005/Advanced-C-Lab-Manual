## EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

# Aim:

To write a C program to display stack elements using an array.

# Algorithm:

1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
# Program:

```c
#include <stdio.h>
#define MAX 5
int stack[MAX];
int top = -1;
void push(int value) {
    if(top == MAX - 1) {
        printf("Stack Overflow\n");
    } else {
        stack[++top] = value;
    }
}
void display() {
    if(top == -1) {
        printf("Stack is Empty\n");
    } else {
        printf("Stack Elements:\n");
        for(int i = top; i >= 0; i--) {
            printf("%d\n", stack[i]);
        }
    }
}
int main() {
    push(10);
    push(20);
    push(30);
    display();
    return 0;
}
```

# Output:

<img width="626" height="251" alt="image" src="https://github.com/user-attachments/assets/5d826975-d790-4260-a7be-09d75625e082" />

# Result:

Thus, the program to display stack elements using an array is verified successfully.
 

## EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.

# Aim:

To create a C program to push the given element in to a stack using array.

# Algorithm:

1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
# Program:

```c
#include <stdio.h>
#define MAX 5
float stack[MAX];
int top = -1;
void push(float value) {
    if(top == MAX - 1) {
        printf("Stack Overflow\n");
    } else {
        stack[++top] = value;
        printf("%.2f pushed into stack\n", value);
    }
}
int main() {
    push(12.5);
    push(7.8);
    push(3.4);
    return 0;
}
```

# Output:

<img width="612" height="216" alt="image" src="https://github.com/user-attachments/assets/46e80bce-cbb6-4015-a331-8c4261bcdfac" />

# Result:

Thus, the program to push the given element in to a stack using array is verified successfully

 
## EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.

# Aim:

To write a C program to display queue elements using array

# Algorithm:

1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
# Program:

```c
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = 0, rear = -1;

void enqueue(int value) {
    if(rear == MAX - 1) {
        printf("Queue Overflow\n");
    } else {
        queue[++rear] = value;
    }
}

void display() {
    if(front > rear) {
        printf("Queue is Empty\n");
    } else {
        printf("Queue Elements:\n");
        for(int i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
    }
}

int main() {
    enqueue(5);
    enqueue(15);
    enqueue(25);

    display();
    return 0;
}

```

# Output:

<img width="642" height="240" alt="image" src="https://github.com/user-attachments/assets/80ae30d0-be5d-4950-8bf5-f9fd6745f8fb" />

# Result:

Thus, the program to display queue elements using array is verified successfully.


## EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.

# Aim:

To write a C program to insert elements in queue using array.

# Algorithm:

1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

# Program:

```c
#include <stdio.h>
#define MAX 5

float queue[MAX];
int front = 0, rear = -1;

void enqueue(float value) {
    if(rear == MAX - 1) {
        printf("Queue Overflow\n");
    } else {
        queue[++rear] = value;
        printf("%.2f inserted into queue\n", value);
    }
}

int main() {
    enqueue(10.5);
    enqueue(20.2);
    enqueue(30.8);

    return 0;
}

```

# Output:

<img width="555" height="202" alt="image" src="https://github.com/user-attachments/assets/d21c5ec6-0116-42d2-b2ad-6ccbab23df41" />

# Result:

Thus, the program to insert elements in queue using array is verified successfully.

 
## EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

# Aim:

To create a function in C that deletes an element from a queue implemented using an array.

# Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.

# Program:

```c
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = 0, rear = -1;

void enqueue(int value) {
    if(rear == MAX - 1) {
        printf("Queue Overflow\n");
    } else {
        queue[++rear] = value;
    }
}

void dequeue() {
    if(front > rear) {
        printf("Queue is Empty\n");
    } else {
        printf("Deleted Element: %d\n", queue[front]);
        front++;
        if(front > rear) {
            front = rear = -1;
        }
    }
}

int main() {
    enqueue(10);
    enqueue(20);
    enqueue(30);

    dequeue();
    dequeue();

    return 0;
}

```

# Output:

<img width="561" height="175" alt="image" src="https://github.com/user-attachments/assets/92f59583-7898-47ce-9ce9-becc439acedb" />

# Result:

Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
