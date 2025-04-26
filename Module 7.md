EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:

```
#include<stdio.h>
typedef struct
{
    int age;
    char name[10];
}vac;

int main()
{
    vac v;
    scanf("%d %s",&v.age,v.name);
    printf("Age:%d\n",v.age);
    printf("Name:%svaccine:%d\n",v.name,v.age);
    if (v.age>18)
    {
        printf("eligibility:yes");
    }
    else
    {
        printf("eligibility:no");
    }
}
```


Output:

![WhatsApp Image 2025-04-26 at 10 16 28_a70cb087](https://github.com/user-attachments/assets/5c041229-289c-4bcc-9540-b8a38b6ec60d)

Result:
Thus, the program is verified successfully. 



EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
Aim:
To write a C program for passing structure as function and returning a structure from a function

Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
Program:

```
#include <stdio.h>
struct addition
{
    int a,b,c;
};
struct addition get(struct addition add)
{
    struct addition a;
    scanf("%d %d",&a.a, &a.b);
    a.c = a.a+a.b;
    return a;
}
int main()
{
    //ptr->c=ptr->a+ptr->b;
    //return ptr->c;
    struct addition b = get(b);
    printf("%d",b.c);
}
```

Output:

![WhatsApp Image 2025-04-26 at 10 53 23_bec34498](https://github.com/user-attachments/assets/a720750d-e84c-4917-b787-b57f09695fa0)

Result:
Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
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
 
Program:

```
#include <stdio.h>
int main()
{
    FILE *fp;
    char ch[40];
    scanf("%s",ch);
    fp=fopen(ch,"w");
    if(fp!=NULL)
    {
        printf("%s File Created Successfully\n%s File Opened\n",ch,ch);
        
    }
    fclose(fp);
    printf("%s File Closed",ch);
    
}
```



Output:

![WhatsApp Image 2025-04-26 at 10 23 29_255f689b](https://github.com/user-attachments/assets/68ca2c90-a5e5-476f-bd0d-2bbf6fe83388)

Result:
Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
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
 
Program:
```
#include <stdio.h>
int main()
{
    FILE *fp;
    char ch[20],ele[20];
    int n;
    scanf("%s %d",ch,&n);
    fp=fopen(ch,"w");
    if(fp!=NULL)
    {
        printf("%s Opened\n",ch);
    }
    for(int i=1;i<=n;i++)
    {
        scanf("%s",ele);
        fprintf(fp,"%s",ele);
    }
    printf("Data added Successfully");
    fclose(fp);
}

```


Output:

![WhatsApp Image 2025-04-26 at 10 26 59_84992c7e](https://github.com/user-attachments/assets/0eea79c6-c804-417f-8d3d-efb0fcf8db2b)


Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm:
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

Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Subject {
    char name[100];
    int marks;
};

int main() {
    int n, i;
    struct Subject *s;
    printf("Enter the number of subjects: ");
    scanf("%d", &n);
    s = (struct Subject *)malloc(n * sizeof(struct Subject));
    if (s == NULL)
    {
        printf("Memory allocation failed.\n");
        return 1; 
    }
    for (i = 0; i < n; i++) {
        printf("Enter name of subject %d: ", i + 1);
        scanf("%s", s[i].name);
        printf("Enter marks for %s: ", s[i].name);
        scanf("%d", &s[i].marks);
    }
    printf("\nSubject Details:\n");
    for (i = 0; i < n; i++) {
        printf("Subject %d: %s, Marks: %d\n", i + 1, s[i].name, s[i].marks);
    }
    free(s);
    return 0;
}
```


Output:

![Screenshot 2025-04-26 110030](https://github.com/user-attachments/assets/bf7424ef-3988-4f7b-8652-61992f844730)

Result:
Thus, the program is verified successfully
