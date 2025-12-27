# Program-5-a
## C-Module 5
## EX_NO-05)a)-Pointers
### Date: 17-10-25
### Name: Sujhan Prasanth S B
### Register Number:25018059
## AIM:
Write a C program to check whether the number 8887 is even number or odd number using pointers.
## ALGORITHM:
1. Start the program.
2. Declare an integer variable to store the input number and an integer pointer variable.
3. Read the integer value from the user using scanf.
4. Assign the address of the integer variable to the pointer.
5. Check if the value pointed to by the pointer is even using the modulus operator (%):

    a. If it is even, print "<number> is even."

    b. Otherwise, print "<number> is odd."

6. End the program.
## PROGRAM:
```
#include<stdio.h>
int main()
{
    int num,*p1;
    scanf("%d",&num);
    p1=&num;
    if(*p1%2==0)
    printf("%d is even.",num);
    else
    printf("%d is odd.",num);
}
```
## OUTPUT:
<img width="842" height="289" alt="Screenshot 2025-10-20 083200" src="https://github.com/user-attachments/assets/32154267-7939-4bc5-84c7-1326442e306d" />

## RESULT:
Thus the program to check whether the number 8887 is even number or odd number using pointers has been executed successfully
# Program-5-b
## C-Module 5
## EX_NO-05)b)-Functions & Storage Classes
### Date: 17-10-25
### Name: Sujhan Prasanth S B
### Register Number:25018059
## AIM:
write a program to print even numbers in given range using recursion
## ALGORITHM:
1. Start the program.
2. Define a function named even that takes two integer arguments: st (start) and end.
3. Inside the function:
 
    a. If st is greater than end, return (stop recursion).

    b. If st is even (st % 2 == 0), print the value of st.

    c. Recursively call the even function with st + 1 and end as arguments.
4. In the main function:
 
    a. Declare two integer variables st and end.

    b. Read the values of st and end from the user using scanf.

    c. Print a message indicating the range of even numbers.

    d. Call the even function with st and end as arguments.
5. End the program.

## PROGRAM:
```
#include<stdio.h>
void even(int st,int end)
{
    if(st>end)
    return;
    if(st%2==0)
    printf(" %d",st);
    even(st+1,end);
}
int main()
{
    int st,end;
    scanf("%d%d",&st,&end);
    printf("Even Numbers from %d to %d are:",st,end);
    even(st,end);
}
```
## OUTPUT:
<img width="1173" height="353" alt="Screenshot 2025-10-20 083757" src="https://github.com/user-attachments/assets/c65ce71f-ec8e-41ba-a0d2-a20e4cf26ad0" />

## RESULT:
Thus the program to print even numbers in given range using recursion has been executed successfully
# Program-5-c
## C-Module 5
## EX_NO-05)c)-Arrays & Its Operations
### Date: 17-10-25
### Name: Sujhan Prasanth S B
### Register Number:25018059
## AIM:
Write a C Program to displays the lower triangular and its sum of a matrix
## ALGORITHM:
1. Start the program.
2. Declare two integer variables to store the number of rows and columns.
3. Read the values of rows and columns from the user using scanf.
4. Declare a two-dimensional array with the given number of rows and columns.
5. Print a message "matrix is".
6. Use nested for loops to read elements into the matrix:

    a. Outer loop iterates over rows.

    b. Inner loop iterates over columns.

    c. Read each element using scanf.
7. Use nested for loops to display the matrix in proper format:
 
    a. Print each element followed by a space.

   b. Move to a new line after each row.

8. Initialize a variable sum to 0.
9. Use nested for loops to find and print elements of the lower triangle:

   a. Check if the current element position satisfies the lower triangle condition 
       (i == 3) or (i == 2 && j != 3) or (i == 1 && j == 1).

    b. If true, print the element and add it to sum.

10. After processing all elements, print the total sum of the lower triangle.
11. End the program.

