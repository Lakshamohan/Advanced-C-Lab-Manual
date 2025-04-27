## EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

## Aim:
To write a C program to display stack elements using an array.
## Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
## Program:
```
#include<stdio.h>
int stack[100],size=3,top=-1,i;
void push (int data)
{if(top==size-1)
  {printf("stack is full\n");
   return;
  }
else
 stack[++top]=data;
}
void display()
{if(top==-1)
   printf("stack is empty\n");
 else
 {for(i=top;i>=0;i--)
   printf("%d\n",stack[i]);
 }
}
int pop ()
{if(top==-1)
   {printf("stack is empty\n");
   return -1;
   }
 else
   return stack[top--];
}
void peek()
{if(top==-1)
   printf("stack is empty\n");
 else
  printf("%d\n",stack[top]);
}
int main()
{push(10);
push(20);
push(30);
display();
peek();
push(40);
pop();
display();
pop();
pop();
display();
}
```
## Output:

![Screenshot 2025-04-27 164303](https://github.com/user-attachments/assets/92de8392-6197-457a-ac47-b3c6b2a51e18)


## Result:
Thus, the program to display stack elements using an array is verified successfully.
 

## EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
## Aim:
To create a C program to push the given element in to a stack using array.
## Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
## Program:
```
#include <stdio.h>

int size = 3, top = -1;
float stack[100];

void push(float data) {
    if (top == size - 1) {
        printf("Stack is full\n");
        return;
    }
    stack[++top] = data;
}

int main() {
    push(10.2);
    push(20.2);
    push(30.2);
    push(40.2); 

    for (int i = 0; i <= top; i++) {
        printf("%.2f\n", stack[i]);
    }

    return 0;
}

```
## Output:

![Screenshot 2025-04-27 164444](https://github.com/user-attachments/assets/f4d209aa-d0f5-4deb-a652-d23a8f5d0d0c)


## Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
## EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
## Aim:
To write a C program to display queue elements using array

## Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
## Program:
```
#include <stdio.h>

int front, rear, i;
float queue[50];


void enqueue(float data) {
    if (rear == 49) { 
        printf("Queue is full\n");
        return;
    }
    if (front == -1 && rear == -1) {
        front = rear = 0;
    } else {
        rear++;
    }
    queue[rear] = data;
}


void display() {
    if (rear == -1 && front == -1) {
        printf("No elements to display\n");
    } else {
        for (i = front; i <= rear; i++) {
            printf("%.1f\n", queue[i]);
        }
    }
}

int main() {
    rear = -1;
    front = -1;
    
    enqueue(100.5);
    enqueue(200.5);
    enqueue(300.5);
    
    display();

    return 0;
}
```
## Output:

![image](https://github.com/user-attachments/assets/75fef34b-29bd-4634-8f97-5cd7cb93d580)


## Result:
Thus, the program to display queue elements using array is verified successfully.


## EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
## Aim:
To write a C program to insert elements in queue using array.

## Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

## Program:
```
#include<stdio.h>
#define size 50
int front,rear;
float queue[size];
void enqueue(float data)
{if(rear==size-1)
  {printf("queue is full");
  }
else
 
  {if(front==-1 && rear==-1)
    {front=0;
     rear=0;
   }
   else
    rear++;
 queue[rear]=data;
  }
}
void display()
{if(front==-1 ||  front>rear)
  {printf("No elements to display\n");
  }
else
{ for(int i=front;i<=rear;i++)
   {printf("%.2f\n",queue[i]);
   }
}
}
int main()
{rear=-1; front=-1;
enqueue(100.5);
enqueue(200.5);
enqueue(300.5);
display();
}
```
## Output:

![Screenshot 2025-04-27 165156](https://github.com/user-attachments/assets/e193dcc7-1a3e-493f-bd3d-217282c097c6)


## Result:
Thus, the program to insert elements in queue using array is verified successfully.

 
## EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

## Aim:

To create a function in C that deletes an element from a queue implemented using an array.

## Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.

## Program:
```
int size=10;
int front=-1,rear=-1;
char queue[50];
void enqueue(char data)
{if(rear==size-1)
  {printf("queue is full");
  }
else
  {if(front==-1 && rear==-1)
    {front=0;
     rear=0;
   }
   else
    rear++;
 queue[rear]=data;
  }
}
void display()
{if(front==-1 ||  front>rear)
  {printf("No elements to display\n");
  }
else
{ for(int i=front;i<=rear;i++)
   {printf("%c\n",queue[i]);
   }
}
}

 void dequeue()
{
    if(front==-1||front>rear)
    {
        printf("Queue Underflow\n");
        return;
    }
    else
    {
        front=front+1;
    }
}

int main()
{rear=-1; front=-1;
enqueue('A');
enqueue('B');
enqueue('C');
enqueue('D');
display();
dequeue();
display();
}
```
## Output:

![image](https://github.com/user-attachments/assets/8891b966-7609-429c-9cd1-d00217ca2b08)


## Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
