Experiment No. 6

Name: Pranav Menon

PRN No.: 25070123085

Batch: ENTC - B1

Aim: To study Conditional Statements in Python and understand decision-making structures, comparison operations, and their practical applications.

THEORY:

1) Introduction to Conditional Statements

Conditional statements in Python allow programs to make decisions and execute different code blocks based on specified conditions. They enable dynamic program behavior by evaluating boolean expressions and controlling the flow of execution. These statements form the foundation of decision-making in programming, allowing code to respond differently based on varying inputs and situations.

Key Characteristics:
• Decision Making – Enables programs to choose between different execution paths
• Boolean Evaluation – Conditions are evaluated to True or False
• Sequential Testing – Conditions are checked in order from top to bottom
• Single Execution – Only the first matching condition's block executes
• Indentation-Based – Code blocks are defined by consistent indentation

2) The if Statement

The if statement is the simplest conditional statement that executes a block of code only when the specified condition evaluates to True. If the condition is False, the code block is skipped entirely and program execution continues with the next statement after the if block.

Syntax:
if condition:
    statement(s)

Example:
num = 10
if num > 0:
    print("Positive number")
Output: Positive number

3) The if-else Statement

The if-else statement provides two alternative execution paths. When the condition is True, the if block executes; when False, the else block executes. This ensures that exactly one of the two blocks will always execute, making it useful for binary decisions.

Syntax:
if condition:
    statement(s)
else:
    statement(s)

Example:
num = 7
if num % 2 == 0:
    print("Even number")
else:
    print("Odd number")
Output: Odd number

4) The if-elif-else Statement

The if-elif-else statement allows testing multiple conditions in sequence. It checks conditions from top to bottom and executes the block corresponding to the first True condition. All remaining conditions are skipped after a match is found. This is useful when you have more than two possible outcomes.

Syntax:
if condition1:
    statement(s)
elif condition2:
    statement(s)
elif condition3:
    statement(s)
else:
    statement(s)

Example:
marks = 85
if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
elif marks >= 60:
    print("Grade C")
else:
    print("Grade D")
Output: Grade B

5) Nested Conditional Statements

Nested if statements occur when one if statement is placed inside another if statement. The inner if statement is evaluated only when the outer if condition is True, creating a hierarchy of conditions. This allows for complex decision-making where one decision depends on another.

Syntax:
if outer_condition:
    if inner_condition:
        statement(s)
    else:
        statement(s)
else:
    statement(s)

Example:
num = 12
if num > 0:
    print("Positive")
    if num % 2 == 0:
        print("Even")
    else:
        print("Odd")
else:
    print("Not positive")
Output: Positive, Even

6) Other Control Flow Statements in Python

a) for Loop
Used to iterate over a sequence (list, tuple, string, range, etc.) or any iterable object. It executes a block of code repeatedly for each element in the sequence, making it ideal when the number of iterations is known.

Syntax:
for variable in sequence:
    statement(s)

Example: for i in range(5): print(i)

b) while Loop
Repeats a block of code as long as the specified condition remains True. It is used when the number of iterations is not known beforehand and depends on a dynamic condition.

Syntax:
while condition:
    statement(s)

Example: while x < 10: print(x); x += 1

Example: while True: x = int(input("Enter positive: ")); if x > 0: break

7) To check whether the given Number is Positive, Negative or Zero

This program classifies a number into three categories using if-elif-else structure. It demonstrates basic conditional logic with comparison operators.

Logic: If num > 0 then positive, else if num < 0 then negative, else zero

Syntax:
num = float(input("Enter the Number : "))
if num > 0:
    print("The Number is Positive .")
elif num < 0:
    print("The Number is Negative .")
else:
    print("The Number is Zero .")

8) To check whether the given Number is Odd or Even

This program determines parity using the modulo operator. A number divisible by 2 (remainder 0) is even, otherwise odd.

Logic: If num % 2 == 0 then even, else odd

Syntax:
num = int(input("Enter the Number : "))
if (num % 2) == 0:
    print("The Number is Even .")
else:
    print("The Number is Odd .")

