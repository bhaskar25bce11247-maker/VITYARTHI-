# VITYARTHI-
The aim of the project is to design a program that works as a plain ticket booking and seat selection simulator. This program offers easy seat booking and a user friendly interface.


print("\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n//////////////////////////////////////   BLUE  PLANE   //////////\n\n\n")
print("Hello user!! \n \nthis is the main menu for the blue plane application\n\n")
#print("*********** HELLO TRAVELLERS ***********\n") 
print("//////////START YOUR BOOKING PROCESS HERE:")
print("\n\n\n\n") 
pasa = int(input("ENTER THE NUMBER OF PASSANGERS TRAVELLING!! :- "))
money = 0


namelist = []
for i in range(0,pasa):
    Name = input("\nENTER THE NAME ->")
    namelist.append(Name)

print("\n\n\n\nThe name of ",pasa," passangers are listed as follows :-\n\n")
print(namelist)

print("\n")

print("//"*20)
print("//"*20)
print("\n\n\nNow we are going to select the destination ")
# entering the boarding and destination of passengers
print("\n\nYOUR BOARDING LOCATION IS BHOPAL(BHO)") 
print("=*="*10)
print("\n\n")
print("PLEASE SELECT ONE OF THE DESTINATION:-\n")
print("please enter (DEL)-> FOR DELHI")
print("please enter (VNS)-> FOR VANARASI")
print("please enter (LKO)-> FOR LUCKNOW\n\n") 
Destination = input("PLEASE ENTER YOUR DESTINATION-> ")
print() 

if(Destination == "DEL" or Destination == "LKO" or Destination == "VNS"):
  print("YOUR DESTINATION IS", Destination)
else:
  print("PLEASE ENTER THE DESTINATION FROM THE GIVEN LIST:" )
  Destination = input("PLEASE ENTER YOUR DESTINATION-> ")
print("\n") # Replaced print() with \n
print("*********************************************\n\n") # Replaced 2 print() with 2 \n
#Information of flights
Flight1 = {
    1 : "6E 642 (BHO -> DEL) {PRICE = 14000}",
    2 : "438(BHO->DEL) {PRICE = 15000}",
    3 : "910(BHO->DEL) {PRICE = 13500}",
}
Flight2 = {
    1 : "A1 871(BHO -> VNS) {PRICE = 16000}",
    2 : "7109 (BHO-> VNS) {PRICE = 11590}",
}
Flight3 = {
    1 : "UK 924(BHO -> LKO) {PRICE = 14000}",
    2 : "5672(BHO-> LKO){PRICE = 13000}",
}
#Checking where the passenger wants to travel
if(Destination == "DEL"):
  print(Flight1)
  print("\n") # Replaced 2 print() with 2 \n
  print("ENTER THE SERIAL NO. OF THE FLIGHT YOU WANT TO BOOK-> ")
  flightno = int(input())
  if(flightno == 1 or flightno == 2 or flightno == 3):
    print("YOUR SELECTED FLIGHT IS-> " , Flight1[flightno])
    if(flightno ==1):
       money = pasa*14000
    if(flightno == 2):
        money = pasa*15000
    if(flightno == 3):
       money = pasa*13500

  else:
    print("PLEASE SELECT THE SERIAL NO FROM THE LIST")
    flightno = int(input())
    print("YOUR SELECTED FLIGHT IS-> " , Flight1[flightno])
  print("\n\n") 
  #money transaction
  print("******PLEASE ENTER YOUR BANK INFO FOR PAYMENT******\n\n") 
  bankno = input("PLEASE ENTER YOUR BANK ACCOUNT NO-> ")
  password = int(input("PLEASE ENTER YOUR PASSWORD. -> "))


  print("AS PER THE NUMBER OF SEATS BOOKED THE NET AMOUNT IS ",money ," INDIAN RUPEES :-")
  print("PLEASE ENTER THE COST OF FLIGHT TO CONFIRM -> ") 
  amount = int(input())
  print("PLEASE ENTER (1) TO CONFIRM OR (2) TO CANCLE YOUR BOOKING: ")
  confirm = int(input())
  print() 
  if(confirm == 1):
    print("\n\nPAYMENT SUCCESSFUL!!!!\n\n\n") 
  else:
    print("PAYMENT UNSUCESSFULL!!!!!")
