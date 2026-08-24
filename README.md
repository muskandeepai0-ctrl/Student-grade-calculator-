# Student-grade-calculator-
This is my first repo
# Student Grade Calculator

print("=================================")
print("     STUDENT GRADE CALCULATOR")
print("=================================")

name = input("Enter student name: ")

subjects = ["English", "Mathematics", "Computer Science",
            "Data Science", "Statistics"]

marks = []

for subject in subjects:
    while True:
        try:
            mark = float(input(f"Enter marks for {subject} (0-100): "))

            if 0 <= mark <= 100:
                marks.append(mark)
                break
            else:
                print("Please enter marks between 0 and 100.")

        except ValueError:
            print("Please enter a valid number.")

total = sum(marks)
percentage = total / len(subjects)

if percentage >= 90:
    grade = "A+"
elif percentage >= 80:
    grade = "A"
elif percentage >= 70:
    grade = "B"
elif percentage >= 60:
    grade = "C"
elif percentage >= 50:
    grade = "D"
else:
    grade = "F"

result = "PASS" if percentage >= 40 else "FAIL"

print("\n=================================")
print("          RESULT")
print("=================================")
print("Student Name:", name)
print("Total Marks:", total, "/ 500")
print("Percentage:", round(percentage, 2), "%")
print("Grade:", grade)
print("Result:", result)
print("==================