## PROGRAM:
```
#include<stdio.h>
int main()
{
    int row,col;
    scanf("%d%d",&row,&col);
    int arr[row][col];
    printf("matrix is\n");
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        scanf("%d",&arr[i][j]);
    }
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        printf("%d ",arr[i][j]);
        printf("\n");
    }
    int sum=0;
    printf("\n");
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        {
            if(i==3||(i==2&&j!=3)||(i==1&&j==1))
            {
                printf("%d ",arr[i][j]);
                sum+=arr[i][j];
            }}
            printf("\n");
    }
    printf("Sum of Lower Triangle is %d",sum);
}
```
## OUTPUT:
<img width="837" height="620" alt="Screenshot 2025-10-20 084241" src="https://github.com/user-attachments/assets/1ed2762d-a812-44d5-8fa7-2e3ecdce5401" />

## RESULT:
Thus the program to displays the lower triangular and its sum of a matrix has been executed successfully
# Program-5-d
## C-Module 5
## EX_NO-05)e)-Strings
### Date: 17-10-25
### Name: Sujhan Prasanth S B
### Register Number:25018059
## AIM:
Write a program in C to replace the spaces of a string with a specific character.
## ALGORITHM:
1. Start the program.
2. Declare a character array to store the input string and a character variable to store the replacement character.
3. Read a line of text from the user using fgets.
4. Read a single character from the user using scanf.
5. Use a for loop to iterate through each character in the string until the null character ('\0') is reached:

    a. If the current character is a space (' '), replace it with the given character.

6. After the loop, print the updated string along with a message showing the replacement character.
7. End the program.

## PROGRAM:
```
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[30];
    fgets(str,sizeof(str),stdin);
    char ch;
    scanf("%c",&ch);
    for(int i=0;str[i]!='\0';i++)
    {
        if(str[i]==' ')
        str[i]=ch;
    }
    printf("After replacing the space with  %c the new string is :\n%s",ch,str);
}
```
## OUTPUT:
<img width="1157" height="257" alt="Screenshot 2025-10-20 085227" src="https://github.com/user-attachments/assets/433c4703-390f-44e5-907a-b26e8c0d41b9" />

## RESULT:
Thus the program to replace the spaces of a string with a specific character has been executed successfully
# Program-5-e
## C-Module 5
## EX_NO-05)e)-Arrays
### Date: 17-10-25
### Name: Sujhan Prasanth S B
### Register Number:25018059
## AIM:
Write a C Program to displays the lower triangular of a matrix
## ALGORITHM:
1. Start the program.
2. Declare two integer variables to store the number of rows and columns.
3. Read the values of rows and columns from the user using scanf.
4. Declare a two-dimensional array with the given number of rows and columns.
5. Use nested for loops to read elements into the matrix:

    a. Outer loop iterates over rows.

    b. Inner loop iterates over columns.

    c. Read each element using scanf.
6. Print the message "matrix is".
7. Use nested for loops to display the entire matrix:
 
    a. Print each element followed by a space.

    b. Move to a new line after each row.
8. Use nested for loops to display specific elements based on conditions:
 
    a. If the current position satisfies (i==1 && j==1) or (i==2 && j!=3) or (i==3), print the element.

   b. Move to a new line after each row.
9. End the program.

## PROGRAM:
```
#include<stdio.h>
int main()
{
    int row,col;
    scanf("%d%d",&row,&col);
    int arr[row][col];
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        scanf("%d",&arr[i][j]);
    }
    printf("matrix is\n");
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        {
            printf("%d ",arr[i][j]);
        }
        printf("\n");
    }
    printf("\n");
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        {
            if((i==1&&j==1)||(i==2&&j!=3)||i==3)
            printf("%d ",arr[i][j]);
        }
        printf("\n");
    }
}
```
## OUTPUT:
<img width="831" height="592" alt="Screenshot 2025-10-20 090503" src="https://github.com/user-attachments/assets/b4f94e25-650f-48e3-b22e-dbc695ac9d81" />

## RESULT:
Thus the program to displays the lower triangular of a matrix has been executed successfully

