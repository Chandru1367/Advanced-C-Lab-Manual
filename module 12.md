

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:

```C
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *ptr;
    ptr = head;
    while(ptr != NULL){
        printf("%.2f\n",ptr->data);
        ptr = ptr->next;
    }
}
```

Output:

<img width="659" height="430" alt="image" src="https://github.com/user-attachments/assets/ae3cb37d-9053-4d14-8f8f-73a25cebf1c4" />


Result:

Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.

Aim:

To write a C program to pop an element from the given stack using liked list.

Algorithm:

1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:

```C
struct Node   
{  
float data;  
struct Node *next;  
}*head;  

void pop()  
{
    struct Node *ptr;
    if (head == NULL){
        printf("stack is empty\n");
    }
    else{
        ptr=head;
        head = head->next;
        free(ptr);
    }
}
```

Output:

<img width="1105" height="527" alt="image" src="https://github.com/user-attachments/assets/4443790a-a064-48ae-84ce-fc1abf20fa65" />



Result:

Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.

Aim:

To write a C program to display queue elements using linked list.

Algorithm:

1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:

```C
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    struct Node *ptr;
    if (front == NULL){
        printf("queue is empty\n");
    }
    else{
        printf("Queue elements:\n");
    }
    ptr = front;
    while(ptr!=NULL){
        printf("%.3f\n",ptr->data);
        ptr = ptr->next;
    }
}
```
Output:

<img width="695" height="470" alt="image" src="https://github.com/user-attachments/assets/0dd29aea-44ab-4a69-8657-bcca24253742" />


Result:

Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:

To write a C program to insert elements in queue using linked list

Algorithm:

1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:

```C
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
    struct Node *n;
    n = (struct Node *)malloc(sizeof(struct Node));
    n->data = data;
    n->next = NULL;
    if (front == NULL){
        front = rear = n;
    }
    else{
        rear->next = n;
        rear = n;
    }
}
```

Output:


<img width="736" height="478" alt="image" src="https://github.com/user-attachments/assets/01092755-9c0e-4476-b448-8cd76d3f7a85" />


Result:

Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:

```C
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%.2f",front->data);
}
```

Output:


<img width="677" height="502" alt="image" src="https://github.com/user-attachments/assets/49479c89-10d0-47da-a623-95e7f6645e26" />


Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