elif(Destination == "VNS"):
  print(Flight2)
  print() 
  print("ENTER THE SERIAL NO. OF THE FLIGHT YOU WANT TO BOOK->")
  flightno = int(input())
  if(flightno == 1 or flightno == 2):
    print("YOUR SELECTED FLIGHT IS-> " , Flight2[flightno])
    if(flightno ==1):
       money = pasa*16000
    if(flightno == 2):
        money = pasa*11590

  else:
    print("PLEASE SELECT THE SERIAL NO FROM THE LIST")
    flightno = int(input())
    print("YOUR SELECTED FLIGHT IS-> " , Flight2[flightno])
  print("\n\n") 
  print("******PLEASE ENTER YOUR BANK INFO FOR PAYMENT******\n\n") 
  bankno = input("PLEASE ENTER YOUR BANK ACCOUNT NO-> ")
  password = int(input("PLEASE ENTER YOUR BANK PASSWORD. -> "))

  print("AS PER THE NUMBER OF SEATS BOOKED THE NET AMOUNT IS ",money ," INDIAN RUPEES :-")
  print("PLEASE ENTER THE COST OF FLIGHT TO CONFIRM -> ")
  amount = int(input())
  print() 
  print("PLEASE ENTER (1) TO CONFIRM OR (2) TO CANCLE YOUR BOOKING: ")
  confirm = int(input())
  print("\n\n") 
  if(confirm == 1):
    print("\nPAYMENT SUCCESSFUL!!!!\n\n") 
    
  else:
    print("BOOKING UNSUCESSFULL!!!!!")
elif(Destination == "LKO"):
  print(Flight3)
  print("ENTER THE SERIAL NO. OF THE FLIGHT YOU WANT TO BOOK->")
  flightno = int(input())
  print() 
  if(flightno == 1 or flightno == 2):
    print("YOUR SELECTED FLIGHT IS-> " , Flight3[flightno])
    if(flightno ==1):
       money = pasa*14000
    if(flightno == 2):
        money = pasa*13000

  else:
    print("PLEASE SELECT THE SERIAL NO FROM THE LIST")
    flightno = int(input())
    print("YOUR SELECTED FLIGHT IS-> " , Flight3[flightno])
  print("\n\n") 
  print("******PLEASE ENTER YOUR BANK INFO FOR PAYMANT******\n\n") 
  bankno = input("PLEASE ENTER YOUR BANK ACCOUNT NO-> ")
  password = int(input("PLEASE ENTER YOUR BANK PASSWORD. -> "))

  print("AS PER THE NUMBER OF SEATS BOOKED THE NET AMOUNT IS ",money ," INDIAN RUPEES :-")
  print("PLEASE ENTER THE COST OF FLIGHT TO CONFIRM -> ")
  amount = int(input())
  print("\n") 
  print("PLEASE ENTER (1) to confirm OR (2) TO CANCLE YOUR BOOKING: ")
  confirm = int(input())
  print() 
  if(confirm == 1):
    print("\nPAYMENT SUCCESSFUL!!!!\n\n") 
    
  else:
    print("BOOKING UNSUCESSFULL!!!!!")






 #/////////////////////////////////////////////////////////////////////
 #/////////////////////////////////////////////////////////////////////
 #/////////////////////////////////////////////////////////////////////




print("\n"*5)
print("PLEASE SELECT THE SEAT ACCORDING TO THE SEAT MATRIX PROVIDED :-\n\n")
print("Legends :-  \"X\" --> booked seat\n            \"O\" ---> seat is empty\n\n\n")



# seat allocator 
seats = {
    "A1": "O", "B1": "O", "C1": "O", "D1": "O", "E1": "O", "F1": "O", "G1": "O", "H1": "O",
    "A2": "O", "B2": "O", "C2": "O", "D2": "O", "E2": "O", "F2": "O", "G2": "O", "H2": "O",
    "A3": "O", "B3": "O", "C3": "O", "D3": "O", "E3": "O", "F3": "O", "G3": "O", "H3": "O",
    "A4": "O", "B4": "O", "C4": "O", "D4": "O", "E4": "O", "F4": "O", "G4": "O", "H4": "O",
}


layout = "                 A  B  C     D  E     F  G  H \n\n" \
"         1.   || {A1}  {B1}  {C1}     {D1}  {E1}     {F1}  {G1}  {H1} ||\n" \
"         2.   || {A2}  {B2}  {C2}     {D2}  {E2}     {F2}  {G2}  {H2} ||\n" \
"         3.   || {A3}  {B3}  {C3}     {D3}  {E3}     {F3}  {G3}  {H3} ||\n" \
"         4.   || {A4}  {B4}  {C4}     {D4}  {E4}     {F4}  {G4}  {H4} ||\n"



#col = ["A","B","C","D","E","F","G","H"]
#row = [1,2,3,4]
#pasa = 2 # number of passangers coming in the group 

