# GitHub Collaboration Guide (C# Project with GitHub Desktop)

## Objective

This activity will teach you how to:

- Work collaboratively using GitHub  
- Create and manage branches  
- Commit and push changes  
- Merge branches  
- Resolve merge conflicts  

You will work in groups of **3-6 students**.

---

## Part 1 — Create the Repository

One student in the group will act as the **Repository Owner (Group Leader)**.

### Step 1: Create Repository

Create a new repository on GitHub.

**Repository name:**
CSharpTeam

Make sure you select:

- ✔ Add README  
- ✔ Add `.gitignore` → **VisualStudio**

---

### Step 2: Invite Team members

Go to:
Settings → Collaborators → Add people


Add the other **3 - 5 students**.

---

## Part 2 — Clone Using GitHub Desktop

Each student must:

1. Open **GitHub Desktop**
2. Click **Clone Repository**
3. Select the repository
4. Choose a local folder
5. Click **Clone**

---

## Part 3 — Create the C# Project

Inside the repository folder, create a **C# Console App**.

In **Visual Studio**:
File → New → Project → Console App (.NET)
**Project name:**
TeamApp


---

## Part 4 — Starter Code

Replace `Program.cs` with the following:

```csharp
using System;

namespace TeamApp
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Welcome to the Team Application");

            ShowMenu();
        }

        static void ShowMenu()
        {
            Console.WriteLine("1 - Greeting");
            Console.WriteLine("2 - Calculator");
            Console.WriteLine("3 - Exit");

            Console.Write("Choose option: ");
            int choice = int.Parse(Console.ReadLine());

            if (choice == 1)
            {
                Greeting();
            }
            else if (choice == 2)
            {
                Calculator();
            }
        }

        static void Greeting()
        {
            Console.WriteLine("Hello from the greeting feature!");
        }

        static void Calculator()
        {
            Console.WriteLine("Calculator feature coming soon...");
        }
    }
}
```
---
## Part 5 — First Commit

In GitHub Desktop:

1. You will see the changes
2. Write a commit message:

Initial C# project setup

3. Click Commit to main
4. Click Push origin

---
## Part 6 — Create Branches

Each student must create their own branch.

In GitHub Desktop:
Branch → New Branch

Example branches:
feature-greeting
feature-calculator
feature-menu
feature-style

## Part 7 — Each Student Adds a Feature
Student 1 — Greeting Feature

Modify:
```csharp
static void Greeting()
{
    Console.Write("Enter your name: ");
    string name = Console.ReadLine();

    Console.WriteLine("Welcome " + name + "!");
}
```
Commit message:

Added personalised greeting


Student 2 — Calculator Feature

Modify:
```csharp
static void Calculator()
{
    Console.Write("Enter first number: ");
    int num1 = int.Parse(Console.ReadLine());

    Console.Write("Enter second number: ");
    int num2 = int.Parse(Console.ReadLine());

    int result = num1 + num2;

    Console.WriteLine("Result = " + result);
}
```
Commit message:

Added simple calculator

Student 3 — Improve Menu

Modify:
```csharp
Console.WriteLine("===== TEAM APPLICATION =====");
Console.WriteLine("1 - Greeting System");
Console.WriteLine("2 - Calculator Tool");
Console.WriteLine("3 - Exit Program");
```
Student 4 — Exit Feature

Add:
```csharp
else if (choice == 3)
{
    Console.WriteLine("Goodbye!");
}
```

## Part 8 — Create Pull Requests

Go to GitHub website.

For each branch:

Click Compare & Pull Request
Add a description

Example:

This feature adds a calculator for adding two numbers.
Click Create Pull Request


## Part 9 — Merge the Branch

Once approved:

Merge Pull Request

The feature is now part of the main branch.

## Part 10 — Pull Latest Code

In GitHub Desktop:

Fetch Origin
Pull Origin

Now everyone has the updated project.

## Part 11 — Practice a Merge Conflict

To simulate a conflict:

Two students edit the same line.

Student A:
```csharp
Console.WriteLine("Welcome to the Team Application");
```
Student B:
```csharp
Console.WriteLine("Welcome to the C# Collaboration Project");
```
Both push their changes.

GitHub will detect a merge conflict.

Part 12 — Resolve Conflict

Git will show:

<<<<<<< HEAD
Console.WriteLine("Welcome to the Team Application");
=======
Console.WriteLine("Welcome to the C# Collaboration Project");
>>>>>>> branch

Resolve it like this:

Console.WriteLine("Welcome to the C# Team Collaboration Application");

Then:

Commit the merge
Push changes


**Tip: The best way to learn Git is by making mistakes and fixing them!**