9) To find the Largest among the three Numbers

This program compares three numbers using logical AND operators. It checks each number against the other two to determine the maximum.

Logic: If a >= b AND a >= c then a is largest, else if b >= a AND b >= c then b is largest, else c is largest

Syntax:
a = int(input("Enter the First Number : "))
b = int(input("Enter the Second Number : "))
c = int(input("Enter the Third Number : "))
if a >= b and a >= c:
    print("The Largest Number is : ", a)
elif b >= a and b >= c:
    print("The Largest Number is : ", b)
else:
    print("The Largest Number is : ", c)

10) To determine the subject mark and Calculate the grade

This program implements a grading system using multiple elif statements to create grade brackets: A(90+), B(75+), C(60+), D(40+), Fail(<40).

Logic: If marks >= 90 then A, elif >= 75 then B, elif >= 60 then C, elif >= 40 then D, else Fail

Syntax:
marks = float(input("Enter the Marks : "))
if marks >= 90:
    print("The Grade is : A")
elif marks >= 75:
    print("The Grade is : B")
elif marks >= 60:
    print("The Grade is : C")
elif marks >= 40:
    print("The Grade is : D")
else:
    print("The Student has failed the Examination")

11) To determine if a year is a leap year or Not

This program validates leap years using the rule: divisible by 400, or divisible by 4 but not 100.

Logic: If year % 400 == 0 OR (year % 4 == 0 AND year % 100 != 0) then leap year, else not leap year

Syntax:
year = int(input("Enter the Year : "))
if (year % 400 == 0) or ((year % 100 != 0) and (year % 4 == 0)):
    print("The Year is a Leap Year")
else:
    print("The Year is not a Leap Year")

12) To calculate the Gross Salary of an employee

This program calculates gross salary by adding HRA and DA to basic salary. Different percentage rates apply to salary brackets.

Logic: Determine bracket, calculate HRA and DA percentages, Gross = Basic + HRA + DA

Syntax:
basic_salary = int(input("Enter the Basic Salary : "))
hra = 0
da = 0
if basic_salary <= 10000:
    hra = 0.02 * basic_salary
    da = 0.08 * basic_salary
elif basic_salary <= 20000:
    hra = 0.025 * basic_salary
    da = 0.09 * basic_salary
else:
    hra = 0.03 * basic_salary
    da = 0.095 * basic_salary
gross_Sal = basic_salary + hra + da

13) To calculate the income tax

This program computes progressive income tax across slabs: 0-250000 (0%), 250001-500000 (5%), 500001-1000000 (20%), >1000000 (30%).

Logic: If income <= 250000 then tax=0, elif <= 500000 then 5% on excess, elif <= 1000000 then cumulative, else progressive taxation

Syntax:
income = int(input("Enter the Income : "))
if income <= 250000:
    tax = 0
elif income <= 500000:
    tax = (income - 250000) * 0.05
elif income <= 1000000:
    tax = (250000 * 0.05) + (income - 500000) * 0.20
else:
    tax = (250000 * 0.05) + (500000 * 0.20) + (income - 1000000) * 0.30

14) To identify if a given character is vowel or consonant

This program classifies characters as vowels or consonants using membership operator.

Logic: If char in vowel list then vowel, else consonant

Syntax:
char = input("Enter the character : ")
vowel_list = ['a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U']
if char in vowel_list:
    print("The Character is a Vowel")
else:
    print("The character is a consonant")

15) To increment a date

This program increments a date by one day, handling month-end, year-end transitions, and leap years.

Logic: Determine max days for month, validate date, increment accordingly

Syntax:
date = input("Enter date in dd/mm/yyyy format: ")
dd, mm, yy = map(int, date.split("/"))
if (mm == 1 or mm == 3 or mm == 5 or mm == 7 or mm == 8 or mm == 10 or mm == 12):
    max1 = 31
elif (mm == 4 or mm == 6 or mm == 9 or mm == 11):
    max1 = 30
elif mm == 2 and (yy % 4 == 0 and yy % 100 != 0 or yy % 400 == 0):
    max1 = 29
