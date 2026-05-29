

# **Introduction to OOPS Programming – Assessment**





# Section A – Concept Application





### **1. Compiler vs Interpreter in Food Delivery App**

### 

### In a food delivery application, I would prefer using a compiler during the final deployment stage because compiled programs execute faster and provide better performance. Food delivery apps handle many operations like order tracking, payment processing, and live notifications, so speed is important.

### 

### A compiler also detects many errors before execution, which helps in improving software reliability. Interpreters are useful during testing because code can run line by line, making debugging easier.

### 

### For deployment, compiled programs are preferred because they are optimized and more secure.

### 

### **2. Employee Salary Program Logic**

### 

### To calculate employee salary with bonus, tax, and overtime, I would combine:

### 

### Variables → to store salary data

### Conditional statements (if-else) → for bonus and tax conditions

### Arithmetic operators → for calculations

### Functions → to organize code properly

### 

### This combination makes the program easier to manage and reusable.

### 

### **3. Why Loops are Preferred**

### 

### Loops are preferred in menu-driven applications because they allow the program to run repeatedly until the user chooses to exit.

### 

### I would use a while loop because:

### 

### It is simple

### It keeps the menu running continuously

### It is suitable when the number of repetitions is unknown

### 

### Without loops, the program would stop after one execution.

### 

### **4. Incorrect Average Marks Output**

### 

### The probable cause is using the int data type while calculating average marks.

### 

### Integer variables only store whole numbers, so decimal values are lost during division.

### 

### Using float or double solves the issue because they store decimal values accurately.

### 

### **5. Program Crashes at Runtime**

### 

### This is called a Runtime Error.

### 

### Two debugging practices:

### 

### 1 .Use print statements or debugger tools to identify the problem line

### 2\. Check memory access and input values carefully

### 

### Runtime errors happen after successful compilation.

### 

### **6. Why Structure is Better than Multiple Arrays**

### 

### A structure is better because it stores related data together.

### 

### Example:

### 

### struct Student

### {

### &#x20;   char name\[50];

### &#x20;   int marks;

### &#x20;   char grade;

### };

### 

### Advantages:

### 

### Better organization

### Easier data management

### Improves readability

### Reduces confusion compared to multiple arrays







\------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



# Section B – Practical Coding Tasks



## 1\. Study Mood Assistant

### \#include <stdio.h>

### 

### int main()

### {

### &#x20;   int hours;

### 

### &#x20;   printf("Enter study hours today: ");

### &#x20;   scanf("%d", \&hours);

### 

### &#x20;   if(hours >= 8)

### &#x20;   {

### &#x20;       printf("Excellent dedication!\\n");

### &#x20;   }

### &#x20;   else if(hours >= 5)

### &#x20;   {

### &#x20;       printf("Good job, keep improving!\\n");

### &#x20;   }

### &#x20;   else if(hours >= 2)

### &#x20;   {

### &#x20;       printf("You can do better tomorrow.\\n");

### &#x20;   }

### &#x20;   else

### &#x20;   {

### &#x20;       printf("Focus more on studies!\\n");

### &#x20;   }

### 

### &#x20;   return 0;

### }

\-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 2\. Loops + Arrays

### \#include <stdio.h>

### 

### int main()

### {

### &#x20;   float screen\[7];

### &#x20;   float total = 0, average;

### &#x20;   int i;

### 

### &#x20;   for(i=0; i<7; i++)

### &#x20;   {

### &#x20;       printf("Enter screen time for day %d: ", i+1);

### &#x20;       scanf("%f", \&screen\[i]);

### 

### &#x20;       total = total + screen\[i];

### &#x20;   }

### 

### &#x20;   average = total / 7;

### 

### &#x20;   printf("\\nTotal Screen Time = %.2f", total);

### &#x20;   printf("\\nAverage Screen Time = %.2f", average);

### 

### &#x20;   if(average > 6)

### &#x20;   {

### &#x20;       printf("\\nWarning: Screen time exceeds healthy limit!");

### &#x20;   }

### 

### &#x20;   return 0;

### }

\-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **3. Functions \& Pointers**

#### \#include <stdio.h>

#### 

#### void swap(int \*a, int \*b)

#### {

#### &#x20;   int temp;

#### 

#### &#x20;   temp = \*a;

#### &#x20;   \*a = \*b;

#### &#x20;   \*b = temp;

#### }

#### 

#### int main()

#### {

#### &#x20;   int x, y;

#### 

#### &#x20;   printf("Enter first number: ");

