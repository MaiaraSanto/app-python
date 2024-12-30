# Python Application with Docker Support
## 📋 Sobre este repositório
Este repositório foi criado para armazenar o código-fonte de uma aplicação Python desenvolvida com Flask e os arquivos necessários para criar e gerenciar sua imagem de container usando Docker. O principal objetivo é fornecer um ambiente isolado, escalável e portátil para a execução da aplicação.

📁 Estrutura do Repositório
Abaixo está a estrutura do repositório e a descrição dos principais arquivos:

````
 bash
 Copiar código
app/
├── app.py        # Código principal da aplicação Flask.
├── Dockerfile    # Configuração para criar a imagem Docker.
└── README.md     # Documentação do repositório (este arquivo).
````
## 📄 Arquivos principais:
* app.py: Contém o código principal da aplicação. Essa aplicação utiliza o framework Flask e expõe uma API ou interface na porta 5000.
* Dockerfile: Arquivo utilizado para construir a imagem Docker da aplicação. Ele define a base da imagem, instala as dependências e expõe a aplicação Flask para execução no container.
* README.md: Arquivo de documentação que explica como usar este repositório.

## 🚀 Tecnologias utilizadas

* Python: Linguagem de programação utilizada para desenvolver a aplicação.
* Flask: Framework web minimalista para Python.
* Docker: Ferramenta para criar, gerenciar e executar containers.
# 🛠️ Como configurar e executar
## Pré-requisitos:
Antes de começar, certifique-se de ter as seguintes ferramentas instaladas em seu ambiente:

1.0 Python 3.8 ou superior

2.0 Docker e Docker Compose

3.0 Editor de texto ou IDE (como VS Code, PyCharm ou outro de sua preferência)

1️⃣ Clonar este repositório

````
bash
Copiar código
git clone https://github.com/seu-usuario/nome-do-repositorio.git
cd nome-do-repositorio
````

2️⃣ Criar e executar a aplicação localmente (sem Docker)

1 Instale as dependências:
````
bash
Copiar código
pip install flask
````
2. Execute a aplicação:
````
bash
Copiar código
python app.py
````
3. Acesse a aplicação no navegador: http://127.0.0.1:5000

3️⃣ Construir e executar usando Docker

1. Construir a imagem Docker:
````
bash
Copiar código
docker build -t my-python-app .
````
Executar o container:
````
bash
Copiar código
docker run -p 5000:5000 my-python-app
````
Acesse a aplicação no navegador: http://127.0.0.1:5000

#

## 🐳 Detalhes do Dockerfile
O Dockerfile usado neste projeto possui as seguintes etapas principais:

1. Utiliza a imagem base oficial do Python (python:3.9-slim).
2. Instala as dependências necessárias, incluindo o Flask.
3. Copia o código da aplicação para o container.
4. Define o comando de execução padrão como python app.py.

Exemplo do Dockerfile:
````
dockerfile
Copiar código
# Usar a imagem base do Python
FROM python:3.9-slim

# Definir o diretório de trabalho dentro do container
WORKDIR /app

# Copiar os arquivos da aplicação para o container
COPY . /app

# Instalar dependências
RUN pip install flask

# Expor a porta 5000 para acesso externo
EXPOSE 5000

# Comando para rodar a aplicação
CMD ["python", "app.py"]
````

## 🔧 Solução de Problemas
1️⃣ Erro ao executar o comando docker build
Se receber a mensagem de erro:
````
bash
Copiar código
ERROR: failed to read dockerfile: open Dockerfile: no such file or directory
````
Certifique-se de estar no mesmo diretório que o arquivo Dockerfile ao executar o comando.

2️⃣ Não consegue acessar a aplicação no navegador
Verifique se a porta 5000 está liberada no seu sistema e se o container está em execução:
````
bash
Copiar código
docker ps
````
## 📚 Referências e Aprendizado
* Documentação oficial do Flask
* Documentação oficial do Docker
## 🤝 Contribuindo
Se você deseja contribuir com este repositório, siga as etapas abaixo:

1. Faça um fork deste repositório.
2. Crie uma nova branch com sua feature/bug fix:
````
bash
Copiar código
git checkout -b minha-feature
````
3. Faça suas alterações e faça commit:
````
bash
Copiar código
git commit -m "Adicionei uma nova feature"
````
4. Envie para o repositório remoto:
````
bash
Copiar código
git push origin minha-feature
````
5. Abra um Pull Request.

#
📄 Licença
Este projeto está licenciado sob a [MIT License](LICENSE).  

