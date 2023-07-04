Conditional statements in bash scripting are essential for decision-making and controlling the flow of a script based on various conditions. There are different types of conditional statements available, such as `if`, `else`, `elif`, and `case`. Let's dive into each of them, discussing their syntax, usage, and providing practical examples.

1. `if` statement:
The `if` statement is used to execute a block of code if a condition is true. It has the following syntax:
```bash
if condition; then
  # code to execute if the condition is true
fi
```

Example 1: Simple if statement
```bash
#!/bin/bash

number=10

if [ $number -gt 0 ]; then
  echo "Number is positive"
fi
```
Output:
```
Number is positive
```

2. `if-else` statement:
The `if-else` statement allows you to execute one block of code if a condition is true and another block of code if the condition is false. It has the following syntax:
```bash
if condition; then
  # code to execute if the condition is true
else
  # code to execute if the condition is false
fi
```

Example 2: If-else statement
```bash
#!/bin/bash

number=-5

if [ $number -gt 0 ]; then
  echo "Number is positive"
else
  echo "Number is not positive"
fi
```
Output:
```
Number is not positive
```

3. `elif` statement:
The `elif` statement allows you to check multiple conditions and execute different blocks of code based on those conditions. It has the following syntax:
```bash
if condition1; then
  # code to execute if condition1 is true
elif condition2; then
  # code to execute if condition2 is true
else
  # code to execute if all conditions are false
fi
```

Example 3: Elif statement
```bash
#!/bin/bash

number=0

if [ $number -gt 0 ]; then
  echo "Number is positive"
elif [ $number -lt 0 ]; then
  echo "Number is negative"
else
  echo "Number is zero"
fi
```
Output:
```
Number is zero
```

4. `case` statement:
The `case` statement is useful when you want to perform different actions based on multiple possible values of a variable. It has the following syntax:
```bash
case variable in
  pattern1)
    # code to execute if pattern1 matches the variable
    ;;
  pattern2)
    # code to execute if pattern2 matches the variable
    ;;
  *)
    # code to execute if no patterns match the variable
    ;;
esac
```

Example 4: Case statement
```bash
#!/bin/bash

fruit="apple"

case $fruit in
  "apple")
    echo "It's an apple"
    ;;
  "banana")
    echo "It's a banana"
    ;;
  *)
    echo "It's something else"
    ;;
esac
```
Output:
```
It's an apple
```

5. Logical operators:
Logical operators (AND, OR, NOT) are used to create complex conditional expressions by combining multiple conditions. They have the following syntax:
- AND (`&&`): Executes the next command only if the previous command succeeds.
- OR (`||`): Executes the next command only if the previous command fails.
- NOT (`!`): Inverts the result of a condition.

Example 5: Logical operators
```bash
#!/bin/bash

number=15

if [ $number -gt 

0 ] && [ $number -lt 10 ]; then
  echo "Number is between 0 and 10"
fi
```
Output: (No output because the condition is false)

These examples demonstrate how conditional statements and logical operators allow you to make decisions and control the flow of a script based on various conditions. By utilizing these statements effectively, you can create dynamic and flexible scripts that respond to different scenarios.
