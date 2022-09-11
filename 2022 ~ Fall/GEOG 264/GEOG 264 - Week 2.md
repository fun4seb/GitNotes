# GEOG 264 - Week 2: Algorithms
- Mathematical concepts used in this course:
    - Fractions, integers
    - Exponents, square root, absolute value, factorials (!)
    - Algebra, expanding algebraic expressions, order of operations
    - Basic statistical measures (mean, median, mode)
    - Basic trigonometry (sin cos)
    - Pythagorean theorem
    - Summation

- Outline:
    - R
        - Brief history
        - What is it?
        - Why learn it?
    - Programs
    - Algorithms
        - Conditionals
        - Conditional loops
        - For loops
    - Nesting

# R (Data Science Coding Language)
- Developed by Ross Ihaka and Robert Gentleman in the 1990s
- Stable version released in 2000
- Open-source high-level programming language now maintained by the R core-development team
- Widely used in data sciences (e.g. biology, quantitative social sciences)

## What is R?
- It is "open-source" software (which for our purposes means that it can be freely downloaded)
- It is available for a number of different operating systems, including Windows, Linux, and Macintosh;
- It is a complete programming language;
- It has extensive graphics and statistical capabilities.
- R has a fairly steep learning curve, which this class is designed to diminish
- The home page for the "R project" is at http://www.r-project.org

