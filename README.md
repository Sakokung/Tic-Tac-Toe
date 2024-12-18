ox_table = ["-", "|", "-", "|", "-", "\n-", "|", "-", "|", "-", "\n-", "|", "-", "|", "-"]

#Select_Channel_x
def x_channel(x_inp):    
    if x_inp == "1":
        ox_table[0] = "x"
    elif x_inp == "2":
        ox_table[2] = "x"
    elif x_inp == "3":
        ox_table[4] = "x"
    elif x_inp == "4":
        ox_table[5] = "\nx"
    elif x_inp == "5":
        ox_table[7] = "x"
    elif x_inp == "6":
        ox_table[9] = "x"
    elif x_inp == "7":
        ox_table[10] = "\nx"
    elif x_inp == "8":
        ox_table[12] = "x"
    elif x_inp == "9":
        ox_table[14] = "x"
    else :
        print("")
        print("----------------------------")
        print("You didn't enter a number or it wasn't 1-9.\nTry type again!")
        print("----------------------------")
    print("")
    print(ox_table[0],ox_table[1],ox_table[2],ox_table[3],ox_table[4],ox_table[5],ox_table[6],ox_table[7],ox_table[8],ox_table[9],ox_table[10],ox_table[11],ox_table[12],ox_table[13],ox_table[14])

#select_Channel_o
def o_channel(o_inp):
    if o_inp == "1":
        ox_table[0] = "o"
    elif o_inp == "2":
        ox_table[2] = "o"
    elif o_inp == "3":
        ox_table[4] = "o"
    elif o_inp == "4":
        ox_table[5] = "\no"
    elif o_inp == "5":
        ox_table[7] = "o"
    elif o_inp == "6":
        ox_table[9] = "o"
    elif o_inp == "7":
        ox_table[10] = "\no"
    elif o_inp == "8":
        ox_table[12] = "o"
    elif o_inp == "9":
        ox_table[14] = "o"
    else :
        print("")
        print("----------------------------")
        print("You didn't enter a number or it wasn't 1-9.\nTry type again!")
        print("----------------------------")
    print("")
    print(ox_table[0],ox_table[1],ox_table[2],ox_table[3],ox_table[4],ox_table[5],ox_table[6],ox_table[7],ox_table[8],ox_table[9],ox_table[10],ox_table[11],ox_table[12],ox_table[13],ox_table[14])

#welcome
xwin = ("\n----------------------------\nx win!\n----------------------------")
owin =("\n----------------------------\no win!\n----------------------------")
print("----------------------------")
print("Welcome to tic tac toe game!")
print("----------------------------\n")
print("1 | 2 | 3 \n4 | 5 | 6 \n7 | 8 | 9 ")

x = 0
while True :
    print("\n----------------------------")
    print("You are x")
    print("----------------------------")
    x_inp = str(input("Select channel (1,2,3,4,5,6,7,8,9) > : "))
    x_channel(x_inp)
    #x_win
    if ox_table[0] == "x" and ox_table[2] == "x" and ox_table[4] == "x" or ox_table[5] == "\nx" and ox_table[7] == "x" and ox_table[9] == "x" or ox_table[10] == "\nx" and ox_table[12] == "x" and ox_table[14] == "x":
        print(xwin)
        break
    elif ox_table[0] == "x" and ox_table[5] == "\nx" and ox_table[10] == "\nx" or ox_table[2] == "x" and ox_table[7] == "x" and ox_table[12] == "x" or ox_table[4] == "x" and ox_table[9] == "x" and ox_table[14] == "x":
        print(xwin)
        break
    elif ox_table[0] == "x" and ox_table[7] == "x" and ox_table[14] == "x" or ox_table[4] == "x" and ox_table[7] == "x" and ox_table[10] == "\nx":
        print(xwin)
        break
    #draw
    x += 1
    if x >= 0 :
        if ox_table[0] != "-" and ox_table[2] != "-" and ox_table[4] != "-" and ox_table[5] != "\n-" and  ox_table[7] != "-" and ox_table[9] != "-" and ox_table[10] != "\n-" and ox_table[11] != "-" and ox_table[12] != "-" :
            print("\n----------------------------")
            print("draw!")
            print("----------------------------")
            break
    print("\n----------------------------")
    print("You are o")
    print("----------------------------")
    o_inp = str(input("Select channel (1,2,3,4,5,6,7,8,9) > : "))
    o_channel(o_inp)
    #o_win
    if ox_table[0] == "o" and ox_table[2] == "o" and ox_table[4] == "o" or ox_table[5] == "\no" and ox_table[7] == "o" and ox_table[9] == "o" or ox_table[10] == "\no" and ox_table[12] == "o" and ox_table[14] == "o":
        print(owin)
        break
    elif ox_table[0] == "o" and ox_table[5] == "\no" and ox_table[10] == "\no" or ox_table[2] == "o" and ox_table[7] == "o" and ox_table[12] == "o" or ox_table[4] == "o" and ox_table[9] == "o" and ox_table[14] == "o":
        print(owin)
        break
    elif ox_table[0] == "o" and ox_table[7] == "o" and ox_table[14] == "o" or ox_table[4] == "o" and ox_table[7] == "o" and ox_table[10] == "\no":
        print(owin)
        break
    #draw
    x += 1
    if x >= 0 :
        if ox_table[0] != "-" and ox_table[2] != "-" and ox_table[4] != "-" and ox_table[5] != "\n-" and  ox_table[7] != "-" and ox_table[9] != "-" and ox_table[10] != "\n-" and ox_table[11] != "-" and ox_table[12] != "-" :
            print("\n----------------------------")
            print("draw!")
            print("----------------------------")
            break
