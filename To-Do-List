#IMPORTO LE LIBRERIE
from tkinter import*
from tkinter import messagebox

#CASELLA PER AGGIUNGERE NUOVI PROMEMORIA
def newTask():
    task = my_entry.get()
    if task != "":
        lb.insert(END, task)
        my_entry.delete(0, "end")
    else:
        messagebox.showwarning("ATTENZIONE", "NON HAI INSERITO NESSUN PROMEMORIA")


#CANCELLIAMO UN PROMEMORIA
def deleteTask():
    lb.delete(ANCHOR)

#CREAMO LA FINESTRA PER LA VISUALIZZAZIONE DEL PROGRAMMA
ws = Tk()
ws.geometry('500x450+500+200')
ws.title('To-Do-List')
ws.config(bg='GREY')
ws.resizable(width=False, height=False)

#CREAMO IL FRAME
frame = Frame(ws)
frame.pack(pady=10)

#DEFINIAMO LA FINESTRA DI INTERAZIONE
lb = Listbox(
    frame,
    width=30,
    height=10,
    font=('Times', 20),
    bd=0,
    fg='BLACK',
    highlightthickness=0,
    selectbackground='YELLOW',
    activestyle="none",

)
lb.pack(side=LEFT, fill=BOTH)

#DATI PREIMPOSTATI
task_list = [
    'Fare colazione',
    'Vestirsi',
    'Lavare i denti',
    'Preparare lo zaino',
    'Prendere il bus',
    'Fare merenda',
    'Pranzare',
    'Studiare',
    'Andare in palestra',
    'Cenare',
]

for item in task_list:
    lb.insert(END, item)

#BARRE DI SCORRIMENTO
sb = Scrollbar(frame)
sb.pack(side=RIGHT, fill=BOTH)

lb.config(yscrollcommand=sb.set)
sb.config(command=lb.yview)

#SPAZIO PER SCRIVERE
my_entry = Entry(
    ws,
    font=('times', 24)
)

my_entry.pack(pady=20)

#AGGIUNGIAMO LA CORNICE PER I BOTTONI
button_frame = Frame(ws)
button_frame.pack(pady=20)

#CREAMO I BOTTONI
addTask_btn = Button(
    button_frame,
    text='AGGIUNGI',
    font=('times 14'),
    bg='GREEN',
    padx=20,
    pady=10,
    command=newTask
)
addTask_btn.pack(fill=BOTH, expand=True, side=LEFT)

delTask_btn = Button(
    button_frame,
    text='CANCELLA',
    font=('times 14'),
    bg='RED',
    padx=20,
    pady=10,
    command=deleteTask
)
delTask_btn.pack(fill=BOTH, expand=True, side=LEFT)

ws.mainloop()
