# ProyectoFinalCreatividadDigital2025B-MarthaLopez
Esté es un proyecto para la materia de Programación I de la carrera de Creatividad Digital en el CUGDL. Consiste en el juego snake hecho de forma sencilla.
import tkinter as tk

import random

#Instanciar una ventana nueva
ventana = tk.Tk()
#Asignarle dimensiones y titulo
ventana.title("Mi Ventana")
ventana.geometry("800x500")

#Remover configuracion de la ventana por defecto
ventana.resizable(False, False)

#Agregar un lienzo a la ventana
lienzo = tk.Canvas(ventana, width=750, height=450, bg="pink")
lienzo.pack_configure(expand=True, anchor="center")
lienzo.pack()

#Aleatoridad en el punto a comer cuando aparezca
def punto_aleatorio():
    x = random.randint(5, 775)
    y = random.randint(5, 475)
    return (x, y)

#Agregar un rectangulo(punto a comer) al lienzo
lienzo.create_rectangle(x, y, x + 20, y + 20,  fill="white")
#Configurar serpiente
lienzo.create_rectangle(390, 240, 390 + 20, 240 + 60, fill= "green")

#Configuracion para que se vea la ventana
ventana.mainloop()