elif mm == 2:
    max1 = 28
if (mm < 1 or mm > 12):
    print("Date is invalid")
elif (dd < 1 or dd > max1):
    print("Date is invalid")
elif (dd == max1 and mm != 12):
    dd = 1
    mm = mm + 1
    print("The incremented date is:", dd, "/", mm, "/", yy)
elif (dd == 31 and mm == 12):
    dd = 1
    mm = 1
    yy = yy + 1
    print("The incremented date is:", dd, "/", mm, "/", yy)
else:
    dd = dd + 1
    print("The incremented date is:", dd, "/", mm, "/", yy)

ALGORITHMS:

Algorithm 1: Checking if a Number is Positive, Negative, or Zero

Step 1: Start
   - Begin the process of number classification

Step 2: Accept input from user
   - Command: num = float(input("Enter the Number : "))
   - Function: input() - Built-in function for accepting user input as string
   - Function: float() - Built-in function to convert string to floating-point number
   - Source: Built-in Python functions (no import required)

Step 3: Check if number is greater than zero
   - Command: if num > 0:
   - Function: > - Comparison operator (greater than)
   - Source: Built-in Python operator (no import required)

Step 4: Display positive message if condition is True
   - Command: print("The Number is Positive .")
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 5: Check if number is less than zero
   - Command: elif num < 0:
   - Function: < - Comparison operator (less than)
   - Source: Built-in Python operator (no import required)

Step 6: Display negative message if condition is True
   - Command: print("The Number is Negative .")
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 7: Handle remaining case (number equals zero)
   - Command: else:
   - Function: else - Conditional statement keyword for default case
   - Source: Built-in Python keyword (no import required)

Step 8: Display zero message
   - Command: print("The Number is Zero .")
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 9: Stop
   - End the algorithm

Algorithm 2: Determining if a Number is Even or Odd

Step 1: Start
   - Begin the process of checking parity

Step 2: Accept integer input from user
   - Command: num = int(input("Enter the Number : "))
   - Function: input() - Built-in function for accepting user input
   - Function: int() - Built-in function to convert string to integer
   - Source: Built-in Python functions (no import required)

Step 3: Calculate remainder when divided by 2
   - Command: if (num % 2) == 0:
   - Function: % - Modulo operator (returns remainder of division)
   - Function: == - Equality comparison operator
   - Source: Built-in Python operators (no import required)

Step 4: Display even message if remainder is 0
   - Command: print("The Number is Even .")
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 5: Handle odd case (remainder is not 0)
   - Command: else:
   - Function: else - Conditional statement keyword
   - Source: Built-in Python keyword (no import required)

Step 6: Display odd message
   - Command: print("The Number is Odd .")
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 7: Stop
   - End the algorithm

Algorithm 3: Finding the Largest Among Three Numbers

Step 1: Start
   - Begin the process of finding maximum value

Step 2: Accept first number from user
   - Command: a = int(input("Enter the First Number : "))
   - Function: input() - Built-in function for user input
   - Function: int() - Built-in function for type conversion
   - Source: Built-in Python functions (no import required)

Step 3: Accept second number from user
   - Command: b = int(input("Enter the Second Number : "))
   - Function: input() - Built-in function for user input
   - Function: int() - Built-in function for type conversion
   - Source: Built-in Python functions (no import required)

Step 4: Accept third number from user
   - Command: c = int(input("Enter the Third Number : "))
   - Function: input() - Built-in function for user input
   - Function: int() - Built-in function for type conversion
   - Source: Built-in Python functions (no import required)

Step 5: Check if first number is largest
   - Command: if a >= b and a >= c:
   - Function: >= - Greater than or equal to operator
   - Function: and - Logical AND operator
   - Source: Built-in Python operators (no import required)

Step 6: Display first number as largest
   - Command: print("The Largest Number is : ", a)
   - Function: print() - Built-in function for output
   - Source: Built-in Python function (no import required)

Step 7: Check if second number is largest
   - Command: elif b >= a and b >= c:
   - Function: >= - Greater than or equal to operator
   - Function: and - Logical AND operator
   - Source: Built-in Python operators (no import required)

