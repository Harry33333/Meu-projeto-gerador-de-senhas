🔐 Gerador de Senhas Fortes em Python
Este projeto é um gerador de senhas aleatórias, criado para praticar programação em Python e estudar segurança digital. Ele permite gerar senhas seguras, com letras, números e símbolos, e salva automaticamente cada senha gerada em um arquivo .txt.
📌 Funcionalidades
Gera senhas fortes com comprimento entre 8 e 64 caracteres

Usa letras maiúsculas, minúsculas, números e símbolos

Salva automaticamente cada senha em senhas_geradas.txt

Interface simples em modo texto
omo usar
Certifique-se de ter o Python 3 instalado na sua máquina.

Execute o script:
Navegue no cmd até a pasta onde está o script e digite:
python nome_do_arquivo.py
Digite o tamanho da senha (entre 8 e 64).

A senha gerada será exibida na tela e salva no arquivo senhas_geradas.txt.

💻 Interface do script:
=== Gerador de Senhas Fortes ===

Informe o tamanho da senha (8 a 64): 16

Senha gerada: H8m@x$W9z!r2Q#Lp

Senha salva em 'senhas_geradas.txt'

Deseja gerar outra senha? (s/n): n

Encerrando o gerador. Até mais!
📁 Arquivo de saída
As senhas geradas são salvas em um arquivo chamado senhas_geradas.txt, no mesmo diretório onde o script é executado.
🚀 Objetivo
Esse projeto foi criado como prática de programação em Python, com foco em segurança da informação e automação de tarefas simples.

CODIGO DO SCRIPT:

import random
import string
import os

def gerar_senha(tamanho):
    if tamanho < 8 or tamanho > 64: #Aqui é o tamanho minimo e o tamanho máximo da senha
        raise ValueError("O tamanho da senha deve ser entre 8 e 64 caracteres.")

    caracteres = string.ascii_letters + string.digits + string.punctuation
    senha = ''.join(random.choice(caracteres) for _ in range(tamanho))
    return senha

def salvar_senha(senha, arquivo="senhas_geradas.txt"):#Aqui é a pasta e o nome da pasta que vai criar e salvar suas senhas
    with open(arquivo, "a") as f:
        f.write(senha + "\n")

def menu():
    print("=== Gerador de Senhas Fortes ===\n")
    
    while True:
        try:
            tamanho = int(input("Informe o tamanho da senha (8 a 64): "))#Aqui é a pergunta do tamanho da senha
            if 8 <= tamanho <= 64:
                senha = gerar_senha(tamanho)
                print(f"\nSenha gerada: {senha}\n")
                salvar_senha(senha)
                print("Senha salva em 'senhas_geradas.txt'\n")
            else:
                print("❌ Tamanho inválido! Digite um número entre 8 e 64.\n")#Aqui é a mensagem de erro se o numero não estiver entre 8 a 64
                continue

            outra = input("Deseja gerar outra senha? (s/n): ").lower()#Aqui é a pergunta para encerramento ou continuação
            if outra != 's':
                print("\nEncerrando o gerador. Até mais!")
                break
        except ValueError:
            print("❌ Entrada inválida! Digite apenas números.\n")#Aqui é a mensagem de erro se selecionar resposta diferente de "s" ou "n"

if __name__ == "__main__":
    menu()




