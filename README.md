# hackathoncal
#E-CALCULATOR (EMOJI-CALCULATOR)
'''Welcom to E-Calculator. This is an impractical emoji calculator which accepts all mathematical operators with a twist! The results you will be receiving willnot be numbers
Instead, they will be in the form of a random emoji which makes this calculator impractical to use!'''
from tkinter import*
def btnClick(numbers):
    global operator
    operator=operator+str(numbers)
    text_input.set(operator)

def btnClearDisplay():
    global operator
    operator=""
    text_input.set("")
def btnEqualInput():
    global operator
    import random
    lst=["\U0001f600","\U0001F601","\U0001F602","\U0001F606","\U0001F923","\U0001F642","\U0001F60A","\U0001F60B","\U0001F603","\U0001F604","\U0001F605","\U0001F923","\U0001F642"\
         "\U0001F643","\U0001F607","\U0001F970","\U0001F929","\U0001F618","\U0001F617"]
    sumup=str(eval(operator)) #Enter the numbers in the calculator without using keyboard
    text_input.set(random.choice(lst))
    operator=""
cal=Tk()
cal.title('Calculator')
operator=""
text_input=StringVar()
textDisplay=Entry(cal,font=('ariel',20,'bold'),textvariable=text_input,bd=20,insertwidth=10,bg='darkgrey',justify='right').grid(columnspan=4)
btn7=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='7',command=lambda:btnClick(7)).grid(row=1,column=0)
btn8=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='8',command=lambda:btnClick(8)).grid(row=1,column=1)
btn9=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='9',command=lambda:btnClick(9)).grid(row=1,column=2)
Addition=Button(cal,padx=16,bd=8,fg='black',bg='gray',font=('Agency FB',20),text='+',command=lambda:btnClick('+')).grid(row=1,column=3)
#===============================================================================================================================================================#
btn4=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='4',command=lambda:btnClick(4)).grid(row=2,column=0)
btn5=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='5',command=lambda:btnClick(5)).grid(row=2,column=1)
btn6=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='6',command=lambda:btnClick(6)).grid(row=2,column=2)
Multiplication=Button(cal,padx=16,bd=8,bg='gray',fg='black',font=('Agency FB',20),text='*',command=lambda:btnClick('*')).grid(row=2,column=3)
#===============================================================================================================================================================#
btn1=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='1',command=lambda:btnClick(1)).grid(row=3,column=0)
btn2=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='2',command=lambda:btnClick(2)).grid(row=3,column=1)
btn3=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='3',command=lambda:btnClick(3)).grid(row=3,column=2)
Subtraction=Button(cal,padx=16,bd=8,bg='gray',fg='black',font=('Agency FB',20),text='-',command=lambda:btnClick('-')).grid(row=3,column=3)
#===============================================================================================================================================================#
Deci=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='.',command=lambda:btnClick('.')).grid(row=4,column=0)
btn0=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='0',command=lambda:btnClick(0)).grid(row=4,column=1)
Division=Button(cal,padx=16,bd=8,fg='black',bg='darkgrey',font=('Agency FB',20),text='/',command=lambda:btnClick('/')).grid(row=4,column=2)
Equal=Button(cal,padx=16,bd=8,fg='black',bg='gray',font=('Agency FB',20),text='=',command=btnEqualInput).grid(row=4,column=3)
C=Button(cal,padx=16,bd=8,width=27,fg='black',bg='gray',font=('Agency FB',20),text='C',command=btnClearDisplay).grid(columnspan=5,rowspan=1)
cal.mainloop()