Step 8: Display second number as largest
   - Command: print("The Largest Number is : ", b)
   - Function: print() - Built-in function
   - Source: Built-in Python function (no import required)

Step 9: Handle remaining case (third number is largest)
   - Command: else:
   - Function: else - Default case keyword
   - Source: Built-in Python keyword (no import required)

Step 10: Display third number as largest
   - Command: print("The Largest Number is : ", c)
   - Function: print() - Built-in function
   - Source: Built-in Python function (no import required)

Step 11: Stop
   - End the algorithm

Algorithm 4: Grade Calculation Based on Marks

Step 1: Start
   - Begin the grade assignment process

Step 2: Accept marks from user
   - Command: marks = float(input("Enter the Marks : "))
   - Function: input() - Built-in function for user input
   - Function: float() - Built-in function for decimal conversion
   - Source: Built-in Python functions (no import required)

Step 3: Check if marks are 90 or above
   - Command: if marks >= 90:
   - Function: >= - Greater than or equal to operator
   - Source: Built-in Python operator (no import required)

Step 4: Assign grade A
   - Command: print("The Grade is : A")
   - Function: print() - Built-in output function
   - Source: Built-in Python function (no import required)

Step 5: Check if marks are 75 or above
   - Command: elif marks >= 75:
   - Function: >= - Greater than or equal to operator
   - Source: Built-in Python operator (no import required)

Step 6: Assign grade B
   - Command: print("The Grade is : B")
   - Function: print() - Built-in function
   - Source: Built-in Python function (no import required)

Step 7: Check if marks are 60 or above
   - Command: elif marks >= 60:
   - Function: >= - Greater than or equal to operator
   - Source: Built-in Python operator (no import required)

Step 8: Assign grade C
   - Command: print("The Grade is : C")
   - Function: print() - Built-in function
   - Source: Built-in Python function (no import required)

Step 9: Check if marks are 40 or above
   - Command: elif marks >= 40:
   - Function: >= - Greater than or equal to operator
   - Source: Built-in Python operator (no import required)

Step 10: Assign grade D
   - Command: print("The Grade is : D")
   - Function: print() - Built-in function
   - Source: Built-in Python function (no import required)

Step 11: Handle failing case (marks below 40)
   - Command: else:
   - Function: else - Default case keyword
   - Source: Built-in Python keyword (no import required)

Step 12: Display failure message
   - Command: print("The Student has failed the Examination")
   - Function: print() - Built-in function
   - Source: Built-in Python function (no import required)

Step 13: Stop
   - End the algorithm

Algorithm 5: Leap Year Determination

Step 1: Start
   - Begin leap year validation process

Step 2: Accept year from user
   - Command: year = int(input("Enter the Year : "))
   - Function: input() - Built-in function for user input
   - Function: int() - Built-in function for integer conversion
   - Source: Built-in Python functions (no import required)

Step 3: Check leap year conditions
   - Command: if (year % 400 == 0) or ((year % 100 != 0) and (year % 4 == 0)):
   - Function: % - Modulo operator for remainder calculation
   - Function: == - Equality operator
   - Function: != - Not equal operator
   - Function: or - Logical OR operator
   - Function: and - Logical AND operator
   - Source: Built-in Python operators (no import required)

Step 4: Display leap year message
   - Command: print("The Year is a Leap Year")
   - Function: print() - Built-in output function
   - Source: Built-in Python function (no import required)

Step 5: Handle non-leap year case
   - Command: else:
   - Function: else - Default case keyword
   - Source: Built-in Python keyword (no import required)

Step 6: Display non-leap year message
   - Command: print("The Year is not a Leap Year")
   - Function: print() - Built-in function
   - Source: Built-in Python function (no import required)

Step 7: Stop
   - End the algorithm

Algorithm 6: Gross Salary Calculation

Step 1: Start
   - Begin salary calculation process