#### &#x20;   scanf("%d", \&x);

#### 

#### &#x20;   printf("Enter second number: ");

#### &#x20;   scanf("%d", \&y);

#### 

#### &#x20;   printf("\\nBefore Swapping:");

#### &#x20;   printf("\\nX = %d", x);

#### &#x20;   printf("\\nY = %d", y);

#### 

#### &#x20;   swap(\&x, \&y);

#### 

#### &#x20;   printf("\\n\\nAfter Swapping:");

#### &#x20;   printf("\\nX = %d", x);

#### &#x20;   printf("\\nY = %d", y);

#### 

#### &#x20;   return 0;

#### }



\-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 4\. File Handling Program



### \#include <stdio.h>

### 

### int main()

### {

### &#x20;   FILE \*fp;

### &#x20;   char goals\[100];

### 

### &#x20;   fp = fopen("goals.txt", "w");

### 

### &#x20;   printf("Enter your daily goals: ");

### &#x20;   gets(goals);

### 

### &#x20;   fprintf(fp, "%s", goals);

### 

### &#x20;   fclose(fp);

### 

### &#x20;   fp = fopen("goals.txt", "r");

### 

### &#x20;   printf("\\nSaved Goals:\\n");

### 

### &#x20;   fgets(goals, 100, fp);

### &#x20;   printf("%s", goals);

### 

### &#x20;   fclose(fp);

### 

### &#x20;   return 0;

### }

\-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Section C – Mini Capstone Project

#### Mini Project: Student Productivity Tracker

#### \#include <stdio.h>

#### 

#### int main()

#### {

#### &#x20;   int choice;

#### &#x20;   float hours\[7];

#### &#x20;   float total = 0, average;

#### &#x20;   int i;

#### 

#### &#x20;   FILE \*fp;

#### 

#### &#x20;   while(1)

#### &#x20;   {

#### &#x20;       printf("\\n===== Student Productivity Tracker =====\\n");

#### 

#### &#x20;       printf("1. Log Daily Study Hours\\n");

#### &#x20;       printf("2. Generate Weekly Report\\n");

#### &#x20;       printf("3. Exit\\n");

#### 

#### &#x20;       printf("Enter your choice: ");

#### &#x20;       scanf("%d", \&choice);

#### 

#### &#x20;       switch(choice)

#### &#x20;       {

#### &#x20;           case 1:

#### 

#### &#x20;               fp = fopen("study.txt", "w");

#### 

#### &#x20;               for(i=0; i<7; i++)

#### &#x20;               {

#### &#x20;                   printf("Enter study hours for Day %d: ", i+1);

#### &#x20;                   scanf("%f", \&hours\[i]);

#### 

#### &#x20;                   fprintf(fp, "%.2f\\n", hours\[i]);

#### &#x20;               }

#### 

#### &#x20;               fclose(fp);

#### 

#### &#x20;               printf("Study hours saved successfully!\\n");

#### 

#### &#x20;               break;

#### 

#### &#x20;           case 2:

#### 

#### &#x20;               fp = fopen("study.txt", "r");

#### 

#### &#x20;               if(fp == NULL)

#### &#x20;               {

#### &#x20;                   printf("No data found!\\n");

#### &#x20;                   break;

#### &#x20;               }

#### 

#### &#x20;               total = 0;

#### 

#### &#x20;               for(i=0; i<7; i++)

#### &#x20;               {

#### &#x20;                   fscanf(fp, "%f", \&hours\[i]);

#### 

#### &#x20;                   total = total + hours\[i];

#### &#x20;               }

#### 

#### &#x20;               fclose(fp);

#### 

#### &#x20;               average = total / 7;

#### 

#### &#x20;               printf("\\n===== Weekly Report =====\\n");

#### 

#### &#x20;               for(i=0; i<7; i++)

#### &#x20;               {

#### &#x20;                   printf("Day %d = %.2f Hours\\n", i+1, hours\[i]);

#### &#x20;               }

#### 

#### &#x20;               printf("\\nTotal Study Hours = %.2f", total);

#### &#x20;               printf("\\nAverage Study Hours = %.2f\\n", average);

#### 

#### &#x20;               break;

#### 

#### &#x20;           case 3:

#### 

#### &#x20;               printf("Exiting Program...\\n");

#### &#x20;               return 0;

#### 

#### &#x20;           default:

#### 

#### &#x20;               printf("Invalid Choice!\\n");

#### &#x20;       }

#### &#x20;   }

#### 

#### &#x20;   return 0;

#### }