### RStudio
- RStudio is a user-friendlier interface that is installed on top of R.
- RStudio (http://www.rstudio.com) is an IDE (integrated development environment) that provides a consistent environment for running R across different platforms (i.e. Windows, Mac OS X, Linux).
- The “environment” contains four “panes” two of which include the standard command-line “console” interface of R, and a code or script editor that is generally more useful that those built into the standard R applications for Windows or the Mac, plus two other panes that provide a graphics window, help window, workspace summary and so on.
- The panes are tiled, and remain in the foreground, making it a little easier to navigate around the different windows that appear in the Windows and Mac applications.
- **This is what we will be using in this course**

## Why Learn R?
- **Strengths of R:**
    - Wide array of powerful statistical, data analysis and visualization tools
    - Free and open-source
    - Can utilize user-created ”packages” and “libraries”
- **Weaknesses of R:**
    - The packages can be confusing (redundant, messy naming, limited support info)
    - Steep learning curve

- While every programming language has a learning curve; the programming logic acquired in R is transferable to other languages (Ex: Python)

# Programs
- **Program** = a sequence of instructions
    - An author/programmer writes it; the instructions are written in a language that the processor understands
    - A processor carries out its instruction

- Carrying out the instructions = **executing** or **running** a programs
- a running programs = a **process**

- Examples of "programs":
    - A recipe (instructions for making a cake)
        - Processor: cook
        - Executing a recipe: cooking
    - A musical score (instructions for performing a piece of music)
        - Processor: performer (can read and play a music sheet)
        - Executing a score: performing
    - A knitting pattern (instructions for knitting a sweater)
        - Processor: knitter
        - Executing a pattern: knitting
    - A computer program (instructions telling the computer what to do)
        - Processor: the computer (very dumb; needs very specific instructions)
        - Executing (or running) a program = carrying out the instructions
        - Author: you

- Computers are dumb; instructions have to be much more detailed (and explicit) than ones written for a person
- Computer programs are written in a **programming language** = a language the computer can understand (this course mainly uses R)

- Computers are actually very dumb; They only understand **machine language**
    - This language is too tedious to write programs in, therefore we write a program in a high-level language like R and the computer takes our R program and turns it into machine language which it can understand by running a **compiler/interpreter**

# Algorithms
- Algorithmic process:
    1. Problem specification; diagnose problem
    2. Technique for finding the solution
    3. Specification of the solution = write an algorithm, a precise step by step procedure for solving a problem
    4. Implementation of the solution = write the actual program in R
    5. Debug and test your code. Code will have something initially wrong with it, most of the time

- **Algorithm example: going to Concordia in the morning**
    - Problem: going to school
    - Algorithm:
        1. Get up
        2. Eat
        3. Get ready
        4. Leave apartment
        5. Commute

- Sequential order: you do one step after the other and the **order matters!**
- Natural question: what level of detail is needed

## Writing Algorithms
- Start with a "high level" description of the procedure
    - **Overview of the problem** is more important at first
- Then, if needed, concentrate on each aspect of the problem at a time **(called a sub-problem**; nested problem/task to solve)
- "Get ready" for example, is a sub-problem with many steps
    - Can be solved independently of the other steps of the algorithm

- Writing algorithms ultimately comes down to breaking up a larger problem into smaller sub-problems, each with sub-algorithms to complete

> **Sub-problem: get ready**
    Sub-algorithm:
        Brush your teeth
        Shower
        Get dressed
        Comb your hair

- It is important to think about the **order** of the steps (Ex: you don't get dressed and comb hair before the shower, they must be done after); the order of the steps matters
- The steps in the sub-algorithm are at different levels of detail
    - Depending on the processor you are writing instructions for, some steps will require a higher level of detail, and some will not
    - We might assume that **"Brush your teeth"** and **"Comb your hair"** are **"atomic" steps** (they cannot be reduced to more detail), while **"Shower"** and **"Get dressed"** are far more complex and require separate sub-sub-algorithms

- This process of iteratively increasing the level of detail of the steps, down to the level of comprehension of the programming language used, is what programming is

# Conditional If Statements
- **Conditional step** = decide whether to do something based on whether or not a stated condition is met; Ex: if x, then do x

- Basic algorithmic construction: **the if statement**, which allows us to branch the program into multiple paths

> **If** condition is true **then**
    do A
**else**
    do B
**end if**

> **Sub-sub-problem: Get dressed**
    Sub-sub-algorithm (Get dressed):
        Put on underwear
        Put on shirt
        Put on pants
        **If** it is cold outside **then**
            Put on sweater
        **End if**
        Put on socks
        Put on shoes

- The **if statement** is the **most common** algorithmic construct in programming

## Example: Write an Algorithm for Buried Treasure
> **Possible solution:**
    Problem: get buried treasure
    Algorithm:
        Go to where the treasure is buried
        **Dig until you can see the treasure**
        Remove the treasure

- This is fine, but second step is not **atomic**; Assuming the algorithm is written for R (or any other programming language), the second step is not reduced to an instruction simple enough that the processor will understand

> **We could try this:**
    Sub-problem: Dig until you can see the treasure
    Sub-algorithm:
        Remove a shovel-full of dirt
        If you cannot see the treasure then
            Remove a shovel-full of dirt
        End if
        If you cannot see the treasure then
            Remove a shovel-full of dirt
        End if
        If you cannot see the treasure then
            Remove a shovel-full of dirt
        End if
        (repeating infinitely until you possibly find the treasure)

- The problem is that we **cant write an algorithm this way**
    - Since we don’t know how deeply the treasure is buried, we don’t know how many times to write down "If you cannot see the treasure then, Remove a shovel-full of dirt, End if"
    - What we need is an algorithm that **loops**

# Conditional Loops
``` 
**Loop**
    Do A
    **If** condition is true **then**
        Leave the loop
    **End if**
    Do B
**End Loop**
```

> **Loop**
    Remove a shovel-full of dirt
    **If** you can see the treasure **then**
        Leave the loop
    **End if**
    (Do nothing)
**End Loop**

- This algorithm will then loop the instructions **until the conditions to leave the loop have been met** (if you can see the treasure)

- The **conditional loop** is another **very common** algorithmic construct

- Sometimes, the same step has to be performed a fixed number of times (as opposed to the previous problem, for which the amount of shovels of dirt were unknown)

## Example: Write an Algorithm for Washing 20 Dishes
- Possible algorithm:
    - Pick up 1st dirty dish
    - Scrub dish with sponge
    - Rinse dish
    - Put dish in drainer
    - Pick up 2nd dirty dish
    - Etc. until 20 dishes are washed

- This would get the job done but is **tedious and an inefficient way to solve the task**
- What we need is an algorithm that loops **for a specific amount of times**

## Conditional For Loops
> **For** some fixed number of repetitions
Do A
**End for**

> Efficient algorithm:
    **For** dishes 1 to 20
        pick up dirty dish
        scrub dish with sponge
        rinse dish
        put dish in drainer
    **End for**

- If you only wanted to wash 10 dishes you could change the for statement to say "1 to 10"

- You could also use a more general algorithm:
    - "**For** dishes 1 to **N**"

# Conclusion
1. Basic technique for algorithm writing and problem solving
    1. Carefully define the problem
    2. Break the problem into smaller sub-problems
    3. Repeat the process with each sub-problem until each sub-problem is solved
2. The order of statements is usually very important
3. Three important algorithmic constructs
    1. **“If” statement** (branching)
    2. **Loop + if statement** -> conditional loop (unknown number of repetitions)
    3. **“For” loop** (known number of repetitions)

- **Ifs** and **loops** are what we build programs out of
    - We put together these constructs to get our algorithm and then our program
    - Your algorithm might be a **sequential list of commands** that can repeat and branch with ifs and (for)loops

- The algorithmic constructs may be **nested** within each other
    - Ex: multiple for loops inside each other
    - You can nest any algorithmic construct inside any other:
        - Loop within a loop
        - If within an if
        - If within a loop
        - Loop within an if
    - But it must be **completely inside it**; must be formatted correctly

## Conditional If Statements
- Basic algorithmic construction: **the if statement**, which allows us to branch **if condition is true**

> **If** condition is true **then**
    Do A
**Else**
    Do B
**End if**

- If statements can branch further with **"else if"** statements

> **If** condition1 is true **then**
    Do A
**Else if** condition2 is true **then**
    Do B
**Else**
    Do C (only gets done if none of condition1 and condition2 are true)
**End if**

- You can include as many branching "else if" statements as you need

## Conditional Loops
> **Loop**
    Do A
    **If** condition **then**
        Leave the loop
    **End if**
    Do B
**End loop**

- This form is used when you **don’t know the number of repetitions**

## Conditional For Loops
> **For** some fixed number of repetitions
    Do A
**End for**

- Use when you **know exactly the number of repetitions beforehand**
- Anything a for loop can do, a conditional loop can also do (just more verbosely)