Step 2: Accept basic salary from user
   - Command: basic_salary = int(input("Enter the Basic Salary : "))
   - Function: input() - Built-in function for user input
   - Function: int() - Built-in function for integer conversion
   - Source: Built-in Python functions (no import required)

Step 3: Initialize allowance variables
   - Command: hra = 0
   - Command: da = 0
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)

Step 4: Check if basic salary is 10000 or below
   - Command: if basic_salary <= 10000:
   - Function: <= - Less than or equal to operator
   - Source: Built-in Python operator (no import required)

Step 5: Calculate allowances for low salary bracket
   - Command: hra = 0.02 * basic_salary
   - Command: da = 0.08 * basic_salary
   - Function: * - Multiplication operator
   - Source: Built-in Python operator (no import required)

Step 6: Check if basic salary is 20000 or below
   - Command: elif basic_salary <= 20000:
   - Function: <= - Less than or equal to operator
   - Source: Built-in Python operator (no import required)

Step 7: Calculate allowances for medium salary bracket
   - Command: hra = 0.025 * basic_salary
   - Command: da = 0.09 * basic_salary
   - Function: * - Multiplication operator
   - Source: Built-in Python operator (no import required)

Step 8: Handle high salary bracket (above 20000)
   - Command: else:
   - Function: else - Default case keyword
   - Source: Built-in Python keyword (no import required)

Step 9: Calculate allowances for high salary bracket
   - Command: hra = 0.03 * basic_salary
   - Command: da = 0.095 * basic_salary
   - Function: * - Multiplication operator
   - Source: Built-in Python operator (no import required)

Step 10: Calculate gross salary
   - Command: gross_Sal = basic_salary + hra + da
   - Function: + - Addition operator
   - Source: Built-in Python operator (no import required)

Step 11: Display all salary components
   - Command: print(f"The Basic Salary is : {basic_salary}")
   - Command: print(f"The HRA is : {hra}")
   - Command: print(f"The DA is : {da}")
   - Command: print(f"The Gross Salary is : {gross_Sal}")
   - Function: print() - Built-in output function
   - Function: f-strings - Formatted string literals
   - Source: Built-in Python features (no import required)

Step 12: Stop
   - End the algorithm

Algorithm 7: Income Tax Calculation

Step 1: Start
   - Begin tax calculation process

Step 2: Accept income from user
   - Command: income = int(input("Enter the Income : "))
   - Function: input() - Built-in function for user input
   - Function: int() - Built-in function for integer conversion
   - Source: Built-in Python functions (no import required)

Step 3: Check if income is 250000 or below
   - Command: if income <= 250000:
   - Function: <= - Less than or equal to operator
   - Source: Built-in Python operator (no import required)

Step 4: Set tax to zero
   - Command: tax = 0
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)

Step 5: Check if income is 500000 or below
   - Command: elif income <= 500000:
   - Function: <= - Less than or equal to operator
   - Source: Built-in Python operator (no import required)

Step 6: Calculate tax at 5% for income above 250000
   - Command: tax = (income - 250000) * 0.05
   - Function: - - Subtraction operator
   - Function: * - Multiplication operator
   - Source: Built-in Python operators (no import required)

Step 7: Check if income is 1000000 or below
   - Command: elif income <= 1000000:
   - Function: <= - Less than or equal to operator
   - Source: Built-in Python operator (no import required)

Step 8: Calculate tax for middle income bracket
   - Command: tax = (250000 * 0.05) + (income - 500000) * 0.20
   - Function: * - Multiplication operator
   - Function: + - Addition operator
   - Function: - - Subtraction operator
   - Source: Built-in Python operators (no import required)

Step 9: Handle high income bracket
   - Command: else:
   - Function: else - Default case keyword
   - Source: Built-in Python keyword (no import required)

Step 10: Calculate tax for high income bracket
   - Command: tax = (250000 * 0.05) + (500000 * 0.20) + (income - 1000000) * 0.30
   - Function: * - Multiplication operator
   - Function: + - Addition operator
   - Function: - - Subtraction operator
   - Source: Built-in Python operators (no import required)

