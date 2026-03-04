# Data-structure-program-1students = []

def insert_end():
    sid = input("Enter ID: ")
    name = raw_input("Enter Name: ")
    marks = input("Enter Marks: ")
    students.append([sid, name, marks])

def delete():
    sid = input("Enter ID to delete: ")
    for s in students:
        if s[0] == sid:
            students.remove(s)
            print "Deleted"
            return
    print "Not Found"

def search():
    sid = input("Enter ID to search: ")
    for s in students:
        if s[0] == sid:
            print s
            return
    print "Not Found"

def display():
    for s in students:
        print s

while True:
    print "\n1.Insert 2.Delete 3.Search 4.Display 5.Exit"
    ch = input("Choice: ")
    if ch == 1: insert_end()
    elif ch == 2: delete()
    elif ch == 3: search()
    elif ch == 4: display()
    else: break
