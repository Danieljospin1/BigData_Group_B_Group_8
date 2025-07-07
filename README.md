# Group work from Big Data group 8 in team 8
## Group members:
1.BISUBIZO Daniel Jospin-26695
2. Teta kevin-27973
3. RUTAYISIRE Tevin 27343
4. Ezeugo-Ugonu Solomon .O 25862


---

# ----------------------------------------------
# Question I: Student Management System Function
# ----------------------------------------------

def student_management_system():
    students = []
    num_students = int(input("Enter the number of students: "))

    for i in range(num_students):
        name = input(f"Enter student {i + 1} name: ")
        num_courses = int(input(f"Enter number of courses for {name}: "))
        grades = []

        for j in range(num_courses):
            grade = float(input(f"Enter grade for course {j + 1}: "))
            grades.append(grade)

        average = sum(grades) / len(grades)
        students.append((name, average))

    print("\n--- Student Results ---")
    for student in students:
        print(f"Student: {student[0]} - Average Grade: {student[1]:.2f}")

# Sample Output:
# Enter the number of students: 2
# Enter student 1 name: Alice
# Enter number of courses for Alice: 3
# Enter grade for course 1: 75
# Enter grade for course 2: 85
# Enter grade for course 3: 80
# Enter student 2 name: Bob
# Enter number of courses for Bob: 2
# Enter grade for course 1: 60
# Enter grade for course 2: 70
# --- Student Results ---
# Student: Alice - Average Grade: 80.00
# Student: Bob - Average Grade: 65.00

# -------------------------------
# Question II: Check Palindrome
# -------------------------------

def check_palindrome():
    text = input("Enter a string: ")
    if text == text[::-1]:
        print("Yes, it is a palindrome")
    else:
        print("No, it is not a palindrome")

# Sample Output:
# Enter a string: madam
# Yes, it is a palindrome

# Enter a string: hello
# No, it is not a palindrome

# ----------------------------------------
# Question III: Iterating Over Two Inputs
# ----------------------------------------

def iterate_two_inputs():
    text1 = input("Enter first text: ")
    text2 = input("Enter second text: ")

    combined = text1 + text2
    characters = [char for char in combined]

    print("\nCombined Characters:", characters)
    print("\nThank you for using my application")

# Sample Output:
# Enter first text: Big
# Enter second text: Data
# Combined Characters: ['B', 'i', 'g', 'D', 'a', 't', 'a']
# Thank you for using my application

# ---------------------------
# Run all functions together:
# ---------------------------

if __name__ == "__main__":
    print("\n--- Question I ---")
    student_management_system()

    print("\n--- Question II ---")
    check_palindrome()

    print("\n--- Question III ---")
    iterate_two_inputs()

