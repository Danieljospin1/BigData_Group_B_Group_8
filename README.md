# Group work from Big Data group 8 in team 8
## Group members:
1.BISUBIZO Daniel Jospin-26695
2. Teta kevin-27973
3. RUTAYISIRE Tevin 27343


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
