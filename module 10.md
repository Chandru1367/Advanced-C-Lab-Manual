EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.

Aim:

To write a C program to search a given element in the given linked list.

Algorithm:

1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

```c
struct Node{
    char data; 
    struct Node *next;
}*head;

void search(char data)
{
    struct Node *temp;
    temp = head;
    int flag = 1;
    int i=0;
    int value = data;
    while (temp != NULL){
        if (temp->data == value){
            printf("item %c found at location %d",temp->data,i+1);
            flag = 0;
            break;
        }
        else{
            temp = temp->next;
            i++;
        }
    }
    if (flag == 1){
        printf("Item not found");
    }
 
 
 
 
}
```

Output:

<img width="866" height="547" alt="image" src="https://github.com/user-attachments/assets/781733b4-7538-4d50-813c-8a31222da1bf" />


Result:

Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.

Aim:

To write a C program to insert a node in a linked list.

Algorithm:

1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:
```c
struct Node{
    char data; 
    struct Node *next;
}*head;


void insert(char value)
{
    struct Node *temp;
    struct Node *n = (struct Node *)malloc(sizeof(struct Node));
    n->data = value;
    n->next = NULL;
    if (head == NULL){
        head = n;
        return;
    }
    temp = head;
    while (temp->next != NULL){
        temp = temp->next; 
    }
    temp->next = n;
    
}
```

Output:

<img width="698" height="563" alt="image" src="https://github.com/user-attachments/assets/43f9fc74-ebe4-476d-9f63-877154f29222" />

 
Result:

Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST

Aim:

To write a C program to traverse a doubly linked list.

Algorithm:

1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

```c
struct Node
{
    struct Node *prev;
    struct Node *next;
    char data;
}*head;

void display()
{
    struct Node *ptr;
    ptr = head;
    while (ptr != NULL){
        printf("%c ",ptr->data);
        ptr = ptr->next;
    }
}
```

Output:

<img width="690" height="538" alt="image" src="https://github.com/user-attachments/assets/3fabf7ea-b8aa-471f-b649-f538d29e3f9c" />


Result:

Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST

Aim:

To write a C program to insert an element in doubly linked list

Algorithm:

1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:

```c
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void insert(float data)
{
    struct Node *ptr,*temp;
    ptr = (struct Node *)malloc(sizeof(struct Node));
    if (ptr == NULL){
        printf("OVERFLOW\n");
    }
    else{
        ptr->data = data;
        if (head == NULL){
            ptr->next = NULL;
            ptr->prev = NULL;
            head = ptr;
        }
        else{
            temp = head;
            while(temp->next != NULL){
                temp = temp->next;
            }
            temp->next = ptr;
            ptr->prev = temp;
            ptr->next = NULL;
        }
    }
    
}
```

Output:

<img width="994" height="536" alt="image" src="https://github.com/user-attachments/assets/a39adfad-fd7c-40b1-8919-f1ddcfddcda0" />


Result:

Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:

To write a C function that deletes a given element from a linked list.

Algorithm:

1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:

```c
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void display()
{
    struct Node *ptr;
    ptr = head;
    while(ptr != NULL){
        printf("%.2f ",ptr->data);
        ptr = ptr->next;
    }
}

void insert(float data)
{
    struct Node *ptr,*temp;
    ptr = (struct Node *)malloc(sizeof(struct Node));
    if (ptr == NULL){
        printf("OVERFLOW\n");
    }
    else{
        ptr->data = data;
        if (head == NULL){
            ptr->next = NULL;
            ptr->prev = NULL;
            head = ptr;
        }
        else{
            temp = head;
            while (temp->next != NULL){
                temp = temp->next;
            }
            temp->next = ptr;
            ptr->prev = temp;
            ptr->next = NULL;
        }
    }
}

void search(float data)
{
    struct Node *ptr;
    int flag = 1,i=0;
    float val = data;
    ptr = head;
    while (ptr != NULL){
        if (ptr->data == val){
            printf("item %.2f found at location %d\n",ptr->data,i+1);
            flag = 0;
            break;
        }
        else{
            ptr = ptr->next;
            i++;
        }
    }
    if (flag == 1){
        printf("Item not found\n");
    }
}

void delete()
{
    struct Node *ptr;
    if (head == NULL){
        printf("UNDERFLOW\n");
    }
    else if(head->next == NULL){
        head = NULL;
        free(head);
        printf("Node deleted\n");
    }
    else{
        ptr = head;
        head = head->next;
        head->prev = 0;
        free(ptr);
        printf("Node deleted\n");
    }
}
```
Output:

<img width="1120" height="710" alt="image" src="https://github.com/user-attachments/assets/6b4e8585-5aa6-43a4-91ff-f403a5593d59" />


Result:

Thus, the function that deletes a given element from a linked list is verified successfully.





