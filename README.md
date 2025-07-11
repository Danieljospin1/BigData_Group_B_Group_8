# Group work from Big Data group 8 in team 8
## Group members:
1. BISUBIZO Daniel Jospin-26695
2. Teta kevin-27973
3. RUTAYISIRE Tevin 27343
4. Ezeugo-Ugonu Solomon-25862
5. kayonga calvin 27753

---

## Question I: Student Management System Function

### Problem Statement:

Create a system that:
- Inputs student info (name, age, and marks of 2–3 courses)
- Calculates the average grade
- Displays student data and average
- Uses **separate functions** for input, processing, and output

### Python Solution:

```python
def input_student_info():
    name = input("Enter student name: ")
    age = int(input("Enter student age: "))
    marks = []
    num_courses = int(input("Enter number of courses (2 or 3): "))
    
    for i in range(num_courses):
        mark = float(input(f"Enter mark for course {i+1}: "))
        marks.append(mark)
    
    return name, age, marks

def calculate_average(marks):
    return sum(marks) / len(marks)

def display_student_info(name, age, average):
    print("\n--- Student Report ---")
    print(f"Name: {name}")
    print(f"Age: {age}")
    print(f"Average Grade: {average:.2f}")


def student_management_system():
    name, age, marks = input_student_info()
    average = calculate_average(marks)
    display_student_info(name, age, average)

student_management_system()
```
## Question II: Palindrome Checker
### Problem Statement:
Write a function that:

1. Asks the user to input a string

2. Checks if it's a palindrome (reads the same backward and forward)

3. Prints a message accordingly

### Python solution:
``` python
def is_palindrome(text):
    return text == text[::-1]

def check_palindrome():
    user_input = input("Enter a string to check if it's a palindrome: ")
    cleaned = user_input.replace(" ", "").lower()
    if is_palindrome(cleaned):
        print("Yes, it is a palindrome")
    else:
        print("No, it is not a palindrome")

check_palindrome()
