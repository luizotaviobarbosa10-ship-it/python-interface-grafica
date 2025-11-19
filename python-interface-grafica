import tkinter as tk
from tkinter import messagebox

produtos = []

def adicionar():
    nome = entrada.get()
    if nome:
        produtos.append(nome)
        lista.insert(tk.END, nome)
        entrada.delete(0, tk.END)
    else:
        messagebox.showwarning("Erro", "Digite um nome válido")

def salvar():
    with open("produtos.txt", "w") as f:
        for p in produtos:
            f.write(p + "\n")
    messagebox.showinfo("Sucesso", "Produtos salvos!")

janela = tk.Tk()
janela.title("Cadastro de Produtos")

tk.Label(janela, text="Produto:").pack()
entrada = tk.Entry(janela)
entrada.pack()

tk.Button(janela, text="Adicionar", command=adicionar).pack()

lista = tk.Listbox(janela)
lista.pack()

tk.Button(janela, text="Salvar", command=salvar).pack()

janela.mainloop()
