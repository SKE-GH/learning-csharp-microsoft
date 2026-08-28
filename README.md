# learning-csharp-microsoft

Fortschrittsanzeige und Übungen, während des "Free Foundational C# with Microsoft Certification" Kurses.

---

## Your First Code Using C#
7 of 7 challenges completed  
- Write Your First C# Code  
- Store and Retrieve Data Using Literal and Variable Values in C#  
- Perform Basic String Formatting in C#  
- Guided Project - Calculate and Print Student Grades  
- Guided Project - Calculate Final GPA  
- Trophy - Write Your First Code Using C# 

## Create and Run Simple C# Console Applications
8 of 8 challenges completed
- Install and Configure Visual Studio Code  
- Call Methods From the .NET Class Library Using C#  
- Add Decision Logic to Your Code Using if, else, and else if statements in C#  
- Store and Iterate Through Sequences of Data Using Arrays and the foreach Statement in C#
- Create Readable Code with Conventions, Whitespace, and Comments in C#  
- Guided Project - Develop foreach and if-elseif-else Structures to Process Array Data in C#
- Challenge Project - Develop foreach and if-elseif-else Structures to Process Array Data in C#  
- Trophy - Create and Run Simple C# Console Applications  

## Add Logic to C# Console Applications
8 of 8 challenges completed  
- Evaluate Boolean Expressions to Make Decisions in C#
- Control Variable Scope and Logic Using Code Blocks in C#
- Branch the Flow of Code Using the switch-case Construct in C#  
- Iterate Through a Code Block Using the for Statement in C#
- Add Looping Logic to Your Code Using the do-while and while Statements in C#
- Guided Project - Develop Conditional Branching and Looping Structures in C#
- Challenge Project - Develop Branching and Looping Structures in C#
- Trophy - Add Logic to C# Console Applications  

## Work with Variable Data in C# Console Applications
8 of 8 challenges completed
- Choose the Correct Data Type in Your C# Code  
- Convert Data Types Using Casting and Conversion Techniques in C#
- Perform Operations on Arrays Using Helper Methods in C#
- Format Alphanumeric Data for Presentation in C
- Modify the Content of Strings Using Built-In String Data Type Methods in C#
- Guided Project - Work with Variable Data in C#
- Challenge Project - Work with Variable Data in C#  
- Trophy - Work with Variable Data in C# Console Applications  

## Create Methods in C# Console Applications  
1 of 6 challenges completed  
- Write Your First C# Method  

## Debug C# Console Applications
0 of 7 challenges completed

## Foundational C# with Microsoft Certification Exam
Not Passed

---

## Code examples  

### 1 - Guided Project - Calculate Final GPA
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
### 2 - Guided Project - Develop foreach and if-elseif-else Structures to Process Array Data in C#
```
using System;

// initialize variables - graded assignments 
int currentAssignments = 5;

int[] sophiaScores = [90, 86, 87, 98, 100, 94, 90];
int[] andrewScores = [92, 89, 81, 96, 90, 89];
int[] emmaScores = [90, 85, 87, 98, 68, 89, 89, 89];
int[] loganScores = [90, 95, 87, 88, 96, 96];
int[] beckyScores = [92, 91, 90, 91, 92, 92, 92];
int[] chrisScores = [84, 86, 88, 90, 92, 94, 96, 98 ];
int[] ericScores = [80, 90, 100, 80, 90, 100, 80, 90];
int[] gregorScores = [91, 91, 91, 91, 91, 91, 91];    

// Student names
string[] studentNames = ["Sophia", "Andrew", "Emma", "Logan", "Becky", "Chris", "Eric", "Gregor"];

int[] studentScores = new int[10];

string currentStudentLetterGrade = "";

// Write the Report Header to the console
Console.WriteLine("Student\t\tGrade\n");

foreach (string name in studentNames)
{
    if (name == "Sophia")
        studentScores = sophiaScores;
    else if (name == "Andrew")
        studentScores = andrewScores;
    else if (name == "Emma")
        studentScores = emmaScores;
    else if (name == "Logan")
        studentScores = loganScores;
    else if (name == "Becky")
    studentScores = beckyScores;
    else if (name == "Chris")
        studentScores = chrisScores;
    else if (name == "Eric")
        studentScores = ericScores;
    else if (name == "Gregor")
        studentScores = gregorScores;
    else
        continue;

    // initialize/reset the sum of scored assignments
    decimal sumAssignmentScores = 0;

    // initialize/reset the calculated average of exam + extra credit scores
    decimal currentStudentGrade = 0;

    // initialize/reset the amount of Scores
    int scoreCount = 0;

    foreach (int score in studentScores)
    {
        scoreCount ++;

        if (scoreCount <= currentAssignments)
            // add the exam score to the sum
            sumAssignmentScores += score;

        else
            sumAssignmentScores += (decimal)score / 10m;

    }

    currentStudentGrade = (decimal)(sumAssignmentScores) / currentAssignments;

if (currentStudentGrade >= 97)
        currentStudentLetterGrade = "A+";

    else if (currentStudentGrade >= 93)
        currentStudentLetterGrade = "A";

    else if (currentStudentGrade >= 90)
        currentStudentLetterGrade = "A-";

    else if (currentStudentGrade >= 87)
        currentStudentLetterGrade = "B+";

    else if (currentStudentGrade >= 83)
        currentStudentLetterGrade = "B";

    else if (currentStudentGrade >= 80)
        currentStudentLetterGrade = "B-";

    else if (currentStudentGrade >= 77)
        currentStudentLetterGrade = "C+";

    else if (currentStudentGrade >= 73)
        currentStudentLetterGrade = "C";

    else if (currentStudentGrade >= 70)
        currentStudentLetterGrade = "C-";

    else if (currentStudentGrade >= 67)
        currentStudentLetterGrade = "D+";

    else if (currentStudentGrade >= 63)
        currentStudentLetterGrade = "D";

    else if (currentStudentGrade >= 60)
        currentStudentLetterGrade = "D-";

    else
        currentStudentLetterGrade = "F";

    Console.WriteLine($"{name}\t\t{currentStudentGrade}\t{currentStudentLetterGrade}");
}

Console.WriteLine("Press the Enter key to continue");
Console.ReadLine();
```
### Output
```
Student         Grade

Sophia          95,88   A
Andrew          91,38   A-
Emma            90,94   A-
Logan           93,12   A
Becky           94,88   A
Chris           93,76   A
Eric            93,4    A
Gregor          94,64   A
Press the Enter key to continue
```