Step 11: Display calculated tax
   - Command: print(f"The Income Tax is : {tax}")
   - Function: print() - Built-in output function
   - Function: f-string - Formatted string literal
   - Source: Built-in Python features (no import required)

Step 12: Stop
   - End the algorithm

Algorithm 8: Vowel or Consonant Identification (Method 1 - Multiple OR Conditions)
Step 1: Start

Begin character classification process

Step 2: Accept character from user

Command: char = input("Enter the character : ")
Function: input() - Built-in function for user input
Source: Built-in Python function (no import required)

Step 3: Check if character is a vowel using multiple OR conditions

Command: if (char == 'a' or char == 'e' or char == 'i' or char == 'o' or char == 'u' or char == 'A' or char == 'E' or char == 'I' or char == 'O' or char == 'U'):
Function: == - Equality operator
Function: or - Logical OR operator
Source: Built-in Python operators (no import required)

Step 4: Display vowel message

Command: print("The Character is a Vowel")
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 5: Handle consonant case

Command: else:
Function: else - Default case keyword
Source: Built-in Python keyword (no import required)

Step 6: Display consonant message

Command: print("The character is a consonant")
Function: print() - Built-in function
Source: Built-in Python function (no import required)

Step 7: Stop

End the algorithm

Algorithm 8A: Vowel or Consonant Identification (Method 2 - Membership Operator)
Step 1: Start

Begin improved character classification process

Step 2: Accept character from user

Command: char = input("Enter the character : ")
Function: input() - Built-in function for user input
Source: Built-in Python function (no import required)

Step 3: Create list of vowels

Command: vowel_list = ['a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U']
Function: List creation using square brackets []
Source: Built-in Python list data structure (no import required)

Step 4: Check if character is in vowel list

Command: if char in vowel_list:
Function: in - Membership operator
Source: Built-in Python operator (no import required)

Step 5: Display vowel message

Command: print("The Character is a Vowel")
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 6: Handle consonant case

Command: else:
Function: else - Default case keyword
Source: Built-in Python keyword (no import required)

Step 7: Display consonant message

Command: print("The character is a consonant")
Function: print() - Built-in function
Source: Built-in Python function (no import required)

Step 8: Stop

End the algorithm

Algorithm 8B: Vowel or Consonant Identification (Method 3 - Set Operations with Validation)
Step 1: Start

Begin advanced character classification with validation

Step 2: Import string module

Command: import string
Function: string - Module containing string constants like ascii_lowercase, ascii_uppercase
Source: Python standard library module

Step 3: Accept character from user

Command: char = input("Enter the character : ")
Function: input() - Built-in function for user input
Source: Built-in Python function (no import required)

Step 4: Create vowel list

Command: vowel_list = ['a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U']
Function: List creation
Source: Built-in Python data structure (no import required)

Step 5: Convert list to set

Command: vowel_set = set(vowel_list)
Function: set() - Built-in constructor to create set from iterable
Source: Built-in Python function (no import required)

Step 6: Create set of lowercase letters

Command: lower = set(string.ascii_lowercase)
Function: set() - Built-in constructor
Function: string.ascii_lowercase - Constant containing 'abcdefghijklmnopqrstuvwxyz'
Source: Built-in function with string module

Step 7: Create set of uppercase letters

Command: upper = set(string.ascii_uppercase)
Function: set() - Built-in constructor
Function: string.ascii_uppercase - Constant containing 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
Source: Built-in function with string module

Step 8: Calculate consonants using set difference

Command: consonant_lower = lower - vowel_set
Command: consonant_upper = upper - vowel_set
Function: - - Set difference operator (elements in first set but not in second)
Source: Built-in Python operator (no import required)

Step 9: Check if character is a vowel

Command: if char in vowel_set:
Function: in - Membership operator
Source: Built-in Python operator (no import required)

Step 10: Display vowel message

Command: print("The Character is a Vowel")
Function: print() - Built-in function
Source: Built-in Python function (no import required)

Step 11: Check if character is a consonant

Command: elif char in consonant_lower or char in consonant_upper:
Function: in - Membership operator
Function: or - Logical OR operator
Source: Built-in Python operators (no import required)

