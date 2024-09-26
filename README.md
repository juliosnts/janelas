# janelas
import tkinter as tk


Window = tk.Tk()
Window.title("jj")
Window.geometry("500x500")
Window.configure(background="#696969")


nome = tk.Label(Window, text="julio")
nome.pack()


txtentrada = tk.Entry(Window)
txtentrada.pack()


def machado_de_assis():
    
    new_window = tk.Toplevel(Window)
    new_window.title("Nova Janela")
    new_window.geometry("300x200")
    new_window.configure(background="#FF1493")
     

    inspiracao = txtentrada.get()   
    
    t = tk.Label(new_window, text=inspiracao)
    t.pack()


btn = tk.Button(Window, text="mostrar", command=machado_de_assis)
btn.pack()


#janela 2
import tkinter as tk

janela = tk.Tk()
janela.title("Calculadora")
janela.geometry("300x300")
janela.configure(background="#000000")  

tk.Label(janela, text="Número 1:", fg="white", bg="#000000").pack()
num1 = tk.Entry(janela)
num1.pack()

tk.Label(janela, text="Número 2:", fg="white", bg="#000000").pack()
num2 = tk.Entry(janela)
num2.pack()

def mostrar_resultado(resultado):
    janela_resultado = tk.Toplevel(janela)
    janela_resultado.title("Resultado")
    janela_resultado.configure(background="#0000FF")  
    tk.Label(janela_resultado, text=f"Resultado: {resultado}", fg="white", bg="#0000FF").pack()

def adicionar():
    resultado = float(num1.get()) + float(num2.get())
    mostrar_resultado(resultado)

def subtrair():
    resultado = float(num1.get()) - float(num2.get())
    mostrar_resultado(resultado)

def multiplicar():
    resultado = float(num1.get()) * float(num2.get())
    mostrar_resultado(resultado)

def dividir():
    if float(num2.get()) != 0:
        resultado = float(num1.get()) / float(num2.get())
    else:
        resultado = "Erro: Divisão por zero"
    mostrar_resultado(resultado)

tk.Button(janela, text="Adicionar", command=adicionar, fg="white", bg="#000000").pack()
tk.Button(janela, text="Subtrair", command=subtrair, fg="white", bg="#000000").pack()
tk.Button(janela, text="Multiplicar", command=multiplicar, fg="white", bg="#000000").pack()
tk.Button(janela, text="Dividir", command=dividir, fg="white", bg="#000000").pack()

janela.mainloop()





Window.mainloop()