buyed = []
cnt = 0


if pasa == 1:
    seats["A1"] = "X"
    seats["B3"] = "X"
    seats["E2"] = "X"
    seats["A3"] = "X"
    seats["B2"] = "X"
    seats["A2"] = "X"
    seats["B3"] = "X"
    seats["E1"] = "X"
    seats["H3"] = "X"
    print(layout.format(**seats))
elif pasa == 2:
    seats["A4"] = "X"
    seats["B3"] = "X"
    seats["G2"] = "X"
    seats["E3"] = "X"
    seats["F3"] = "X"
    print(layout.format(**seats))
elif pasa == 3:
    seats["C1"] = "X"
    seats["F3"] = "X"
    seats["E2"] = "X"
    seats["A3"] = "X"
    seats["B2"] = "X"
    seats["A2"] = "X"
    seats["B3"] = "X"
    seats["E3"] = "X"
    seats["E1"] = "X"
    seats["H3"] = "X"
    print(layout.format(**seats))
elif pasa == 4:
    seats["A3"] = "X"
    seats["B2"] = "X"
    seats["A2"] = "X"
    seats["B3"] = "X"
    seats["B3"] = "X"
    seats["E3"] = "X"
    seats["E1"] = "X"
    seats["A3"] = "X"
    seats["B2"] = "X"
    seats["A2"] = "X"
    print(layout.format(**seats))



while pasa-cnt > 0:
    
    print("\n\nYou can select ", pasa - cnt ," seats now")
    chair = input("Enter the seat-")
    if chair not in seats:
        print("Please enter the valid value !!")
        continue
    if seats[chair] == "X":
        print("\n\n!!! Seat is booked !!!\n\n")

    else :
        seats[chair] = "X"
        buyed.append(chair)
        print("Seat booking succesfull !!\n\n -------------------------\n\n\n")
        print(layout.format(**seats))
        print()
        cnt += 1
    if pasa - cnt  == 0:
        print("All the seats for the passangers are selected !!\n\nThank you!!")

if(Destination == "DEL" and confirm == 1):
    print("\nBOOKING SUCCESSFUL!!!!\n\n") 
    print("********** YOUR FLIGHT DETAILS ARE ********** \n\n") 
    print("(YOUR BOOKING REFFERENCE)PNR -> ABRZ202512")
    print("AIRLINE -> Air India: ", Flight1[flightno])
    print("SEAT BOOKED -> ",buyed)
    print("ROUTE -> BHOPAL(BHO) TO DELHI(DEL)")
    print("DEPARTURE -> Mon, 15 jan 2026, 11:30 AM")
    print("ARRIVAL -> Mon, 15 jan 2026, 01:00 pm")
    print("DURATION -> 1h 30m")
    print("PASSSENGER NAMES -> ", namelist)
    print("PRICE PAID -> ", amount)
    print("\n\n") 
    print("*********************************************")
if(Destination == "VNS" and confirm == 1):
    print("\nBOOKING SUCCESSFUL!!!!\n\n") 
    print("********** YOUR FLIGHT DETAILS ARE ********** \n\n") 
    print("(YOUR BOOKING REFFERENCE)PNR -> ABRZ202512")
    print("AIRLINE -> Air India: ", Flight2[flightno])
    print("SEAT BOOKED -> ",buyed)
    print("ROUTE -> BHOPAL(BHO) TO VARANASI(VNS)")
    print("DEPARTURE -> Mon, 15 jan 2026, 11:30 AM")
    print("ARRIVAL -> Mon, 15 jan 2026, 01:00 pm")
    print("DURATION -> 1h 30m")
    print("PASSSENGER NAMES -> ", namelist)
    print("PRICE PAID -> ", amount)
    print("\n\n") 
    print("*********************************************")
if(Destination == "LKO" and confirm == 1):
    print("********** YOUR FLIGHT DETAILS ARE ********** \n\n") 
    print("(YOUR BOOKING REFFERENCE)PNR -> ABRZ202512")
    print("AIRLINE -> Air India: ", Flight3[flightno])
    print("SEAT BOOKED -> ",buyed)
    print("ROUTE -> BHOPAL(BHO) TO LUCKNOW(LKO)")
    print("DEPARTURE -> Mon, 15 jan 2026, 11:30 AM")
    print("ARRIVAL -> Mon, 15 jan 2026, 01:00 pm")
    print("DURATION -> 1h 30m")
    print("PASSSENGER NAMES -> ", namelist)
    print("PRICE PAID -> ", amount)
    print("\n\n") 
    print("*********************************************")