Step 12: Display consonant message

Command: print("The character is a consonant")
Function: print() - Built-in function
Source: Built-in Python function (no import required)

Step 13: Handle invalid input

Command: else:
Function: else - Default case for error handling
Source: Built-in Python keyword (no import required)

Step 14: Display error message

Command: print("Error! Please try again")
Function: print() - Built-in function
Source: Built-in Python function (no import required)

Step 15: Stop

End the algorithm

Algorithm 9: Date Increment

Step 1: Start
   - Begin date increment process

Step 2: Accept date input from user
   - Command: date = input("Enter date in dd/mm/yyyy format: ")
   - Function: input() - Built-in function for user input
   - Source: Built-in Python function (no import required)

Step 3: Parse date string into components
   - Command: dd, mm, yy = map(int, date.split("/"))
   - Function: split("/") - String method that splits by delimiter
   - Function: map(int, ...) - Applies int() to each element
   - Source: Built-in Python functions (no import required)

Step 4: Determine maximum days for months with 31 days
   - Command: if (mm == 1 or mm == 3 or mm == 5 or mm == 7 or mm == 8 or mm == 10 or mm == 12):
   - Command: max1 = 31
   - Function: == - Equality operator
   - Function: or - Logical OR operator
   - Source: Built-in Python operators (no import required)

Step 5: Determine maximum days for months with 30 days
   - Command: elif (mm == 4 or mm == 6 or mm == 9 or mm == 11):
   - Command: max1 = 30
   - Function: == - Equality operator
   - Function: or - Logical OR operator
   - Source: Built-in Python operators (no import required)

Step 6: Check for February in leap year
   - Command: elif mm == 2 and (yy % 4 == 0 and yy % 100 != 0 or yy % 400 == 0):
   - Command: max1 = 29
   - Function: % - Modulo operator
   - Function: ==, != - Comparison operators
   - Function: and, or - Logical operators
   - Source: Built-in Python operators (no import required)

Step 7: Handle February in non-leap year
   - Command: elif mm == 2:
   - Command: max1 = 28
   - Function: == - Equality operator
   - Source: Built-in Python operator (no import required)

Step 8: Validate month range
   - Command: if (mm < 1 or mm > 12):
   - Command: print("Date is invalid")
   - Function: <, > - Comparison operators
   - Function: or - Logical OR operator
   - Function: print() - Output function
   - Source: Built-in Python operators and function (no import required)

Step 9: Validate day range
   - Command: elif (dd < 1 or dd > max1):
   - Command: print("Date is invalid")
   - Function: <, > - Comparison operators
   - Function: or - Logical OR operator
   - Function: print() - Output function
   - Source: Built-in Python operators and function (no import required)

Step 10: Handle month-end (not December)
   - Command: elif (dd == max1 and mm != 12):
   - Command: dd = 1
   - Command: mm = mm + 1
   - Command: print("The incremented date is:", dd, "/", mm, "/", yy)
   - Function: ==, != - Comparison operators
   - Function: and - Logical AND operator
   - Function: + - Addition operator
   - Function: print() - Output function
   - Source: Built-in Python operators and function (no import required)

Step 11: Handle year-end (December 31)
   - Command: elif (dd == 31 and mm == 12):
   - Command: dd = 1
   - Command: mm = 1
   - Command: yy = yy + 1
   - Command: print("The incremented date is:", dd, "/", mm, "/", yy)
   - Function: == - Equality operator
   - Function: and - Logical AND operator
   - Function: + - Addition operator
   - Function: print() - Output function
   - Source: Built-in Python operators and function (no import required)

Step 12: Handle normal date increment
   - Command: else:
   - Command: dd = dd + 1
   - Command: print("The incremented date is:", dd, "/", mm, "/", yy)
   - Function: else - Default case keyword
   - Function: + - Addition operator
   - Function: print() - Output function
   - Source: Built-in Python keyword, operator, and function (no import required)

Step 13: Stop
   - End the algorithm

CONCLUSION

The study of conditional statements in Python was completed successfully.
