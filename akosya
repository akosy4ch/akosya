students = []

# Ask user for the number of students
num_students = int(input("Enter the number of students: "))

# Ask user for information about each student
for i in range(num_students):
    first_name = input("Enter first name of student {}: ".format(i + 1))
    last_name = input("Enter last name of student {}: ".format(i + 1))
    group = input("Enter group of student {}: ".format(i + 1))
    mobile_number = input("Enter mobile number of student {}: ".format(i + 1))
    dob = input("Enter date of birth of student {}: ".format(i + 1))

    students.append({
        'first_name': first_name,
        'last_name': last_name,
        'group': group,
        'mobile_number': mobile_number,
        'dob': dob
    })

# a) Find out if there are namesakes. If there is, then display the list on the screen.
namesake_list = []
for i in range(len(students)):
    for j in range(i + 1, len(students)):
        if students[i]['first_name'] == students[j]['first_name'] and students[i]['last_name'] == students[j][
            'last_name']:
            namesake_list.append([students[i], students[j]])

if len(namesake_list) > 0:
    print("List of namesakes:")
    for pair in namesake_list:
        print(pair[0]['first_name'], pair[0]['last_name'], "and", pair[1]['first_name'], pair[1]['last_name'])
else:
    print("No namesakes found.")

# b) Arrange the list of groups in ascending order by surname
students.sort(key=lambda x: x['last_name'])
print("\nStudents arranged in ascending order by surname:")
for student in students:
    print(student['first_name'], student['last_name'], student['group'])

# c) Display information about students of speciality SE on the screen
print("\nInformation about students of speciality SE:")
for student in students:
    if student['group'] == 'SE':
        print(student['first_name'], student['last_name'], student['mobile_number'])

# d) Bring out the youngest and oldest student in the group
students.sort(key=lambda x: x['dob'])
print("\nYoungest student:", students[0]['first_name'], students[0]['last_name'], students[0]['dob'])
print("Oldest student:", students[-1]['first_name'], students[-1]['last_name'], students[-1]['dob'])
