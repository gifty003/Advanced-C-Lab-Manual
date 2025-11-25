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
