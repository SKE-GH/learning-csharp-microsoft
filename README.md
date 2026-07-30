# learning-csharp-microsoft

Fortschrittsanzeige und Übungen, während des "Free Foundational C# with Microsoft Certification" Kurses.

---

## Your First Code Using C#
7 of 7 challenges completed  
-Write Your First C# Code  
-Store and Retrieve Data Using Literal and Variable Values in C#  
-Perform Basic String Formatting in C#  
-Guided Project - Calculate and Print Student Grades  
-Guided Project - Calculate Final GPA  
-Trophy - Write Your First Code Using C# 

## Create and Run Simple C# Console Applications
0 of 8 challenges completed

## Add Logic to C# Console Applications
0 of 8 challenges completed

## Work with Variable Data in C# Console Applications
0 of 8 challenges completed

## Create Methods in C# Console Applications
0 of 6 challenges completed

## Debug C# Console Applications
0 of 7 challenges completed

## Foundational C# with Microsoft Certification Exam
Not Passed

---

## Code examples  

### Guided Project - Calculate Final GPA
```
string studentName = "Sophia Johnson";
string course1Name = "English 101";
string course2Name = "Algebra 101";
string course3Name = "Biology 101";
string course4Name = "Computer Science I";
string course5Name = "Psychology 101";

int course1Credit = 3;
int course2Credit = 3;
int course3Credit = 4;
int course4Credit = 4;
int course5Credit = 3;

int totalCredit = course1Credit + course2Credit + course3Credit + course4Credit + course5Credit;

int course1Grade = 4;
int course2Grade = 3;
int course3Grade = 3;
int course4Grade = 3;
int course5Grade = 4;

decimal finalGPA = (course1Credit * course1Grade + course2Credit * course2Grade + course3Credit * course3Grade + course4Credit * course4Grade + course5Credit * course5Grade) / (decimal)totalCredit;

int leadingDigit = (int)finalGPA;
int firstDigit = (int)(finalGPA * 10) % 10;
int secondDigit = (int)(finalGPA * 100) % 10;


Console.WriteLine($"Student: {studentName}\n");

Console.WriteLine($"Course\t\t\tGrade\tCredit Hours");
Console.WriteLine($"{course1Name}\t\t{course1Grade}\t{course1Credit}");
Console.WriteLine($"{course2Name}\t\t{course2Grade}\t{course2Credit}");
Console.WriteLine($"{course3Name}\t\t{course3Grade}\t{course3Credit}");
Console.WriteLine($"{course4Name}\t{course4Grade}\t{course4Credit}");
Console.WriteLine($"{course5Name}\t\t{course5Grade}\t{course5Credit}");
Console.WriteLine($"\nFinal GPA:\t\t{leadingDigit},{firstDigit}{secondDigit}");
```
### Output
```
Student: Sophia Johnson

Course			     Grade  Credit Hours
English 101		       4    3
Algebra 101		       3    3
Biology 101		       3    4
Computer Science I     3    4
Psychology 101		   4    3
Final GPA:             3,35
```
