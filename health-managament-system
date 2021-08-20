# Health Management System
name = input("enter your name : ")
id_no=input("enter you id number: ")
log_list = {1:"Exercise", 2:"Diet"}

def getdate():
    import datetime
    return datetime.datetime.now()

try:
    print("Selected Client : ", f"{name}", "\n", end="")
    print("Press 1 for Log")
    print("Press 2 for Retrieve")
    op = int(input())
    if op is 1:
        for key, value in log_list.items():
            print("Press", key, "to log", value,"\n", end="")
        log_name =  int(input())
        print("Selected Job : ", log_list[log_name])
        f = open(f"{name}" + "_" + log_list[log_name] + ".txt", "a")
        k = 'y'
        while(k is not "n"):
            print("Enter", log_list[log_name], "\n", end="")
            mytext = input()
            f.write("[ " + str(getdate()) + " ] : " + mytext + "\n")
            k = input("ADD MORE ? y/n:")
            continue
        f.close()
    elif op is 2:
        for key, value in log_list.items():
            print("Press", key, "to retrieve", value,"\n", end="")
        log_name =  int(input())
        print(f"{name}", "-", log_list[log_name], "Report :","\n", end="")
        f = open(f"{name}" + "_" + log_list[log_name] + ".txt", "rt")
        contents = f.readlines()
        for line in contents:
            print(line, end="")
        f.close()  
    else:
        print("Invalid Input !!!")
except Exception as e:
    print("Wrong Input !!!") 
