```python
students = {
    "Hermione": "Gryffindor",
    "Harry": "Gryffindor",
    "Ron": "Gryffindor",
    "Draco": "Slytherin",
}

# keys == student and values == students[student]
for student in students:
    print(student, students[student], sep = " ==> ")
```
results:
```text
Hermione ==> Gryffindor
Harry ==> Gryffindor
Ron ==> Gryffindor
Draco ==> Slytherin
```
