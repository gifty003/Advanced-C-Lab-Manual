# EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.
# NAME: GIFTSON RAJARATHINAM N 
# REG NO: 212222233002
## Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

## Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
## Program:
```c
#include<stdio.h>
struct eligib
{
   int age;
   char n[4];
};
int main()
{
   struct eligib e;
   scanf("%d%s",&e.age,e.n);
   if(e.age<=6)
   {
     printf("Age:%d\nName:%svaccine:%d\neligibility:no",e.age,e.n,e.age);
   }
  else
  {
     printf("Age:%d\nName:%svaccine:%d\neligibility:yes",e.age,e.n,e.age);
  }
}
```


## Output:

![image](https://github.com/user-attachments/assets/2cfad7f9-a3fb-4df1-a7df-1c7224f0af48)



## Result:
Thus, the program is verified successfully. 



# EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
## Aim:
To write a C program for passing structure as function and returning a structure from a function

## Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
## Program:
```c
#include<stdio.h>
struct numbers
{
   int a;
   int b;
}n;
int add(struct numbers n);
int main()
{
   scanf("%d %d ",&n.a,&n.b);
   printf("%d",add(n));
}
int add(struct numbers n)
{
    return n.a+n.b;
}

```
## Output:
![image](https://github.com/user-attachments/assets/a912c4e0-a539-4abb-b75d-ac5b2e7e9fe8)

## Result:
Thus, the program is verified successfully


 
# EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

## Aim:
To write a C program to read a file name from user

## Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
## Program:
```c
#include <stdio.h>
int main()
{
   FILE *p;
   char name[30];
   scanf("%s",name);
   printf("%s File Created Successfully",name);
   p=fopen("name","w");
   printf("\n%s File Opened",name);
   fclose(p);
   printf("\n%s File Closed",name);
}
```
## Output:

<img width="946" height="325" alt="Screenshot 2025-11-18 134903" src="https://github.com/user-attachments/assets/8ee235e1-63c8-4926-941b-b15e65c90391" />


## Result:
Thus, the program is verified successfully
 


# EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
## Aim:
To write a C program to read, a file and insert text in that file
## Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
## Program:
```c
#include <stdio.h>
int main()
{
   FILE *p;
   char name[20];
   int num;
   char text[50];
   scanf("%s%d",name,&num);
   p=fopen("name","w");
   printf("%s Opened",name);
   for(int i=0;i<num;i++)
   {
      scanf("%s",text);
      fputs(text,p);
   }
   printf("\nData added Successfully");

}
```
## Output:

![image](https://github.com/user-attachments/assets/3baf2414-bb13-4a8a-81c9-cd5792311b62)

## Result:
Thus, the program is verified successfully



# Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

## Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

## Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

## Program:
```c
#include <stdio.h>
#include <stdlib.h>
struct Subject
{
    char name[20];
    int marks;
};
int main()
{
    int i,n;
    scanf("%d",&n);
    struct Subject *s = (struct Subject *)malloc(n*sizeof(struct Subject));
    if(s==NULL)
    {
        printf("Memory Alocation Failed\n");
        return 1;
    }
    for(i=0;i<n;i++)
    {
        scanf("%s %d",s[i].name,&s[i].marks);
    }
    for(i=0;i<n;i++)
    {
        printf("%s  %d\n",s[i].name,s[i].marks);
    }
    free (s);
    return 0;
}
```
## Output:

![image](https://github.com/user-attachments/assets/e9c8ca61-aa99-49be-a68a-56c21bdd0829)

## Result:
Thus, the program is verified successfully

# EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
# NAME: GIFTSON RAJARATHINAM N
# REG NO: 212222233002
### Aim:
### To write a C program print the lowercase English word corresponding to the number
### Algorithm:
1.	Start 
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
### Program:
```c
#include <stdio.h>

int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    switch (n) {
        case 5:
            printf("seventy one\n");
            break;
        case 6:
            printf("seventy two\n");
            break;
        case 7:
            printf("seventy three\n");
            break;
        case 8:
            printf("seventy four\n");
            break;
        case 9:
            printf("seventy five\n");
            break;
        case 10:
            printf("seventy six\n");
            break;
        case 11:
            printf("seventy seven\n");
            break;
        case 12:
            printf("seventy eight\n");
            break;
        case 13:
            printf("seventy nine\n");
            break;
        default:
            printf("Greater than 13\n");
            break;
    }

    return 0;
}

```
### Output:


<img width="483" height="194" alt="image" src="https://github.com/user-attachments/assets/3bbbfb26-3a2f-4452-8fbb-73dbaf1922e2" />



### Result:
Thus, the program is verified successfully
 
# EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .

### Aim:
### To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
### Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
### Program:
```c
#include <stdio.h>

int main() {
    char a[50];
    int h, c, i;

    
    printf("Enter the string (digits 0-9): ");
    scanf("%s", a);

    for (h = 0; h <= 3; h++) {
        c = 0; 

        for (i = 0; a[i] != '\0'; i++) {
            if (a[i] - '0' == h) {  
                c++;
            }
        }

        printf("%d ", c);
    }

    printf("\n"); 
    return 0;
}

```


### Output:


<img width="530" height="265" alt="image" src="https://github.com/user-attachments/assets/19e81c69-8ddc-4982-9b82-3ec372e3decf" />


### Result:
Thus, the program is verified successfully

# EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
### Aim:
### To write a C program to print all of its permutations in strict lexicographical order.

### Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
### Program:
```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int next_permutation(char *str) {
    int i = strlen(str) - 2;
    while (i >= 0 && str[i] >= str[i + 1]) {
        i--;
    }
    if (i < 0) return 0; 
    int j = strlen(str) - 1;
    while (str[j] <= str[i]) {
        j--;
    }
    char temp = str[i];
    str[i] = str[j];
    str[j] = temp;
    
    int left = i + 1, right = strlen(str) - 1;
    while (left < right) {
        temp = str[left];
        str[left] = str[right];
        str[right] = temp;
        left++;
        right--;
    }
    return 1;
}

int main() {
    char str[50];
        printf("Enter a string: ");
    scanf("%s", str);
    qsort(str, strlen(str), sizeof(char), (int(*)(const void*, const void*))strcmp);
    do {
        printf("%s\n", str);
    } while (next_permutation(str));

    return 0;
}

```


### Output:


<img width="541" height="369" alt="image" src="https://github.com/user-attachments/assets/8382b964-539f-49c5-bbe5-7df63ef004cb" />






### Result:
Thus, the program is verified successfully
 
# EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW.
### Aim:
### To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
### Program:
```c
#include <stdio.h>

int main() {
    int n, i, j;
    printf("Enter the value of n: ");
    scanf("%d", &n);
    for (i = 0; i < 2 * n - 1; i++) {   
        for (j = 0; j < 2 * n - 1; j++) { 
            int min = i < j ? i : j;  
            min = min < (2 * n - 2 - i) ? min : (2 * n - 2 - i); 
            min = min < (2 * n - 2 - j) ? min : (2 * n - 2 - j); 
            printf("%d ", n - min);
        }
        printf("\n"); 
    }

    return 0;
}

```
### Output:


<img width="736" height="572" alt="image" src="https://github.com/user-attachments/assets/817f08d5-7696-4f9e-8de2-f83f9ae30a2a" />






### Result:
Thus, the program is verified successfully

# EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

### Aim:

### To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

### Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

### Program:
```c
#include <stdio.h>
int square() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num); 
    return num * num; 
}

int main() {
    int result;
    result = square();
    printf("The square of the number is: %d\n", result);

    return 0;
}
```

### Output:

<img width="549" height="254" alt="image" src="https://github.com/user-attachments/assets/f960aa9d-5c38-4d06-9988-a6b67ee42dd7" />


### Result:
Thus, the program is verified successfully

# EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.
# NAME: GIFTSON RAJARATHINAM N
# REG NO: 212222233002
### Aim:
 To write a C program to display stack elements using an array.
### Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
### Program:
```c
float stack[100];
int top,i;
void display()
{ for(i=top;i>=0;i--){
    printf("%.1f\n",stack[i]);
}
}
```
### Output:

![image](https://github.com/user-attachments/assets/598437ce-8378-44a5-a97a-dfa7fc269615)



### Result:
Thus, the program to display stack elements using an array is verified successfully.
 

# EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
### Aim:
To create a C program to push the given element in to a stack using array.
### Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
### Program:
```c
int size=3,top=-1,stack[100];
void push (int data)
{
    if(top==size-1){
        printf("stack is full\n");
    }
    else
    top++;
    stack[top]=data;
}
```
### Output:


![image](https://github.com/user-attachments/assets/0faee522-17c2-4adf-b47f-a0db64e9190e)


### Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
# EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
### Aim:
 To write a C program to display queue elements using array

### Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
### Program:
```c
int queue[50], rear=-1, front=-1;
void display()
{
    if(front>rear||front==-1)
    printf("No elements to display");
    else
    for(int i=front;i<=rear;i++){
        printf("%d\n",queue[i]);
    }
}
```
### Output:


![image](https://github.com/user-attachments/assets/29bc39f1-200f-4166-98fa-78a667014225)


### Result:
Thus, the program to display queue elements using array is verified successfully.


 
# EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
### Aim:
To write a C program to insert elements in queue using array.

### Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

### Program:
```c
int queue[50],size=10,front=-1,rear=-1;
void enqueue(int data)
{
    if(rear<size){
        if(front==-1)
        front=0;
    }
    rear++;
    queue[rear]=data;
}
```
### Output:


![image](https://github.com/user-attachments/assets/bd5e8688-4765-4d0a-85ae-7d6e25cbe754)

### Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
# EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

### Aim:

To create a function in C that deletes an element from a queue implemented using an array.

### Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



### Program:
```c
int front, rear;
void dequeue()
{  if(front>rear||front==-1)
printf("Queue Underflow.\n");
else
    front++;
}
```
### Output:


![Screenshot 2025-04-27 154900](https://github.com/user-attachments/assets/43b0b3ad-ed81-4442-9545-e52dd3b68bcb)


### Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.

# EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
# NAME: GIFTSON RAJARATHINAM N
# REG NO: 212222233002
## Aim:
To write a C program to search a given element in the given linked list.

## Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
## Program:
```c
struct Node
{
   struct Node *next;
   int data;
}*head;
void search(int data)
{
   struct Node *ptr;
   char item=data;
   int i=0,flag;
   ptr = head;
   if(ptr == NULL)
   {
     printf("Empty List\n");
   }
   else
   {
     while (ptr!=NULL)
     {
       if(ptr->data == item)
       {
          printf("item %d found at location %d ",item,i+1); flag=0;
       }
       i++;
       ptr = ptr -> next;
     }
     if(flag!=0)
     {
        printf("Item not found\n");
     }
   }
}
```

## Output:

<img width="732" height="323" alt="image" src="https://github.com/user-attachments/assets/db0b7745-b19d-4a93-876a-354b2f5c4bf1" />

## Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
# EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
## Aim:
To write a C program to insert a node in a linked list.
## Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
## Program:

```c
struct Node
{
   int data;
   struct Node *next;
}*head;

void insert(int data)
{
    struct Node n=(struct Node)malloc(sizeof(struct Node));
    struct Node *temp;
    if(head==NULL)
    {
       head=n;
       n->data=data;
       n->next=NULL;
       temp=head;
       return;
    }
    while(temp->next!=NULL)
    {
       temp=temp->next;
    }
    n->data=data;
    n->next=NULL;
    temp->next=n;
}
```

## Output:

<img width="448" height="319" alt="image" src="https://github.com/user-attachments/assets/14d188e3-61ac-42cb-a256-8c05d3f1891c" />

## Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
# EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
## Aim:
To write a C program to traverse a doubly linked list.

## Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
## Program:

```c
struct Node
{
   struct Node *prev;
   struct Node *next;
   float data;
}*head;
void display()
{
   struct Node *temp;
   temp=head;
   while(temp!=0)
   {
      printf("%.2f ",temp->data); temp=temp->next;
   }
}
```

## Output:

<img width="387" height="307" alt="image" src="https://github.com/user-attachments/assets/1c0ade87-eda9-49fc-b99f-58c991fe34a3" />

## Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



# EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
## Aim:
To write a C program to insert an element in doubly linked list

## Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
## Program:
```c
struct Node
{
   struct Node *prev;
   struct Node *next;
   char data;
}*head;
void insert(char data)
{
    struct Node n=(struct Node)malloc(sizeof(struct Node));
    struct Node *temp;
    if(head==NULL)
    {
       head=n;
       n->data=data;
       n->next=NULL;
       n->prev=NULL;
       temp=head;
    }
    else
    {
       while(temp->next!=NULL)
       {
          temp=temp->next;
       }
       n->data=data;
       n->next=NULL;
       n->prev=temp;
       temp->next=n;
     }
}
```

## Output:

<img width="355" height="319" alt="image" src="https://github.com/user-attachments/assets/9b7dfaae-85f0-41e1-958e-6098ec795b3a" />

## Result:
Thus, the program to insert an element in doubly linked list is verified successfully.


# EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

## Aim:
To write a C function that deletes a given element from a linked list.

## Algorithm:
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


## Program:

```c
struct Node
{
    float data; 
    struct Node *next;
}*head;
void delete()
{
    if(head==NULL)
    {
        printf("List is empty\n");
        return;
    }
    else if(head->next==NULL){
        head=NULL;
        free(head);
        printf("Node deleted from the begining ...\n");
    }
    else
    {
        struct Node *ptr;
        ptr=head;
        head=head->next;
        free(ptr);
        printf("Node deleted from the begining ...\n");
    }
}
```

## Output:

<img width="701" height="417" alt="image" src="https://github.com/user-attachments/assets/a59e1223-d308-45e9-bb23-b9ee18097913" />

## Result:
Thus, the function that deletes a given element from a linked list is verified successfully.

