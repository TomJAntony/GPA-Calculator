# GPA-Calculator
Tom Antony's GPA Calculator for Fall 2024 and Spring 2025.


labGrades = []
assignGrades = []

glab1 = input("Enter grade for lab 1: ")
labGrades.append(int(glab1))
glab2 = input("Enter grade for lab 2: ")
labGrades.append(int(glab2))
glab3 = input("Enter grade for lab 3: ")
labGrades.append(int(glab3))
glab4 = input("Enter grade for lab 4: ")
labGrades.append(int(glab4))
glab5 = input("Enter grade for lab 5: ")
labGrades.append(int(glab5))
glab6 = input("Enter grade for lab 6: ")
labGrades.append(int(glab6))
glab7 = input("Enter grade for lab 7: ")
labGrades.append(int(glab7))
glab8 = input("Enter grade for lab 8: ")
labGrades.append(int(glab8))
glab9 = input("Enter grade for lab 9: ")
labGrades.append(int(glab9))
glab10 = input("Enter grade for lab 10: ")
labGrades.append(int(glab10))
glab11 = input("Enter grade for lab 11: ")
labGrades.append(int(glab11))
glab12 = input("Enter grade for lab 12: ")
labGrades.append(int(glab12))
glab13 = input("Enter grade for lab 13: ")
labGrades.append(int(glab13))

ga1 = input("Enter grade for assignement 1: ")
assignGrades.append(int(ga1))
ga2 = input("Enter grade for assignement 2: ")
assignGrades.append(int(ga2))
ga3 = input("Enter grade for assignement 3: ")
assignGrades.append(int(ga3))
ga4 = input("Enter grade for assignement 4: ")
assignGrades.append(int(ga4))
ga5 = input("Enter grade for assignement 5: ")
assignGrades.append(int(ga5))
ga6 = input("Enter grade for assignement 6: ")
assignGrades.append(int(ga6))
ga7 = input("Enter grade for assignement 7: ")
assignGrades.append(int(ga7))
midtermExam = int(input("Enter your midterm grade: "))
finalExam = int(input("Enter your final grade: "))

def calculate_average(labGrades, assignGrades, midtermExam, finalExam):
    for value in labGrades:
            labsum = sum(labGrades)
            lowlabgrade = min(labGrades)
            flabsum = labsum - lowlabgrade
    flabavg = flabsum / 12
    print(f"Lab Average (after dropping the lowest score): {flabavg}")

    for value in assignGrades:
            assignsum = sum(labGrades)
            lowassigngrade = min(labGrades)
            fassignsum = assignsum - lowassigngrade
    fassignavg = fassignsum / 6
    print(f"Assignment Average (after dropping the lowest score): {fassignavg}")

    if finalExam > midtermExam:
        midtermExam = finalExam

    labworth = flabavg * 0.1
    print("Final grade components:")
    print(f"Labs (10%): {labworth}")

    assignworth = fassignavg * 0.4
    print(f"Assignments (40%): {assignworth}")

    mtworth = midtermExam * 0.2
    print(f"Midterm/Final Exam (20%): {mtworth}")

    finalworth = finalExam * 0.3
    print(f"Final Exam (30%): {finalworth}")

    overallGrade = labworth + assignworth + mtworth + finalworth
    print(f"Final Numeric Grade: {overallGrade}")

    if overallGrade >= 89.5:
        finalLetterGrade = "A"
    elif overallGrade >= 79.5 and overallGrade <= 89.4:
        finalLetterGrade = "B"
    elif overallGrade >= 69.5 and overallGrade <= 79.4:
        finalLetterGrade = "C"
    elif overallGrade >= 59.5 and overallGrade <= 69.4:
        finalLetterGrade = "D"
    else:
        finalLetterGrade = "F"

    print(f"Letter Grade: {finalLetterGrade}")

calculate_average(labGrades, assignGrades, midtermExam, finalExam) 
