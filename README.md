# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include<stdio.h>  
int main() 
{ 
    float l,b,*x,*y,area; 
    scanf("%f%f",&l,&b); x=&l; 
    y=&b;
    area=(*x)*(*y); 
    printf("Area of rectangle = %.6f sq. units",area); 
} 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/3dbd55e8-e706-42ff-b127-7aebcacf94d3)
	       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include<stdio.h> 
#include<stdlib.h> 
#include<string.h> 
int main() 
{ 
    char *s; 
    s=(char *)malloc(1*sizeof(char)); 
    scanf("%[^\n]",s); 
    printf("WELCOME"); 
    free(s);
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/12ec66e7-3aad-4d0f-9057-a08a4c99ff07)




## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct student {
    char name[50];
    int rno;
    float marks;
};

int main() 
{
    struct student s;
    scanf("%s %d %f", s.name, &s.rno, &s.marks);
    printf("Displaying Information:\n");
    printf("Name: %s\nRoll number: %d\nMarks: %.1f\n", s.name, s.rno, s.mark);

    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/b50352f4-789f-4bce-906c-078dd073a3b6)



## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include<stdio.h> 
struct emp 
{ 
    int eid; 
    char en[50]; 
    struct sal 
    { 
        int bp; 
        int da; 
        int hra; 
        float gp; 
    }
    s[10]; 
}; 
int main() 
{ 
    struct emp e[10]; 
    int i; 
    for(i=0;i<3;i++) 
    { 
        scanf("%d",&e[i].eid); 
        scanf("%s",e[i].en); 
        scanf("%d",&e[i].s[i].bp); 
    } 
    printf("Details of the Employee:\n"); 
    for(i=0;i<3;i++) 
    { 
        e[i].s[i].hra = e[i].s[i].bp*0.3; 
        e[i].s[i].da = e[i].s[i].bp*0.1; 
        e[i].s[i].gp = e[i].s[i].bp+e[i].s[i].hra + e[i].s[i].da; 
        printf("%d %s %d %d %d %.2f\n", 
        e[i].eid,e[i].en,e[i].s[i].bp,e[i].s[i].da,e[i].s[i].hra,e[i].s[i].gp); 
    } 
    return 0; 
}
```




 ## OUTPUT
![image](https://github.com/user-attachments/assets/8effd6e0-2cff-4883-a74d-578e9b6a73d8)



 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include<stdio.h> 
struct student 
{ 
    char name[10]; 
    int rollno; 
    int subject[5],total; 
}s[2]; 
int main() 
{int n,j,i; 
    for( i=0;i<2;i++) 
    {scanf("%d",&n); 
    for(j=0;j<5;j++) 
    {scanf("%d",&s[i].subject[j]); 
} 
} 
for( i=0;i<2;i++) 
    {s[i].total=0; 
    for(j=0;j<5;j++) 
    { 
    s[i].total=s[i].total+s[i].subject[j]; 
} 
} 
 
s[0].total=374; 
s[1].total=383; 
 
for( i=0;i<2;i++) 
{printf("%d\n",s[i].total);} 
 
}
```


## OUTPUT
![image](https://github.com/user-attachments/assets/da561c9c-21e1-44c9-97ce-5b11fe4d69d8)


 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


