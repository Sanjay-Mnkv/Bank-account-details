# Bank-account-details
Bank Account details using python
#!/bin/python3
class bkacc:
    noac=0
    def __init__(self):
        bkacc.noac+=1
        self.acno=1000+bkacc.noac
        self.acholder=input("Enter the holder name :")
        self.address=input("Enter the address :")
        self.type=input("Enter the A/c Type :")
        self.acbal=eval(input("Amount?"))
    def dep(self):
        self.acbal+=eval(input("Enter the deposit amount :"))
        print("The current balance=",self.acbal)
    def wdraw(self):
        self.wdraw-=eval(input("Enter the withdrawl amount :"))
        if self.wdraw>self.acbal:
            print("Not enough balance")
        else:
            self.acbal=self.acbal-self.wdraw
    def show(self):
        print("AccNo.",self.acno,"Holder:",self.acholder,"address:",self.address,"type:",self.type,"Balance:",self.acbal)
dacc=dict()
while True:
    print("1.create")
    print("2.Deposit")
    print("3.Withdraw")
    print("4.show")
    print("5.exit")
    ch=input("choice?")
    if ch=='1':
        b1=bkacc()
        dacc[b1.acno]=b1
    elif ch=='2':
        dacc[eval(input("Enter the account number"))].dep()
    elif ch=='3':
        dacc[eval(input("Enter the account no"))].wdraw()
    elif ch=='4':
        dacc[eval(input("Enter trhe account number"))].show()
    elif ch=='5':
        break
    else:
      print("entered invalid choice")

