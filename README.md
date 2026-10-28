# project1
#using basic python programing 
#student management system
#student management system
print("*"*50)
print("Welcome to Student Management System")
print("*"*50)
print("1:add student ")
print("2:update student ")
print("3:delete student ")
print("4:search student")
print("5:exit")
print("*"*50)
students=[]
while True:
    choice=int(input("Enter your choice:"))
    if choice==1:
        s_id=int(input("Enter student ID:"))
        name=input("Enter student name:")
        phone=input("Enter student phone number:")
        course=input("Enter student course:")
        fees=input("Enter student fees:")
        student={
            "s_id":s_id,
            "name":name,
            "phone":phone,
            "course":course,
            "fees":fees
        }
        students.append(student)
        # update student
    elif choice==2:
            update_id=int(input("Enter student ID:"))
            found=False
            for student in students:
              if student["id"]==update_id:
                  print("Enter new information ")
                  student=[name]=input("Enter new student name:")
                  student=[phone]=input("Enter new student phone number:")
                  student=[course]=input("Enter new student course:")
                  student=[fees]=input("Enter new student fees:")
                  found=True
                  break
              print("updated successfully")
            if found==false:
                print("student not found ")
                #delete the student form the system
    elif choice==3:
        s_id=int(input("Enter student ID:"))
        if s_id in students:
            students.remove(student)
            print("deleted successfully")

    #search student
    elif choice==4:
        s_id=int(input("Enter student ID:"))
        if s_id in students:
            print([s_id,student])

    #exit form the program
    elif choice==5:
        sys=input("do you want to exit?(y/n):")
        if sys=="y":
            break
        print("thank you for using this program")














 
