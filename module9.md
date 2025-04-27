EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

#include <stdio.h>
#define SIZE 5

int stack[SIZE];
int top = -1;

void display() {
    if (top == -1) {
        printf("Stack is empty\n");
    } else {
        printf("Stack elements:\n");
        for (int i = top; i >= 0; i--) {
            printf("%d\n", stack[i]);
        }
    }
}

int main() {
    stack[++top] = 10;
    stack[++top] = 20;
    stack[++top] = 30;

    display();
    return 0;
}


Output:

![image](https://github.com/user-attachments/assets/0a957603-2121-4b2b-b5a8-7b526115255b)




Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
#include <stdio.h>
#define SIZE 5

float stack[SIZE];
int top = -1;

void push(float value) {
    if (top == SIZE - 1) {
        printf("Stack Overflow\n");
    } else {
        stack[++top] = value;
        printf("Pushed %.2f\n", value);
    }
}

int main() {
    push(10.5);
    push(20.7);
    push(30.2);
    return 0;
}



Output:

![image](https://github.com/user-attachments/assets/28df0a3d-bcd2-421c-b1fb-a5943b9eefd1)


Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

#include <stdio.h>
#define SIZE 5

int queue[SIZE];
int front = -1, rear = -1;

void display() {
    if (front == -1) {
        printf("Queue is empty\n");
    } else {
        printf("Queue elements:\n");
        for (int i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
        printf("\n");
    }
}

int main() {
    front = 0;
    queue[++rear] = 10;
    queue[++rear] = 20;
    queue[++rear] = 30;

    display();
    return 0;
}


Output:

![image](https://github.com/user-attachments/assets/88c8d44a-cc89-4145-9d24-4cc0f92aa468)



Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

#include <stdio.h>
#define SIZE 5

float queue[SIZE];
int front = -1, rear = -1;

void enqueue(float val) {
    if (rear == SIZE - 1) {
        printf("Queue Overflow\n");
    } else {
        if (front == -1) front = 0;
        queue[++rear] = val;
        printf("Inserted %.2f\n", val);
    }
}

int main() {
    enqueue(12.3);
    enqueue(45.6);
    enqueue(78.9);
    return 0;
}


Output:

![image](https://github.com/user-attachments/assets/becf4b4c-dbb0-4418-b35a-02b824dbf1d1)


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

#include <stdio.h>
#define SIZE 5

int queue[SIZE];
int front = -1, rear = -1;

void dequeue() {
    if (front == -1) {
        printf("Queue is empty\n");
    } else {
        printf("Deleted element: %d\n", queue[front]);
        front++;
        if (front > rear) {
            front = rear = -1;
        }
    }
}

int main() {
    // Initial queue setup
    front = 0;
    queue[++rear] = 100;
    queue[++rear] = 200;

    dequeue(); // should delete 100
    dequeue(); // should delete 200
    dequeue(); // should print "empty"
    return 0;
}

Output:

![image](https://github.com/user-attachments/assets/6a71d48d-3e3c-4493-9482-1819588941a7)



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
