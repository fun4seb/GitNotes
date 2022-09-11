# GEOG 264 - Week 1: Introduction & Computer Basics
- Outline:
    - Hardware
    - Representing information
        - Bits
        - Programs
    - Software
        - Operating systems

# Computer Hardware
- Hardware = the physical components of a computer system

- The functional organization of a computer = input > computer (CPU, main memory, secondary storage) > output

## The Central Processing Unit (CPU)
- The CPU receives, interprets, and carries out instructions
- Responsible for everything that goes on in the computer
- Processors are very small ~1/4 inch square piece of silicon
- In a PC, laptop, or tablet, there are 1-8 processors
- Speed for a PC = 1 instruction/gigasecond (1 billion gigaseconds = 1 second)

# How Information is Represented Inside the Computer
- A computer is an electronic piece of equipment and consequently only understands 2 values: on and off
- In a computer, **on is represented by a 1, off is represented by a 0**
- A 0 or 1 is called a **bit** (short for binary digit)
- All information in a computer is represented by a pattern of 0’s and 1’s, this is called **binary**

- Examples:
    - 0 = 0000
    - 1 = 0001
    - 2 = 0010
    - 3 = 0011
    - 4 = 0100
    - 5 = 0101
    - ...
    - 15 = 1111

- The first 16 numbers (0-15) can be represented with 4 bits (i.e. digit spaces containing either 1 or 0); 24=2x2x2x2=16
    - 5 bits allow 2^5 (32) numbers to be represented (0-31)
    - 10 = 1024

## Expanding on Bits
- A basic unit of information is a **byte, made up of 8 bits**
- Kilobyte “K” = 1024 bytes (~ 1,000)
    - Note: 2^10 = 1024
- Megabyte “Meg” = 1024 kilobytes = 1024 x 1024 ~ 1,000,000 bytes
- Gigabyte “Gig” = 1024 megabytes
- Terabytes = 1024 gigabytes

## Representing Characters (Alphanumeric)
- We use characters, called ASCII characters, when we communicate with the computer (typing at the keyboard); the computer turns them into bits which it can understand
- Usually ASCII (American Standard for Information Interchange) code is used; 7 bit pattern for each printable character on the keyboard
    - There are others (Ex: UTF-8, UTF-16)

# Programs
- A program is a sequence of instructions to be completed by the computer performing a task
    - A program is written by a human author
    - The CPU runs the program

- Carrying out the instructions = "executing" or "running a program"
- Software, programs, and apps are all the same thing

## Computers Only Understand Very Simple Instructions
- Example of a series of simple instructions:
    1. Load 1010 in register AL
    2. Load 1101 in register BL
    3. Add registers AL and BL
    4. Store 0011 in register CL

- They understand only **machine language (binary)**; this language is too tedious to write programs in
    - Therefore, we write a program in a **high-level language** (meaning abstracted away from communicated directly to the CPU with 1's and 0's) like R (or Python or Java or C++)
    - The computer takes our R program (high-level) and translates it into machine language (low-level) which it can understand by running a **compiler** or **interpreter**

## Types of Software
1. System software = integral software that runs the computer
    - Operating systems: Windows, OSX, Linux
    - Compiler/interpreter: R interpreter, Python interpreter, etc.
    - User interface: GUI environment (Mac/Windows), shell command line (UNIX) 
2. Application software = programs you use
    - General purpose: word processors, spreadsheet software, browsers, search engines, communication, etc.
    - Specific purpose: payroll software, MyConcordia, games, etc.

# Operating Systems (OS)
- The heart of all the computer's software
- A set of programs that manage the overall operations of the computer system
    - Keeps track of everything in main memory
    - Manages the flow of information to and from the disks
    - Manages the information from the keyboard and to the screen and printer
    - Coordinates the resources (i.e, CPU, main memory, secondary storage, printers)

- When you turn the computer on it must boot itself up. i.e., it must read/load the OS from the internal hard disk into main memory
    - The instructions for booting are stored in the ROM (read-only memory) chip