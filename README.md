🔐 Gerador de Senhas Fortes em Python
Este projeto é um gerador de senhas aleatórias, criado para praticar programação em Python e estudar segurança digital. Ele permite gerar senhas seguras, com letras, números e símbolos, e salva automaticamente cada senha gerada em um arquivo .txt.
📌 Funcionalidades
Gera senhas fortes com comprimento entre 8 e 64 caracteres

Usa letras maiúsculas, minúsculas, números e símbolos

Salva automaticamente cada senha em senhas_geradas.txt

Interface simples em modo texto
Como usar
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

🚀 Etapas para deixar esse script executavel. 
1. 📦 Instale o PyInstaller
Abra o terminal (Prompt de Comando ou PowerShell) e digite:

pip install pyinstaller

💻 Vá até a pasta onde está seu arquivo .py
Use o comando cd para navegar até a pasta onde está o seu script:

cd "C:\Users\SeuNome\Documents\meu-projeto"
Substitua o caminho pelo local onde está seu arquivo .py.

⚙️ Gere o executável
Agora use o comando abaixo para criar o .exe:

pyinstaller --onefile --console nome_do_arquivo.py
--onefile: cria um único arquivo .exe
--console: mantém a janela do console aberta (necessário para entrada de dados via input())

Exemplo real:
pyinstaller --onefile --console gerador_senha.py

4. 📂 Onde está o .exe?
Após o comando rodar com sucesso:
Vá até a pasta do projeto.
Abra a pasta chamada dist.
Dentro dela estará o arquivo gerador_senha.exe.
Você pode copiar esse .exe para qualquer pasta, e ele vai funcionar em qualquer PC com Windows — mesmo sem Python instalado.

Dica (Remover arquivos extras)
O PyInstaller cria várias pastas e arquivos (como build, __pycache__, e .spec).
Se quiser limpar tudo e ficar só com o .exe, você pode apagar:

Pasta build/
Pasta __pycache__/
Arquivo .spec
