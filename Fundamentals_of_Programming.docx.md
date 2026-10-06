**Fundamentals of Programming**

*Everything from three years of CSE, explained in simple words*

# **Introduction**

A computer is built in layers, called levels. Programming languages work at the upper layers (Levels 4 and 5), the ones humans can read and write. At the bottom, Level 0, is the physical hardware logic of the CPU (the processor, the computer's brain), which only understands electrical signals written as 1s and 0s. Programming languages act as an automated translation pipeline, bridging the gap between human logic and that hardware logic. The purposes of programming languages are as follows:

* **Communicating with the Computer:** They translate human intent into structured instructions the CPU can execute.

* **Task Automation:** They allow developers to write scripts that eliminate tedious, repetitive tasks.

* **Problem Solving:** They let us break complex problems into smaller, manageable steps.

* **Digital Infrastructure:** Software written in them powers everything from mobile apps to operating systems.

A computer also keeps information in different places, a bit like a cook in a kitchen. Registers are the ingredients in your hands and cache is the cutting board: extremely fast to reach, but tiny. RAM is the kitchen counter, the main working space: fast, but it is cleared when the power goes off. Storage such as an SSD or hard drive is the pantry and fridge: slower to fetch from, but much larger, and it keeps your data even when the computer is off. The closer to the cook, the faster the access and the smaller the space.

![Four kitchen stations matched to registers, cache, RAM and storage, from fastest and smallest to slowest and biggest][image1]

*Computer memory explained as a kitchen*

## **The four core ideas of programming**

At its heart, Computer Science is the art of solving problems using a very fast, but completely clueless, assistant (the computer). Here are the four fundamental concepts behind almost everything in programming, in plain English:

### **1\. Data (The Ingredients)**

A computer doesn't know what a "user", a "photo", or a "song" is. It only knows information, which we call data. To work with data, we store it in labeled boxes called variables.

* Imagine a labeled box on a desk named **Age**. Inside, you put the number 20\.

* Another box named **Username** holds the text "Alex".

* Every time the computer needs to check how old you are, it opens the box labeled Age.

### **2\. Algorithms (The Recipe)**

An algorithm is simply a step-by-step set of instructions to complete a task. You already use algorithms every day\! Example: making toast.

1. Take a slice of bread.

2. Put it in the toaster.

3. Push the lever down.

4. Wait 2 minutes.

5. Remove the toast.

If you miss step 2, the algorithm fails. Computers need every single step spelled out in exact order because they cannot "fill in the blanks" like humans do.

### **3\. Control Flow (Making Decisions)**

A computer needs to know what to do when situations change. We guide it using if / else statements (logic) and loops (repetition). You will see both in detail later, in the Conditionals and Loop sections.

**Logic (if / else):**

* If the alarm time is 7:00 AM → ring the alarm.

* Else (if it is not 7:00 AM) → stay quiet.

**Loops (repetition):**

Instead of telling the computer "Check email, check email, check email", you tell it:

* Repeat checking for new messages until a new email arrives.

### **4\. Functions (The Recipe Cards)**

Once you write a great set of instructions, say how to send a message, you don't want to rewrite those steps every single time someone clicks "Send". You package those steps into a function and give it a name, like SendMessage(). Anytime you need that action performed, you just call its name, and the computer runs the saved steps automatically.

## **How they all fit together**

Imagine building a basic vending machine:

| Concept | How the vending machine uses it |
| :---- | :---- |
| **Data (Variables)** | MoneyInserted \= \$2.00, ItemPrice \= \$1.50 |
| **Algorithm** | The steps in order: take the money, check it, give the snack, give change. |
| **Logic (if / else)** | If MoneyInserted is greater than or equal to ItemPrice, dispense the snack. Else, ask for more money. |
| **Loop** | Keep flashing the light until a button is pressed. |
| **Function** | GiveChange() calculates and drops the leftover coins. |

Programming languages (like Python or JavaScript) are just the specific words and grammar we use to translate these simple ideas into instructions the machine understands.

# **Print**

Let's say you want to read something from a paper, so you print the document using a printer. Now imagine the screen is the paper and your computer is the printer. To read your statement on the screen, you need to tell the computer to print it, otherwise nothing will appear. Different languages use different syntax for this command. For example:

**C:** printf("Hello");

**C++:** std::cout \<\< "Hello";

**Java:** System.out.println("Hello");

**Python:** print("Hello")

**JavaScript (JS):** console.log("Hello");

**SQL:** SELECT 'Hello';

**PHP:** echo "Hello";

**Kotlin:** println("Hello")

**Dart:** print('Hello');

**Go:** fmt.Println("Hello")

**TypeScript (TS):** console.log("Hello");

**R:** cat("Hello")

**C\#:** Console.WriteLine("Hello");

**MIPS:** la \$a0, msg, then li \$v0, 4, then syscall

*Note: in MIPS, msg is a label for the stored text "Hello", and 4 is the code that means "print a string". Some languages (like Java and C) also need a little extra setup around these lines, so here we only show the printing part.*

# **Syntax**

The term "syntax" comes from the Ancient Greek word σύνταξις (syntaxis), meaning "arrangement together" or "coordination". In linguistics, syntax studies how words and morphemes combine to form larger units like phrases and sentences, focusing on word order, grammatical relations, and hierarchical sentence structure. Different languages have different syntactic rules; for instance, English typically follows a Subject-Verb-Object (SVO) order.

Likewise, in programming, syntax is the set of rules that define how code must be written: its structure, order, and valid combinations of symbols, keywords, and punctuation, so that a computer can correctly interpret and execute it. If the syntax is wrong, a syntax error occurs, just like a grammar mistake in a sentence.

The syntax of programming languages is built on key components:

1. **Keywords:** words reserved by the language that have a fixed meaning (e.g. if, while, return).

2. **Operators:** symbols that work on values (e.g. \+, \-, \==).

3. **Punctuation Marks:** brackets, braces, semicolons and similar symbols that give code its structure.

4. **Identifiers:** names you choose for things like variables and functions (e.g. age, calculateTotal).

5. **Data Types:** the kind of value being stored, such as whole numbers, decimals, text, or true/false.

6. **Control Structures:** tools that direct the flow of the program, including conditionals, loops, and switch branches.

7. **Comments:** notes written for humans that the computer ignores.

The importance of syntax in programming cannot be overstated. Here's why it matters:

* **Clarity and Readability:** Clean and well-structured syntax enhances code readability, making it easier for developers to understand, maintain, and debug code.

* **Correctness and Accuracy:** Accurate syntax ensures that instructions are interpreted correctly by the computer, reducing the likelihood of errors and bugs in the code.

* **Consistency and Maintainability:** Consistent syntax conventions across a codebase facilitate collaboration among developers and simplify code maintenance and updates.

* **Early Error Detection:** The computer checks syntax before running your code, so mistakes are caught immediately instead of causing strange behavior later.

# **Conditionals**

Assume you want to go on a hangout but your mom says, "You can go only if your friend goes, else you can't." This is a conditional statement. You can express it in two ways: if-else and switch-case.

**if-else:** if holds the condition and what happens when it is true, and else holds what happens when it is not.

**switch-case:** switch holds the variable being checked, each case is one possible value with its own consequence, and default covers everything else (it plays the role of else). Switch is handy when there are many fixed options, like days of the week.

Below are the same two examples written in every language from the Print section. In every if-else example, "friend goes" is true, so the program says "Go hangout". In every switch example, the day is 2, so it says "Tuesday".

### **C**

**if-else**

int friendGoes \= 1;  
if (friendGoes) {  
    printf("Go hangout");  
} else {  
    printf("Stay home");  
}

**switch-case**

int day \= 2;  
switch (day) {  
    case 1: printf("Monday"); break;  
    case 2: printf("Tuesday"); break;  
    default: printf("Another day");  
}

### **C++**

**if-else**

bool friendGoes \= true;  
if (friendGoes) {  
    std::cout \<\< "Go hangout";  
} else {  
    std::cout \<\< "Stay home";  
}

**switch-case**

int day \= 2;  
switch (day) {  
    case 1: std::cout \<\< "Monday"; break;  
    case 2: std::cout \<\< "Tuesday"; break;  
    default: std::cout \<\< "Another day";  
}

### **Java**

**if-else**

boolean friendGoes \= true;  
if (friendGoes) {  
    System.out.println("Go hangout");  
} else {  
    System.out.println("Stay home");  
}

**switch-case**

int day \= 2;  
switch (day) {  
    case 1: System.out.println("Monday"); break;  
    case 2: System.out.println("Tuesday"); break;  
    default: System.out.println("Another day");  
}

### **Python**

**if-else**

friend\_goes \= True  
if friend\_goes:  
    print("Go hangout")  
else:  
    print("Stay home")

**switch-case**

day \= 2  
match day:  
    case 1:  
        print("Monday")  
    case 2:  
        print("Tuesday")  
    case \_:  
        print("Another day")

*Python calls its switch "match-case" (Python 3.10 or newer). The underscore \_ works as the default.*

### **JavaScript (JS)**

**if-else**

let friendGoes \= true;  
if (friendGoes) {  
    console.log("Go hangout");  
} else {  
    console.log("Stay home");  
}

**switch-case**

let day \= 2;  
switch (day) {  
    case 1: console.log("Monday"); break;  
    case 2: console.log("Tuesday"); break;  
    default: console.log("Another day");  
}

### **SQL**

*SQL is mainly for asking questions of a database, so it has no true if-else or loops in its standard form. The closest tools are shown below. The while loop uses T-SQL, the version of SQL used by Microsoft SQL Server.*

**if-else**

SELECT CASE  
    WHEN 1 \= 1 THEN 'Go hangout'  
    ELSE 'Stay home'  
END;

*CASE ... WHEN ... ELSE plays the role of if-else. Here 1 \= 1 stands for "friend goes" (always true).*

**switch-case**

SELECT CASE 2  
    WHEN 1 THEN 'Monday'  
    WHEN 2 THEN 'Tuesday'  
    ELSE 'Another day'  
END;

### **PHP**

**if-else**

\<?php  
\$friendGoes \= true;  
if (\$friendGoes) {  
    echo "Go hangout";  
} else {  
    echo "Stay home";  
}

**switch-case**

\<?php  
\$day \= 2;  
switch (\$day) {  
    case 1: echo "Monday"; break;  
    case 2: echo "Tuesday"; break;  
    default: echo "Another day";  
}

### **Kotlin**

**if-else**

val friendGoes \= true  
if (friendGoes) {  
    println("Go hangout")  
} else {  
    println("Stay home")  
}

**switch-case**

val day \= 2  
when (day) {  
    1 \-\> println("Monday")  
    2 \-\> println("Tuesday")  
    else \-\> println("Another day")  
}

*Kotlin calls its switch "when", and uses else as the default.*

### **Dart**

**if-else**

bool friendGoes \= true;  
if (friendGoes) {  
  print('Go hangout');  
} else {  
  print('Stay home');  
}

**switch-case**

int day \= 2;  
switch (day) {  
  case 1: print('Monday'); break;  
  case 2: print('Tuesday'); break;  
  default: print('Another day');  
}

### **Go**

**if-else**

friendGoes := true  
if friendGoes {  
    fmt.Println("Go hangout")  
} else {  
    fmt.Println("Stay home")  
}

**switch-case**

day := 2  
switch day {  
case 1:  
    fmt.Println("Monday")  
case 2:  
    fmt.Println("Tuesday")  
default:  
    fmt.Println("Another day")  
}

*Go stops after the matching case by itself, so no break is needed.*

### **TypeScript (TS)**

*TypeScript is JavaScript plus type labels (like : boolean), so the structure is the same.*

**if-else**

let friendGoes: boolean \= true;  
if (friendGoes) {  
    console.log("Go hangout");  
} else {  
    console.log("Stay home");  
}

**switch-case**

let day: number \= 2;  
switch (day) {  
    case 1: console.log("Monday"); break;  
    case 2: console.log("Tuesday"); break;  
    default: console.log("Another day");  
}

### **R**

**if-else**

friend\_goes \<- TRUE  
if (friend\_goes) {  
  cat("Go hangout\\n")  
} else {  
  cat("Stay home\\n")  
}

**switch-case**

day \<- "Tue"  
switch(day,  
  Mon \= cat("Monday\\n"),  
  Tue \= cat("Tuesday\\n"),  
  cat("Another day\\n")  
)

*R's switch picks the option whose name matches. The last item, with no name, is the default.*

### **C\#**

**if-else**

bool friendGoes \= true;  
if (friendGoes)  
{  
    Console.WriteLine("Go hangout");  
}  
else  
{  
    Console.WriteLine("Stay home");  
}

**switch-case**

int day \= 2;  
switch (day)  
{  
    case 1: Console.WriteLine("Monday"); break;  
    case 2: Console.WriteLine("Tuesday"); break;  
    default: Console.WriteLine("Another day"); break;  
}

### **MIPS**

*MIPS is assembly language, which is very close to what the processor actually understands. It has no if, else or loop keywords. Instead, you put labels (names for places in the code) and jump to them when a condition is true. Lines starting with \# are comments.*

**if-else**

.data  
msgGo:   .asciiz "Go hangout"  
msgStay: .asciiz "Stay home"  
.text  
main:  
    li  \$t0, 1              \# friendGoes (1 \= yes, 0 \= no)  
    beq \$t0, \$zero, stay    \# if friendGoes is 0, jump to stay  
    la  \$a0, msgGo          \# otherwise prepare "Go hangout"  
    j   show  
stay:  
    la  \$a0, msgStay        \# prepare "Stay home"  
show:  
    li  \$v0, 4              \# 4 \= print a string  
    syscall  
    li  \$v0, 10             \# 10 \= end the program  
    syscall

**switch-case**

.data  
mon:   .asciiz "Monday"  
tue:   .asciiz "Tuesday"  
other: .asciiz "Another day"  
.text  
main:  
    li  \$t0, 2              \# day \= 2  
    li  \$t1, 1  
    beq \$t0, \$t1, case1     \# is day 1?  
    li  \$t1, 2  
    beq \$t0, \$t1, case2     \# is day 2?  
    la  \$a0, other          \# default  
    j   show  
case1:  
    la  \$a0, mon  
    j   show  
case2:  
    la  \$a0, tue  
show:  
    li  \$v0, 4  
    syscall  
    li  \$v0, 10  
    syscall

*A switch is just a chain of comparisons, each one jumping to its own label. The last line before the labels is the default.*

# **Loop**

Suppose a teacher punishes you by making you write "I am sorry" 100 times. Writing the same thing over and over is annoying. The same goes for playing a turn-based game like chess, counting from 1 to 100, or adding up a list of expenses. These are all repetition problems, and loops exist to solve them easily. The main types are for, while, do-while, and for-each.

* **for loop:** needs a starting point, an ending condition, and a step (how the counter changes each round).

* **while loop:** needs only a condition. It checks the condition first, so if the condition is false from the start, it never runs.

* **do-while loop:** runs the code once first, then checks the condition to decide whether to repeat.

* **for-each loop:** needs a collection (like a list). It runs once for every item in it, with no counting required.

Below are the examples in every language. The for, while and do-while examples each print "I am sorry" three times. The for-each example prints every fruit in a list of three. Where a language is missing a loop type, a note explains the closest alternative.

### **C**

**for loop**

for (int i \= 1; i \<= 3; i++) {  
    printf("I am sorry\\n");  
}

**while loop**

int i \= 1;  
while (i \<= 3\) {  
    printf("I am sorry\\n");  
    i++;  
}

**do-while loop**

int i \= 1;  
do {  
    printf("I am sorry\\n");  
    i++;  
} while (i \<= 3);

**for-each loop**

char \*fruits\[\] \= {"apple", "banana", "mango"};  
for (int i \= 0; i \< 3; i++) {  
    printf("%s\\n", fruits\[i\]);  
}

*C has no built-in for-each, so we walk through the list position by position.*

### **C++**

**for loop**

for (int i \= 1; i \<= 3; i++) {  
    std::cout \<\< "I am sorry\\n";  
}

**while loop**

int i \= 1;  
while (i \<= 3\) {  
    std::cout \<\< "I am sorry\\n";  
    i++;  
}

**do-while loop**

int i \= 1;  
do {  
    std::cout \<\< "I am sorry\\n";  
    i++;  
} while (i \<= 3);

**for-each loop**

std::string fruits\[\] \= {"apple", "banana", "mango"};  
for (std::string f : fruits) {  
    std::cout \<\< f \<\< "\\n";  
}

### **Java**

**for loop**

for (int i \= 1; i \<= 3; i++) {  
    System.out.println("I am sorry");  
}

**while loop**

int i \= 1;  
while (i \<= 3\) {  
    System.out.println("I am sorry");  
    i++;  
}

**do-while loop**

int i \= 1;  
do {  
    System.out.println("I am sorry");  
    i++;  
} while (i \<= 3);

**for-each loop**

String\[\] fruits \= {"apple", "banana", "mango"};  
for (String f : fruits) {  
    System.out.println(f);  
}

### **Python**

**for loop**

for i in range(3):  
    print("I am sorry")

**while loop**

i \= 1  
while i \<= 3:  
    print("I am sorry")  
    i \+= 1

**do-while loop**

i \= 1  
while True:  
    print("I am sorry")  
    i \+= 1  
    if i \> 3:  
        break

*Python has no do-while. The trick is to loop forever and break out at the end of each round once the condition is met.*

**for-each loop**

fruits \= \["apple", "banana", "mango"\]  
for f in fruits:  
    print(f)

*In Python, the normal for loop already works as a for-each.*

### **JavaScript (JS)**

**for loop**

for (let i \= 1; i \<= 3; i++) {  
    console.log("I am sorry");  
}

**while loop**

let i \= 1;  
while (i \<= 3\) {  
    console.log("I am sorry");  
    i++;  
}

**do-while loop**

let i \= 1;  
do {  
    console.log("I am sorry");  
    i++;  
} while (i \<= 3);

**for-each loop**

const fruits \= \["apple", "banana", "mango"\];  
for (const f of fruits) {  
    console.log(f);  
}

### **SQL**

*SQL is mainly for asking questions of a database, so it has no true if-else or loops in its standard form. The closest tools are shown below. The while loop uses T-SQL, the version of SQL used by Microsoft SQL Server.*

**for loop**

*SQL has no for loop. Use the while loop below to count.*

**while loop**

DECLARE @i INT \= 1;  
WHILE @i \<= 3  
BEGIN  
    PRINT 'I am sorry';  
    SET @i \= @i \+ 1;  
END

**do-while loop**

*SQL has no do-while loop.*

**for-each loop**

SELECT name FROM fruits;

*A SELECT already goes through every row of a table, which is the for-each idea. Here, fruits is a table with a name column.*

### **PHP**

**for loop**

for (\$i \= 1; \$i \<= 3; \$i++) {  
    echo "I am sorry\\n";  
}

**while loop**

\$i \= 1;  
while (\$i \<= 3\) {  
    echo "I am sorry\\n";  
    \$i++;  
}

**do-while loop**

\$i \= 1;  
do {  
    echo "I am sorry\\n";  
    \$i++;  
} while (\$i \<= 3);

**for-each loop**

\$fruits \= \["apple", "banana", "mango"\];  
foreach (\$fruits as \$f) {  
    echo \$f . "\\n";  
}

### **Kotlin**

**for loop**

for (i in 1..3) {  
    println("I am sorry")  
}

**while loop**

var i \= 1  
while (i \<= 3\) {  
    println("I am sorry")  
    i++  
}

**do-while loop**

var i \= 1  
do {  
    println("I am sorry")  
    i++  
} while (i \<= 3\)

**for-each loop**

val fruits \= listOf("apple", "banana", "mango")  
for (f in fruits) {  
    println(f)  
}

### **Dart**

**for loop**

for (int i \= 1; i \<= 3; i++) {  
  print('I am sorry');  
}

**while loop**

int i \= 1;  
while (i \<= 3\) {  
  print('I am sorry');  
  i++;  
}

**do-while loop**

int i \= 1;  
do {  
  print('I am sorry');  
  i++;  
} while (i \<= 3);

**for-each loop**

var fruits \= \['apple', 'banana', 'mango'\];  
for (var f in fruits) {  
  print(f);  
}

### **Go**

**for loop**

for i := 1; i \<= 3; i++ {  
    fmt.Println("I am sorry")  
}

**while loop**

i := 1  
for i \<= 3 {  
    fmt.Println("I am sorry")  
    i++  
}

*Go has only one loop keyword, for. Giving it just a condition makes it behave like a while loop.*

**do-while loop**

i := 1  
for {  
    fmt.Println("I am sorry")  
    i++  
    if i \> 3 {  
        break  
    }  
}

*Go has no do-while. A for loop with no condition runs forever, and break ends it once we are done.*

**for-each loop**

fruits := \[\]string{"apple", "banana", "mango"}  
for \_, f := range fruits {  
    fmt.Println(f)  
}

*range goes through the list. The underscore \_ ignores the position number, since we only want the item.*

### **TypeScript (TS)**

*TypeScript is JavaScript plus type labels (like : boolean), so the structure is the same.*

**for loop**

for (let i: number \= 1; i \<= 3; i++) {  
    console.log("I am sorry");  
}

**while loop**

let i: number \= 1;  
while (i \<= 3\) {  
    console.log("I am sorry");  
    i++;  
}

**do-while loop**

let i: number \= 1;  
do {  
    console.log("I am sorry");  
    i++;  
} while (i \<= 3);

**for-each loop**

const fruits: string\[\] \= \["apple", "banana", "mango"\];  
for (const f of fruits) {  
    console.log(f);  
}

### **R**

**for loop**

for (i in 1:3) {  
  cat("I am sorry\\n")  
}

**while loop**

i \<- 1  
while (i \<= 3\) {  
  cat("I am sorry\\n")  
  i \<- i \+ 1  
}

**do-while loop**

i \<- 1  
repeat {  
  cat("I am sorry\\n")  
  i \<- i \+ 1  
  if (i \> 3\) break  
}

*R has no do-while. repeat runs forever until break stops it, which gives the same effect.*

**for-each loop**

fruits \<- c("apple", "banana", "mango")  
for (f in fruits) {  
  cat(f, "\\n")  
}

### **C\#**

**for loop**

for (int i \= 1; i \<= 3; i++)  
{  
    Console.WriteLine("I am sorry");  
}

**while loop**

int i \= 1;  
while (i \<= 3\)  
{  
    Console.WriteLine("I am sorry");  
    i++;  
}

**do-while loop**

int i \= 1;  
do  
{  
    Console.WriteLine("I am sorry");  
    i++;  
} while (i \<= 3);

**for-each loop**

string\[\] fruits \= { "apple", "banana", "mango" };  
foreach (string f in fruits)  
{  
    Console.WriteLine(f);  
}

### **MIPS**

*MIPS is assembly language, which is very close to what the processor actually understands. It has no if, else or loop keywords. Instead, you put labels (names for places in the code) and jump to them when a condition is true. Lines starting with \# are comments.*

**for loop**

.data  
msg: .asciiz "I am sorry\\n"  
.text  
main:  
    li  \$t0, 1              \# i \= 1  
    li  \$t1, 3              \# last value  
loop:  
    bgt \$t0, \$t1, done      \# if i \> 3, leave the loop  
    li  \$v0, 4  
    la  \$a0, msg  
    syscall  
    addi \$t0, \$t0, 1        \# i++  
    j   loop                \# go back to the top  
done:  
    li  \$v0, 10  
    syscall

**while loop**

.data  
msg: .asciiz "I am sorry\\n"  
.text  
main:  
    li  \$t0, 1  
    li  \$t1, 3  
loop:  
    bgt \$t0, \$t1, done      \# check the condition first  
    li  \$v0, 4  
    la  \$a0, msg  
    syscall  
    addi \$t0, \$t0, 1  
    j   loop  
done:  
    li  \$v0, 10  
    syscall

*In assembly, for and while look the same: check, run, jump back.*

**do-while loop**

.data  
msg: .asciiz "I am sorry\\n"  
.text  
main:  
    li  \$t0, 1  
    li  \$t1, 3  
loop:  
    li  \$v0, 4              \# run the body first  
    la  \$a0, msg  
    syscall  
    addi \$t0, \$t0, 1  
    ble \$t0, \$t1, loop      \# then repeat while i \<= 3  
    li  \$v0, 10  
    syscall

**for-each loop**

.data  
nums: .word 10, 20, 30  
.text  
main:  
    la  \$t0, nums           \# address of the first item  
    li  \$t1, 0              \# how many items we have visited  
    li  \$t2, 3              \# how many items there are  
loop:  
    beq \$t1, \$t2, done  
    lw  \$a0, 0(\$t0)         \# load the current item  
    li  \$v0, 1              \# 1 \= print a number  
    syscall  
    li  \$v0, 11             \# 11 \= print a character  
    li  \$a0, 10             \# 10 \= new line  
    syscall  
    addi \$t0, \$t0, 4        \# move to the next item  
    addi \$t1, \$t1, 1  
    j   loop  
done:  
    li  \$v0, 10  
    syscall

*MIPS has no for-each, so we move a pointer through a list of numbers, one item (4 bytes) at a time.*

# **Array**

An array is a set of data of the same type, stored together side by side, like a row of boxes of equal size. It can hold any data type (characters, integers, decimals and so on), but in most languages every item in the array must be of the same type. Each box has a position number, called an index, and counting usually starts at 0, so the first item sits at index 0\. (A few languages, like Python and JavaScript, are more relaxed and let one list hold different types.)

To insert data into an array or print all of it, you can use a loop, which visits one box after another. In the examples below, the array holds 10, 20 and 30\. We print the first item, then every item.

### **C**

**create and print**

int numbers\[3\] \= {10, 20, 30};  
printf("%d\\n", numbers\[0\]);           // first item: 10  
for (int i \= 0; i \< 3; i++) {  
    printf("%d\\n", numbers\[i\]);       // 10, 20, 30  
}

### **C++**

**create and print**

int numbers\[3\] \= {10, 20, 30};  
std::cout \<\< numbers\[0\] \<\< "\\n";      // first item: 10  
for (int n : numbers) {  
    std::cout \<\< n \<\< "\\n";           // 10, 20, 30  
}

### **Java**

**create and print**

int\[\] numbers \= {10, 20, 30};  
System.out.println(numbers\[0\]);       // first item: 10  
for (int n : numbers) {  
    System.out.println(n);            // 10, 20, 30  
}

### **Python**

**create and print**

numbers \= \[10, 20, 30\]  
print(numbers\[0\])                     \# first item: 10  
for n in numbers:  
    print(n)                          \# 10, 20, 30

*Python calls its arrays "lists". A list can even mix different types.*

### **JavaScript (JS)**

**create and print**

const numbers \= \[10, 20, 30\];  
console.log(numbers\[0\]);              // first item: 10  
for (const n of numbers) {  
    console.log(n);                   // 10, 20, 30  
}

*A JavaScript array can mix different types.*

### **SQL**

**create and print**

CREATE TABLE numbers (value INT);  
INSERT INTO numbers VALUES (10), (20), (30);  
SELECT value FROM numbers;            \-- 10, 20, 30

*Standard SQL has no arrays. A table with one column is the closest thing, and SELECT walks through every row. (PostgreSQL does have real arrays.)*

### **PHP**

**create and print**

\$numbers \= \[10, 20, 30\];  
echo \$numbers\[0\] . "\\n";              // first item: 10  
foreach (\$numbers as \$n) {  
    echo \$n . "\\n";                   // 10, 20, 30  
}

### **Kotlin**

**create and print**

val numbers \= intArrayOf(10, 20, 30\)  
println(numbers\[0\])                   // first item: 10  
for (n in numbers) {  
    println(n)                        // 10, 20, 30  
}

### **Dart**

**create and print**

List\<int\> numbers \= \[10, 20, 30\];  
print(numbers\[0\]);                    // first item: 10  
for (int n in numbers) {  
  print(n);                           // 10, 20, 30  
}

*Dart calls its arrays "lists".*

### **Go**

**create and print**

numbers := \[3\]int{10, 20, 30}  
fmt.Println(numbers\[0\])               // first item: 10  
for \_, n := range numbers {  
    fmt.Println(n)                    // 10, 20, 30  
}

*\[3\]int means an array of exactly 3 whole numbers.*

### **TypeScript (TS)**

**create and print**

const numbers: number\[\] \= \[10, 20, 30\];  
console.log(numbers\[0\]);              // first item: 10  
for (const n of numbers) {  
    console.log(n);                   // 10, 20, 30  
}

### **R**

**create and print**

numbers \<- c(10, 20, 30\)  
cat(numbers\[1\], "\\n")                 \# first item: 10  
for (n in numbers) {  
  cat(n, "\\n")                        \# 10, 20, 30  
}

*R counts from 1, not 0, so numbers\[1\] is the first item. c() combines values into a list.*

### **C\#**

**create and print**

int\[\] numbers \= { 10, 20, 30 };  
Console.WriteLine(numbers\[0\]);        // first item: 10  
foreach (int n in numbers)  
{  
    Console.WriteLine(n);             // 10, 20, 30  
}

### **MIPS**

**create and print**

.data  
numbers: .word 10, 20, 30  
newline: .asciiz "\\n"  
.text  
main:  
    la  \$t0, numbers        \# address of the array  
    lw  \$a0, 0(\$t0)         \# first item (position 0\)  
    li  \$v0, 1              \# 1 \= print a number  
    syscall  
    la  \$a0, newline  
    li  \$v0, 4  
    syscall  
   
    li  \$t1, 0              \# items visited  
    li  \$t2, 3              \# number of items  
loop:  
    beq \$t1, \$t2, done  
    lw  \$a0, 0(\$t0)         \# load the current item  
    li  \$v0, 1  
    syscall  
    la  \$a0, newline  
    li  \$v0, 4  
    syscall  
    addi \$t0, \$t0, 4        \# next item (each number takes 4 bytes)  
    addi \$t1, \$t1, 1  
    j   loop  
done:  
    li  \$v0, 10  
    syscall

*In assembly, an array is just numbers placed side by side in memory. Each number takes 4 bytes, which is why we move 4 at a time.*

# **String**

A string is a set of characters stored together in one box. It is basically an array of characters. In some languages (like C) a string really is an array of characters, while in many others it is its own built-in type. Most languages also come with ready-made tools (built-in functions or libraries) for string input, output, reversing, finding the length and more.

In the examples below, the text is "Hello". We print its length (5) and then the text reversed (olleH).

### **C**

**length and reverse**

\#include \<string.h\>  
   
char s\[\] \= "Hello";  
printf("%d\\n", (int)strlen(s));       // length: 5  
for (int i \= (int)strlen(s) \- 1; i \>= 0; i--) {  
    printf("%c", s\[i\]);               // reversed: olleH  
}

*In C, a string really is an array of characters, ending with a hidden 0 that marks the end.*

### **C++**

**length and reverse**

std::string s \= "Hello";  
std::cout \<\< s.length() \<\< "\\n";      // length: 5  
std::string r(s.rbegin(), s.rend());  // reversed copy  
std::cout \<\< r;                       // olleH

### **Java**

**length and reverse**

String s \= "Hello";  
System.out.println(s.length());                        // 5  
System.out.println(new StringBuilder(s).reverse());    // olleH

### **Python**

**length and reverse**

s \= "Hello"  
print(len(s))                         \# length: 5  
print(s\[::-1\])                        \# reversed: olleH

*\[::-1\] means "walk through the text backwards".*

### **JavaScript (JS)**

**length and reverse**

const s \= "Hello";  
console.log(s.length);                          // 5  
console.log(s.split("").reverse().join(""));   // olleH

### **SQL**

**length and reverse**

SELECT LENGTH('Hello'), REVERSE('Hello');   \-- 5, olleH

*This works in MySQL and PostgreSQL. In SQL Server, use LEN instead of LENGTH.*

### **PHP**

**length and reverse**

\$s \= "Hello";  
echo strlen(\$s) . "\\n";               // length: 5  
echo strrev(\$s);                      // reversed: olleH

### **Kotlin**

**length and reverse**

val s \= "Hello"  
println(s.length)                     // length: 5  
println(s.reversed())                 // reversed: olleH

### **Dart**

**length and reverse**

String s \= 'Hello';  
print(s.length);                      // length: 5  
print(s.split('').reversed.join());   // reversed: olleH

### **Go**

**length and reverse**

s := "Hello"  
fmt.Println(len(s))                   // length: 5  
r := \[\]rune(s)  
for i, j := 0, len(r)-1; i \< j; i, j \= i+1, j-1 {  
    r\[i\], r\[j\] \= r\[j\], r\[i\]           // swap the ends, moving inward  
}  
fmt.Println(string(r))                // reversed: olleH

*Go has no ready-made reverse, so we swap letters from both ends.*

### **TypeScript (TS)**

**length and reverse**

const s: string \= "Hello";  
console.log(s.length);                          // 5  
console.log(s.split("").reverse().join(""));   // olleH

### **R**

**length and reverse**

s \<- "Hello"  
cat(nchar(s), "\\n")                   \# length: 5  
cat(paste(rev(strsplit(s, "")\[\[1\]\]), collapse \= ""), "\\n")   \# olleH

*The reverse line splits the text into letters, flips their order, and joins them back.*

### **C\#**

**length and reverse**

string s \= "Hello";  
Console.WriteLine(s.Length);          // length: 5  
char\[\] letters \= s.ToCharArray();  
Array.Reverse(letters);  
Console.WriteLine(new string(letters));   // reversed: olleH

### **MIPS**

**length and reverse**

.data  
str: .asciiz "Hello"  
.text  
main:  
    la  \$t0, str            \# address of the first character  
    li  \$t1, 0              \# length counter  
loop:  
    lb  \$t2, 0(\$t0)         \# load one character  
    beq \$t2, \$zero, done    \# a 0 marks the end of the text  
    addi \$t1, \$t1, 1  
    addi \$t0, \$t0, 1  
    j   loop  
done:  
    move \$a0, \$t1  
    li  \$v0, 1              \# print the length: 5  
    syscall  
    li  \$v0, 10  
    syscall

*MIPS has no ready-made string tools, so we count the characters ourselves. Reversing would need even more code, so it is left out here.*

# **Function**

In programming, a function is simply a reusable block of code designed to perform a specific task. Think of a function like a recipe or a shortcut button on your microwave. Instead of writing out a long list of instructions every single time you want to do something, you group those instructions together, give them a name, and press that "button" whenever you need them.

A function can also take inputs (called parameters) and give back an answer (the return value), like putting bread in a toaster and getting toast out. In the examples below, the function adds two numbers: we give it 2 and 3, and it gives back 5\.

### **C**

**define and call**

int add(int a, int b) {  
    return a \+ b;  
}  
   
int main() {  
    printf("%d", add(2, 3));          // 5  
    return 0;  
}

### **C++**

**define and call**

int add(int a, int b) {  
    return a \+ b;  
}  
   
int main() {  
    std::cout \<\< add(2, 3);           // 5  
    return 0;  
}

### **Java**

**define and call**

public static int add(int a, int b) {  
    return a \+ b;  
}  
   
// then, inside main:  
System.out.println(add(2, 3));        // 5

*In Java, functions live inside a class and are called methods.*

### **Python**

**define and call**

def add(a, b):  
    return a \+ b  
   
print(add(2, 3))                      \# 5

### **JavaScript (JS)**

**define and call**

function add(a, b) {  
    return a \+ b;  
}  
   
console.log(add(2, 3));               // 5

### **SQL**

**define and call**

CREATE FUNCTION add\_numbers (@a INT, @b INT)  
RETURNS INT  
AS  
BEGIN  
    RETURN @a \+ @b;  
END;  
GO  
   
SELECT dbo.add\_numbers(2, 3);         \-- 5

*This is T-SQL (SQL Server). The way functions are written differs a lot between databases.*

### **PHP**

**define and call**

function add(\$a, \$b) {  
    return \$a \+ \$b;  
}  
   
echo add(2, 3);                       // 5

### **Kotlin**

**define and call**

fun add(a: Int, b: Int): Int {  
    return a \+ b  
}  
   
println(add(2, 3))                    // 5

### **Dart**

**define and call**

int add(int a, int b) {  
  return a \+ b;  
}  
   
print(add(2, 3));                     // 5

### **Go**

**define and call**

func add(a int, b int) int {  
    return a \+ b  
}  
   
fmt.Println(add(2, 3))                // 5

### **TypeScript (TS)**

**define and call**

function add(a: number, b: number): number {  
    return a \+ b;  
}  
   
console.log(add(2, 3));               // 5

### **R**

**define and call**

add \<- function(a, b) {  
  return(a \+ b)  
}  
   
print(add(2, 3))                      \# 5

### **C\#**

**define and call**

static int Add(int a, int b)  
{  
    return a \+ b;  
}  
   
Console.WriteLine(Add(2, 3));         // 5

### **MIPS**

**define and call**

.text  
main:  
    li  \$a0, 2              \# first input  
    li  \$a1, 3              \# second input  
    jal add                 \# call the function  
    move \$a0, \$v0           \# take the answer  
    li  \$v0, 1              \# print it: 5  
    syscall  
    li  \$v0, 10  
    syscall  
   
add:  
    add \$v0, \$a0, \$a1       \# the answer goes in \$v0  
    jr  \$ra                 \# go back to where we were called from

*jal means "jump and remember where I came from", and jr \$ra means "go back".*

# **Pointers**

A pointer is a variable that stores the memory address of another variable instead of holding the data value directly.

## **The House Address Analogy**

* **Regular variable:** think of it as a house containing a specific item (like the number 42).

* **Pointer:** think of it as a slip of paper with the house's street address written on it.

Instead of carrying around a heavy box of items (large data), you just carry the tiny slip of paper with the address telling you where the items are kept.

Only some languages (like C, C++, Go and MIPS) let you work with addresses directly. Many others hide them and give you references instead, which work like a second slip of paper with the same address: two variables leading to the same house. In every example below, we start with 42 in the house, change it to 50 through the address (or reference), and check the result.

### **C**

**pointer or reference**

int x \= 42;  
int \*p \= \&x;                          // p holds the address of x  
printf("%d\\n", \*p);                   // follow the address: 42  
\*p \= 50;                              // change the value at that address  
printf("%d\\n", x);                    // 50

*& means "the address of", and \* means "the value at that address".*

### **C++**

**pointer or reference**

int x \= 42;  
int \*p \= \&x;                          // p holds the address of x  
std::cout \<\< \*p \<\< "\\n";              // follow the address: 42  
\*p \= 50;                              // change the value at that address  
std::cout \<\< x;                       // 50

### **Java**

**pointer or reference**

int\[\] a \= {42};  
int\[\] b \= a;                          // b points to the same array as a  
b\[0\] \= 50;                            // change it through b  
System.out.println(a\[0\]);             // 50

*Java has no pointers you can see. Variables holding objects store a reference, which works like a copy of the slip of paper: both slips lead to the same house.*

### **Python**

**pointer or reference**

a \= \[42\]  
b \= a                                 \# b points to the same list as a  
b\[0\] \= 50                             \# change it through b  
print(a\[0\])                           \# 50

*Python has no visible pointers. Variables are references, like slips of paper that lead to the same house.*

### **JavaScript (JS)**

**pointer or reference**

const a \= \[42\];  
const b \= a;                          // b points to the same array as a  
b\[0\] \= 50;                            // change it through b  
console.log(a\[0\]);                    // 50

*JavaScript has no visible pointers. Arrays and objects are passed around as references.*

### **SQL**

*SQL has no pointers.*

### **PHP**

**pointer or reference**

\$x \= 42;  
\$p \= &\$x;                             // \$p is another name for the same value as \$x  
\$p \= 50;                              // change it through \$p  
echo \$x;                              // 50

*PHP has no real pointers, but & creates a reference: a second name for the same house.*

### **Kotlin**

**pointer or reference**

val a \= intArrayOf(42)  
val b \= a                             // b points to the same array as a  
b\[0\] \= 50                             // change it through b  
println(a\[0\])                         // 50

*Kotlin has no visible pointers. Variables holding objects are references.*

### **Dart**

**pointer or reference**

List\<int\> a \= \[42\];  
var b \= a;                            // b points to the same list as a  
b\[0\] \= 50;                            // change it through b  
print(a\[0\]);                          // 50

*Dart has no visible pointers. Variables holding objects are references.*

### **Go**

**pointer or reference**

x := 42  
p := \&x                               // p holds the address of x  
fmt.Println(\*p)                       // follow the address: 42  
\*p \= 50                               // change the value at that address  
fmt.Println(x)                        // 50

### **TypeScript (TS)**

**pointer or reference**

const a: number\[\] \= \[42\];  
const b \= a;                          // b points to the same array as a  
b\[0\] \= 50;                            // change it through b  
console.log(a\[0\]);                    // 50

*Like JavaScript, TypeScript has no visible pointers. Arrays and objects are passed around as references.*

### **R**

**pointer or reference**

e1 \<- new.env()  
e1\$value \<- 42  
e2 \<- e1                              \# e2 points to the same environment as e1  
e2\$value \<- 50                        \# change it through e2  
print(e1\$value)                       \# 50

*R has no pointers. Normal values are copied, but an environment is shared, so it behaves like a reference.*

### **C\#**

**pointer or reference**

int\[\] a \= { 42 };  
int\[\] b \= a;                          // b points to the same array as a  
b\[0\] \= 50;                            // change it through b  
Console.WriteLine(a\[0\]);              // 50

*C\# normally hides pointers and uses references. Real pointers exist only inside special "unsafe" code.*

### **MIPS**

**pointer or reference**

.data  
x: .word 42  
.text  
main:  
    la  \$t0, x              \# \$t0 holds the address of x (the pointer)  
    lw  \$a0, 0(\$t0)         \# follow the address and read: 42  
    li  \$v0, 1  
    syscall  
    li  \$v0, 11             \# print a new line  
    li  \$a0, 10  
    syscall  
    li  \$t1, 50  
    sw  \$t1, 0(\$t0)         \# follow the address and write 50  
    lw  \$a0, 0(\$t0)         \# read again: 50  
    li  \$v0, 1  
    syscall  
    li  \$v0, 10  
    syscall

*In assembly you work with addresses all the time, so every la/lw/sw line is pointer work.*

# **Structures**

Think of a structure like the blueprint for a building. The blueprint lays out which rooms (pieces of data) the building has, and every building made from it follows the same layout. In the same way, a structure is a blueprint for a piece of your software: it groups several related pieces of data, which can be of different types, under one name. This lets you create your own custom data types.

A structure is not a function. A function does something, while a structure holds data. In the examples below, a Student blueprint holds a name (text) and an age (number). We make one student, Ana, aged 20, and print the details.

### **C**

**define and use**

struct Student {  
    char name\[20\];  
    int age;  
};  
   
struct Student s \= {"Ana", 20};  
printf("%s is %d", s.name, s.age);    // Ana is 20

### **C++**

**define and use**

struct Student {  
    std::string name;  
    int age;  
};  
   
Student s \= {"Ana", 20};  
std::cout \<\< s.name \<\< " is " \<\< s.age;   // Ana is 20

### **Java**

**define and use**

record Student(String name, int age) {}  
   
Student s \= new Student("Ana", 20);  
System.out.println(s.name() \+ " is " \+ s.age());   // Ana is 20

*Java has no struct. A record (Java 16 or newer) or a class does the same job.*

### **Python**

**define and use**

from dataclasses import dataclass  
   
@dataclass  
class Student:  
    name: str  
    age: int  
   
s \= Student("Ana", 20\)  
print(s.name, "is", s.age)            \# Ana is 20

*Python has no struct. A dataclass is the simplest way to make a custom data type.*

### **JavaScript (JS)**

**define and use**

const s \= { name: "Ana", age: 20 };  
console.log(s.name \+ " is " \+ s.age); // Ana is 20

*JavaScript has no struct. An object groups named pieces of data in the same way.*

### **SQL**

**define and use**

CREATE TABLE Student (  
    name VARCHAR(20),  
    age INT  
);  
INSERT INTO Student VALUES ('Ana', 20);  
SELECT name, age FROM Student;        \-- Ana, 20

*In SQL, a table is the blueprint, and each row is one building made from it.*

### **PHP**

**define and use**

class Student {  
    public \$name;  
    public \$age;  
}  
   
\$s \= new Student();  
\$s-\>name \= "Ana";  
\$s-\>age \= 20;  
echo \$s-\>name . " is " . \$s-\>age;     // Ana is 20

*PHP has no struct. A class does the same job.*

### **Kotlin**

**define and use**

data class Student(val name: String, val age: Int)  
   
val s \= Student("Ana", 20\)  
println(s.name \+ " is " \+ s.age)      // Ana is 20

*Kotlin has no struct. A data class is the simplest way to make a custom data type.*

### **Dart**

**define and use**

class Student {  
  String name;  
  int age;  
  Student(this.name, this.age);  
}  
   
var s \= Student('Ana', 20);  
print(s.name \+ ' is ' \+ s.age.toString());   // Ana is 20

*Dart has no struct. A class does the same job.*

### **Go**

**define and use**

type Student struct {  
    Name string  
    Age  int  
}  
   
s := Student{"Ana", 20}  
fmt.Println(s.Name, "is", s.Age)      // Ana is 20

### **TypeScript (TS)**

**define and use**

interface Student {  
    name: string;  
    age: number;  
}  
   
const s: Student \= { name: "Ana", age: 20 };  
console.log(s.name \+ " is " \+ s.age); // Ana is 20

*An interface is the blueprint, and the object made from it is the building.*

### **R**

**define and use**

s \<- list(name \= "Ana", age \= 20\)  
cat(s\$name, "is", s\$age, "\\n")        \# Ana is 20

*R has no struct. A list with named items does the same job.*

### **C\#**

**define and use**

struct Student  
{  
    public string Name;  
    public int Age;  
}  
   
Student s \= new Student { Name \= "Ana", Age \= 20 };  
Console.WriteLine(s.Name \+ " is " \+ s.Age);   // Ana is 20

### **MIPS**

**define and use**

.data  
student:  .word 20          \# field 1: age (starts at position 0\)  
          .asciiz "Ana"     \# field 2: name (starts 4 bytes in)  
is\_text:  .asciiz " is "  
.text  
main:  
    la  \$t0, student        \# address of the whole structure  
    addi \$a0, \$t0, 4        \# the name begins 4 bytes in  
    li  \$v0, 4  
    syscall  
    la  \$a0, is\_text  
    li  \$v0, 4  
    syscall  
    lw  \$a0, 0(\$t0)         \# the age is at position 0  
    li  \$v0, 1  
    syscall                 \# prints: Ana is 20  
    li  \$v0, 10  
    syscall

*MIPS has no struct. You decide the layout yourself and remember how far into the memory each field sits.*

# **File**

A file is a named container for data that is kept on your computer's storage (like the pantry and fridge in our kitchen picture). Variables and arrays live in memory and disappear when the program ends. A file keeps its data even after the program stops or the computer is switched off.

Using a file is like using a paper document. You follow three steps:

1. **Open** the file, saying what you want to do.

2. **Read or write:** take data out of it, or put data into it.

3. **Close** the file when you are done.

When you open a file, you choose a mode:

* **Read:** you can only look at what is inside. If the file does not exist, you get an error.

* **Write:** you start with a blank page. If the file already had text, the old text is erased.

* **Append:** you add new text to the end and keep what was already there.

Many newer languages hide these steps and open and close the file for you. In the examples below, we write one line, "Hello from the file", into a file called notes.txt, then read it back and print it. The file is created in the same folder where the program runs.

### **C**

**write and read**

FILE \*f \= fopen("notes.txt", "w");        // open for writing  
fprintf(f, "Hello from the file\\n");     // write a line  
fclose(f);                                // close it  
   
char line\[100\];  
f \= fopen("notes.txt", "r");              // open for reading  
fgets(line, 100, f);                      // read one line  
printf("%s", line);                       // Hello from the file  
fclose(f);

*In C, fopen opens a file, and the letter says what you want to do: w for write, r for read, a for append.*

### **C++**

**write and read**

\#include \<fstream\>  
   
std::ofstream out("notes.txt");           // open for writing  
out \<\< "Hello from the file\\n";           // write a line  
out.close();                              // close it  
   
std::ifstream in("notes.txt");            // open for reading  
std::string line;  
std::getline(in, line);                   // read one line  
std::cout \<\< line;                        // Hello from the file  
in.close();

### **Java**

**write and read**

import java.nio.file.\*;  
   
Files.writeString(Path.of("notes.txt"), "Hello from the file\\n");  
String text \= Files.readString(Path.of("notes.txt"));  
System.out.print(text);                   // Hello from the file

*These shortcuts open and close the file for you (Java 11 or newer). They must sit inside a method that handles IOException, Java's way of reporting file problems.*

### **Python**

**write and read**

with open("notes.txt", "w") as f:         \# open for writing  
    f.write("Hello from the file\\n")  
   
with open("notes.txt", "r") as f:         \# open for reading  
    print(f.read())                       \# Hello from the file

*A with block closes the file automatically when it ends, so you cannot forget.*

### **JavaScript (JS)**

**write and read**

const fs \= require("fs");  
   
fs.writeFileSync("notes.txt", "Hello from the file\\n");  
const text \= fs.readFileSync("notes.txt", "utf8");  
console.log(text);                        // Hello from the file

*This is Node.js, which runs JavaScript outside a web page. JavaScript inside a browser cannot freely read or write files on your computer, for safety.*

### **SQL**

*SQL does not read or write ordinary files itself. A database keeps its data in tables, and the database software manages the files behind the scenes. Importing or exporting files uses commands that differ from one database to another.*

### **PHP**

**write and read**

file\_put\_contents("notes.txt", "Hello from the file\\n");  
echo file\_get\_contents("notes.txt");      // Hello from the file

*These two functions open, use and close the file for you.*

### **Kotlin**

**write and read**

import java.io.File  
   
val file \= File("notes.txt")  
file.writeText("Hello from the file\\n")  
println(file.readText())                  // Hello from the file

### **Dart**

**write and read**

import 'dart:io';  
   
final file \= File('notes.txt');  
file.writeAsStringSync('Hello from the file\\n');  
print(file.readAsStringSync());           // Hello from the file

*File access in Dart works in command-line programs, but not in a web browser.*

### **Go**

**write and read**

os.WriteFile("notes.txt", \[\]byte("Hello from the file\\n"), 0644\)  
data, \_ := os.ReadFile("notes.txt")  
fmt.Print(string(data))                   // Hello from the file

*0644 is a permission code (the owner can read and write, everyone else can only read). The \_ ignores the error value to keep the example short. Needs Go 1.16 or newer and the os package.*

### **TypeScript (TS)**

**write and read**

import \* as fs from "fs";  
   
fs.writeFileSync("notes.txt", "Hello from the file\\n");  
const text: string \= fs.readFileSync("notes.txt", "utf8");  
console.log(text);                        // Hello from the file

*Like JavaScript, this runs in Node.js, not in a browser.*

### **R**

**write and read**

writeLines("Hello from the file", "notes.txt")  
text \<- readLines("notes.txt")  
cat(text, "\\n")                           \# Hello from the file

### **C\#**

**write and read**

using System.IO;  
   
File.WriteAllText("notes.txt", "Hello from the file\\n");  
string text \= File.ReadAllText("notes.txt");  
Console.Write(text);                      // Hello from the file

*These shortcuts open and close the file for you.*

### **MIPS**

**write and read**

.data  
fname:   .asciiz "notes.txt"  
message: .asciiz "Hello from the file\\n"  
buffer:  .space 64                \# empty space to hold what we read  
.text  
main:  
    \# \---- write \----  
    li  \$v0, 13                   \# 13 \= open a file  
    la  \$a0, fname  
    li  \$a1, 1                    \# 1 \= write mode  
    li  \$a2, 0  
    syscall  
    move \$s0, \$v0                 \# keep the file handle  
    li  \$v0, 15                   \# 15 \= write to a file  
    move \$a0, \$s0  
    la  \$a1, message  
    li  \$a2, 20                   \# 20 characters  
    syscall  
    li  \$v0, 16                   \# 16 \= close the file  
    move \$a0, \$s0  
    syscall  
   
    \# \---- read \----  
    li  \$v0, 13  
    la  \$a0, fname  
    li  \$a1, 0                    \# 0 \= read mode  
    li  \$a2, 0  
    syscall  
    move \$s0, \$v0  
    li  \$v0, 14                   \# 14 \= read from a file  
    move \$a0, \$s0  
    la  \$a1, buffer  
    li  \$a2, 20  
    syscall  
    li  \$v0, 16  
    move \$a0, \$s0  
    syscall  
   
    la  \$a0, buffer               \# print what we read  
    li  \$v0, 4  
    syscall  
    li  \$v0, 10  
    syscall

*File syscalls work in simulators like MARS. The file handle returned by "open" is like a ticket number that you hand back for every later step.*

[image1]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAmwAAAFbCAIAAADnYEX6AACAAElEQVR4Xuy9B3zURrvonbzvOd8953z3u18CuFNtsA3udNNDTwKBFNI7ISEECAkEML2Y6kIn9BoSOrgABoyxwQ3ce++99+5d3Wc0a7HWrO21vd4ij/IPP3v0aDSjXeu/z2ikfY2hC13oQhe60IUuXVpe4xfQhS50oQtd6EIX+RYqUbrQhS50oQtdurhQidKFLnShC13o0sWFSpQudKELXehCly4uVKJ0oQtd6EIXunRxoRKlC13oQhe60KWLC5UoXehCF7rQhS5dXKhE6UIXutCFLnTp4kIlShe60IUudKFLFxcqUbrQhS50oQtdurhQidKFLnShC13o0sWlGxKtyGCKopgcP4oyKE9lRE3scRfzXgcFLA2JTE0gU/WA0vM8ZOpjGXEje9wV/FKKxKKiuvyMquT48khKT5NQHlVQl9Ny7BX+UjIFVc3RuY0xeZQeJza/Ma+ymf8ayL10VqLse6Uoksl4wmQ9Z3lGUQbZcKh9mNwApq6EESvkL1aMTuXgzopbTKU7ixtFKdxjKl2RTZsKFHXybRY3gTtjykLjysJjEWEUJQBHO7o0BGxa1VghVtRLKWLSSpoicxvBoFEUZRGd1xiRg2zKdP5vspMSzfKm4lQ96Y/ZrLSzr3XrpdKFOLlTlE7F9ZastOsLuJM8v1OUTETJi2Zx17MZvETm8E/uFOUTmtUIH2XkXzojUZR9Eid0imrwRilplxeUfRIndIpqcOG/Op1ZokqDyBM6RSXApxn+y9OZJSybfzanqAr4NMN/edpe5JOoWIwuf/LP4xTV4sN/meRaxEztC+I8TlEtXfGomBFnVKeQp3KKCumaR8XUoOpHhNwelUOiYFA0ikuexCmqJsOL/2J1sIjpKK6aUnGb/1p1tNBRXPUkqjSos9dHI+gorloCn2zkeSHlkCgsaFYLcQanqBx4XQrD+S9W+wudQKSmuDM1fvwXq+2lsrGcPH1T1IG4snCRuBOX1CrrROTpm6IOROc2iuSwaEcSpQO5ak72M/5L1uYiZmoDiXM3RZ2Qb4FEJ7o0mDx9U9QE+Qd14RQdTtNQNUaei6MdSZSh84nUnuaOX2bJQucTqTniBv5L1sbC3srCP3dT1ASQaLMY39Xd8UJvZVFnInM7nqnbkUQrMuhYrrqT689/1WQsYqY+kY7lqjtVD/mvG7FAGlpUl0+euClqRUJ5FP+VIxZIQwsrm8kTN0WtwDePtrN0JFE6lqsByDdNl47lagCu/FdN1kIn5WoE/JdN1pJW0kSetSlqBSSj7V8Y7UiiOf7EKZuiZmQ84b9qMpcqD+KUTVEzKm7xXzVZS3x5JHnKpqgVUaVB/JdN1hKTxz9lU9SNDufodihRP/4pm6JuyCvRB/xTNkXdoBIVClSigoFKtBdAJSoYqESFApWoYKAS7QVQiQoGKlGhQCUqGKhEewFUooKBSlQoUIkKBirRXgCVqGCgEhUKmivRyJyGKPTVYE0qgWyPyqES7QVQiQoGKlGhoIkSBX16RxfsOXsP2Hf+gUo4cMUzLLMWi1xNoBLtBVCJCgYqUaGgcRIFbz2PK3K4+BDYcdLt4BVPJXPgr8d7zz9wvPRwz7n7d54nkC1UFVSivQAqUcFAJSoUNE6iF+4Fg8C8ghKaReLKmobqukblU1WLHnt5yT0ARP4stlBN8lEq0V4AlahgoBIVChon0d1n7tmfuVelIn1K09DYvPvs/T1n78UXicl2Kh8q0V4AlahgoBIVCpol0ei8RkhD/cJTSKWphMqa+v0XPJ5G5ZNNVT5Uor0AKlHBQCUqFDRLomGZtfvOPyirqiV9phJEYsbp8qM7volkU5UPlWgvgEpUMFCJCgVNlGhppXpJ9LZ6TC8SuETF2c8Lku+hL6YmVikEUaZ3Y45fSMgZcpUaQSUqGKhEhQKVqDyALJ3/euxw8WFdQxOvnEpUiRQEb7n+LZP/kl9O0JzpzWT7SpCjXxD/0NepKuOpOMuHXKtGUIkKBipRoUAl2iG19U3YoPsveGw+7iI9JZhKVNmIwY75Qc8Cj0LiSK5FAVk+dZk+prsGTXSywEx2svQPOtFWPCLvxYpL77cXoD5QiQoGKlGhQCXaISDRg1c8waDA9pNuVKKqB1LGz0/NFGXKyhqzfd89NmGqs/UUZysO671DmcJQfmTWs6YML4h/4OskIlapKVSigoFKVChQiXYIlag60pz5dLzD8POPNkBi2mpVtu/cI+N4ErXcY8STqBgEXBQxZLsukxtAVq6+qIdExeUuTPU9QeNO9lrBUIkKBSrRDqESVVdy/DZe/8bWYQS68MkVyiFRcZZPVYbXkO16bKGsdFZtUblE6x82V7ime255cfDDF4cEy8tDH8X+s6yx4DrT5MlUEAdBIVCJCgUq0Q6hElVfRJnegUEn5h4ey+S1zDbqSKJgULtrX9vsHdacrXn9VaFEUfZZ++D5nnf89s0LcFro7/CesAlwXOC/f77PjllNxbdR34kD0l2oRIUClWiHUImqPXkvJzlZ/vHPF0ilbUsUjOv/8k9bRzNIQzVjGhGJiiQKFvHd+05vcKcMHBc83TpdXH2fPCzdgkpUKFCJdgiVqCaQG2C2a/C0A9ZMYYhMiYoLQkLCL8EPz18cR1N8yRo0AlVIFAxaFvMnysxIwfQafHbOFlfxj0y3oBIVClSiHUIlqglk+jRn+TD18Rdv/Db+gKW0QRGHRu7YNYNJfdac80ycrrEGzVKBRMUVrnHXl/eSHNRv/3y/ffPb6qzv3neZOg/yEHURKlGhQCXaIVSi6k2mD1PysjnKLf2tMSlmRqnjzOfut5raWqI2x6wKR1mm2VpmTB9Xsus3piQIbUVWpf4oXaJM3cPnu98mjSI8Xh5e1FR4o6n4VrrXtue75pIqhVy8Iu4k//h0GSpRoUAl2iFUouoKiDDXV5TwMG28ZfpE6/RJNkDmRJsZjjIkWjoGrU2fbJMxdXTqSNO8JR8xRS+YDE3LSpUu0VSPDaROBAZ0sDzxDFMlua0FTSNqeJTptc2fGMEOcF5IHqIuQiUqFKhEO4RKVP0AfZYGZ86ZmGZrlT55JNYnR9FY5FEQJ0fWBJu01jGIKaPSRo+o9bygSSpVrkRBJ947ZpHWERgVYFCi70DcjRU8j/rtm4fuIiUiuwKVKEFMaWh0UXB0sVKJKQ4hW9IpqEQ7BCTqyD7zD9h2wpVKVA3I90+1MYW0ku/FFrIm2pSMkQA5qAyDSlHrekJjRneVK1EQBmiDtI6QeHlkEZeD8ml49Mx+jnQw5KxM42N+WNegEm0NGDQk5dm9W+fdb51TJvdunfPyvkW2R36oROWhrqFp83EXMGhcWr50OZWo0snxLVj5ZcbU0aQLu0PaWHOmQsZzAdUOKlGFAr1rKrjB73ULkIhneG6RjqcS7Tmii4Lcb5+7d/u88rl/50JCdRTZJDmhEpUTSEClc1AMlahyKQgo+OXzjGljSAt2n7TxlkzxSyZDvVNSKlGFgiRadIvf6xaQRJ9slY6nEu05oouDUV5IGE4JUImqECpRJZLvlz7OkjCfBTg1461xqaOHk17sLBlvjS07YMffr1pBJapQQIqZXtvafCBR9b3AA60mVVGJ9ihx5eGuV0+7XlMqbtdOByf7kI2RHyrR7kAlqiTE2c8Kln3Gc17aBKvaIw41B/cAdcccU8eMIL3YaWytmNJgsgHqApWoonm+ey7T8IjfcUz9w2e75koHC02ipUSJqkmoiYKkUMl08zhQiXYHKlElUetyPGPKKJ7w6o471RzYzVF7eG/aOHO+FDtP3nfvg7PJNqgFVKKKBiej/I4DFa4BB94ngwUj0dS66NDcF+H5L5VGREFQfEUE2RJNRxMlWlxeg69QqpymZjGVaM9TGMifSTRlVNGyb6UNKsHZnpRip5k8Mm2chVg973uhEu0BAhwXxN1YAfmouNwFDe1WuUMOGujMNyiKFIpEk2oiv12x4etf7JTJN8vtvli6Lrmm61cf1RONk+j+Cx47TrptVxNOuDpcfEgl2oNAUpi3+EO+5yZaVzvu4Bv0wG7ITdOJhLULQNbLFL8gG6N6qER7BvDoM/s5GZ5bICsNcH7/+a655JMWUJhAJBq60cGZlJxycH9xP6Y0lGiSBkMl2i2oRHuasgN2/DR0EkoWy+x+JSVae2gP+eyFrpE5ZwKTK/U1pWqCGkvU1+G9KIf3nzjM83KYF+6w0I8IkAbWBji8F+jw3lM2PkKO+GCHBTje22H+C4cFvkSMNFxjnrKNgXgypgsIQ6LxFeE//L6F1JtyOHXrr+iS7j7fQK3QOInS4dy2EKBExelPU6yMScMBGdPH1TjvaiVRx52FP35JRnYRWytR/EO1ewiDWkoUG26745RRBy0mOiHGHLD8xmlsUBuqg3gQ59vOI8c7W05g48ey8YFEpHT8JGcrHA+85Wz9l+PstuKlGzOBbQzEt9WYTiEYif64ZhupN+Vw9u7fVKIqhE4sagfBSTTTByTaTmaZ88Hc2qMOSKVO9jUH98h8BGB3SLEcpnZPYFA/iYLhfnAaN83Z+sNz0y7FbjsTuRG4HLd95d2PJ+43m+Bs+dxhfisPsfFj9pjs8l56IXrLWTb+bOQmiJ90wPqC4yxe/EuHBaMOWED8yXA7iMf1HwlaM8XZCuIhheU1BuLJxkA8bgwvvrMIQ6Kx7DXRjxev+Xblxm9XbPxmxYZvlvcssBfMwi9XxZXzG6PpUIl2ByrRHkSc5ZP3w0ek214xZWT6BKvCxZ8V/fwN0qdCDQpkTB5Z636SbJgqUT+JhjosnOpkud1ryamIDaelOBm2/lzU5vH7hl91mCPtxZ+cxkP83/E7T4Xb8eI/uTBjygFriOeC/Rzmj3JGCSXESwcDF2K2QLyts2WolBfhZ4gnGwPgxtgSUu8UgpEokFIXffzqxZM3L9sf/fPXTftXbNjXc5y4cfnUrb/O3P07vTGWbImmQyXaHahEe5LKsBRr2WO5rZg8SiGTiWQweWTWvKnqNaKrZhINdHhvurP18jsfnQhbz5MWAJoENdo4W0Q4SGa6QjxoEuLJYOBs1Ka3DtpAPPYcHsUdu9f07/gdZDCOnwb+dpyCK/djGwPx7TQG4rnGdAEhSTQWPSQoJKY0dOfBM5v2nehRrnm6RxYFC2wUl4NKVE5q6ptqG5qqWhdSifYYGd6QBfKtpnTSRo/gN0y1qJlEzzvOmuxkQRqL42S4ne2+Ed87jfNjJ/tA/JxjY8kwjsux2yA+oOU66yRnq5NhrRJWHr+7fWZ7wAo3BuKhMe3EQ2MgHhpDdkROBCZRIK4ifMeBM5v3n+xRQKLRJYKakSsNlWiHVNU2xqTm7Tl3f/8Fj6sPg6RXUYn2IAW/fN5TKWZnQF87SrRNZaiTRMFzS5zGT3Gy5A3M8vj04sypB6x92eQS4nd4/dhO/Ck2/qLDLIiHtHX8AcsL0VvIMI6zkZsm7DcDffrhNNep43hoTHBXJ+tSiXYNKlGmd0tU+vtEd5xyr6RfhaYMykPamperVCaPFCU9VqMRXTWT6GxnmxmHR5Gukmb5nY/GHERXIgPZ+OMha8kYDkgWIX6H4xSIf+owb6KTxZnIjWQYB8pc9w6PcHjfj737BRrTYTw0pssjulSiXYNKlKESpV/KrWwqQlMsh/GVpnyoRNuV6NvOIzuU6LJbH4xtkSjEHwlaQ8ZwgEQhfpfjVIj3lkOil2K2gkTDWYl6yyFRiIfGhFOJtkAl2n2oRDuESlQFgLrSx/O/s0UllB/ZJE5/SrZQNaiTRIE9jlMn7jcjp8JynAq3m+Rk8Y7zSJAceBHiP7kwo534C9FbIN7HYR7EQ7449oDl2XaluN1rySRnK3zDKMRDY9qJh8ZAPDSmrRtMO4RKtGtQiTJUolSiSkaU+Cjd1opUmvIpO2BHJdoWoQ4Lxzpb7vL5+WQblzlBimOl7kJB98M4W0E8GXmaTUM/vzwb4v3YC6i+DvP/cpg9xdmqrcucED/RwezblolCEA/bQnw7jYF46VtiOguVaNeQX6IxJSF+off9Qh8oB/+wB3HdfiY+lWiHUImqACpR2aiZRCFffOYwf8J+s3ORm3jThU6xFyAnOlnscJzyrOXWTIh/y9ka4s9GbeIZ7hSbVk53tt7RcsuKPztXaNIBa0heZcSzaaWVs3m0wwdcPOwI4snGnG5pDMRzjekCVKJdQ36JRhcHk1+a3XM8uHsRfRUa0YxOQSXaIVSiKkCNJHpwA5Vo+1x0nDX+gNUEB7PDL1f/Fbf9ctw2cNisI6OnOVv/4DSe97A9cBjET3Oy/PTCzLORGy/FboP47U+XQLzVAfOXxMP5IhwW2jpbQvzv7p9BPLjwYszWn24unORgDvEBRGMgvlVjYlFjIB43hozvFFSiXaNTEnW/ebYoN7kwJ6mnKS1Id7lxmkpUCVCJqgBxjm/qKEV8yXa3qXU/qUZfi6aWEsXPRpjjPHKSk6Xt3uHABCcLMN/fjnP8iGAcv91xyugDFqA6230ofpKzFcRHs/ODyPhQh4UQb8uqEdW/b8SYg5bfOo2Nbnt+EK8xEN9WYzoFlWjXkF+ioDS362dK8tMKshN7mtyMOBB2XHk42YxOQSXaIVSiqqAyLMXciFSaspk8UhTvQWfnykmgw3uRDu9HOLzf4bes+LMqDXFYGIF4P5B9FAMZw4ONh/oX4rtO26d1YzqOlwcq0a4hv0TjKyPu3T4PeiOdp3DCXz4BiZJt6CxUoh1CJaoKcp5nzp6g8MfhdpaMqaOZqnB+21SIektU8FCJdg35JQp5oYfb5cSYF6TzFM7zJ3fcbpzp/pebUol2CJWoChCnPy3d/4eMbxJVMrZWTJ4aHRYqUdVCJdo15JcoKC0k9Zmv113SeYolPysBUl4vn1tkGzoLlWiHUImqgkwfUbKnyucWpVibqNGsoiwqURVDJdo15JcoEF8V6XrjTFFuCmk+BVKcl+J+40x8VXfvb4mlEpUDKlEVUfwiTaXPW8iYMir/50/5rVItVKIqhUq0a3RKopCMut04++zxLdJ8igLS0MSYFx5ul7s/qyiWSlQOqERVRKZPc8x9FV4WRV/KXRnGb5VqoRJVKVSiXaNTEgVC0p7fu30+JS6Y9J9CgDTX7aZi0tBYKlE5oBJVHaVBGZNV80UuKA398WNxptrc3IKhElUpVKJdo7MSja+MBIm63TwLKSOpwO7j8/imQublYqhEO4RKVJWAyTJU8YVoqaNHMCUvyfaoGCpRlSJIie482OMSvf6kcxKNZa+MgkcTogMV7lGfR2DQc4pKQ2OpROWASlSlFL1ItTYhJdfT1HmcVaNnLHAoV6LichefHbNIl/Ra4CMFfLAgD1RXUA+JxpSFHbtydYvDKdJ8CuRJlHeX7iQJdbt5pig3mRRhlynJT7t/50Jwsk+X2iMbKtEOoRJVJeI0r7JDG0jJ9SwTrNXrzhYO5UoUCHDq4vdXCxL4SAEfLMij1BXUQ6JAWF7Qpn0nSPMpiq2Op5JqutIL8BykjC7XTxfmJJE67AJgUPdbZ728FXBbizRUoh1CJapixOlPk00H8z3XY6SNtQBzk81QC5Qu0cbCG3REFxPgtDDTaxt5iLqI2kgUXBVfEb7FgS8/hbBxz59PIp+SO5WTmJJQyBpdrp/Kz+zWoG5+VkJxXgq6MfTpTQXmoBgq0Q4BiTpefIgluu2EK5WoCgCrpY9T0u0u6vW1LTyULlGm+l7ggff9HWk++t7TbTMUdkG0UnkSBWfEVURE5ge2Q0RegGfoo027j25yOq8wHM9v23csJNMPKif3KD+w+b3bF1xvnMYuJAUpDylxwWDix4/+iSp4IV05/BrbbadSicpDXUPT5uMuYNC4tHzpcipRJVIZimYYTbbpOTKmjc777n1GDS+FcihfopVu4kq32KvLSKn0Kvz2z2dqFXlUlSPRxNpYh8XTD66Yd2D5uwd+eac9cAD8q0DIvXSJg8vnOf0064HrZRBhQlSg/KO7kH3mZcaDgB+4/HVwxXyyZmik45KZfuF3yUMnP1SicgIJqHQOiqES7R6ZPkz2c3Gmt1xkPM3/5bOMWbYZM8f1EOlvjWFKXvL3KxMQbS4cLqU/mF4VEkVUuffmGUa+e98tjfmTf0y6Sc9LFBLQw6sWKFBmqsVp6Sz3G2fu373o4XI5Jz0GVAqJqczcFA/ewr9uN8+43zp77aS909I5ZIUce7+eHFMSQh5AOaES7Q5Uot2iIc6t8sWFyhfn5SXwfGXQpZ7kotztuVDhf7Y+5g6T7Uv2qwdRlUSBOg9wSUBvG9d1XPB06/SmMhdxhSv/gHQTpUjU4YcZpDM0F+dlbx9e9T6klffuXHhw92JooGdSzAuwaUl+GiYvMw78Gv7Sy/3WOdCn67UTp7Z8L8/HCEjZyQMoJ1Si3YFKtIs0JXlUBJ5jjaXpXKyNuA75NNnHHkGFEq10QyKpuZ/ttyfAaSEkpj47ZwsYv33z0zw2Nle4Kmw6Lo+el2hkfqDzz3NJYWg8y98Fm8K/l53XgSbv37n40P0fjNuN06DPiw6/Oy+b67R0Nn/DNji4Yl5yYyJ5AOWESrQ7UIl2BbAOuIewkeZyEVJkJaWkKpUoBkml+h7T9BjNshEwdR49pU8MlWi3Obh8HtgUZOn44wwMuBOAcjK4HahEVQiVaKcRZz0TlkFbCDhHdlbxqIFEKYqBSlRtoBJVIVSineV51ctLfP0IhItMTs8no1SigoFKVG2gElUhVKKdQ5zxFM/KESR10Xd6fL4ulahgoBJVG6hEVQiVaOeoj7krzLFcFkiyIdUme61IqEQFgxIkWvCCSlQekEQbEsgDKCdUot2BSrRzCHcsF1ERcLbHjyGVqGDoeYniJy2QzqDw2P/9W+TRkx8q0e5AJdo5qES7C5WoYOh5icayX8x5ft/SA2yy1YqV6PE9B3sVy9+BXvOPwwo0jzeq8AV56OSHSrQ7UIl2jtrw66R7hESP3+hCJSoYlCJRzLOX191uO7necsS43XK673Jo1ftjexW/vj/u0cMT0HfuOADudw8m1sWRR6xTUIl2ByrRzuIj4IlFDfFudGIRRV6UKFEe8RURa7+YtnLBmN7GjzOHpzUnkwekm2iiREsqakifqQQq0U6S7Yse3UfoRxBcVMZzi6hEBYNKJbrm08mkYwTPkummVKLhWbUOFz14X6WiQtC3pF16eNcviWyq8tEEiQI5/oKcoFsFEiU7q3CoRAUDlajSoRIFovOaIBPdftKtorqeVJqSwV/WbX/KLb5ITDZV+WiIRLOeVSGJCsqjFf5nmFx/sqeKh0pUMFCJKh0qUYzjpUeQ/FXW1FfV8q2mTGobmiISs/df9Lj1LD4yp4Fsp/LRGIkyOb41Yf8IyaP8DvYcVKKCgUpU6VCJYpJKme1/uuw9/+Cv+y8qaxpEYkbJNIsZMCjkoPsveOw5ey8mv5lspErQHIlisn2rgi5XBJxlbappvLzI6vNiU/KjHp9MJA2VqGBQnURjS0P3/PEZ6RjBs3S2eXK35+KSaJxEAcj8zri82H3mnsMFD6fLj5QPZMP2p91uP0tQH4NGaZ5EMTl+DbGu9bEuGkbMXTH7jeL87vQ0VKKCQYUSLQtLaUz4ceaIJdOHQ3LWe4iviIQPEOTR6CaaKNEo1qPReU1Po/JvP09QPnf9kuKLGDUZxeXQTIlSOgWVqGBQqUSB6OLg3gZ5EBSChkqUQkIl2gugEhUMqpYoRVFQiQoGKtFeAJWoYKASFQpUooKBSrQXQCUqGKhEhQKVqGCgEu0FUIkKBipRoUAlKhioRHsBVKKCgUpUKFCJCgYq0V4AlahgoBIVClSigoFKtBdAJSoYqESFApWoYKAS7QVQiQoGKlGhQCUqGKhEewFUooKBSlQoUIkKBipRucl+zuT6IshVPUEO3p0iDm9PSlRcAbiS5Yqh5p4EcpVCwJVXufPLlQluQ7V8fewZiSZURiRURgLkKnno5ua9k14uUfbRffI+vS8iuy46rym2QASQazHRec3tB8QWiNsP6DJKlCi8aarCEDnK8pBCOe1gN9LKwtrSXJzpIybWKpbmdO+9G5dbmpsZDTVSgLZ7SKK19xmxZ03BrZqCm6wG3OW1qUw1EoVQ2+SJo6wszQBG9JhfSbepLbg5YriJpcUIjzu7mstcyABlIPYcNGiwtZX50h8W8lfJpEsSzWVSc5iUbCaFK0mpi4USII9Ji6+MGD9xnIWlubGxcVpjPA7AUowrDyfP/jxiSkPJzQVJvEI/K3RHoikVTEatFDVMXBETkVVHRnaNHpINJqmMgX+DUsrBo+nV6Of2gbBLd7zmvrvQzNzC0somvUb2JjudTsDaYcOMZT5ZFw7OoEGDzCwsjYyGkmu7ifIkumLxp8NNTYYONcoJuYOew04EqDnHdv9hPGwYtF85Et3+x0+GhoY6evrqKNFq9+MHf4WzvzEcj6FGABwY+HXDH1/yIwkgc50yeczgwUP69NNlmCftFrqOHWNlYmIMMGLFS7Qm/+bAgYPgILvf2KEyiTKeffrqwkH85st3+Ktk0nmJJtVE9zcwMDYxNrMwi2EfpJ7ZnAgdH2Y8TF/PIK0hDtwwcowNBMBZJr0pAWIiCl/q6+kPGTLE4dQe8uzPA+KtbODcZNTfoD9sTgYIg/iK8AmTbAcPHqzVTztTlEQGdJYuSxQk8fUPvwwzNn7FMGNomI6OdmKpbMHID1QemlENtQ0ZYphW1d3aeEDl3hGZ8FaBNzzsAv4dPtwsvqi9vURk199+EgKbGBoZjTAzb0ei2/YfNR0+YuDAgW1JVKtfX/hj19PVJdd2E+VJdNl3Hw9jjx0nUWSjFpuCNprSn5JbcUgHS5dIF8LPqJ60p6IM71aRxOa8baV/hW2hBunNMTyJQmt5DUZ7z0C9gM2b05/yWsvtBf9ANhIDm0MX2pKopH42hqy/TRQqUVGF66pli+AvF5oHb24T42EW5sORUI2H2a35AseA/6SzUvwrLhGVu741bRxsqK2jLxZ7suWyC8WVbicO/Xpw/zKAqZe0TbrmplKXJlnyAyNyUuS1RBqeRIGm0rtkGIPajFaRooVm460A+Jm3VnrXvMpf/aoUierq6MKxNR1uCsLLECWCHaHXsNOU+tiYktC4ivAdB7Zs2rt+vf0fEBxdEhJe8GJA/wEQ4Hh6L2yC1csBAVFFwVHFwbiclCi7NoTUBkRKbyhdzu0F2gMxvACZRLORqLYSfnB0MWphNNEGfl9K+SXSv/J6EVceNmnqROimro5eRnMiuSG0pP2u4ePGreqORL/8fqkhu/Tt80a/Pm/o6ergXxcu+jwqh43JrgdthGfWAuAhsgbONOFZtQC3CoJD0qtYzw1LrRRLR3I/w79oE/ZXnrFwiUyNAQklDNKhoeGA/gaBCcX/3POd/fb8hGLZUsSEZ9X9tHItbKKrox2TL8LfgCa9F2gw7uPVB/4bdx1Yu3Wf9N4jc9BaKGlLolwAV20Uv0f17CGqa6tTUSqUaG3ioxEjTK0szO9dcvzhyw909Qze7Kf9+9IvmXx/ctumDB9rS3MbS4vLR7ZKCgsDoMTSwszG2oIpCBBn+DDFL2ysLHR09d/oqzXEcMjW1UtEmSgS9rX6569srMzh3MEUvUDbFgVamZtZWZiNsrEUgYpyfaElluZm4IMn1w7DZ7B//6//zZSwkVJwEmVynp9z3tRPS1dLR/feZSdUA7sX6GD/AQP7aeu+2VdLW0fP1MS4IdVLzJoStHfawQ52ATUweX4Tx4+GRsIZHDZ/tYuSoCVffvBmX209fYOskDtbfl8iLVFx9vPPP3x3wMBBffpp9+kHxQawL6YsmNdI2ShUovZbFhsbD4W2GZsMY5inIlYVoBnwQUzQCXBJhP8xK4sRYNaEsFMM6xIItrQYAS89pLDjxlnDMYQSOJNbWo6A8g8XTLcdb8MrXDBvGlPlzhvOPX3kt5E2FrB3pvreuT/X9NPS09LWu3drJycwUZnL4m/m6+r119Pvv2LZRwzzbKS1ubWVOX/omIWTqOu17S99DunoGIDPtqz/mmnweBXW9PCXnz6AjwhvvKkN1W61+/pVTtz0CDSjr9//zT46ALy7fl/5CSN6hNdyY8X3b+984rZHR0f/3//5f6Cd0MLEyLNQVZ8+OquWL4IWKlOiB845oBQDnZL00luGXlsN5zbEjx47ytzSHJ+UTU1NzC3MjE1MQLQQmVofu/Dj9wYNHNSvTz89XX0LS7OUutgYKYkWMpmffvtxvz5aBvoGLzKec3oDn+05uhNyX1gFjbG0toS9Y7XA3ocPN0V7MTZ+EOQybNiwfn21IC2Gzbku8CkPW2m3HM7G0AwdbV34owQ/4dqg/dudN0NLYNXAAQPnfzgvuTYGb3XX94a5uZmZ+QiPYFdoGMT/sOI72C+8LfHmIbkBcBCAAqleLF7+HQQnVEWOGDHcqOUtas6GzX53Vkwp6lpYXiB0TQdOB2zX3AJucV2DA4u7ls9kwDtER0sXWojb032JopbnNSFTZtXq6+lBiYG+HgT888Af3lEGBvr9+vbp1/dNaPHiZb8ll0tcxQ17gpB2Hzyjo91PV0fr5BU3sAXUPGoMNNgSv/rwg5mFpYmJCSgKtoKfYauXKaVm5hbaWv1cfCJgLxaWNvuOXsAjyRE5DRaW1mjM1domoVhMygbaMKB/f6h5wID+4Zl48LlNM0WxPYX3A6Ta7GEfAvsdPmJEfDEzfsJkcwsrY2OTnEZmyJDB0IVvf1yx05E/nJtSzrBvpzdNTE2fhmXwJAqduu8fAwFaffsYm5hCVfBnDm3//NsfJQFZ9bsOnIa9s4dIGypPqZD9LWwqk2hN4qNBgwdDr/745evhpibwl4D+aE2M7VZ+R27L5PoNHDQY/lDBIs2slkRZz8AjsNWt03sgLatM9gT94IGCQWwk6Grn2p9EbPK3/PtPIE/S0tHjJDoURRrBOQJLFFoCm8ABZYcopSKlwBKFsMWfL4R24pM+dCfx+VXIKWEvS776AMTWV0vnjT5aUA+sBdGWxT9kWInC5rCtgcEAsCBsjt+myCuFgbhJUAiNhJjBg4fo6BnABwvDFomK0r1vnLSHzsJaqB/o338AeIIpD+EfKJkoTqIgS9w1aElF9jVekockUe4a6ntkKPt5Mz7kJMNKVFvHAOLBeSBRG2tzdiVaTEyGAfPfmTrKxoJX+PacSSDRUSPNh7ILVtcx5xUmJsZwDBd/Pa/VSxB+GhoGhPofxSkyHEP4Ydb08XDQ4GVtX6KrflkEnYK/UmgD7Hr2TFsRGy+uuQd2ZD84GUEA/AB1gvNEuNfNIFEjeBXAr337IUvB26MvrC1HCStUjt+H2MHo7aetD9lndNCJ/v0HGqJE0Ai3UEfXQAkShT1aWFkMZv/iYMHDtjgAzvXWI62gDZB9gtusrNF5E4cNhS6bGMOhAYmmNcYPQ8cCvQkHw+EaPMR0uEmWOJmTqBEacBsBqsbbgsZSG9B3WYNmzt45MYwd+odCA/3+EKnVVwvrDfY+mD1QoChogDF7xsSCBLe9EmcLceXhXy7+DFoCYdAG6BFsEp7/ApoBLYQa0I6GDYU68TsHugamhw1vP7tmZIjeMPeDXLBEv/7pC9gtyE8i0ZwAiIcA6V7AoYBeJFRG4o7jQjgmJqYmb82eBqkndA1cC2vhcwnuGgRwXYO9G7EnFvQ+NB5mamqaWi/5fm+FSDSOHQuFvBM+6MCOQFFhGTVX3J9De0Co/fq8CbZjG2AMCsEp6Za9h0E//Q0MFn3xnYmJqRHbZajqvn8suBBUAYUt3YRTkglYCjaEraCe/v0NoEKobZixyQP/eJtRY6Bw4MCByexlzujcJjA3lBw6e106u30lm8zaw+euG6L31bC4oiZOSPgSLHwgIHs6aNBAeGdI2mOM+ggStbYZBR2UHNNhxnBUl/yyesseSb9wtYmljDF6G6N31uDBg/T1dPX0UL7OSfSWZ9DAgQNQY5CVBk2eNlNfHz6QDfvws2+iWMWevnoPDMq+sjq4X1r9+iSUyPhwoEqJDhyETmFwKFYv+3rlks8k4tHWbUrnj3OCpYzZPxuIYfJQqnpg+2/oU4aWLlMaBBKFRBbWwjnxjPOmspgHULMR+2temCvs65fvP4G9QM2QraIKiwKN2D9UeJNgieKWwAL53c61Sy3MzdqSqCH7snw4b9bc6ZPQ62NkNNl2DJPjK856tu2PnxrSvND8qcrQvOh7egb94e8Okk5xpkSieBf6/fvv3bgcTr64qvqUJxDgcnYv/hgBuXVW8J0Viz/BhpBkonn+I4abwtFb/v2n0HjYRWPa0y8/mqf8TLS5zKVPX/RehHeXuOXipTRYokbsJ0cuEwV/wCZgGnGl6zHnlTY2KNEBlxw8iEZr/zqz7vgBfuGlU2vFlW4jbczxQeYkyg0jf7hw+tyZE9C6oUaTJ44GPTNiT/C0Ifu6ZyVcCvY/aiDR1dD2JQrL3p1LEiLO4HFO+D8p/HRzmauX2x68LwuL4WVZ17Zt/NaIlV9eyl/Io02P7t3dhWb2Ml6QsELeCZEoS2YPC1c5xBsYDHTe8zNUAnmqtg46FLDq4um1wQHHWoSqDIniZYghutIpPeoI5/pX47GN8ducNm3YvXYQ/AUZGX3y9aJNe9fb7VoLYR9+/j4rQiP4q/FLeuoZcf9Xu+XZTAonUai6f//+S1Z+j87LRvB3PWzvn/awYWJ1FAgGAiAtyxIlQVbX32AAvGqQtMG2sPdB+FVgM7yNe9YPZs8DsHmWWMalx38eXcRnVX09/ccR932TvPb9uQtyQahq3gfvYLku+vLDgFSfyW9NggMLb5j19mtA5CBR1PkhQx4Et0j0xy8gWLufNidR1Av0JnzVC1igFxAPxwE+XhiiocgBaPR7n93+E7sTq1DXoBC6BnbEXYNfoWvQa3xg8WGH896qjSuWrf4JsnkFSjS3CU0sAmFgH4DhIFu6+sD/9D/3wEnpNUxSKWM6fIQR69E0dhYP6BB+NmTf2G/P/2Dq9Nn4j2jchEnRec2wdv0OB7x22/6DG+yd12/fH55VB+W4I2AjSPvWbN59+0mI+/MY1IxBg3yicqDmtCqU+YHdoA2kaYAXSUVY6rAVpHc4OYZgcNUIM/MHAfFkT9du3QcthPj+Bvp2O53sdjjGFoqtrEfiSuAI/Lpu29JV679ZshwkCv0y0NePRKPNdUfO3xrK5jyQGfvFFX61+BfcfixRcDw0AHdz75Gz/nGFOEWGN8yHn34NAXFFzZB9wtpxtpOSypjYwuYBBgbwloAPGWQyqmKJwjH/+duPGfaa6NbVaABTV9+A3BYFZD3T00emDHQ71Zjq1VcLnRdO7l8PGzIlL5ESDQ1dzu9vxtcpS4IgXYNDYG1pDgLGEoUSiERr25AopLbcCDDZAIlEjQzDH12AbFic5z/cFL0X+w8YgMQJMfn+EPPe3Ok2VhaW5mbYgrBTfBWTk6iI1XN64A2cFnhcOdCY5oXSIDhxDB0qbvHih/NnGXISzX4+e/okQ/bkC/9+++mC66d2k5pvE8VJlDOiUYvYeHAShVwwJfKs9CYgUcjSxBVu3OVP6YlFsgpd25JouN9R0Lm47oHkJeg/kBE9fv7QAVINOOx3/tkqaU+1O0p/OpLonm0/NJexVyhFnmBB2B0YHRLNAexaXb3+YrEnw36AgC5AibWVGZqZXOFWkXN9y/qvx4y2srSADzkoe4Nt6wpvQXe4yue9M0VUIelO4NMD7FvA8MblTfhqrrjKTU+vvzIlCqfLRV99KJ3ktZJoy8Qi7pqoJKYiQl8XvYjjJozlTdnlJKqjrYvTrLSGeK1+2rA5WA1+/eDThZAaGhj03+68GVQEmvzmp68M0QfiQWAdTqKweRT7Ddgr1i/DKa/0XjDQ7JZgnazWs3tiykJxC2FHuCSpJsqEHfLR6qudzSRLJDp4yKMw9xj2OqVMicKupXsBAagX5WhiEXdNlJtYhLsGC+raPjvprr3M8OUkChkqOc+5+xKFBU8sAm8Zsi1/EpoWyV7YC0ws+WX1xpGjxqDxWNPh6HU3MgpOrYRVnERveQZHZNfFFYpxwIAB/fFwZWhGtRF7TZSbWBSeWYslCj3lClmXNEG+a4jOSwMgAwbhsS9Nv3BZ84RTK5BioeZHQUkmpijZhVfj+KU7IenVsGvtfn2TZakX9vLV4mXoZdKSZNIxBSIsUfAll7xGsrkyJ1HQHvuB2EhPVye1SpI74qZiiUIA/oQEnwlwa2Pym+FnLFGo4f2Pv4Cfwdxb2U8SG3Y6ff0D0jC8srEF/GRUxRKFU97tM3sYdsDTaesq1En9/uiOTGJzJtdv/Bh07MCLTHkIegMNGyYRSWUoO9RpmOJ3DV+hZMqDQT84bwDLyilRbV29diY3Sa6JGhmxk4ZQeyzMRxiyySuSaEHAmJFWaMQP8mP2sigerO7Tr5VEwdO4d+UxHjjzdr/o0JD6RIf9+0dXbdnRXZD0FvYjBZYoHK6GTB80fI0GMfCf7VB0TbSY7U6HKE6iTaV3cbYHOQmkX2SAEiSqrz8AGbQC3WNjYY7+/g0MBkDAtYsb4eWGYxgTdELSHvFjdhCxA4m6XNsmmTTEeA5Fo3ZodASawQ7SojcJU4+ukkKMji76GAchTKMHAJaFSF1dgzf76OBV0NSaglYS/ee8HTf76drFDXhQMObln5LruGJP2ItyJGpuIflgBwllRGEQ51F5JAqp3sABKGn+efWPvFFWTqIG+gYZ7MQiMFa/Pv1g87nvzQH3jBk3GvV5iOHwEcOHj4C8yNTU1AQPuqbUxXAShc3xRB5IfPHYr3S6jAHLarNiMzY2hn5JrwLNDxyIWqjdDw3PQklcRfjUGZOhRFdbN7k25pVEw+9hiX615HM2vpVE4UOGdC8gAHoBCiQlCptIumYoo2sufjc5ierp6PGUj/qiCIniiUVaffvA7g+dvYY18/tGe7AanB7BCv36vgn/GrLvzKDUCk6ioAd0ITOnARI7M3MLQ5TqGXQoUbBdq0FX9hqqERreHwTBgwfDn8Owz7/9idfgKHZ09EFAHLQCEj6oAYLxqA+0c84778FrDfXEyLqpph2JgiBxbo2RlmhqFYMnW8HpMrEExUBntaWuiUIDhqKRBiMIiGSrhb5DACfR0WPHs2/aIcNHoJcWvbqmw9HnlZYKpVGxRKGhYBFY25T29MD231An25IoUPRCS0cPjr7jlpWG6IqjDkpDUXkgekEMDf/cu64pzQuVFASAlqDyqZPGgZDWLPsanexASHl+ogwfqEcbreVLFHQoqVAW/FtcWkv06omdIFj4nFIZ5wF9AedZsmt5EuV6B2GcRCETRXZGZhqGL3OKsp9Psh1tSMzOZSpCoAueN4+CQWGTP5Z9TbZTBoqTKGC/+XupiUVe5MSiuOCTRmhGutGzhw7ooqn4MXuekSFRkQhNxGVaS1SqULZE4RjCKnElurXUwoJ9CViJ5iddHjR4CByW9as/hwDwfWbsBfi82aFEf/npQ4lEGx6yH5OMpk0dC45k31OGfbUkd900l7nqsIOxUyePgQrnzJqAO4Vn5+63/9GY3ZYnUen7ZxLDTrOnDsPDDr/AJtDIuqLbAwYMVIJEjdiJRUnVUTpa6OQCJ/q3F8zF81fblyj2TUp9rGTDYUOT6yRTdbDkOIlys3OzmZS+b0okCn76din89Q2DrK6UycM3pwJZ4qQiJgvvHUsUNsft2bhnXVsShdrwewka8+o+k1LJKh12dAoOO54GldYQ15K26sHu7r24iy97X7l/PrIoGJqKPxbwJWpkJN0LwxaJxklJlLuijLsGi3TXYEPoWkJlBCdRmTf/dF+ig7mJRS3zS6PYjApUh/ql1RfPOfpjyx6wi1FriWLZROU2xBaI2pJoSqUoks1rOYlKJ3+YpFJGRwd9rIE0dMjgwTpa/VIr+Y6JYp+WcP7WY0M2T8D34SSz0kKvJSt4mVtFtStR3GAuUrpfCSUo64WKYSssWmj2gAFoxBtLNK5IjAcCocGhGTWwiWdwCrSNk+g3P66AGqCFRQyT2XI/bno1kyeS0U5Nkiioa+E7M/Bxh6o+XjAXl4P5+rJ/4bp6BpUpT5iK0DkzJg9F9y8O9blxFAR2+fA2dnzICDZPCbyBRxUUK9F/ju+AUyh80o31vsLkPM8Muj2A/Vwsj0Rhp/brfjZmr4muXvolUxYc4nEeN4kbzl37y9co7QZy/Zi6KPhAAE35dclnZDtloFCJorsy2FFNOBTg8qTw0xU5154/chzM3icKYmgouYMPL/xXkvHPovclL5lEopVuny6ahbbtPzDA+2BV3g2kE5mFnZQoZHVabJYMWspJvBwccEzOa6L6BgOyUq9ADQvfm2bIesLt+nYwn4P9j3jz39A0Wq/UuAs4k/O5vw80OWuGLfwMe0S33zR46OpJLnK3I1FGhPJOKITktbr0LiN6PHoU0o/SJAqpHqtD1AYQ1csMX/AWT6Kx7O0c+npoLtikaRODs/2Ds/0SKiNtRlkbsfcEf7P0KxBYemO8b6IXvtmjfYn6JT8dhMachn6x+DNoTEJVZFpjvFvgbfgQBms7JVFg8/4NkIaiS6pWFmkN8dCSqKIg8F9MSaiFpQV+t1x5cAHKdx7caoQGOYcuWDQfRBtR8BJZk31j+iZ5vbvw7aHsX5y8Ei0Le++jeUPZ6VfXva7AYYkqCsZdgxjoWiZ7uRe6BjkxdA2OjxIkiicWSYMkyl7e09XWii9iQCf67DCmkXwSRdNl85rQudJo6NX7fi+TSl8klbYjUQCnkobsMm/hokj2HhuSuMLmoewVa0hVE8uY+CLxjyvWoFcD/f3q43tXSLomUcg7V9lth1+hYYt//g3yzpuPX+B9tVwTrdPR1mIPy1Dnk1f844p410SfRefgNy20FvJayNeTyxkX7zBjYzRXmddIjZJo5rPKeA98LMBAheFu3KpHVw/h4VM4rb/RVwsPmo0dZSW5YSY/QJsdL4XywUOG6Bv0NzU1UaxEm3N88ZAs/ArloHNr9j4BOSUKNbzZT9sIpU1Gffppw2eicaNtDKUkuvCdmf20daHc3Gw4TrLRrfEvbpLtlIFCJYo0WenWty86L0ML4XjijpiYDFuP7xMVPWLzajRgjlfhf7FEIeDpPcksKrzq7j9bQDNkIXi0UxKFysMDjvNm5+LPUu1LdOxoKziw/dCwKpKEnl5/ppm9U0X0GLccCt94U5udbWuoo2sA1oQGP7xjzyZFhqYmKAMdO8bKsCOJispcDu1fBgfKkL2OC3kt+zqieaTKkShOKyFFw3dr6GrrBaT6kBIFAejpSa58w9sMNgdhgCH6sVIZiibZammxb1fp2bkyJRrLzqdd9NVH+IVAz3wwH4GtCTLrgkRR41sW8B+0BNSIZ+cCWn20jNi3Zb8+kgksEIAnCYPeYBe4UzgLGT1ulKHcEo0qDr7odobNb9AyeMjgY1cO4q7h1urp6uOu6aMLSUb4KRbKlyjoQRelhqjveDrryNFjca/lkyg706elm+jV19UJSa9qU6Ls9deBbJIH+3gWlctWy29zFLps2dCv75tD2QUEr6erMxRdnEKeg01/WrE2KocvJ7RVlyQaxfZCq18fQ8nb9c0h6DSF3mbc7Nw7XiG42UNbZufq6aEmYYlG5zUu+vw73FrYxMzMfBCbFMF7SpUSdb/keHjnajAliBA81Jjq5bx91aGdvyc8+5th598GuJ48uON3xy2/kttyiDN8tNnpcLPfmsR3bWGg87ZVM6ZOsLI0W/bdorTAm62eZlDyEjwEYnt87TBTFAj7BY7sWoPmEGU/h5bArp22/ooGe4mdYl66nz5svxq2kkg0+/nxPWvxVhJVF7/89IO3ra3MP33/bZDipcNbYO3ejcuhGQBsLt27+pQncCigBLov2Wn28xf3z9hYWbwzaypT/OLpjaOw1mHLStzN/DDXDb9+/+7saaNsLKdOGrf5t8WS67vyoFCJYsAHBSlXNq//GnIp23HWi7+dX1twi6lrqaHu/k+LF1hbmaHnJIge77f/CX7Yt3MJN04Loj335xr8IIX4kJOicva5BPxClxOHfj20/xcAP2zhpffBw47LHXf/JJFolfvxAysh2Gn3Uu5pDJAUXru48dZfm5nGh+JKV/SHajyUYWcG8WgsueO892fYPC7kJDR4xlvjoS8pUeckd7BgGj3C/I9+99W78KZ6e/aktJhzaEoRuwra4O3hMHvmBMDTfW9EwLFDDsuhqY0lkEO/qjwh9JT0cxhQN5sfzZk1YdRIi/DA4+K6B/t2/njI4Zc7/2whWyiDzksUTuXrdq7etM9uq+NGTkvJtTHr7dfgwsTqqB0H0XRTu13oYQuSrSoizt05BWkffggDvuMTNr/kfvb9TxZAzjdt1tR1O1aDRaCQt3lKXeyabb9t3md34JwDrg1iwHMr7X6xsrEaNWYkpHSX3c/hYKhhw+517BxgyV6uPr4M+4XNZUo0lr1nxivqwbdLv7awshg/adyPq36QnrYD6fXc+bNh1fwP373gclr6UQyQT3/+/aew6p0Fb4NTT10/Bvtdu/13LOCIwiDoBSDdCwiQ7gXkvnuO7YRCCLv/8i4uzGhKgK5NmGyLu7bNaRPUAOXQKnRk2K7xruDGdk+if/7lssHe2W6nk8wEDgov3fGaOn0WcP7moztPQjbuOrDR3jksE41bXn3gv2nXwXXb9mOJghS37jsCtUFJfJGkNsi6zl73QBNq2PLwrFrYCv9M7g7s+N3SX7GG+YrlR9aD4yFbtbC0fue9D4+cv5layXgExqPm7TqwfocD70EHaJOchhN/ucKu12zeje0Iu9jucHxj6wYDrfuFSiDyxxV/WFrZLPt9Q1IZs2bzHqhn7dZ93CYJxcx9/7ite488fJkECbS+nh5oePmaTeHZaKoR1BOSVrVi7eYJk6aOGjNu/gefXLjtGS/r0RDKkyh62k4aepoPV4J/5abC4kcFyXxaEBcPSZsWO0sixRfdnckLQCkd+9x25Dlyhm02pI+++DZTvCNuX7xfZQKq47effTgRf6uWS5jNrdfK2Lx199kYb5x34p+l48Xs45DQKgjIeY57IS89IFGG9QHKsdBTc++hBwyxc1Cl18IqnIThq4bSj+xBhS3P+sFmlVnI2xBsxKtHOgAaUFt4C5wNvzYU3wEv/r7yE0P2bsJXim1NqwZUu0ODyQcPsYJnH+1bxX84cDMk1lXuAHSzrbbxNpFQ9WpfOOzVkG/7dF6iQGRRMHr+jtTjcniF+AdeAH7uDxApVY6TRfxYXTyZVubmkUVB7BN/XpWAVPDQMegZ1SM1O4m3eTR+IlLrxvBA2isJhWZAbeREJ2gbfsKtzIcWcQ+/xR2U7l2HvUAxxZLWSjseda1C0jXpePLIvFrVVYlGsZcY8aVQchUXEJ3XDMAP+KE8XDB+xI/0tuiJPERt3C5wObmVZFt02bUOS5Qd6uRbkAAF4Afz4mmxXPNk3loa1dKSsI4bLKOFUAiZawQrxTCp7gDBqRUJ7BShkLTKiKy6xct+g7x4yODBnsGpnIbxyDB8KInJRw3G9ZAoT6LdpCHV67//9/+vpY0mTL7ZV4s0KKVNekai6gboqib/5tBhQ7V19Pv01WFHX9FMpZfPDpPBmkqXJEpRQ7ojUTUB7PJ//t//0dFGQ+j9+r6JnyyvKQSllBux04P79XlTTxfdDzl06NDrHgHhWfzR2g7RMIm+0UdrxAjTisTHZAClTXqNRBtL75qaGuvqGrzRR1tXz8DG2hyyZHwhViBQiQoFwUi0X583+hvoB6WUypGGqhGQzk6eOn3w4EGgf22tvpbWNievuJLXO+VBYyTKyBr/pMhF75AoBg8y4wFS2UOpGg2VqFAQgESj8HBuZq0Cv4VNqeQ0SAaBs17dI9QFNEmilC7SmyQqcKhEhYIwJEqJohLtFVCJCgYqUaFAJSoYqER7AVSigoFKVChQiQoGKtFeAJWoYKASFQpUooKBSrQXQCUqGKhEhQKVqGCgEu0FUIkKBipRoUAlKhg0TaIZT9Ees301G+hFlhJv1NFYiYrL7zBV91WFuOIuU6lmN8kIRaJRJeghPvHlET0Erl+dUaxEw7MbgJj8JoqigKMaId99L5oiUR8m/6U407vqzq/5uywK9o7UZGyqXFaLku4xxWFKUqnmSdSVqfUUVbgUh36f+Pf/JF1VDUUvFjUXXWEanhHNUx0aLtGYMvRMvvSaBAfvrb+7/PDh+Zk9wScX5xzy3ZVQEQmQbVATFCXRyNzG9HJmv2vKzpuJM7Z4T6cogplbfX44Hno1oCC1VBzd0UugCRLN8RWleORvN0HsssjfOSJ/p5lmA73YMTx306CSUwvgwwHT04+P0CyJVt1vLrkaf+k1IPHvfyf89bqqSLzy74TLr8Wdey3zwUiQulpkpZos0ejSkJAC/08uzp122GrBmanvnZ4y/9TkHgLqn3V8DPybXBXb1oPsVUv3JRqZ05hYJPrmSLDVqoeTNnhN3uA1cf0TiqKYZOc1Yf0Ti5Uec7Y/Sy1j2slK1VuiGU+Z3IC87aase0YIE3uzgt2WPetRTZFoxd3sx+PAnazDXlMzXk/8+3+r3qMaK9HEiqhZx0eD3uadmqRMQNWz/xx7O/YvdVNpNyWaU8VM2fgUn+gpPQ18QBn5+6OkYvQYehK1lmj9ixN5Wwz51hEe9mal5xbxv9lNgWiCRMUVd6qTt6Hkj28vteHK69mPRjNVMr6aVHlopkQzahPBoKThlMb805PB4pAKk21TFd2RaExek+kv9yfa8c/1lB5l9JrHabIesq+uEs142hB6Id/enO8b4ZK7cQAa2iUPRfdRe4mKK+7GX/wXWIrvLfUj9txr4grVPdFe0yQaVRL8IPn2u6cmkmJTMgvPTPvDfSnZQlXRZYkmF4ssfvUgT/EUJWC7zjOZyEfVVaIFL/M2DSJNI2jM8rYZM5ntfadpF1F7iTK1TxKv/Is0llryem36fnbiLtELJaBpEk2tjpt+dCSpNFWRWh1PNlIldE2i4TkNY/54PJE4uVOUxk8nwyI1QKLZvvm7rdq9Dio9T4dc20nwlKUdw/nlyme3JVMUyj8a3UfNJVp1P/Gf/yJcRfJ64t//mfj3f3T5imn8ZUTCZX55Z4k5+xpT78PvhXLQKInGlIUuPPtWO9dBebOByAAuRmYhr1xmIY+Dz+3V5O6Xrkk0vYyZsrGD66CTN3hNaZlnJF0+iSuXGgfmzaYhayORGTZurSdAlncHOetsPwyvtV3HL+8y49d6vkyrk/aoOkq0yu2Pllm4Mii99J24vhojqiltSPErOf95vn1XbbrdRFRfBf0ou/pzvn2bOy3YN6Zg/5h2WqUoCvaNRjeSEsekW6i3RIuDPu3gUuiVf+X4fCRqrMDNbKxMTr8/prMqBQHjzWvyn3Z2W4LXk679f+heUqIvPY5GSRTSvgVnppImw8w4NqqmsUZCQ3VOeeaau0vfOWkrHfPR+Vk1DVU1jdXLb37z3ukpvA0r6spnHR/TUjiyGkWi8jl/jiN3h3nn5ITg/Odgd7K1SqYLEo3Jb5q51Yc8rXNY//bQJ6aQ2zajsGbpiRAon2jnteTYq93VN4qgfJIdmoBaXd+EKa9uTMmvOuyeOPYPT5maxMzc6g3Bay9GSBeOWOGBaybjuwyYHtdptrK9sev2w0Cf1XVNsHbNhXBybZexXOWRUiJWY4lmeudBXkjYhaP0rx8YRswC/4gw+duMW4e1laQShdtNcD/Kr6+QkmjrzbebiBvrIKbs7x+Jy7Rt7YhbK2ekhLwtRoo/pGosUXGFS/zl/yAs9Qrwa9bj6Yy4Gb3QkkUkFtXHX3yltBb420qtbZGouLkmz7Pt+LbK+cRdeE1crYLDpUESjS4NcYn7h9QYB7hQzIjF+A+ZYZpFzSKxODD9ORcw//SUZymeOCa7POPdk5ILq9yGwKcX3553ajL4ddnNr7jCdiQKkb+5/KAOM3W7ING4/KaRvz8iz+kYSDQZdBhfnc8bmkR/PkiG8t/PhYtbn+ahHLJSkGjLmRQtYrEYb45GjNuYtXTDPwuq4jUDJIo3xL+SDu4wzZVei3+GBojYRsu0o3QYw/aaDJvIShR3bf2lSLIGkg7byYVdCyxQY4nmv2g/rWQlipZcO73c9TqMCD5oiOtjHki2sjeHZK6pIEFcV1ntdzpvc8uFVXvzchc7UVVhbdiNXDvdKp+jQP4uy/wdplVPD1U/P1F8/B2Iyds2rOz6iuaKfFFtWW347ZILX8C2Vd5HxE0NsMe6SNcqn2Nl11ei65ebB1W4bhBVlzRX5sOO8neyo8E7TCs9naq8jxYfe6f00tfQhuJTH+RtHgw1NBenwd7rE72LDs0gO/UKe/PSsx8q+CEMaixRphYrjW8pCVf+nR/wrVjcBAZNv2cDvyZe+Y+4i6+l37Nk7yL9z8KQ3xsqE0WN5Q0V8WmuI7iq4i+/luY6vDrbXdRQWlvwLPHv/+eVRPO98vy+aq7NK086HXee29G/ILuFJLW5vrgy7QoE81vSmsQr/8p6aK2CO140R6IpVbFvn2iVVvIAFzLsB6LJh8whQfz5+hdYqPNPS8Zj556wxd2pb0IfYT+/9C4eqsUbsgs6y8Kvbx21bilBSzsSBSB5jS+PIBusZDor0cjcxsXHQ9q5p8Vq1UO8CcRM2YgEabnq4eQNXrgchDR6zWMsTsg1oXwCeyskw0p07+04+BXUeD8kD38SWbTfn9wF9rRfXBFPsZxEx6/1DEgoTiuo/vLAC9xU23Wef3lnJOZUVdQ2xWRWbLoShcuhhWcepwLmKz0ehOYVVtSPWv0YMumb/lmVtU17b8WB/9qSKNTwsWMAhL1MKsGaxBIdv85Tus6quqaRqx+dfJhywSvtU8eApSeCT7NrcSXwQQEHT9/iPYHt+1/e6VAnNH7b1ejJbR9nzNi1ntydo+on0eKw9kdNX0l08+D87caiugp4G1QHnENGtDevfLjnVduQXxl2KzOUccKv6FWBc3I9AL8W7B2FhnOrixlRY9nfP8F+G5KeM6LmVzWIRaBAnIai35ob4OfasFuwL/y7JEzUVBdzH+0I19bcWBf7EK8tufgVDpBEMkxTbky711/NCvaP6UUSbfBtZywX0k1xcz0c6MaqlIS/pGYesbOQsp/OR36VWkqi7Nm1r9cWBTDsK41KxSKITPznv/DPtYV+7OhFs1jU0FxfhG5LvfJ68g09dDJhXzKxqBH+hVyTbI8UrydfU8Vto5oj0cy65LeOWJMO4+AkOvPYqIVnpi06Pxvnke+dlowAXw29IBI3pxQn3o+50yxuDsoMwH7lJCpiBye+/+cjO/cVkEWd8j+Iy9uX6NsnbaNLVH+vS2clGp3XNGubTzt5EhiIYY34y6lQUIsVa1CuHJaAhJKZW32gnKuEk+j+O/E4eOTvj5vgL0MsziisIXcxavUjiP/YwX9SGxLFC8565+96PoGVKHYhw6oOfn5/rx/sd8YWb9gRwMajcnB8kwiV4LCQlFKxLImCyH8+EYJrg38hDP8MYdBr6TrhX+hsaVVDY7MYcnGQNKyC7Nzi14eoHrsnsLtG9lcQKgTjDWERicTLToZMYg9IW5j/6hGeraYS9RGnPmp/2JOTKLeI6quwlkovf4dfwLwN+lBJQ1oAnBGrHjvkbTVCcWIRZJyQLBYdnok3lEi0thzWlf2ztGC3NfuOEueu04JNIDJv21BIMeFXcR26blp67tPcDQZ5W4aUsDsCE6P0d7sp2pGoGXYkqQ3aIGrKXaeNNt86FO8rb7sxpLlQZ/u9y0f3ugxkH65LHpyuor4SdRWVXmsnE409K3n75fl/AzkoP+DKv0F1kE3Gnnst8shrYnZMAlyL1It0KM599hE4EmJS7xpCMsp1FAJiTr2GFQtyhV/Z152JOY3qzPKcifRbk9P+FCT2Xhelz9HVHImGFQZAfkk6jEMqoZQs1Q3V3M0w752ewrCafPfkxOnHbJrZj7a8DT++MEd68833f8c/tC/RBWemHvbbTTZYyXRWoullTPt3tky088ovqxOjBWmAMxmUL9zjy7Buw+ByMBkpUUhVz3mm4V3jEg6wDugTagYb8XaNJQqrRqx4YLsOnW1gL9AYNDpqh26vtP7tEaTFNr8jB8MCP4BE8c9/XAgf+8djq9+QybAXoW3w83W/LBzAk+iYNY/ZXoghbPzaJxAG++UkKl0nREJmXFGDDLf6fDhI8XZgNkSeepQC3cwrRccKfoVuBsQXww/uwbnQ4OHLH+CjNIPNUNsCasbP1xWARFHjIfnDlyrrIu7iPFJcX4WAdFMsbsyNyd3YH0fjMO5XnkQhExU3VHOZaH3Mg4K9I9Em203E9dVQUnZlCfrV3hztCLZpbpTaUXMjSjFNsUQr7+9EmTE0eJcFWxk+yOLGnMgOHx9BJfpKVC0SLQxeRUo0/sJr1bmSP0tugfJ0d0t8wOPOcckrmtmLVkP6WR4Dv4J6cUzS9TfT77HjCvBGaqwQNZazM5jQZ6lXg72yoBJtny5ItLy2dObxUXjtW0etcaI549jIuSfGMUiozS5R16U3nHbEUiQZDRJX1ldsfbAal3co0UO+u8gGKxmFS3QC+zSA386FYU22pH/IhWgId61nflm9dDnURkoUSm4HZOMAXioGOvSLKz7/JI0n1wlSmahty5Av7KWmvhkbFHQl2WXLAskflihsZc7mhRAJpsdts2Bz5akbn+LklidR/IFAJEJhE9gwXA8nUa7OCew1UU6iE1BaLBE8fA5AlYjFu2/Gws8idk+1Dc3VdU2AiM2Mt12N4XVTGoFINHvVf1c+2oeG5kTN7AVRs/oYj1YSRVQ35cXlbjTAm2CJ5rUlUXsLSEAbMtFYAVrYqthckydRdkfSEgXqqpryYjmJ4tpwgwsdbdEYL17Y80LepoFkvzioRDlQTilqQB8+qpKJ4dx/QboPGaOoobQ4amdR2DYsRagt02M8/jnu/KuaeROLpCXKxqOFNSgGbFoJmiSbxEEl2j5yShRMab1/4Mzjo9mf0eDtPPZmlSVXP8F9qW2sAbiuLTg9lZPoOydt93puRmc8RvzbnR+2yJ2JHnxuTzZYyfSERCewDhu5+hHgeDcef3QHc+DLkOPXeZqv9IByfMbHt7swrSUKOSIezk0nhnMtf0XDwjJvsJGeWCQtUajTLSgXq/GKT8Z5rzR2z68kCmsgSZ3ASvQTR38ciQecYVuZ10QhDNdvxUoUd0FaolydEwiJQnpaxU7WhSQVVw6VwLHCaTs0GEu0ur6pqrZpz010nbgt1Fmiz5iiUHmviW7sD5F10ffwpazcTQOLDs9gByxEeRsMwHx5mwfn7xhedHwebNVUmomGAJoaChxtQav48xhforssSy9+DYqFrfK2G6N9iJorH+wENTaXZUO1dZCb7h8HYZIdgQ63DME7KrnwJdpRy3CutESLDs9k6zRF06Ca0fW2gj02ZL9aMCvYa9OLronWP2/nmijKIK/8L9Q2sbi5Li/uAlJXuvtIkFz8JfTOhFc07hy69TP9Ph6KZ+BnpDc0VCuqzvWAn+Muvpb1ZFbi37geGRKFGvABSHMxRveSXkQjwMURW1ppm8/rSVf/m14TbYeM2iQ5r4lOO2KFf8WXwyAHhXwUn9camuvxXSu1jbWS4KNWM1skOufPsUBJTXF6SfK7JyfIKVFQe3hhINlgJdNZicIp+63N3u1cEx25+nFEWvnnzoGWqx6CpX44FoSHdiEXhHoOuSXCD2YrPFA5KyHwpUR4DHPQLfHtHc+Wsdca8YIVJY3d5UgoBxOTu25LopDkofMxw8BOYdW9kFysLlKiE9iJUc3sKLTj3QTzXz1SC1DewhAS5eZPQRjUA2EidlRWHomi5tk9waqG7NPJJQGl6Ru8rj7PgLKSqoaxf3hCyg4H8Mzj1NHEqLU0Fmp8TfQZVCiZ6doG3C0uSKLonhBD1AyRqOzaL3k7TBrzYvEsHnGD5NNr0Z/z2SFZY3ZikYg98dbjLLNFomWwPdLebitJIttYi2LYkywS3i6LSo/d7GwUlEeCL6GFqGr2V8mORM1oR7g2MVsblqi9GW4GW6FkQU4l+iUB9nVrBf+YdBN1lmjVg3i+n1rB3uIyQ8YtLpfxOxMVQtbI/ozeFehC5pV/oV/EjdzMr2yvd9iJRfAH3VST97hFoujNABKF+PyAxfgSKaqK3ao86VRC23aHVhX6v8fvixLQHIkmVETOb7mzUyb4ThUQJ5bo/NOTGfYV2vlwPTfJaPpRm7dP2AKTD5mza0XLb34z6/gYvBYMiqWIU16QaEt5exKddtgKBE82WMl0VqJwyt58NY4cSuUAYzU2c38jaIGcMjK9HA9XSq+CYwTlE9jBW/Q386q8zVtcQN55ZWhUVmYDQKJoDLRFomL0J8pU1zdD/d7RkvtWIQWsa0BTd8QtEkVhUsLDY8vc0sDWKCYkCmHXfDObWrqDw5paJMqrE0rKaxpFUhKFTxKoDWzN1r9JPihYsXOvoCI4SnWN6M8ffuAqIZnIyph73oL6STTLh81E2x7R3WVRsJ999AHnWlyybwz62d48b9PA8jtrq7yPsCZ7dVsn5IsF+0aDdOEH1HKxmJ031OpBCrC26OicKk/HKq8DhQen5W1tuX5pbwapZOtHLsDezVDkEyfYETdCK+OxDDuGl5z7tPLh7qrHDsVnPmr/IwIayy0MJo5J91BniVa6shc72xzRxYDzUm7pFYVtKAz5HXTYMnX2dVQYvjHNZRg4Nena/wEkm1z5N2yS5TmjOGJzjs9C9pthJAFJV/8Hx7TEt9wVc+G17Cezi8M35fl9kXTtDbxJW8See52p8yb60vNojkRjykJf5Hq3//ygj8/PBl9KTSaauogt+ej8LFj1wbkZ0sF4Bu8nF+ZCPKwFeLUtODNVZjkvZt/TTerw0KLOShRILRW3P6ILcpq73eeAWyIkUjuvx6KvSGMHckeufgQ62fJ39AmPFCiftunV17/M2uqDAauBIM1XeshMdm3XPQEl77oRS67Ca2du9Z7V8iAIXCGUTGCd99Ofwacfpa46GwY/41W2UmH4ZwykuR/v94fg6Zu9IRjXST5saKKdFxgOwtZciMB1QiQOI+vElUi7H8dM3fhUus5Rqx+9vfPZyYcph9wTIW/GM3jbZN0T36Rq7nVRQ4k+awg6QzzTgAf54ILWJeAw9o4XrjBvy5BqvzMgyJJznzFNDWh4sKowX/JUh9bbgi9hW7Q5KXJiv5JI6dYSMTuR2mVFyqDk9EIm05s8Jt1CrSXqVpu6C9+y0hEyH/uHCls2Jx6VcOXf7FouocQBXIzs+A6ljm4S9TAXVyh9LLdSkyQayz6xiHvMkEzIp/RxJeSqDte2U84x69jolKo4sqnKpwsSjchp/O5oMP+E3hrIIEEYUzai6528VaiceBwgfrwAB1khBtJZEDPpM1490j9zv4Ln8P2pMsP49dihGcK4XGYAB6qT7WP7dbZVQtaMd40GeDu6SRQ+lCSr9ROLstBDi8ouftbOQ/i6ACSdrwZUxaKaALX8ihh7Myb/Bf9odB/1lihT4ZrjOZZ0lRrzX+x3dBMdUQIaJVFgnfvPC1ru+1Q54Nf7iTfV5AvRuiBRIKlY1NazhCjKYfTqRwmFrb7IRS0lCuQGyEoEu0Xe1qG5GwxyN+ijm0zanbukGuzNS89/zD8OCkHNJQrUPEr4q80LkGoFpKEileSgGE2TaFJl9PzTHWSHSmPOn+PU4YF/mK5JFPjxRGiHqRKlh4D89R//fO5ZReot0SwfcaaP5FbL3gB64qAxfHQgjoMiUH+JVrpmPxrV7jRd9eDK6/GX/qWCO1s4NE2iMWWh4K32p+kqh3dPTrwTd4VsoaroskQTCpvH/NHexFFKz2H5qwfve9DUWaIsOX4dPppAABTssqgP/JPJ8OJ3X1FogERBDy7i6gft3lWiYhL//nd18lZxxR1+y5WJpkkUE1ceMevY6Pfa/kaXngZyUHWYkStNlyXKnrUbJm9EFxrJszylh5i8wWvpybCYPMm9oZoj0SwfpjAkx85AHUdfFQR6PL3bWsVPJpJGIySKcK1J3x9zBt1AQjpMtcSef6046EtGhTkoRjMlCqTXJCy/9ZXyr4/imU3qM4rL0R2JAvGFzXvuJNNxXeUwfp3nV4eCeKO4miJRloynTGFo6dmPcjcNQs/IRTNvNZwdprkbBhQ62qIEtEf1idEYiSLQYGm9T9bDkXHn0JexQP6XiL68RQXA3mPPvpZ8483q5B2QKJNNVQEaK1FMRk3iyZfOIDb8vWYLzkztCaD+d05OePuE7b6nm1Oq4tRkJhGPbkoUk1Qs+ieg4O2dz8ev9YQT/WR2cilFIUxgv9oFPqYcuJfGPZxIJpogUY7iMFHyg6o7v0Hqpsn8IUq+zxSFMtnPlWHQLA2T6CsanosqXIoCPysOUg3NxVeYem+myl1dDFqp8RIFokqCEyoigwt878b9fch3V09wNGBfWFGg2uoToxCJRqH7Xhqi85qCMuoCUmr23EnaTVEEe+8mXw0sAHfG5jdxTyZqC42SKMIHJaaajmKf6tchGipRFnH5XchNVYIKnurXIZovUUxMWSgYDoTaE0SjZymo3fgtD0VJFBPJAqd7iqJoa/CWROMkSuk8mixRSiuEIlGKYiVKUSFUor0AKlHBQCUqFKhEBQOVaC+ASlQwUIkKBSpRwUAl2gugEhUMVKJCgUpUMFCJ9gKoRAUDlahQoBIVDFSivQAqUcFAJSoUqEQFA5VoL4BKVDBQiQoFKlHBQCXaC6ASFQxUokKBSlQwUIn2AqhEBQOVqFCgEhUMVKK9ACpRwUAlKhSoRAUDlWgvgEpUMFCJCgUqUcFAJdoLoBIVDFSiQoFKVDBQifYCqEQFA5WoUKASFQxUor0AKlHBQCUqFKhEBQOVaC+ASlQwUIkKBSpRwUAl2gugEhUMVKJCgUpUMAhKomKiREMRZyr0W7tVJ1FxBb+ECOjcF193Np5HW5u3Va529EKJlhIlZWExpYr5zm2oR1FVdRZNlWhOA4Ioj5RV2DUUWJVyUKlEc30x4AyFaKMu2ZMslElT2lOyUDk0p3tzP0MzpH/lqIp/SBZ2nZ6WaLU7U3MP01zmIr2qtvAWP1iKptK71Xk3yXJeJR3Gy09V7g2yEKqt6l61ykOlEk2ojEiojJSGjOk+UUXB0r+G5b0gY0Ky/XlhXSC+MgIqD8nxJ1cpATWRaGyBKCa/mVdChnEEp1UGp1aQ5S+Ty8Kz6sjyzhKeWQtVkeXqjOokWhg4YoTZqJE2o0fZrFjyRUXcQ3GGDJ3ICeSgokyf7z5/n1xFAsJ23LqKLFcCsOtbZ/bgn0Gft87s9b3zp4jouP6AQaIMBXyqkNCTEhWVu27Z8J2t7ehRo6wn2I65fGY90/RQsrba/dOP5zBV7uRWDGvKW1e2mJiYisr5yoRymSlsW/HyUu2ubzAEGswrd7+5c9gwk+YuV6tMVCfR5NqYsePG2oy0GTlKgs1I6+iSEDKym9jtWhuLs8NSJNTPvvuUFwA7HTFixKnrx8ht5Se+ImLhogUWlhYjRgwn1yoBdZBoZHb9eNuJP61cy5WEZVSbW1jE5Lfp0Y+/+G7e/2Xvv8Oayr43bvj543nf9/edqjM2ShKSkFCkF+uoY+91dOxjHcvYHWfUsfcCKvbeey9gQcQCKtJ7RzqiNGmCtJz33meHwyEBRx1RjPG6r1wn+6y99j4R+GTttgb8EpZexi8MTimWSsRHLrqp27+T4GfboXNGRkbBqa/V79ZbfUqICg0kTI4PCUazvGVGRhuWzKS3CFQynjD5AUz646oIFWYv/Uhh2sNqftI8mTxYPgJEJ4z6hS1RMWDj3epVdPVFyjiYK4TzvICa0ZXqWc2y8pr0Db8J6FKuP7FhC5WdJ116rOonhTQ9+td+tGlA9NLBDY+u7KlAMAonL7yqHrYopKqJF14qTbyz6hiiC/4cZWFuTmD56saMqUOEImkFF0oy7vSCjJeW3FK+Rcxa4AKIXjq1DH8NiTHKS24px1RfuYwe0YspZEPbgmptUXtFHmvP3OGPwRKyMncY5i6fkcSAWN4lTSv786DK4eub5FaZ6/WLq42NTShESZWiG6RWmWsNtC4iPa96Sx75uvKaPN1dRuFW1SsaoHPG/Ov31ieFqKWVZXxxhEokqhKPIryjF0Dd0+KIFEVcTGEoN2RKjHMCYwpC0pinwBi/YmRuEITqAj1hdF4QLCNfBgGiIyeMgKtUJi6hNIpjdjqTgP7QWoiP4TOlIhYl/LFZvEWtShvVDwSto6HIvCBlN3JI32Af/zqSsyF9yA3CU6QyT1Wq/3fVE4haWlqNmzyTKwFEgUMlRNNKEJUmFjKxLxmOasNGT+g36FcK0ZC0koQCJqGQAfzkMsOjl+5QG9gnvmJQMTJDodpoWklMDrnF+lSNXOFn++Hz+B3HBdxGZzHc0G44Lz5G61y4jI7F5ZLmcMFnP96Shl6hD4xKKx9cnxqimU/I9bNHLexs2v/UmlLE49JuI2OTr7770d7W5tVTd2KQ9rBt65aNmup99X2jrp3aMy8q+ZTl3bPrzw0bNbOytARHAVGQ6cyeNW5nttJhUiCtbesWwHNVtJf+yMTYhAbBNtbW6AZujR0+sImO/jcNGi+e8zvz3EulqzvW/t2xfVsl4VI95UbGZAg66UFa4DVdPeH/vv3xh8Y6N09sRosAOe08XKHzeK5qrtimzc3N2PjbBpQFRP1vHRozbMA33zcyNzcvqhxkxlcK4Jw2YWFhwW9CpW9vpY8CUUqvzIRThjIjJTAKXcaO7gvSKHKvZaedwwN++32zEUN7wtjztiOFKOg1ZlQflONjKcq5AgLNmTHMytICca2drVWY924+FKn9wH6dv/2+qZ6+uDT3GiVWRZ6zh6tjo8b633zbdO2KSYSC+YSRM6f9+s13Tb/+tqlcZsxU3EZ/ZHJjpcOiG5YWFl9/20RfIL57fQMH0dz0C61a2aE/MrmRl/sW/pMq8p0HDegy7rd+XMmSBWN/bt+K9KHc1ax586++Id6yU8/hefF0OzbP6tihNe0h3pIfG7VP7531qSEaWxjKL0wqizYzM0ssjeJsWrVpFV9COHTy5hFjY+MfvvvR1s42+IVPBAszI7kRbPAj/dX/5+thY37l/IRnB8yYP+1u6K3x08bid9OGjXevPb4QnOELiG4+uLHhtz/IDOWnXY9FsHi2sbM5eGlPaJb/njPbYTl45C8/NiC/QSGZvpSjIDd+olBr4K/90RMbWxt+0JxYFo0S/LG2tbVp2bolbkXlBrX5qU2Dbxqih6AmtYHDq48uiASir/9/36og/7+r/kMUrGrTtl2jH743kssPnrtJDTiIAm/+ifkCfd1GDb8bMHi4oVRCIRqVxeC64XdfNWr4/YAhI1Ri1icx2TJD6Q/ffyOTGTodOB36rNr0J4UofmwGDx/9Y8Pv8PkHJuELV0lEhqJdh45P8wgOYbP7xFVbO3vK9f2nrxtKpQ2/+3r99kO/jhoXls4OTaeVHL96j/z4ff8NLN88QP3f9akhSiPRTG/8iXFa9SdAVRTnPqhPd8C1jMRngcSGIjPLG7QrS7iXE3YDcSSuyxMfCESS68c3lyfch02/np2Vw7mZ3qQWIktcv/QVSwyV15x4kSiw5LRy7rHty8vhPPHezN9HyuRyFVZtXjG3hb0tB9HKuo+a6gpATdTCK/OcdLJn146088RDfiBgWcX7yqarRaIH1uMPCpPrVxp/N/zeCX2hAW1aR19IYmK2CXxQ/CbeRx8FojQsmz55CECinNQsdBk6hAznJoQdMhAbMqWuZSTovGduZnb/5kYK0ebNmyOCRHm4zx59gYRUfGMkit8reCB+Sm7BJ5nLLHTp2b3DoP5dEDii+uqlEwFg9GrK74MmTRiIEuKzzJUBzApddHQNCESLboCUFYUuZTlXcFdkYGhkZEwgqnCTy40Z5j6ponBr3cqOKb9d7XlLbuHpSDxK3roIBOLXWZeZCjf8HKIW6VWhi1Qq97jpAA+b109rYW/DQVRXz0Dlo3sffVKIWlharN2+cvXW5dCabSv2nt0BjO2/sBuQC8vyhwA5sUgcmukf9Ny7V7+eoFFolh/COwORJPZVGCBqbGQ8Ydq4yNxgoO5pUXjbdm2iC0hX8VYkNCBxoVokCocpilj4SSqPMRAagOJgnomJyb5zO9H6zhNO+BFKLo+BgcuTyyKBAeCHtqysrZ4Wh6MQIa+h1BDtqow8R+YGkobILG/wo7h7hhLDwHRv2CN0loilaB3NoSJAi0I8mvoH8h9VTyBqYWHZvVe/lY67qJZv2C4zNAREIzIqpFKxX0JeUEoRAkdzC4uIFwScHEQ9QtMkYoPITAUMkosZ/GICoogv8V8Tn8+gEIEm3qq0SMiXXhaUXIRb7dr/PG3uP9XuAqKHzuM/NL4AHoqvPQg2EArATkDUvkVLuKU2O45cJNFqajFiUFwkFRHjqMwKwBsQRSc7d+vRs+9ARKIoT3rF4BtZVJZaTPzh9IkhCsxABhLpvGljmRdeIMeyeZNLEH3m+ZMxzILAgb27AYrEno1ZX8W6FaY/1tETIqpjMrz0BCIKSBAuxefS+BGDGHauEeC8c3Y7QBvjcXrpn5NUJh1hTECo7IYX4h4m24e+BblFAHD1AeGaIZr5RCiWZEbcJAOtaWSgFZ3HLX7nCQJp53lNjxrSl16zw7nrL+xfB0aSkmcPdeCZHbNVQpRtYvPyOVwT76k6huh8QNTCHOiytbGys7NOjT2uvEshmu88d8awtm1a0PAUOAGHOIiKJTLCnnwy2gnCERIXOI8a3qvGOVHYC4WS8hxiX5F3zdrKcv3KyeAc+FQCmDF36YBq02bCspyrf80egSCJeX0L8FYOsXIQLXPV0zdQ0IA133n10gn4VUSV+NCDCB/psDBeb1xcFeW/r9ocaoFL394dQV9yXX7bxsYKWI3036evL1aOBuc79+vTsVf3DsDzlwBRlCMMtbS0xF3Q6Kf2bUaMGwZczVowHdEn4AeCAmO9+vYAUAFRiYEk8Ll3OLvgFm+F+kJEeGHZAX/8OUU5w8qyjT8n2r13N1jibfzrCPx5BdtUIAr+gXMR7OirQE+AKnGvwoT6IjqwjFv/rJmP/18ViOItaYi9njp3srWNdcwrEmTD3lAq23zQAQ3JZfKNe9bya31A1W+IlsfmMNbWNpEse4CirQfPbdpzHGikEAUIp86eD7DR4VaAzUAkAESjsxmz5mbnXb1AvhrHUUPSSp/mMwGJBU9ispau22pv34K/FpdCFCyka5QQQQr0dEHcGiEamFx06Y7fsvXb0CtqbGffAhBFXaG+XkBSAdgPgiYXMXo6TQFU9c58KH1iiNJI1OvaPonUMC/aFQjp06Pz7g0L9mxcuJfV7g3ziXG2j1Qmv3hoQ0awc+Hzx7pg5wsv4BMBBOWfgjDp3oSR7JxoikfY3eNCkUSR5W0ok6uGoSoQfeknNZRV2WT5IBwkznn2NUOUGHuPH/ULfp/hIeHJefQB8OZ3HrG1etPVIcrOiVLGv/ACOykslRBlm4AfrgkSj1Z3+FaqY4hWRaLFNywtLbp3bcdBi0L0lwFdRgztScNK4EQilXMQJXOidOrx9U0C0cJ/gaiJidIeBr16dBgzqk9J9mWx2HC30+y92+ZQOW2czhpcS40+1raNvUAo6dr5JzIDWglREE5PX8y5vXp2hbGJCfycO7ZkzvShu7cqXe3ZOudpyCHVhUhlrh07tEYwOnRw96KMiwq2V1JDuTL4zndeunAcvkyUZmsgRNWHcyMIdfzFBuJTrsfcQ24iEEwoiQTzuvXqunLLstVOBLcQriNYaoJb3KQp9PvMCe06/BTBhqGB6U9IoRpER04YQY2BYQsLi+SKWBWIcoBEAAqIAt4AoUgggisUIojcdXIr7GuFaE5gz349evXvSVGNmBhAnblgWlJZtFRiSAeQ60L1BKK1DOeWA129+g7k5j5veUVNn7cYcaQSos9Ke/YZMGjoSFoLYJMZSulwbmQmM+3Pf6ysrMQGosVrNldjZGrx2q0H+g8efu1BCCAK/llZ24SkVa0hqpoTZYdqo7IYQDQgsbBmiCa9wsW+0y50bhVd7dVvECCKCzzCCocd3DeDRas3c03UhT41RNn4UvHsUYd2bextbRAILpg5PuLeiZL4u4jPqICTUPdjx7cvf/3UnS60IaNn4FwtkShRji+o/CLoqkAkVl8r9IZIFGAjvaoeie5aPx/hshKiaQ/hs9o6o2yfRO+LiIqYZ49wq1rn1TbSsBDtx7X17xClW2K4Jt5vRPejQJTCJjf1rExmpChmXSmHc51XL5tobW2peE0KgUChSPomiOa/CaI1RKKlrsBkhO8eoJETtWdXCV1nGHe53Dgt6qhKJKqcOiWR6EQ2Er2CmHL+3FElmZc4P/y1S0oVwImIKXcXCCR0vRKiVT0BPxLtBLqX5lzZ5TTb1taaeshPO49OUg/ogCqY3171D6LQ6Ikj2rZr02dgb7ATKAKfps6Z5OJ9OTjDBxSkiqgJooRkuoLpf/9hZUViWVr43yGaWBaNSDS2MIw2MXnWRJM3RqJ//EkjUWIPAMuksi1sJPolQ1QZiWYqI9FtbxeJUidAYHQWE/OSERsIn7Lko0I4iP/BxFcM2oXNhD/mWFlbvxVEX1S0bN2GDg6jDyscdpqZmQHz7v4J0+ctomFrdLbC3NwcEEVdA5Hw2oPggKRC2ECIWbkm6kL1AqIIsHLCbyBqVKQ/Loi53aalPZPnX550n3Ar2wevUfdPblo+m+6q3LRijrmZGZDDzomKyXIbMifq1a9nF26LC8wcls5q16bV4P49VNtNIbgi9M30rpwT/fPkzpXsnOj92ZNHyeRGKnOiQbePoKuAIinP8jE0lJOFRejbS99yMjV7nykMsrO1ZtIfd+3UjnYexpT36k136tCWa/rNEKVNMJSjtIl6D1FF0Y0O7VqlRR8jbyvnREteXjUQG0YH7CMjuhVulhYWb4Aou7ZoOAns2KiU31Ztc6IINNu0tkfFshy2FktrclF0AyUwRtyZyoeo6pyolJsTxTcAhrmj5Bz8qLEc8G7ZwrZ9u5ZoXRl9VrgJhFJlrwpcJFKZxy0HVA96vBNfF2gTv48fSH5s2I8r1Hu3xy3H9+Top4ao+upcyDvREyxE8HfT9yplVUCaV4tWLehcJmK7BHblkTpEYwpD7VvYwS1LRALasBx/ob4QdIzKC+ZW51Ljt4coGurep9tNv6vRBSGJpVEIc43U5kT5EGXnRKXBz0kIiz5LxBI6J/oFQ1Q5JxqQmE/nRC0sa5kTzSBzoimVc6Kh7NJcuEVhdDYjFOjR1UBUKLG0sEx5TWZMk14x4C7+Q98Gomh33JSZaBHRZ1IRI5fL8AMAGziXyWTgdPiLiqv3g8hPAjsn2qFTlxatWqPbaAhv4UflwT+sPiVETU2bK1fngqOJ9+n4J7Dk53oYf2e/adC4iY5+m9YtEOEBJ+3btmrwY7MfGuuUvvAC55R8qlyda4loMv3RtAnDOf+KHD8DiRQGqu2y4WB60LV2bVvZWFtVrc5tpv/N940WzZmovjoXPLt+fHODH5s2aqqHC7mRERBYlvSgW6f23/3QBP20sDCnc5/4NkA7/7/vfkTn50wZpbJAF01vWDITTdPVudeOOj5x3sdBVAbPLETp6lzaBIJmfhPvozqG6LJ/xrUGkzgqKNzIZGSZK1O5OpcUlt9eMG9Uh/at7l7fAGgFPtwBtFw7t9Le3pqDqExuTCNRXA8d3MPezlpldS7sbW2t+vft9M13ZHVuSdXq3Gt+D7fr6hn87+vGhjKjOTOGotBx7R+IP1DSTEcUE3pIkUv4Wm11rqVyda6HqyO+oNBQ8nX2lc4d2/zwo16DH3TJZ16sjFb5Qrgplcqj/PZVFZa7Nm9u9tU3TfTI6tyzCrYJNHT94uoGDXUaNdbHE5ElS3R37ImljmumcsO/76ZPClGVfaIymZySD9DqP7hv+47tYthVQlSXPM7iL2+DbxrqNtNr1aYleEZX5/IhSoW/v3HFyjAUehh7F95s7Gzo6tzx08bSckC0ZauWdE6UvzrX1t6Wgyj805XAIPfUuZNs7WyPOh/YfmwLiVHUIApjeg3jSLI6t7X66txzd07wa31A1ROIvmGfqHJ1bsPvjeSyg2dvUIMxE6cNGTGmcnVuHl2d2/+XYeYWFieu3ovOrvhl2KhmjX9s+N1XYDC7LLba+ltwlF27+/WUWfMddx9r3badCkR3Hb/MrbwF/IzkckAU14B68+bNUXH0hCkHz97kbBBoDho60t6+pVd0ZrcefaIyCS/RtwtuPhYWlg2+/UpPp+n4qbMiMqodKPFh9ekgmlK14VKlhEAFjMwLIEO1nA0u2BISn/ErVu4TZa+rdnCWJNwd1Lc7k1LzehziRGX/aG7t+0Rpl9BKji+54GqRpv1JOS/iVHY+v7Kraq7wLaGq6VTPars/OeJyF2gCv2zVm3hn1SVEiVQ2RObz9kQWVpWTUdYCl7K8a/oCSQWN8Pj7LPm1yC26nbR6Q9S+gN1+qrpP9BrgTRYEVS4jIiWVezerSMxvonKfKL8bpG4hGQEmohFtdSnynM8eWyyVyhjFnWq31PeJ0j6wheQt1zSao98V3kOfDqIRbzyxqGrDZaVAKVAtlYlLKovmLPlVoJBM361HHPec3k5hTEWRhrboJCXfLdkSWumH3mUtq3zyrxHFoi689ezXs8/A3lx5jcZv2CeqXvGDqD5ANPTNJxbVtE8Uxtx2zJDKfaK0FrebJb6AbNBUX5pLhfCRjOimvQ6DK7XNJ/w9oKHVj0+KyaYVS6rvEy1GCXqFfspkhnTelC1/DQYj3kUJf162LvRJIVpHynxia2NN1gfVFIZ+iapriP6rXl2XSOUymTGCvx8b6ydFHaWx2uen4pvGJqZNdYSlBYhHP8UjfFKIfljFFoZaWlnq6ejTFUAfUACnf+pjucwIcXOzxjogaFwRme+sV6onEP2sFZRS9H//7//TvLmplbW1vm6z1Vv2qtt8BGkiRFM8CmNuqx508CXrk0M0nwznluZcIUfpltz8XAnKqvD5BTxLDQuOPo40CKIR7NRpQonyoIYPK0SQCHMDnnkBn3UXTf4XaSH6QRSdTTbM+D7NfZpfFS5/ZGkmRGscR/1yVR8gyg6E1rjm9vPSJ8MnlWZBtG4zqOTUsf//Ji1EP5RC0krqesD2zdJMiGpVTfUDolp9AGkWRL9kaSGqMdJC9AuQFqIaIy1ENUVaiGqMtBD9AqSFqMZIC1FNkRaiGqMvCaIqGc2qS1HTTKp6yX9V7R2oQ9UNRBV5JFcJ9FYznYXX+dtdVPWGW/VB75TF7J2M31X1GKIq21feUnU9bfnfs6+833P9q75AiLIzl9V2sHxA8ffefGR9QRB1ObaJ5F5Wy4DNsHs3HZfNtrSwqHY324ccprx/rbr9uwowzo+9oy8U29vZvv1R8nEPz25bPe89Tyniqy4gWna7U8c2PzTSa9RE0Lvnz6WVJ+3Vpt/HDxj2a3eFWjlRgUv/vp3ezB7HtVPfCtUfWmi0LOdq02ZC9Vs1q8CFGL/xWfi6eHIppF5eqz4WRGMLQ5duXFTjIX81KjI3SLeZ7ruug73sec6uhZ3KMQgfUCBo/yF937VXfCWURMpl8sSyaPVb/1GaCtFth86F1rjMJ62k/+BhIqHA1MREZWfqBxHNFq5ytsPH0SeDaHkiST2mgjRaqGJJzu5hj9zjx4Xs4bSquVloucqhfcpsZUn3rx/fTNJG1gRRUj3tocRQRvJpV5bcOrmFPfOIPeC+0kmVPdsc6bDaAbnkbvW36AM5TYl3tAJ9UvX0MvTQXer89umtpqamiixy8KGK/3fTB4do+W0LC/NdTrOZUlem5NbKJRNEBlLuaAI+7bi1rFfPrjh3fAkH0QpyCnxlFFvgMqh/F95xB6orYFGLJPquPJ+I76G2tbLceQvcwUDKoLm6DUpYJ6rVy3PJYYF4pRClZ8cTD+ppulVU4EKMX10nnqvH6OofCzozZlQfCG/V+1CzPhZEAQ/87OGVHynWmBQMCEQhe6SfgMMVaoVmVjNWiTjp24v3z5iZmXEQhX9SqyamUnvqliup0Tg0y5/0ky1Hf7Yd3Ux7RT3QuxFsGhlO6GeNriLYLxNLNiyMZY/VJZbZxDJU7UN4D9UpRBHzBacUB6WQgwj4haHsKQQ07QkVORiv+s4QemifekXetfKt0iFpqMrh4OGj4UF9xWxI2muhQC8svYx/VgObMa2qda5KUE2n3QankoZqW4hbeTK+8i415uOc9/iqycBRQrtRm/M36xNBNP2x8zHHfQ7/gBOl8XeVhVk+5/etPbR5CT0vlxYqkh5E3DtxcPNi56OO+ZG3FMksvbJ9jm5ddnLnSko4CCQrjL6NoO3kjhXn9q7hH12EeA4N+d885Hx00xsgii61amFfHOdO+Qfs2dla9+/VhQ4CZwa77HP8x+/mQe4Ah4IoV1jePLEFwWKxyjlHqZ6vYtx4bz0KY9wG9+tRGOtGNrCmkBP+rhzeeGDTYq9r+/BE1AwXRbF3DmxadHz78owgZ5RcO+IglxsVpniSR1Pp7Tvpg0K0Ivfq2hWTpIZyZQoz0CXfefSI3ldOLQM5SrIuk52UlcYFz87TCxQWpCuvweAI370Hd81zPr8y/9k5PkQrWNTlpZ3jt/g665Kevrgg/QKcKM8eKrkFD4d2zUut8dyGAnY3Z8mtwEc7Th5aSE4Iqrjtdm39qcP/EFxR+zxnOLxyZsWBnfOKMi5xDCP+K27fvbHx2L75925urIJohduNi6vdXdaTE45UmqvWtBKi+NJweM9fHMJr/FjwXCOG9hwxtAdu8e++SR8LopG5gUZyI7z6pz2OYOERUxC6/diWvWd38s/0wfVR54P7zu1MLI3iIArk3At3Xbt9JYy5WNYv9TE/IvRLeRSS4QuINm/enNIroSRqyyGHNdtXnrl9XD12RHW8Pn56H/FxXFFYdH7Io7h7a7atgAeuP2HZAZF5QTtOOG0+uBExLiUlrch1YPfp7Rt2rebTHa4OX9lHXalzFFW8Ez1pf9DDM27H0cPdp7ap9/BdVXcQBaW843J2Hr24ee9Jv/h8rtwnLicw6dW5W16rNu1mT7gticlhVm/e4+IZysEjOptx9ghZ67TfPSCBw5t3bA5n4Bef55+g9InyuFxm78lr67cdjGVzjfknFg4YPMw37qXv01yoqlfppXgrEujxy72iM9dvP3T2xmPubCPaw/AX5SscdqigLiqLOXzRbfXmvbd9YiPZs/1UxIcoenX4wu1Vm/Zw0A1Lh/OXUZmKS+5+W/afxmNyFWOyGXxQF257R2cxsAl99w/8U0D0pR9JCIqYLz+gDJB7dBYBmduZbRKpITlK96UfvpyuXzQD+GSySUrtwDvHyPl/6Y8Jw1I89jksJGfnZvsCpYYyI58bB1H90sEN9nY2sU/OM7n+L2PcjIyNaRLvHWv/Wjx7Ajk5L9O7hb0NmFQrRFM8ShPutrS3Q0PkbZY3CUNfeClSPXQFosuHNjB5/ol+l4UGEsWLx8Ck1FBG8qzB8wsvvNpaWytP5kt72LVjOwU/D4wKRJ8/XjhrPDkIN9c/JegauE7Po/+pdctJY4aQcwSzfR5e2YMm6idEgRORgeGh3X9VKyxzlUrlDHNn8/ppLVso83+BKCTjGEvHquHcituGhvLAJ7vIuXpFN/w8tnEQRZxnZWXZo2s7hmHPyauUCkSzks+IJbJbV9YyCrct6/6YNmlwhUo8ytyxt7Pu1LENBV5J/jU7WyuSBLTCbeiQ7vgxIKR8fdPv0Q5iwLhPGNvf2MSkgsSd14YO7o4IrJBkJ3Uvyb6ieHUdEJVIZLu2zEJz18+vQsxdW/hLVOACY4gc9Vd6C9/D8p9fgH2NH8tnA9GcwHYdfrKxsYkrDgc8TExMYlg0AqtSqeF591OJZdETp48TG0gIWnIC1+1Y5Zv8MEURBz4J9YVxReHktFsb61kLp1PnSeUxRkZGiWVR3HCuT/JDsUgMHKIWSMmFm5WdCcIvG/7hAt7YqFe46+TWlIrYB5FuqAhsg4tSsbRbr64xr0ITSqPcQ28i9OSGcyFD/MJKDZPKop8WR9jY2vineUXkBMAGriLzgqkrO3tbLuik4oZzaQ/xaaCHMQUhKj18D9UdRO/4P714xxeAhIaNGn/BzRc4RLwolYitrK0BmMRCkl9l9oLlp697JhQw/X8Z6uodG5xWEpFRLpVI9p+5/jSfWbjScfSEqSFpJEoT6OveC0pmnZf06f/LyLGTQ9kQ1tBQumzD9qd5DCQRi6KyKv4VomAwLkJIohUB/KMzLp4hcpkMDK7soc1Nr0iVs/oQxa7Zsi8ygxz7t/3QeUS00dmqSbY5iMblMXD4JCYDj9axSzdjYyM8Phza2tl37NwFwPZ9mk1aZMkdm8sYGxuHpJEk4Xb2LYyNjNAlFc//qk8BUZKlRARWsSO0bGT50hdMunhgPR3MjPE8oy8SgzGXD64HRLlQlY7rouTEzhW0ZPbk0ZYWFkyG16UD60ViKR0KRoBIkrQggsz1N5AYMjnKXGl9enTG38o3QBQUhPOKVE/0KjfiVpeff2LSPMtTPAb07laSQDr2Ou7OojkTi2PvwDkIGuh6hFZkWzR4He9O3j5/LBCKlWf5VgoGvw7oxa1dUsbZzx4yyQ+a6OiTB8z2MTI2uXt+Bx21psO8t045AaL1bTgXsAEv/T23Vytn7hiIDYENfhJNLizD9cRxAwCwspwrl08t27Vldmm2cg6V8IxCtOjGpnV/TBk/kClR7QbQCz90OBfq0a19927tKthz7RVlrkKRVDU6ZO6AsmSoma07ZFC3kpwraJGM3JbeaqYrokfXKjOmvSIn5TZpJiSLmwpc8BSIg2m8S0+HQC2E3RU0j5uC9Vx+W6WHVSpwkcuM3J3Xs9WvIcb99ReSDK7Gj0XBJn1j877Vx+FcQJQO50blBUnEkuAXPmQENcvv2uMLU+b8DvIFv/AlZ9KyAR+4CM5x8VkIe24tGGxtbeV02BG1jlw9IBFLw9gB4bNuJ5Y5LEJhJHvyLVwdubIfzdGRYfWlRgSiMjmIS3PCoKRnvx40w1pg+pPpf00NTPdm039KUxVxtAo1IxAdrIQofpWOXt1Pb6FWv1/64LrvoD5whZiYutLXFcAVv2l8AnguQJT28BkTX2MP30N1B9HQ9DKa/CviRUVCIdOtZ5/w5+VAFMgx/c9FoexQp4mxcZcevULZAcwnMVlT5yxAYUDSq45dutMjcGNyFGIDETAMWOrr6XAQ7d1v0Mixk0JZiOJbSbQya3cR+Hf0sjuuB/06osbhXEior0tbBN4MpRK8snWLx0+ZifA3MPmVXGY4ZtI09eFWKqAUQTYCR2trm837TqrcpRANSi7atOeE466jgUnkE4gl6dhEiDsBUYnYoDKlTFmPPv1J+u7kIoS2Ry/fwUUIeySviYnx5wFRIOH07tUI6SCnlX8CgWUJ9/Aj/tV3P/7vW6L/+/aHho2awbJfzy4D+3SrNr+Y6ikQicsSlCCMe3iWnpGLSJQk1WLZA/86+sKSp+5wq4e7lXWvHnF4M0TBzo7t23bp2A40tbayRDQJcF7Yt66pjj7Xt+9+aHLjxBYFzUjKWyK0ZuE0hMLoXvcuHYYO6q3qPNUTEKUTonicTcvnNNURWFpa2NpYo9vRHqfhMD3YGV+Wgf8W8MMGta4sREnMrdbVd9MHhShgg0jr7l4WilEAAFmUSURBVPUN1QoZdwIzBYlE1WnBVEIUJf16d1SdhmQXFhkYGP4+fiDJtaLeYgGBKK1S/pIg7dKp5XSkFLTTF4jjgg9WHTFPOnMHn6oSdSzd//e/Rv/7ujH0f181IlGgwg0AMzUxbdpMSP4XbMn/AnuC/B04xyvnij8nSlR6i6R2QQyt3kllV9lHLqhcWMTcISMNFW41fyxs+nFI1ckb9LEgmlgaBWYksinMKCCTKhfXIF60trGOLgjZedzp0OW93OwjCelYiN7wvSISGJiZmcHMwtJi2rwpYeQw+lBbezs4hDfQVGWpDkLbIaMGGwgN0OjJG0dUOkOd03W24Oj2Y1t0m+k1+Kbh919DDRo1aLz//K6g597AocooKx+iXPeg5PIYxNMISdETuGL9EFdCfRFc8T1wEFX2UCRGD0eMG6bSw/dQ3UE04kUZfp71dJpa29jY2NpaWFhEZ7FxnlRy8tqDUBZjNrZ2i9dsYecySxCoDRk+hqQhO3R+x+HzwSzDUCgS6CMoBNtqg6iAhSI1RiuOu4+DT4BojQuLgChAlBA6rYTN+D1AJeN3YNIrkPXE1fvqp/cBn86eYU0b/2BmZo5HsrC0/GPOQhUbLkdbzz4D2O8QpA9RWQw+BKAUEMVnQqNPtDjxjzkBiYUw7tG7H9dbINbE2OTzgChDU508e+R+Yadpc9NxIwYCISTPdpY3SX5CVRAI2Iwc0q9jh7bcrCFRqgfQWxzHxnwpHv63DiMEZF761QhRXBPEVq7lOb59Bf5uvgGiEIJLRLSlCXfFEimNlW+e2IwQmYwnc317ToZzCUT5+1XSH5HwOsMLjKczmtXEg+irWDeSSDXPn0arOnpCQJSh4WmOb5TH6THDBkgQQGf51FOIKu4YGspnTB3CL0RUZ2bWHMHflg010YKDaL7zyOG9ijIuqkAUkWjWMzZtdY3H0laHKP78Hdn7N0kdykIOtV7En6xWiw9RhZuRkQnDeJNsKpVS5F579eLir4O7ExwW32CYeyTPNiBa4SYUSRQ8Rr4HRNGfKqIz7ubmZrV+LJ8JRPEKeCQrYukt4MTWzjYyLwgEBc+U2dDygkQCESiFkA4s3HnCKbYwFAxr0dIekSINMU/eOrL16GaEofDGT9vCCfHrpgMbmzdvfvrWUf70pBKibAoX+DlwYfeOE05J5dGpTBwV2kJ02K5DO5UNLXyIGghF4ZU+UxRx5ubmsa/CjI2N4YrzQ13xPXAQpW/xBQI9xE+gSg/fQ3UF0bSSdj937DdwCGJQRKLJxSRueyuIphYfOHtj/faDdJUQuGUgEpAUnkqIJtGK3Xv1HTn299D/AlH2bfufO9EVRghbL9z2mb98A6hGe6gOUcSsBkJBymsmKpPBs7Ro2Wra3JohiotBQ0f6JxTQOJimAUf1GiEa8qxk6KhxAUmFtMMJhQrYfB4QpeO3NJ31hiUz7WytFameNJ21gl2eSiI8NhQriL4tlhoCYMoFt5lPANTWLe17d+9UnnivPOEe/qKNGdYfuK0ZoumPWrW0r2ADStiDjiT3MmxSPU7sWJFHlimpDZOmP27Zwu6n1i379uyiLMnxlcnlTC7pA/EPgiYTKKpAtLxaGnC1TSw8iEbdP8kG0+wq4vwAczMzClHyHSLVkzx+xhMyHJ3jG+R2lIwMvw6lDb0Mv7l11Z+1JWt7kz4oREGCrOQzhiR59d0KmryacZfJjIvJYtRqmaiBMZKJmgdR0Ksg/XzbNi3AOUpBMujKLSwquiEyMFy1eLyCpiDltainb0AcEvC4OG2czqbOZpNgK9zIBHlF9fFVHkRR6/j++SuXTGCKritXQrHZyqL89m1a9wddIYwLkua95Bau0fn1KyczhS6kuUIXRW7tEC2+sc1hhmq6tAIXuZHx6BF9qOdj++cf2k2WF9X4sSjY9ONk7lY9l1xt+lgQRZQmEhpkMMlkuDXLH9jbdGADXYU7/o+xx68fxjXQAgilMU/Zpa0BdDgX5UKByCv+ATAJ+oI3NBKNYOkLe5qCW6U5GMS/jqCrc23tbecumcVfAcuHKISYWCaTJVfE0FW4YGF4TiDuSiWG98JdCbDZwojqEMXv/uARg+gqXIe969btXI3quIArPCN1hScKr75wl4Mo7WF4NlkS/PjpfZUevofqCKIgkKWF5cIVDnREd+FKh7eMREPZUEwuk6UUkyFcXBvJZSAK7pqZm/+9bB0Kw5+XS8XiEWMmhtYC0eDUkglTZwelFIc9L1fZD8qHaI0Zv4Mqe6gO0ZiXjEioH52NjhU/CEnFD1VtkSg64Bn2rEv3XtT4kru/RCzGM9YMUbI8+FWLlq2Tisj88eQZf30ec6Kg4Oun7k109NcvngEkIA6LeHCK3Mr0xkczetiAXevnd+vcoXFTXZRUJD/Y57jIzMzMaeWfE0cPnjN5NBBSnvYQ8eXqhdP+njGOrEViF+giWMQvCQfRxjp6gCguXic/AIY3Lp01beLwQ05LDGVyNp2nZ+/uHVN8L6lDFGB7cHGnkbFxwuPzyg4nPRg2qA9a3L7mr1V/T7W3tSFLolI9m+oIVE9OeO6Frj4PuFqh5hb2v/TroYyJs7zFEsN508cCut82aNxMTxD14DSTF/D//apBv15d8fi9u/28av5U0rdMb0AUfTY2Msa3imSfi+hYaU07av5FHxSiDEsmnwfb9AXixfPHzJs9wsDAsHfPDhUUUWWuhlL5gnmj1y6f1LSZsFETfYqH8WP6Df6lq4IdgJUayhG27toyG2SdM30oHc6lZiV5zvD21+wR/MgS1/CPj8LGxirMezcgZG1lifhy8/o/xGLZi6TTqsErcwc/DFUzl8U39PXFP7dvtX3TzFEjen/9bRNiX35bIpHNmzPSYc2UuTOGNtNhI9F859TY43r64h7d2m11mI5XFJbx94mW3kKcpIRoxW3SCm/sl6jApXETwaa1U+H2j8mDyc6fcna+tqaPBd3ITjnTVEdkZ2NlZ2ddbUS6Nn0siIIZCCjBD2Njk7hXYefvngRTR00c0Wdgb6G+kC4sgg1+Ms0tzP9ePrdpo2Y6TXTAKkSEg4YOkMnkyzctaW7a/OfOHf74UwlR8BX24LHKWC4AtsppOT7YJRv++XPJLPhXWd0TSTah6nEQhbcBQ/oh8F3msGju4pkIi+OKSE7vtdtXonDUhBF/LZ8rZ2dYAdG+g3pTiOrr6i9c/feC1X+NmTRaLJLEl5A1vXgQuGrbvg111fDbH6grToCoRCxBh2kP8YUAPaRLmfhm76E6gii0/8x10GjSjD979Rs0bsos80qIGhiITly9H8pSxMrKetHqTRxEfxk6OpRsVnmNcmNjo39WOkol4ocRz2nG7GNX3PF2xcYd7X/uPGDw8OG/KSGqq9OUtggP+HAcdh1DSPc4KgMhrLWNLTjNxyHwqafTlBvCBWsNRMK5/6xCoCyVSAA/rofqEA17VjZwyIiefQcuW79NLBb93KnL1NkLVGz4+0RB3PYdOy/fsANNrN9+CCWAqJGREQfR8VNmUYgiDjZt3hxhrthAtNZpHxhUWxrUN+hjQ5Qo1bMk/u7x7SuObF0KNlTtlcz0dj7quN9xUYDrYWXAxzIs2O0oCqttccnxOVLjFpfKJgqiXOkFjGPJFpeFfjcPodGCSptXsW41oK6ye6Q6P1d26kM4Rx/O7lmd5H1BpYkq5fjii7YiW9klFRXF3ql6m+V9aMuSK4c2ILYuiHYlwSU68+yR17V9BzYv8nLeXzUNnO2LbtNH27l+PpkuzXj37NwfGqIMuxel4Nn5M0cXTRjTj0z78Zf2lN9G+OV6ZS0ww21rKc64RPKgVRoEe+3cv+NP5RaXfOeiF8pbZP/Jq+uv8FYlHXfxDSCHv8Ul3HfPwV3zUmrb4pJ+oZqHCrfH7pthf/fGhvJK+9zUs+jnlTPLmcLrXD/pFhe3q+tw6/5NB1rIbdSBWM8uijxSfdXSiRVqk7hwpShwhlsag1bdquljIThXuL2qf6tzI9hR3OAMH94Wl5BtRzfvPbtDfYvL3rM7E0qjuM0k0QUh1x5fcNi3PviFT8Azr6DnPrQcQV77ju2GjxmqvjAntjAU4d26HaucDjuiXXUDzjkV6Oif5rVm24qthx3vht1S+s8mtbYe3eSwb90Vz3M0pgxMfxJRGcuiY7tObVu/i8SgfFdnbx+nrtTbjcgN9Gf3xtAebj+2GT2Ezxos31F1B1GwwSsqc63T/ts+sREZZWTbBlvuE5dD5zvZ65dkGLOyCrcTBgHctQcha5z2u/tXbXGBwyfRWWu27PeOzVbZ4sJ5gMPA5FfUGFJdnatmH5peik6CcGduPOJvceF6qKKIDMWmPcc37jzCLq/N9U8sUDHwS8hH3+h1XB5z+Lyr+hYXztg/oao6YlB8FFFZzNN8hZ1dixr3z7xZnwKimqjCGLfOP/9UGOumSKmFzf9N+DawecWc9zy9qA4gygkUeZ15iRy8oDKwqdEC/G5cWq0ouqF+q271ESH6YRX03Ptx3D31MPTjCBQU6ou4WLY+qO4gqtXbK/xFxZot+zxCU0+5PEAY6hufS6H7TtJC9EMo84mtjfX4kYPeZ8LyrVXj0UhvpbqEKKNcffMvx/5pnv799KK60GcL0UmzJrRoaY/A9L/HcO8hMicqN9JCVCsVhaWXDR09vlWbtl179Nl+6Jz6SPLbSAvRDyP16dV6pDqGqFYfT58tRCPUTv77yPq0ratLC9H6IxJ9vnsAykkL0S9AWohqjD5niGrFlxaiGiMtRL8AaSGqMdJCVFOkhajGSAvRL0BaiGqMtBDVFGkhqjH6xBCt11OJH0LVjlv6N6kkUKsq/4+f0ucPUXqMLXddeaG2uaXO9DHbepPqCUSrn0igqpyaDep0VrJOndeF6gNE32Ml6n/Sf5t6rLf6lBAtT7xvYW72xHmf+q2a9fwxkx+oWlifleo5cnA/1TMZatf0iSMqkh6oojTb187GmtsR+z76HCFafJMc0Vf5dvrUIWNH9yUkK3TBBcMeaSSTG7/VAQXvpYrcqw/dNt26spbs9Sy7bWVpwVRUyy3zaVQPIBqVF/zrqMGRtecCGzvlNxioFCaURllYWSbw9pi+q4DJVOZpjbDcc2a7rb3tfzyH7yPr40M0JK00qYjBK30b/rzcSC7nzuH7sIrLZa4/DF+9ee+uY5cjXlTQRsdMnDZkxJiPkzdb5WHrVJ8YolJD2aMre9Rvqas86b7zUcdGTXXffPht/VKq5y99u789RH8fPbgGiOb4mpiYMrWc4fBW+gwh6nx+ZaPGAu6wgmG/9ujVswOF6LBfyUH2DEntIq5TiD645eByYRU9qI8cNKjQQpSIyy+mfouq/5D+XXp0VilMLIuWs2lh1O3fUkll0TpNdLhz8PnaecKJy0v6uejjQzQ+n9Fp0hiv9C0g+v3X/1cXEI3JJklaTExMlm/YPnLc5AbffpX0ijQ67LeJ/X4Z+nEgqvKwdapPDFGJ1NDj0u4nzvv3Of6T5H2BjlvilX9mUEH0bViWJtyl+TXzo1xV8mtWOwwopVpO7NyIm/Ds7XKAi+QKY27Ts+mpZc2pOp89zA67vt9x0fl9a5VHFKU9DHQ9cthp6Zndq/k8I01n+9w4vtn97HaSFlTFT6rnoD7dFWmeOWHXD25eXBTrpuC+AWT7uJ/bjr6VJd7jRmsnVkKUnvlHc4kzhUHkSCCNhqgiz/mx++YDO/+8cmZFRvxJlFw7u0IuN85PO0eP8qnK6V3oQrPB4FpHl+RHU/VWcgsAPrT7r9tX15ZmX2bYw/FJ5rVCl33b5yqPqi91PX98SaTfXuqHySO1VBJ0q0CUnHarhSgr7kBa8jY38KjzgY171t4JvsExzD/tMXfAUPzrCKfDjpsObEhj4mUyuTpEUeu69+U1bAbv6AJlt4Nf+JB8n5U2fqmPIngpTgN4t6gAUVNT06j8YDS09cgm7hj6sOyAR3H30L3NBzdyBy2FZvqhh7BxOuTA5lYjT7Ht6Ob1O1fT1G8qzutIHx+iYemFbOhZyJ0l9Dgyg17Qs4QehKSu23og4oUiOPW1f0L+Gqd9fvF53NbJuJfM5bsBa5323w9OBoDV/VOFpJW0at22V9+B3FgxHNKI8M15s7nzhkLZ/nAJ0dDbMPZDQETrGfYMVc65PuEOOaI9fxievnjtluisql6pP2xkhmLrwbPoP+q+337Q2vSJIWoglp7csXLOlNFr/5kulhiWP3sEfmSFXm/cTI8kTmFtRAbSh5d3+908aGVlie+btjbWxkbGHHgqkh9kBF37Y/wwWgL7jUtmgT0IWP+c+ptQJNm1fr6NtRVoXZFEUnXa29qs/WeG8kT7l37k+NOsavCDTf9eXVBx57r582eMA8BgnPDk/IA+3bat+evvGeMEIjE9Ch/8m/H7iB+b6G5cMtPMrLmFuXnVEYZULET3OSzs26MzuoGHDb17gvSZTS/TuUNbFApEksNbl1F7DqKvkx/oCUQbl876Y8Lwfj06k05qLkQBwpOHFnb+uc3OzbOm/D6od8+fAS0rKwvyf21rRb5AvL6pPHqXjUTfAFHFq+vNdETjx/R32jh94IAuF04sBQIvnlx65sgiYyOTZYvGSyQyz9ubYLPNcYbUUL5p7VRybl/JTV09gyULxu7YNFNfKEE3UKiFaG3iIAr+ffdVg9ETRy5Y9ZfMUOYR5UYJNPS3X/sO6h2hPCdI2K1Xl2WOi7v16orQRAWiYVn+5++exI/3ModFvQf06t67a0xhKMD2z5r5NjY21Bve6jbTfVocYW1jjR8JciarvW1c9aNrAVELSwupRLrccXGX7p2mzp2MuuEgaOw9qVg6f9W86X//gT8aCaVRoVn+O45vMTM3k0oMYRyY/gSYF+gKJs+euHj9Qn0dQch/zrb9lvrIEAU2rG1s2A/Q1tauRVQWE/a8XLcZOcwW0mnaePGazX0GDhn060iBvu7+My6tf2o38Y/ZEgPR3YAEWl0uM7Szb7lo1SZEmUNGjKltPhXlLVq2smvR8mmeKqv4EBUJ9dt16LRsw3Z6vC1QumnPyfO3vVEFtDM2NibZYNj8LXq6zdDbkNSSnn0GSCXi5Rt3tGjRiqbapj1fuMKha4/eYyfPqEwXSk7yU3lYgFMkEowY+/vClQ5Cgd7DiOfqPX9vfWKIgm1SQxkuyhPvvYq906lDW8R8gKiOnpCDqERKhnwBS7cz20hqsFQ2nTXfVaY3SS7G2tP83uQ6/RGcw2cZeJnnb2FhrmAJ3aqF3frFMzmIknQf1SHK5PgayuRMXoAyRmTvEjqmkjODUNixfdtFcyYq2IQzNKkZ8fbSj8BV5Vi+VM/+vboumj2RpmeZO/U3ezsbuMoIdu7ZtSOT8QR9Q4BrIJHSIVwlRJMetGppP3RgbzbTy70L+9dpNkSBKPx5BaJIXpc88haFbtfWIRIld/lJYP4NokzR9UkTBlbkXSPkg03xTVxcOrXM2tqSUdxBPOq4biqbhuV+2curHq6OIpFUeZr865ugJmLWnOQzJGdLmasWorWJH4nSc27BuWdMvKWVZVwRYdvwscNgAMQ+jL3Xb3BfysXtx7eYm5urQDSxLNpAJEZdGMCtoVR2/PphXC9at8DO3o6DqEBPgIuUilhEoniNVjt4iA7nJpeTvC7wKRIY4BUSi8RpbBptRJ8tWtnPXUxSr8DYzMwsWRHLNhrUuVun4Axf9BZv/1wy29rW+uMEox8ZolBiIYPgLJFNkRbKDucK9EhaFcjYyGjW30uBt+gsxs6+BXAVmckAh4Bl+5874wKBac++A9kc3cVJr0im6yg2HXeNOn7lrqmJibWN3Ylr5Lx7DqX8RCudu/akiVYuuvlKJGKEqrgePWEq2gILh44aD34HJRc9iszQ19MJTi0mWWWM5MmVGWbAacSypOfGRuOnzgpPL1OBOv9hg1OKF63etGHHYfQE1cdOmi6Xy2o7pPc99Ikhimjg2lFHZQlJzyIG/GqEKCJLml9TfU4UPPu5XdtZk0YBOZtXzAUXKSM7//wTzZsNMvnfOuywdBaw9GaIohytHNqyhKCX30SqJwJcOEQcjCDJytISLAQXJ4z6RWmT8YT8dc7159eikSg3Lh10+4jIQIL+j/61X3Gcu3LhbiYqWtCHpRBl2Di16pC/PH9TjZ4TVeQ7TxjTr7lp83UrJwF7dB2s65W1gCg3J/q2EC2/LTcy/qmtfcDDHWAe7lKI3r+5EVBE9cTwwzq6IuoWJWwCbRdC7jLXsaP6tmyJL67WJiam8aGHtBCtTXyIIpL7feZ4RIc2ttYioQFJjZKjhCju/jKcpB6jK3UBP/BSBaKHLu/l5xYdP22srZ1tSKZvjRDlpzhVEbiI72F0PBm1YB/8wufI1f1ymXz11uVrtq1YvW3F5FkTQfGQDF8YIyrlBp8lBpJ1O1bBBlrltBzhrLr/utDHhyib3UzOhWt8iAr19ejkKDAze/5yQA5MAmZ2n7iCoBCFg4eNXuGwa9WmPas27YY6de0eXj3TmYoQ/AUkFs5bvAbfVwR6OqBvqGrKz3yKPS7lJ7CNbgCN2w9fCEsvR7tRmYrBw38bOGQE+HronOvo8VNXOqIPu1c67Jo0/c+Tzg/gQSTQC1FrPbT6w8blMSYmxgAqvRWZqTAQCSLe/aD52vSJIYpg8cHFXcqSNE+SQzvF410hCoXdPU7SKWd5I4g8vmMFGWtNuDewbzcKMESxcQ/PLv1zErz9K0TP71t76cAGpQEr8PLwliUjfukTfu9EfpTrjrV/g6QUopPH/Ko0ewNEK+PmoNtHEbkCkwP7dAOklQuIXnjZkMW3pA9KiKZ66gkNqra15Pgam2j4nChTfGPx/DH4diKRyJw2TgftXN8PovnOqdHHxo/tLxBKBAJJQthhCtFHbpv4EKWJRVGXhSjJ8aKnb3Dx9PKM+FOFhTd19Q2iA/ZrIVqbOIhG5QcDnAtWzfNO9Ah87i3QEz59HRFeCVEY9OzXg4vqEBfKDGUqEN153AmFYZWJOWcumGZtYw3OvQdE8YusAtGtRzeDrCu3LANHoVVbli11WARC843RllQspQZUSzYsVPdfF6pXEBXo61IoEoguWP44KoNCdM+Jqwj1cN2tZ58VDjvAMKoVG3eo+1cR9RD7kpHL5X8uWgUQUoiiOUS6gSQQJBAFbq1tbGAGA+D2UcTzrj37PM1npsz6O62M5Dc9dN4Vt5z2nx4/ZdaKjTuVHXDYeetJNKpzPVcR/2Hj8xmZoZRbZESGdgX6iLnVa72fPjFEDWWyUUP6KWOyXH+ZTM689C2Nv6snMGCeEc9Aplhi+JCFqPu57WAkfyVOldIedu3Yfs/GhWRgkEIx1x/0pVRDhDpnyujIeyfhpHf3TpN+G6Kgi2BfeDVvrjqcC5sOP7VWVJKPDORmeTdvblae7cu+fdCuTSsrC4v3hujrp+6nd606uXNlWTwba2axY9FsgjMKUeDfQGLocmwTwwbZaEXjIUpZiNf8Z+f1BRLm9S13lw2GhkZlOVdoYPr2EIUNQtuSzMvbHGdYW1uWZl/5V4g+vrNZLJFRYOemngW83wRR5g7Joa32CB9J9Qai5CI/uM8AMvcZwQaaErGUD1HEoFsOOew7txPcimBZaKS2OhcMk4glNKiFgbm52eQ5k0Iz/Z0OOZqAcyxcz7qdoNFhQmmUiTGZVVUfbq0RongLQHKLlSqRTIZzOeOk8hhDqWGKIk7pKqdqv2kqV1g3+vgQRZBnYmwcm1tBQ8C3hyhiyu2Hzy9dvy0giSQ7Y82UY6FJRWS6UaUhcJFbFhSYXGRkJB8/ZWZI2msK0aDkok17TjjuPh6YRNKGo7rYQBSdzYSmkQj115Fjm/zYENUDk4sXLN+gp9ssvoD4R4ut27aLeKFcOkQfgd9zFfEfNux5eeeuPdB5WuvKvSCxgTDkw60t+sQQBSBt6SbIHN8ZE0ec2LGCQOulr4FEOnfqb0yuX9CdY1ZWloCogk03hvK8SNXVuQyLuhiP02bNzQ47LaVBJEoEIvHMiSPgJMLjNJnmZFfPuhx1lBsZFSeTcdQ2rVqQdSsqC4vSPAUG4q2r/mTy/IFGL+d9ilSPPt07eV8/AEZWpHn+1KalpaUSolN4EEWhOkT5W1wAUZFYSrqX7SOTy7OiXNG3Hl1+Rh/oiiRui8uOtX+R2V/8mmV6w62Gz4kq3Bb9/RtTeoth3JfMHyOVygGtwhcXDcSGeZWrc38fP2DYr0qI1rbFRZFH8pK+TDlLNnSWubZv13Ls6L7qkSjAyUFUT18MiJa+vAqIEkYq3AxlRqamzdUhqtziUujyU9sWSRFHKNo/geoJRNktLiCQsZExqBP/OrJH3+6ISpUQHTcMBhGVsWNIhl9yeYyFpYWVtZUKREG4dj//dOTqfriCQ3ig6b4jcgIAThQSD8bGEgMJbfen9m0vPThb4+pcbosL+iPUFwKicPjL8EF/LZ/7tDgiRRH7MMZ98boFQDXfGK+Hr+zr1LVjdH4IUIpak2ZNRGFwhq+hVBZLO1M3+vgQBTV/atfhgps3XbCKt3QUlwznCvRqg6iJiTEABiYhmDtz41HiKwaMPH3dk85oNm38wx9z/+GYGsriDd9Rlqxzgv+EAsY7NhMVqUNuiwu8yeUy77hMGABvdMQYdY9cdDM3N7eytgZxETjiulXrNhEvyOQrOikSCuYtXoMq4O6DkFQAld/zNz1sWsmjyOc2dnYx2QxiXFMTk9ETpqpXeW99Sogy7PYVxJ0A1T6HfxKfKLe4ED17FOp+7NSuVQgW6RYXZXm276tYN3WIEqnnxE5lt7g4VNviQpp4/hixYPjdE0z6o5pdPXuYEey81+Gfs3vX0C0uqHXz5JYDmxcnPDmPUJKrVRxXtbuGFPJTebMqilVutmHYGLcgujKVdw67xcWh2hYXzhspIVtcSC5x+gmQ5VTVPb+D6jlEAaSiGxdOLCE7TF5cVHDlFW6vXlykEOXn9OYu+LmylSpwiQncf/zAgusXVyGcpYhFOMsNC6OEX6vqms2YzSXophVRS5nirYCk2qZZvtGlik9F0Px6AdGIykzXESSZdtjmgxtPux6LL4mkG1HYu96cAbCKsHLT/g1xReH+qY8jclVd0S0ua8kWlx1c1AgBt+t3rT50aW94dgDnGYAMzvBRhyjZtcLL2l1lnx3gn+a15aDDup2r7obdQh/UjSGQe+/ZnWu2rbjscQ5PRAv5e2zqQh8foqEs4QKSqnZ9cFmy+emyAxILuEU6iBq5XNYxOYzrk5hVm/bsOnb5SUw23bXiE5eDOJXfBLUEFA+dd1237eDpGw+5NNdvzpsNhcEh2dxCItRQtlf85T/gIjqDKlv2nXLze8rZcAYqUnnYyAyF04EzazRsiwtTeaAdjepUBmnJwGYiGfBUKcfbGoZzUz2vHXE4sWMlfy6TGsOJ6s4TNgimS3hqcMWrCDPOoJztZAX7livkH4xQoyuVY//4NtQh30DlmAWu5zV6fgfVc4iyYol1lTvSj4o97Y8Q6+2P/QP/EGhy1FQXvxb/Gq3TWjW65QpVevixVT8gyj/VD7EdFwJW3a1uQJcOqQ/DUgF1ABs3M8qvSAv5FcN5I67VnFSzqXZNOpDpV5sBFV3By602qtHmw+qTQDSURQsHLfULdfFv4RqEA9jeomIJwlNizMdVWrVj/6iBykGAKs3xb9ESVAl6qw4o7/INUJEj9AfUJ4bohxGbE5ssSlLZrKIV1ecAUa3eSvUEolr9Z30qiGr1waUREE0hA7Cqp+VpxUkLUY2RFqKaIi1ENUaaAlGt3iAtRDVGWohqirQQ1RhpIfoFSAtRjZEWopoiLUQ1RlqIfgHSQlRjpIWopkgLUY2RFqJfgLQQ1RhpIaop0kJUY6SxEOXv4PyPKk+8T3ZqstfsZlByUZZQbU9O1VG3rFSzs31aaSGqMapjiIZl+SeVRacycYml0dyeE27bZZ0qNFO5E+btxSVc+xxVnyH6NI/xS8j3T8hXv0UVlPwvG0X84vPeUJ2KHpLA7UP9fKWxEB0/clANCa7fS/cv7iRp2hLvM1k+5KzdHN+K5AfbVs+Le3iWs3FcNruKqWmegwf0VD944ZNJC1GNUV1C9Glx+Pqdq/V19Bt801BfV7DloENMQWhUXrBuM903pOD+IAKw953beczlIH+n5puFLuk204tSy+jyuajeQjT8ebmeblNzc4tR4yar34WiMsuXrHXCq/otqrD0sh69+w3/baL6LU5opf/gYSKhwNTE5A3ZST8LfYYQzQ8AxqqIBVbRc/Xy/JkXXlw5l5tTNW+aylt6HkLmEyYvgMn1r/F0+weXdhnK5ASicP4qGK+AqFxu5HZmG/GWRqSrLyIZY/A2lUB06KDeVRDNeKLa548sLUQ1RnUG0ej8EJmhzOmQAzmdgD2a4G6Y64V7pwFRgZ6AD9Hk8pjEsmg+7WJfhSVXxCKE5R9QEJ0fDBuUQxHsyUTs8XtxMYWhnBku4l6FpVTEAqL7z+86fv2QCkTRK3oRmRfEXUewRwCiSwI9ISAaXRCSoojlEnFTtzEFIYin419H8F2hCvqAcnp0kYr4/vlv0aWE0ig8Bf9D4Buj/D2+ZNRPiIJ/4enlQ0eNC+OBLSaHSXzFRGaQ5GihainVqKKzic3TfAbxJZz06jtw5NhJERkKFNbISLRCjr19Xk7vUleIgJOL0Ao5fTAul0koIMnOuCrUJj6f4fKxoG5t/j+mPiuIZnmPHT7wq+9+1BcaZEfcVCQ9ANiuHXW0s7H+bdiAbxs2MTc3L6ocZVVmRMn2tba2VLBnxxNlPKk6ob5SeZG3pIayr79v9GMT3fP71laotVsF0SwfO1trJtPH7+bB5s2bW1lZtrCznT9z/OzJo0xNSbZwG2vrUPfjqFIF0UxvI2MT9FlXIHr11P3TcFQLUY1R3UAU1PF6+sC+hZ3y6FpWgAdQwYdoeE5gv1/6NmuiI9QX/rVsDj2lL64ozNzCvFHDxkJ90bipY56yfAJlbWytPaLuNG7YxNLKEgg8efOIsbHxD9/9aGtnG/zChzaBCwtLix8bNBr4a/+jzgdVIArgyWVySsehvw0xNTVNYuENtO85syOcPWg+viTSytqqyY9Nf+7yM1fXL/WxfSt7xNP4phv/mpzWG5rljz8OVzzPo5MNv/0B13zo0g6bmZtxKWIQlJOMeOxh96u3LpeIpU0bNevWuxu6FMEe+SuXKfPJAP97z+08d+fE28fQVPUTovtOO9vY2uPzsbG1ux+cAmrGvmTwH9fwu69t7ewDEvPV812HsofIo+SH778RCvVn/r2Ug6iVtTUq/typa0z1Q+oBS7TS3NTU2sa2Zes2cCKXy4FhnaaN/u///X8SCpmVjrukEnHTxj9269mHplGDT9jEZDNNG/+g06zJiN8m4rptu/ZNGjXs1KVbLGvzqfT5QDTHVyASH9u+nJwFmOoJ7Hlc2AmwXTqwHv9/TK4fysPvnSDnFuUQZFKIwgB3t6/9q4LN++181PH07lUqRwOqJ9xWaZoPUcJgdjj3bSLRojh3kqk7kyTfRkwsNJAkPSEn8X5saSGqMaobiEIjxg0/ceOwOgk4iEKduyvzV0fkBPLzV8cUkLTbKF/muBjIRGFSeYyZmZnz44t0mjPouXevfj1BILxFIGggkiB4RbAIOIGvoWxOb7GB+LhLNYiSZGp9e1DnzRrrdOjc4dDlfeB667atEkujcdfYyHjaX1MjcgnvJ84Y7xHlhqaBQyO5URqb6BvXAn1hQkkUIGooNbSwsEBhSIavy5PLf62Yy5+ChYdLD86i//SQwr1nd2455BCS6fco7l7n7p0RuSI6v+xxFh2OYCGqrysA0UnFLP9dp7addj2m/tG9WfUTomHpBFeIRGnY55+QLxIKquXizlTwI1FQ1icux1AqiS9g6Dm3MKbDuWIDYWh6aVBK0YQ/ZgPA3Am6lQ2VCfV1IzMUNHKlubXRSnBqcVXK7mRlyu7QZyXEhs0cDpsaM4erHB/4MfXZQDTywSkCSPZ8eQCpX88uvbp2BPYuHVwvlsroKbtgmI6+iK7x4YZzz+1dI5MbKXJ8mAwvK0tLhotKOSUTQpNj5WNu71j7d8sWdirxojpEy5PuA6Kup5w4G0CUPyfKQtRj2bzJrVvak3Hm/ABoYO9u/8xWJfTHkBaiGqO6gSiLq+43fK6EZ6seGEshClABRQBSOpMACqYq4sAnvWZ6lBxAJj3VHcjR09EHhFAiNpBwA7mzFkxH0JmiiEXdNOZpr749ANT44gj7FvYxbDgLyIHKKhANreQTwGlkZOR0yLH/kH7wjP4gYkafDYTKhN6oddbtxI4TTiGZvm5B15c7LkkqJ8ujYGwgMrjhexXglBnKtx/fQj3DYa/+PVTGYAFFOZuvFMjEV4GE0ii4nTp38p3gG/S7Aps3TZZcEaPBEGXPvH3968ixoWxGl5l/LWnRshV4CYImFzE9+/QHI+Nyq1J1wmbq7PmWllb8M3IBvJ59+3fv1ZdmDD193VMKylam86SCPSBKR2vxKhGL/NiFSCifMuvv294xIWnEYXy+QiaV0nFdA5GQZliDzbS5C108Q0PYVDNbD55FpPRhz5R/J302EEXEKTWU00zd0NI/J9naWJcmAKIbTE1NlUfMv/DS0ReWPHVn+HOiOb6gb/KTC69i7yAuVFlqpEj2UDx71LiZnrGxia21lZUlvq2a01PmOb0nRFM8+vTobGRs/L9vf2T1QzM9wYDeXfmeP5K0ENUY1Q1EI/4tEo1gc3/iZ/77rxuyagA1+bEpyp8WRYgEBgjRyGSGjbWBSAwn4A1+K+PZxGdgVbdeXRt80/D7b5QVQSDiMNP3l2EDaStA0e7T21WGc8PZceaho4fAz7R5UwKeeYmEBg+i7qA/sOfmREn1bP8rD89vPrARqN5+bItuMz3SHNtPob5o//ldwRk+UokhUEc9Iw5GVK0yogsnIoHIPfQmbYj2vGe/HohH6Xn6qIUHjH8d+YVANCy9vFvPPsbGxg2+/Yrom//p6zYLZVN1chBlbfoCrpSXVNxwLn17yd0PUWkCmxaUkwpE6fwodUhSdpPVv8Qhl7JbaVNLvjYEsvx0bB9Znw1Eox6c0uNHor24SPRfIFqeeO/qYQdQEHz8Z/YEVc8kmbYFwsQKkhzGY+6U36ytLT8URBfMHG9paVESfxf9pKIjyfCvnlimDqWFqMaobiAKVj1+ev8Nc6KIRONfRyDyi84PJntRWIEuYTkBk2ZNAF9pGparD8+LhKoQJfHcnEku3pdBMq4uyv81Eo1gB4p1m+qBgog4wTAEHENG/gKsRrCEU4coeoJ4esqcSaAp1xZZKpXl/68QhQByuUyOPwhgNnX7x5+IRG9ykaiMRqL5IXQ6lu2538oty05pIkRpUGhhaRmQVBiUXETEpkABPqtFonMWWFqpRqLvA9FKQE6d/fdtn9iqSNRQGYm+DUT/de9NXeizgSiZEzUQn9y5ks6JSqQyj4u7yJzov0GU1kUwaiCWlqeoreuhybQLg0hWshQPhKpvE4miOZgddlpK50SBTz2BiBhUnxMtiLktlhoyeWTRL7mb7YML9CrU/bjHpV0qrdShtBDVGNUNRCMqV+duPeJIkMOC5154tdW5uPi5c4fbgS6USZF5QUARyDFl7iSv+AcIKxNLo1q2aiExkKhAFApI82rRqkWKIhbIQfUEdkkOmRM1kMItnRNFRXWIAsxCgQisTSqLwa0Z8/+wtLQ8eetoRC0QJSPJZdEyGUFdKDtNm0jWDBNIvw1EURfBqEQsodTE66O4e116dKFzomgCt2g5QtVHsffYKd6ncrlcIyEK+T59aSiVJBaS+U4QCzFoKDvrie8Zz8rpnChJKUpGa6vPib43RNGKZ9izLt170TnRS+7+ErFyTvRfIRqVVf7PKsc37L2pI30+EE2pWp2rV311rr2dDQdRmZERhej0iSM4iMLM5dimv2eMozlEVZXxBEiGWyMjY0C6XdtWKnh7eHWPlaVF1epcOqua/njahGEt7GwXzBoPiKYHXRs6sLeNtRVdnTt2xEDl6twsH0TA3zRo/G3Dxm1at3geeA1+Lh5Y57hsdo3baepEWohqjOoMohHsktR1O1bpVe4TdTrsSPeJGsmNKlfnBgwfOxTo+uH7RojYJkwbhxIErwgQG377Q4dOHWADY4ouW3tbujKW6pLHWQtLC3jWbabXqk1LurI3+IU3WZ37faMBQ/qfvHHk1K2j6ij67fdRps2b0/Lw7IDmps1B6AgWomiLg+i1xxe3HdlMp0gRj7bv2A5tNfmhSbdeXdFDujr33J0T1Ccg2ntAL3WIovq+czunzPk9rHJuGA+4ymkZ2NmkUVO4oqtzId/kh3jqRg0ao3uHr+zTmNW5FKKjx0/hSgBOCwvLHxt8q6fTtFXrNhEZBFGRGUynrj241bkAp6mpScPvvuZW5w4cMmLc5JnUw5V7Ac2bm6rPiRobyTmIGhnJKSBDWY6udNglERuorM7lbFD3r6XrvKIzKUT3n7lubWMDiD7NJ4uEKek/pj4riFLVtk+U6lllf9KUhbAsT/Ho3b1TWY0EpcIPNNy+8FL1RsUv5N0lfaCrc+k1NWPPM+JaJ4LbvACyvOgZiVmVDtM+4lEMWohqjOoSohFs5Kd+YhF/TySgAgPElMAJDdciWPqiCmJTvrHKtkswBugii33Korlb4ZX7RCNq322pskO0tmt+dbgFINEWf3NnNLtPlLOv+ZSGnMAuPbuorK4Kq2mfKJrAU6MQF7X1/M2qrxAlUtl5CVImvmJAQf7GUNjw39K9pHSfKHu3gnMC/vEtOfELVQyC6T7Rwhr2iVLxe8j3X2NDda3PEKLvIoSetjbWMplcbmT8Uach65W0ENUY1TFEv1iRAWHPswivaSStbvDBVZ8hqtU7ScMhChXG3C6KdVM5YOHLkhaiGiMtROtMYGfAsyf8Ieg6lRaiGiPNh6iCLLutfSD3S5AWohojLUTrUtwA9UeQFqIaI82HqFZaiGqOtBDVFGkhqjHSQvQLkBaiGiMtRDVFWohqjLQQ/QKkhajGSAtRTZEWohojLUS/AGkhqjGqY4iSzSH5wXTriMoeFXW9weAtd31E5QWrb9asJwrL9o/i7a5BP+l1zXtj3l1aiGqMtBD9AqSFqMaoLiEKggY882rVpqWpqWlcUbhcZpRUTo6HrVH8QxhUFJrlv+fM9n89fwB3f+rw02WPs+q36oPO3jnRuXsnG1vr+NcRwGf7ju0srSx9kh8aGxsnsqfm/kdpIaox0kL0C5AWohqjuoRoTGGoUF8IfAKQkXlBC1b/RZNXh7PHr4dXHgdIjYHPhav/4iAKIpKDarP8iVmW/84TTvRMdlJFLTMMVVxx+KgJIziH9IKeC8g3Q3V+u5wlUU6t62nJmX+Vh0VwxrRcvT9sn0kGNK7kaXG4RCx5ziTio0iuiDEQGnB5vx32rGvzU+va2n17aSGqMdJC9AuQFqIao7qDaG6gX8ojob7IP80LCkjz8k70oIwMePYEzHiS4LF2x6rA9CdcfAkDepFQEnXG7fia7St3n9rGnihLIHry5pGo/OC121fe8rumPmYLws1fOc8nyZMSGpj0T3uMC4e96+6G3qKHHxGzbP/r3pfh+X74bXpSYASbc5teBL/wwTUHci7XN55l29HN+87vSqg8vBdCz9HPDbvXOHtdVEEyurFxz9rNBzZy9vBpbGyCC3wUUblBQj1h8AtfXMPz06IIPR29GkPwd5IWohojLUS/AGkhqjH6WBANzvAV6AkRhEWymbHJKbVsTGZubo7wEVEd3iJsxV2QUiwSA4EpiriYgpBTt45SiFrbWN8JvpFUHjNk5C/GRsYqQ7vJFbEigQE9ipba29rZXH10HuVjJo+Gw8TSKFCzXYefDl7aCyeL1s4XCQ0QK5N8ZNbWMEPgKDOUmRibPIy5G/EyYOT44SSgzPY7fGUfruE5piDUzMwM4ERvAWmEj0s2LEQn+T0By1dvXf7bpFFoDpZymfzCvdMRKhDNqwbRSDazmxaiWnHSQvQLkBaiGqO6gyg71AlwAkUQTZnJQfR2oAsd7dx5YqupiSmwF1WZ3SWhNAqIfcbEh7FjuWQIl4XitHlTacozkolFX6jSFswMhAYURdQeAAtjA0Q0KhVL91/YDZBLxBJqAyiCiOzR8P6z/5nhk/QQhTpNdWctnLFg1V/og7GxcVJZNGQolcWXRKLpoBc+rv7OCDFpQjRTU1Pu+HhOgLFEIqXJw6EJ08ZZWFqEZ5M8M4Bo/OtIPBH4KtAVROeH0PgVjzNv2Zybvle5Q+rfT1qIaoy0EP0CpIWoxqguIQo+AaL0GjEfB9Fe/XpyS1KvPDxvIBKDSRxEgZYhowajECgdMW5YXFEYf040gk2ZAkuVEV1ErqhCr6k92EztI/OCuvTojPh1xwknxJp0ahO3Zi6YhugWF+G1ZOoG5tUzh/fs2500kek3YvxwfgeUTWf6cSyHbge4iASiMDYLDSBKolg2Pxogiri2srd+63auRryrOuf6jtJCVGOkhegXIC1ENUb1D6K0HEHbpgMbTUxMpBJpcIbPv0JUPRKVyeShLJZg2ean1v//9s7EO6oqz+N/xsw4jr3N6Zmjoza7CMqWRRYhgg1uyBIBaWgWEfQgNrSoqGwu2A2CLAZ0FFsUZUBkEwRBGgSUCEJkl0UkhH1J6s0n90ddb+6rqlQqlZCE3+fck/Pqvrvfd3/f+3vvVaVHv+4zF0wrrct4wNtPfN37Tz0bNGxQ6hpe3onbuvq7zz7d/DEKd/111+OMNmnaGA+Ss2TBLT4Y7JZAArmd+2DuA24DbCD9jugj2A8+f/eG639FjQlEtNQT/cvQxf9UT1TDlaAieg0EFdE6E2qkiIpYbvtp48YDa3/1H7/moFwRPRB6Joouyv1Sezt3W9nbuTff/D/9hvaV7LTt0aF991z8jrOZbTPubHXH6JeeIn5f8ff/+bv/PBDZfaWiE6WPMBOI6P6SXb9zbuc+MrC33M5NIKLfyTNRo7u43YeCAvc1peSDimidCSqi10BQEa0zoYpF9Lp//Xc5RkT/7V+uExG9q0O2FdEFa977j+tvEBG97l+v4+yBYPdNN9004PFHhz09+De/+s3QUYMRxSl5k+1/2EZESel7osc3PTn28Q1715S+DWRE9NY/3PrbX/92zMSnf/ub3+UO6CVp5q+Y99//9d+jJ4xC6rLbZ9GqfPM+bYNGDYjJP1n6BZjl2xb/+obfyKl84xPfcP0N9z7QZeTzT7TKaPn+yv/91nzT5v5e97kNkLDd/OdRtgXDRg999LG+lCkv6CKieMZWRK/7l+usiCLn//5v14u0vzxzAjK/91IqXxtVEa0zodIi+uM632RrqGkhWRH91DfZGmpaKPrAn7VY7Dx5xeJXNNhvj5jjtSIVm39cbyMRJJuGBPlGh9YVrHrtrUkvz5rw9eErKUvf5XEeGUpKLxSc337llVp5Jnrjjd8c/+f4aeOWf7PY+4rL8689s3L7p/YrLoStxza6Td3kfNEl3+wApr37OkUtWP2ezfX14Q02gRtowIZ9a176+/MTZ7zofsWFMhFpOXbbT7FNo98Txed2v2NToZCkiOYf8U22hpoWKi2i50/4JltDTQs/fePPWkwuH/NNtoaaFs5t8GctFqcvFYWtdk0L35b+YlEzdE5EFHdWPNeaHHBb0/WLRfvOFPjTFovTF0rCVltDjQp7fr7sT1tZyhPRSEmwf6VvtTXUqHD+Z3/WYhIpDoo+9K22hhoVLh/1Zy0WkUjJd4WpuEfVHHaY3879xvxMYINGDWq+iOan77dz2ej40xaLSCT4NmS1NdSowEbHn7aylCuikaBwt2+1NdSokCyR4Px232prqFEhOSJB5JsTG8OGuyaH1F7PqaWBLY4/Z3GIBMHXB32rraFGBX/OQpQnokLYcGuoOSGS+I59WU594htuDTUnlBrVpNh/5oew7dZQQ8LZy6cjSU/lvp8vhw23hhoSzl4s37wmIaIUsvcz33BrqAlh/6qgpJz79WWJBEXv+YZbQ40IHwWR8ve8Ltt+jv0qjYarG74t3ORPVXlsOuDbbg01IWxNwg0NkhJR4cAq34JruLrh4JrSx5wVJlJqr30LruGqhqJ/pDSVwfbCa+geaa0I35zYWBIp5xFaTLaFLLiGqxu+PnippFwn1JC0iMKBz307ruFqhYNfJPtSbkxOLfTtuIarFhYlfxc3TL7qaI0J5lFoilN5+kKJ6mjNCd8eTsoHFSoiooDh1pd1r3JYU6qglefchlLz7Rt0DdUZPglO/58/LxVn/5mCWvGybh0OjP93J7f6E1Nx9v58+Vv9+YWrHSqkoEGFRVRQl/SqhINrgv0rgmPJvvhXPhd26K3dqxQWlf6uwtm1/oykyrHzP24v3KxSelXCtyf+uff09/6UpMqRU8W4pPq9l6sSthws/wstYVISUSi+FBxaV6qm+5ZrqI6Agp78wZ+FymJuPUUumB8zWlj6ZE5DNQQc0Av5/lRUDnkX9Pj5IztPfoOafnNio4ZqCOxaTl9O6vugySO3g4+dLs4/UvpYTkM1BLSTXcupisunkKqIXiFS+u6uhmoIVU5EQ3WFqiZ89WiokuAPfLoJXzoaqihUhkqKqKIoiqJcu6iIKoqiKEqKqIgqiqIoSoqoiCqKoihKiqiIKoqiKEqKqIgqiqIoSoqoiCqKoihKiqiIKoqiKEqKqIgqiqIoSoqoiCqKoihKiqiIKoqiKEqKqIjWKSKGcKQXU3MoLk7ln1EriqLUEFRE6xRnz549c+aMG4NKEenG1CiWLl3avXv3e++91z9RlXTp0sWPqvGUlJR89dVXbdq0uVrbjtatW1+4cCHtGzJmPycnx49NmtzcXD9KUaoXFdE6RYcOHTIzMzds2CAfsbzNmjW76667zp8/75q/eKbQSxNOFjNSiBefgOnTp2dkZHiRXhXxik0mjYubpm3bts6ZUmKWkHJkx44d3Y8CaUaNGsWGxkscs0BLw4YN5YCp/PLLL2+77TZENF6WePGWmAliRgah+CZNmiQWUQTejwoV4kF3/Kj4SFFeLQ888IB71iOZyJiTZYkY/NjySCGLUntREa1T3H333W+++SaOnV3GiGi/fv2siGKL+Xvu3Dl77EKywJgATmGsw0bz4sWLksbFLbNC/PWvf/3jH//oRVKpW4Ucu02VJrnVlVs1WWi5/RgW0XCnwpFuvd6weCk7d+7sfrSMHTvWjzJD6kc5NG7cWA6siHJ8+fLlMomiMHRBrGm1UJfbcjmWGxVeLj56PS1XRLOysvyo8qbG9i4ZZJC9WqyIemOSYLK8JsWbLIERk1FNEltvgoFS6hgqonUKRDSIbvCxg1u2bFm3bt19990nIkoMfmqrVq1mz549dOjQO+64Q3I98cQTPXv2zM3NnTNnDglwEFu0aDFjxozHHnusZcuWkqawsPD2229/7rnnpkyZ0rp169WrV4vZJX27du0oYdasWXxs3ry5pEeDqZoqYtp0IteuXYuLTHas2KJFi4ihDbfccgttGD9+PK2luk6dOlEdjaFYKYc9AXUROW7cOPLu2bOHUzNnzqRJ+fn5Xl2infR34MCBr7/+enZ2tsRbEZVO2VqkU7t27eJ4wIABFDtixAixhthoLD5NZegYzyFDhkh8OKXtFH+vtMPw0ksvMVD3GDhFgdRO2xjS3r17y5C66SmNonC8KEpudyOiVMcIiAffqFEjm5he9O/ff9q0aaQPjzkfmYs777wTFWfcbr755sCU/9BDD9F3Jk5G2KanEOkUB7anVkRXrlzpeZCUTyNpUmfD/fffz+zPnz+fi2fq1Kn0grzhvQIppXfMy5kzZ+iXxFMFAzJ8+HCpl3iuiokTJ7766qtdunSxtZw4cSIwd4M5O2nSJPpCB6UE2hOeLMCtpwQuMMacXgTxJ4vE7C169erFUL/22mt05PPPP5dTDHVgLm8GjVmTYzq7efNmDhhGclEv02HXzuOPP86kyzFpmHTGVj4qdQAV0ToFIooFwVaKGcWcBWa3bj1RWfZYw0uXLmF0PvnkE6w5i1wElRWO1WOzv3z5cnn2hgkjJaUhPBjcYsNTTz0lpgSwFCtWrCgxnqvUaC04jSGlHMdk1KhR7tNQ2iPl09SDBw9SXRB988jaRw5GjhxJJM2mqU2bNg2MwgFm1BZl6dix47Zt2yJmA2EjRUSJlE4F0VqkU7QKO8hZiZSUtJMtRRD19qhXXB8vpWAtpsfo0aNdt4baDx8+LHllSL1yAiNdclBiPFGx9ZKMNtA14lEFdiS0R4TKjpWLDBSJ5TIARhhrHjgj/M4775Bg8uTJbDikU1u3brVKQEvEh0NBjx49KpEuno9oxYa/KF/Xrl3ds4LtHdenPabqHj16MNrSVK5MuSrkrFeLvW7tKXKxO4k5WfZqsYMQxJ8sSXPRkJeXx8KRS8g2AEnu06ePHHfr1i2arxRZX+TatGkTudgiMGj2CqzQTWyl5qMiWqdAt2QTzfaZj/Xr1+fvgw8+iJFiDe/bt2/QoEF5hrfeeotNutgaRBQtEauBP2cXObYJd6egoAC7QyQWwcaz4y4qKgrKPqOiClxDXC4OJEvY/3BBOVwRbd++vRzQkhdeeEEMkMSgVVRHPHbw5MmTgamLpkpdkgY/Tw5cSO9aTMGKqHTKliCdYnAw+va5cmDqwsSj2XPnzuUsooX8fPHFF4GRBzelENMuU91f/vIX95kotdtjGdJfUkfxRBQHy8oJVeMABaY7cw0ys0yrzS4ZmUE2Q944MMKU4I6wNBvnzKYhi71dQdU4f9IAm8vFlbfdu3cjolIj6dmrMREJtggJRNRu1wRPRGUPJDz55JOoF7XgtoYni9LwHYlxcpcSc7IC04xTp059/PHHrBRcfBZCsdnePfvss4h0YF5PW7BggVzhtvFALrYjkotlKL1mjrhWAyPh+Nk2sVIHUBGtU4iIAvI5bNiwp59+OoiKKIt55cqVGBcW+dko8pxp+PDheKtis3bt2mXvE4qI7tixI2JurortEBCAnTt3BqEXPQJjbcmIC2gd4nh4Imqfb8GQIUOoTpoklovqRMzskz+aip2ypjn8pFOa7UUGTkrplK1FOiUfP/roI+TESggp8RpxKezQ2YdwXsogjl2OlBXRcNtiOiieiMqLRRKDnGCsA3MzwLZKsNkDM4mrVq2iHE/DGGHmyB1hkU+5V2Gxmsq0zpw5M6abK7jytmbNGlujbHfcHYMlGRF19SkIiaj7YtGoUaPEVx44cGC8yVq/fj3ix8hzVcvFGXOyOPXqq6/m5ubScvZVeO10X9qDi0n5XHvbt2/nI3NKmXIXgVysF3LhqVM7udipSC60Vh4AJ36PSamNqIjWKUREWczZ2dnYO/QyiIoo8cePH+/atWuJuadnCZIQUQwHnsSSJUskHl8QzSAyCIkohWMmJk2a5PpMQei9DyGeiBabu8pUJyXQMCydVFchEQ2id/A8JCUZpVO2FumU2FaJXLRo0ZQpU6T7b7/9ttwJjJS9OeymlOOYdplco0ePPut4otZL5q8MaZkMhmRElEnHZLvTarMHpnA8SPdBqSRghOVOqcTQ5u7duwfRJwI2u1X6JuZ27j/+8Y94XxCyj5yBKw3HWiqiilmzZvHRvR4E2ztG2O4hqL1du3ZDhw6V7J6IurUEsURU7vPHmyw5RtLsbY+YkxVELxIZ1dWrV1vHOjD3kF955RU5ZgfDZfzwww/LR1k7EXMznFzjxo2zuUQ+K/QulVIrUBGtU1jfwuWhhx6yLxaxhjG+2Dg2y08++eSGDRuIHDFiBEIrGVEmu84xBBzLnh3fIiMjg2P2+Ajnc889J+nD31EpNncmx48f7xqvm266yUlyBayP+3YubXBOlpaMN0B1CC2WVKrD1MYT0fDtXNJ89913LVq0wAU/cuTIiy++KPE2pXTK1kKnyIIb9MYbb+zfv7+goIDxxOEgcvfu3ZjLPn364Jfs3btXhATTH04ZmJZPnDhx+vTp0YaUQjtRwc6dO8+ZM4dTfKR2RpIhXbhwoQypm15o1qwZRc2dO5fuk929KYqciIgG5vWuyZMns2fatm0b0/pLfgOtwpp36NABvwpX2woPhdN3eiQjLJHyKtby5cuJp8v2lq+MPM3gVFjviR88eDDKl5eXh4CRZdCgQb169frpp5/Gjh0r3fSyBGWdb+rC6z19+vT777/PKFlP1E3j1iJOp71mIlERlVzhyQqM18gIHDt2jF3jmDFj7AUcnixOkWbYsGFsbrZs2dKpUyfrSdM1jrmoAjOnDAW927Nnj+RiSMlVWFg4YcIEcrkiSmKmjHVha1HqBiqidYpu3brZRWt55JFH7ItFgHFp2LAhRhOjU2we83CQm5srCdAD+y4JZzn+/vvvSwxYT4w4e+2//e1vtnB5H9hDHGI3RoyOxzPPPCPej+B9cZ7qME9UhzGytyjlK/+BsWU0debMmVZUYnpIJBs5ciROOYavX79+EmlTSqdsLRI5e/ZsVJbxwfno3bu3NZ2HDh3Kyclp0KCBvB8rkeGU/J0/fz4bF++FTwELi2Jxqtjc/evZsydDyuC4Q2qJmLeLKUr8de/HFmgMeiPHS5cuZW9E25gvZtOW4IJ2MggMBfbdzg4F1q9fX0bYth/TTzLi+/fvb7PbH1uQ3YD7MNLCpSVv50pRyDZXGp11Hzy72FvHpMdxxPljIvDq+vbty6xJId7t5SBai7yda68ZEqPWVkTDkxWYeecj+0Lb+MSTxWaCEvhLx/lrx4edH6MtE4HYu/tIFJeUXBIMHbkmTZpkhzowbr37UakbqIjWKWIu0XBkscF+jBjcjzGPg1DGIJQAFi9ejDBYo0n6efPmlU3yCwnqCoxKiczbmHAaS4JT4f46J2PXEu5pzPhwjI2P1x73lGSPKTAWL70bb4+DaC8SFBWzrnDfhXCnvDThLBLptTZco0u4TGmMV4ibRmISnLVIaW4vbIyXyy3QxR1SN4HXAC+v5HJjBNbFlClTEoyGUktREVXSCdv85s2bf/DBB/4JRblWKSgoqFevXsy3r5U6gIqokk7kvmvMfb2iXJvgfXqvTCtpIWLeyJMD/1w1oiKqKIqi1D4i5jvx2dnZzZo1W79+fWD2K36iqkdFVFEURal9iIhmZmZmZGRkZWXdcccdSGnMb9NVKSqiiqIoSu3DFVFL48aN58yZI2f9DFWDiqiiKIpS+4gpopCdnZ2TkyM/NVMNqIgqiqIotY94Iipkmv9YVQ1eqYqooiiKUvtILKICXmnjxo2r1CtVEVUURVFqH8mIqIBLmpOTE0R/6Tq9qIgqiqIotY/kRVQQr3TWrFnp/SZMdYjoZUVRFEVJN6dOnUpeRIW2bdvK/1FOl5RWh4jWq1evkaIoiqKkFTxLXySTw36v1JerilMdItqqVSu/B4qiKIpyVUFKW7RoUVRUVJnXd1VEFUVRlGsOFLRZs2Zya7cyVIeIzp49e46iKIqipJUZM2b42pgEci83SNP3R6tDRP1nwYqiKIpSaSr6YpH8AkNaHoVaqkNEFUVRFCW9VOgrLlX3W4AqooqiKErtI0kRJUGV/iq9iqiiKIpS+yhXRK33WRU/VGRREVUURVFqHwlEVH6cqOq8TxcVUUVRFKX2EVNE3X/eUqUOqEVFVFEURal9eCIq3/ssKiry01UxKqKKoihK7cMVUfuzCVV98zaMiqiiKIpS+xARlZ/ArX7ttKiIKoqiKLUPhPPMmTNB+v4fS2qoiCqKoihKiqiIKoqiKEqKqIimjeLi4suXL/uxVUwkEnHrld+TLJtEUZR0EjF4kcVRvPg6hvQx5u3TxCNQh01TmkWUwd24cWNeXp73Q/t+uroFK+rSpUuNGze+8cYbw6ur6mC0ly1bRr1/+MMfAtOM/zH46RRFSQcsscLCwj59+uTk5AwaNGjWrFlWM3r16tWkSZO+ffuWzVHXoON087HHHgsbugQjULdNU5pFlEtq2rRp7dq1y87OviuK/NOZFHjkkUeYlcoPfVoKSYCIaGZm5u233x6+tqoORPTzzz+n3pYtWwamGc0NfrrkoLQVK1Ygybfeeqt/TlGueVhfU6dObdWqVVZWljVuY8aMkSX/5z//mfjK/3PKlBFryV//RFrp3r073Xz66afDhi7BCJC4pcE/UfVUw7CkX0T//ve/o6C33Xbb2SjyApVw8eJFYmK6/OgQp1yX//HHH5fvzzqprnwN6KLBjRekkAsXLriR4ULCkIWMUmb4+hDiNTsw7SlXRM+dO+c1TJB7I+4pKdMjPHTliqiUfP78eTmwN2FsjbbLwqZNmyitRYsWNkZRFOHEiROtW7fGmPz8888Sg1eKuUsgoqxWlpgbkzxSLEbDM3QSj4ngVNha8veXpCHIy6ono3/CgbPhG7bYEGoke5IiSptj2joXyoxpw6XkeONmbRrYj0HlhqWSVJWIIv5yE1yghwcOHMAl5SrMyMi48847mzZt6mZEdFEC0QORgQkTJnAsP+PUqFEjEgRmyI4dO8ZxKwMHEYMU0qZNGymEWijk448/phDSuIVMmjTJrRdefPFF2kNekpEdCfnxxx8DU9ctt9yCZ8bfe++9l8aTrG3btpKLSgcPHow2S4OZ0XgiSgyFk5LyaRjl0DAGatGiRYwS5a9cuVK6Lx0XGSP9yJEjpXfe0OXk5EjJiUWUj8uWLaNkaicX8Tt27JBTBQUFNFUKZBjr16/PHDUzyG9/MFYNGjQ4evSopFcUJT8/n6WERZaPrD53sYdFtGvXrqw7Vhm2jmPJsnv3bnn+IrthDm6++WaOKWrYsGEYBP5Ksc8++6ysR1Zou3btbF0zZ84UcyH2CusUONaSvyze3//+97YZAlVbQwdYgxEjRtizYug2btxIA6iOZGvXrrU1YuiMG9kS49mzZ8/EIkqxnJX01shHQrdzSSxp6GOXLl2oXW4Rw5EjR6QZ2CjsKm3joy3H2jTphbVpqQ1LWqgqEcXo22ei8+bNo/OHDh3q1q3bK6+88tprryESGeZXmiRX586dUYLevXvPnj2bwRVPKKaIFhUVMbIMHyNOSjH3gRlcCqFAKWT8+PEUsmTJkmRElJj27dtPnTp1+vTpFCJllhi4mCQvpTHNHN91110vv/yyZERQM8wvHYuMcRwWUT6eOnWKhlHUlClTaFjHjh1pGAP12WefEV8qWaZGqeiee+6hLi4aiZcSvKHLMgQJRZRTCxYsyDL/wJ1BuPvuuzkmb8S8iERfyDV69GiuPK54FVFFKRcWjhgElnmPHj3kHzvb9e6JKEuMj6RkvWcYW0eMuE1YDLvTZcVxCoPAMXLLqty1axcVPfzww5gaFuyMGTMoWcyX1IW6iLV84403OFWvXr0gCbWgagxdv379MHRjx47FLGC+Jk6cKE2SfomVk3JEt6hx8uTJ1tCRS/qSQEQxziTjINP8kBDWWHYb7v5+3LhxrvEUm2PLFEvLyDB00hgxd+DatJdeesnatCDVYUkLVSWiGWYDJXA1uAnw00+fPi17DbmxQA8ZesRp7969NiVDzw6IYWLoMfGycWP4GCl2SSgThbzwwgt85IKLmHvuVCqF2AmmEDK6hchF4yKJ5T7wmTNnuJRpv+S111ZgblDI7JKAU6wWmd1i83LsF198kRFLREm5bt06SblmzRr3rIgo7Q9M4eIXMg6SS8TSJg6coaN5MnQJRJRjuZTZytlcpFy4cCHlkIbjjz76SG5MyZgwAlIaVcv9A7d2RbnGYU2xUtiPiomQRZ2bmyuL2hXRAQMGsI5YyxHD/v37xYWVj6w+sTCzZs3KMPeWUBQsD6vYLvlMA8tWFi8uHR9lSUrJGDoxnmIYrbXkb7zFaw0dde3bt49yrIdHG/iIlykZxdBt3ryZLLKxpgtSESmzyhPRiNmpb9++nYzijLqmKTBmnFP4BmI8xcxKmQMHDrSFwJdffknDZFgi8W1aUIlhqTxVJaLuM1Gg/3SASJmtTLP74FrEc+fU888/Tz/JxSiQhg2IzNCQIUOyjP7Z8q2LJoVkmSf87dq14xSFcC1KIYw1hdgni14hHkw2Z63Xm2H2R4Gz8eRssYGDDLOp4WyHDh0odvjw4YGZ3QsXLmTGuZ0bGJ9VGkzDSCNPF0RE7fUhaeigSBp1ZUVXXbyhSyCiXKBtzA1qyQLZBrZmlMYpxo2PlEN7+vfvH5gLDpnP1GeiipKQ48eP5+XlibqwWNgBs/SsiNq1TAJrDTgmhjXL6mtpHjmhZDk5OazrbPPwa+7cuRywxiW9iLRdvPIS0w8//MAibdCggVhLyiE7jpdrLflr2+lCGgwdFUntYkVdESUvFkk+NjebbHb/hYWF8hjYltOtW7eshCI6aNCgILrhwNwxPmiea5oC43PbMjl1//33Ux1lkqV9+/YydHKWsXXdiXg2DeOc2rCkhaoSUTs9FmLoNt69fGSzI0oQRHcN27Zt49JsYe70fvjhh0RaERUtIQ37Gs5+//33TsFXcAvp0qVLhvELJVIKKSn7DMMid1EOHjxoP7oimmkkqsR4tOIH85FyevXqxTEVyeWye/duqTFmFXDy5MlPP/2U9JlGa4Oynii52Apkmv/ALm22IhqEhk7EL7GIotPuxtZDqsB7ZrKk+927dyfSiqgdcEVRBHmTJTALzS5MzPrOnTtZia6IPvDAA9ZQBOYdGZEu2dbPmzePJTxq1CikgpRLliwhI5t+ErA1lyzZxsf6pe4QGDrcBpYqKV1rOXTo0PDijZifx2Ol0wwxdLhxmSFPFNWUj2Lo+ChuIsfiCNHNTOO6JBBROiKW9qeffmpt3k0J4niiR48eLQ55olKI3O3j4/r166VGyZjApgkVGpZ0Ua0iygUnN2zRj0zz+o+I6IYNGyQNnXz00Ufp81tvvcXgPvPMM1nmqWFRUdFZ87LWgAEDsoz3aYvdsWPH2rVrGXG3kMAIJ4Ik/rsUsnjxYrkUbF7BqmZgXljNMtuZIKGIshiWLVsm+1DJyNUfU0Qj5pmoG0MhNCyooIi6Q5eRhCcamM0vKceMGROtOWAhXTYvebGllRiOpYR77rmHevPz88lCC/fs2eO+U60oCtaDldijR4+CggJWx+DBgzPNvSUx9+7tXNaUqKAstPvuu89VAsS4pXmARZr58+eLnckwN8DefPPNILqQidmyZYut3b5B477RirUkl2stqchaSwsFolgYDXmzBAYOHJhR1hONKaIcY9NIidgH5u19cSITiGirVq3YVfBRHAaxkK5pYrjEoSTlvn37sDlin6VM8mYaRxlXEsspIyNDx0DFs2lBSsOSLtIvoq+//jr9bNiwoRtvjXXbtm0ZF7qH9834iojKrcVMgzu1gdGSO80bbqITTMA777wjz1nluiQeD4/BkjseUggHFCJzKfNHIeQisdRoiZiX4phUGkaCBx98UHZJQXTOWpv3aUVE5Y1W+Qh8lB5RPhccp6g0LKLUSHtkIjmQi4zsS5cupV5ySTLxLxkWEVF8bnkwYJXSDl2GEW8R0VWrVkmTpJCmBlv7n/70J7lzm2lufZAxEn2xyI4VDbvNvOQsWRo1akThlClvbCmKImCmWel3mMdysnxYj4cOHZK1w/6etSa3DYlBaLEGpGzfvr3YNLtzDcxtSeyAbKZBFMVzPOzylMUrBjCIbvrlFBnRKpuluXksRQLXzRDE0JEFM0JFuBwks1ZaDB3eiHwUQ+d+pEYy0pfevXvT+KeeeiosojICTzzxBHnlyZrd0IdN05+dt3O7d++ead5zjBi8t3PlVrPNGNOmBakOS1pIs4gG5lI7W/a7oQJd3bx5c15enriDJLB+4fHjx1GU999/H4VwN19CsXmhxm4iUA52KJ988snbb7+9fPly++CTQr766ispZNGiRZIyXEh47uHw4cPz5s3jug/MftPWJcfxPgI1fvjhh4Gp62ysXgem4yRbuHAhDaZhpJGGIfzhwm0J7ilv6OSUdMQbHPdYYK/HmLz33nssCVv4gQMHVq9e/e67786dOxeFdtMH8WdQURQWL7t2zMWKFSuKzVdTJF7edrG3fGWNL1myBHMkTqRrjmSJ2aXqfbR8/fXXbxuwitbQ7dq1S6wl7kTYWkozwkUJZKTlQdRueNZGtu/hj4CtEEMn5cf8Dqg7Ah988AFOtmtsvVYxGuej3xNtbd6pxL5JjZJLEm/dujUj+pKKRWwatsu1aZUZlkqSfhENzCjE1KoS48/JKTdNxLhHgnup2bNegW56txApX7CJ7VmvEBcpUM66ybxc3scg2iP3rD3l4jbMTZOgcK+0eEPnffROSYzUW+I8Eo44Y5XMgCuKYkmwlr1Vk+QSi5k3cOyGu3hdY1JuyR6SS47dZF6WcAk2Y/iURU7JWbci96wcI2ni5wAekfiUti9jx449efKkHMsrMu4rWkEcm1aZYakkVSKiiqIoihITHNCGDRuKAyoPj+wTX+jUqZM8Cm3Tpk2TJk2q9MeG0oKKqKIoilLdyM+OymtBYd/x3Llzcme4itzHNKIiqiiKoigpoiKqKIqiKCmiIqooiqIoKaIiqiiKoigpoiKqKIqiKCmiIqooiqIoKaIiqiiKoigpoiKqKIqiKCmiIqooiqIoKaIiqiiKoigpoiKqKIqiKCmiIqooiqIoKfL/RQkA7wvDnVkAAAAASUVORK5CYII=> "Computer memory as a kitchen"