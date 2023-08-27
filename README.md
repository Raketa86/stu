class Student:
    def __init__(self, firstName, lastName, group, averageMark):
        self.firstName = firstName
        self.lastName = lastName
        self.group = group
        self.averageMark = averageMark

    def getScholarship(self):
        if self.averageMark == 5:
            return 2000
        else:
            return 1900


class Aspirant(Student):
    def __init__(self, firstName, lastName, group, averageMark, scientificWork):
        super().__init__(firstName, lastName, group, averageMark)
        self.scientificWork = scientificWork

    def getScholarship(self):
        if self.averageMark == 5:
            return 2500
        else:
            return 2200

            students = [
    Student("Иван", "Иванов", "Группа 1", 4.8),
    Aspirant("Петр", "Петров", "Группа 2", 5, "Научная работа 1"),
    Student("Анна", "Сидорова", "Группа 1", 4.9),
    Aspirant("Мария", "Смирнова", "Группа 2", 4.7, "Научная работа 2")
]

for student in students:
    print(student.getScholarship())
Вывод:

    1900
2500
1900
2200
