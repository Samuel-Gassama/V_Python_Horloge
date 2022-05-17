from tkinter import * 
from calendar import week
import pyglet 
from datetime import datetime
import pyttsx3
import time
pyglet.font.add_file('digital-7.ttf') # Ajout du font digital-7 

# Couleurs 

bc = "#ffffff"
fc = "#e3446"
rd = "#F9A18E"


#Configuration de la fenêtre

window = Tk()
window.title("Horloge Digitale")
window.geometry('500x150') # Taille de la fenêtre
window.resizable(width=False,height=False ) # options taille
window.configure(bg=rd) # 


def clock():  # Création de l'horloge 
    time = datetime.now()
    heure = time.strftime(" %H : %M : %S") # Récupérer l'heure, les minutes, les secondes 
    jourSemaine = time.strftime("%A") # Récupérer le jour actuel en format lettre
    jour = time.day # Récupérer le jour actuel
    mois = time.strftime("%b") # Récupérer le mois actuel
    annee = time.strftime("%Y") # Récupérer l'année actuelle
    l1.configure(text=heure) # Configure le texte du label avec la variable heure
    l1.after(200, clock) # Actualisation de l'horloge toutes les secondes
    l2.configure(text=jourSemaine + " " + str(jour)+ "/" + str(mois) + "/" + str(annee)) # Concatenation des jours, mois et années pour écrire la date sur le label 2 




nom = input("Entrer votre nom: ") # Input entrer votre nom

now = datetime.now()
current_time = now.strftime("%H:%M:%S")
print("Il est : ", current_time) # Affiche l'heure actuelle

Time=input("Entrer votre heure de réveil (HH24:MM): ") # Input te l'heure du réveil

# LOOP REVEIL
while True:
    
    Standard_time=datetime.now().strftime("%H:%M")
    time.sleep(1) # Attente de x secondes
  
    if time==Standard_time:
        count=0
        while count<=5:
            count=count+1
            engine=pyttsx3.init()
            engine.say("il est l'heure de se réveiller" + nom)
            engine.runAndWait()
        break

# FENETRE DE L HORLOGE DIGITALE
l1= Label(window, text = " ", font=('digital-7 80'), bg = rd) # LABEL 1
l1.grid(row = 0, column= 0 ,padx=5, sticky=NW)\

l2= Label(window, text = " ", font=('digital-7 20'), bg =rd) # LABEL 2
l2.grid(row = 1, column= 0, padx=1)

clock()

window.mainloop()
