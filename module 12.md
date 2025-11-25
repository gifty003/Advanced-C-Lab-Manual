## EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
# NAME: GIFTSON RAJARATHINAM N
# REG NO: 212222233002
### Aim:
To write a C program to display stack elements using linked list.

### Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
### Program:

```c
struct Node
{
float data;
struct Node *next;
}*head;
void display()
{
struct Node *p; p=head; while(p!=NULL)
{
printf("%.2f\n",p->data); p=p->next;
}
}
```
### Output:

<img width="389" height="317" alt="image" src="https://github.com/user-attachments/assets/1b1eb0c7-7ce8-4250-a6b6-21a62d517486" />



### Result:
Thus, the program to display stack elements using linked list is verified successfully. 



## EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
### Aim:
To write a C program to pop an element from the given stack using liked list.

### Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
### Program:
```c
struct Node
{
float data;
struct Node *next;
}*head; void pop()
{
if(head==NULL)
{
printf("stack is empty");
}
else
{
head=head->next;
}
}
```
### Output:
<img width="1063" height="259" alt="image" src="https://github.com/user-attachments/assets/a1204932-6e57-4679-bda4-9ab409407a02" />


### Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
## EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
### Aim:
To write a C program to display queue elements using linked list.
### Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
### Program:
```c
struct Node
{
int data;
struct Node *next;
}*front=NULL,*rear=NULL; void display()
{
if(front==NULL)
{
printf("queue is empty");
}
else
{
printf("queue elements:\n"); while(front!=NULL)
{
printf("%c\n",front->data); front=front->next;
}
}
}
```

### Output:
<img width="508" height="371" alt="image" src="https://github.com/user-attachments/assets/ad889baf-2294-4507-9b06-21a3eede92af" />


### Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
## EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

### Aim:
To write a C program to insert elements in queue using linked list

### Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
### Program:
```c
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(char data)
{
    struct Node *ptr=(struct Node *)malloc (sizeof(struct Node));
    ptr->data=data;
    struct Node *p=front;
    if(front==NULL)
    {
        front=rear=ptr;
    }
    else
    {
        while(p->next!=NULL)
        {
            p=p->next;
        }
        p->next=ptr;
        ptr->next=NULL;
    }
}
```

### Output:

<img width="528" height="372" alt="image" src="https://github.com/user-attachments/assets/8f0527ba-f1bd-484b-8475-4373da322692" />


### Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



## EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.

### Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

### Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

### Program:
```c
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%c",front->data);
}

```
### Output:
<img width="369" height="368" alt="image" src="https://github.com/user-attachments/assets/5bdb591e-f066-423d-8951-e45d973fa539" />


### Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.
