| Pipeline CI/CD com GitHub Actions para Aplicação Flask |

Visão Geral:

Este projeto cria uma aplicação Flask simples, containerizada com Docker, com um pipeline CI/CD no GitHub Actions que automatiza testes, build e push da imagem para o Docker Hub.

Tecnologias:

Python (Flask): Backend da aplicação.
Docker: Containerização.
GitHub Actions: Pipeline CI/CD.
Pytest: Testes unitários.

Etapas:

Clonei o repositório: git clone https://github.com/seu_usuario/flask-cicd.git
cd flask-cicd.


Instalei dependências: python -m venv venv
source venv/bin/activate
pip install -r requirements.txt.


Executei testes: pytest test_app.py -v.


Construí e executei a imagem Docker: docker build -t flask-cicd:latest .
docker run -p 5000:5000 flask-cicd:latest.


Acessei: http://localhost:5000 ao qual exibiu "hello-world", e confirmou a execução bem-sucedida da etapa acima.

Pipeline CI/CD:

Trigger: Push na branch main.

Etapas:
Checkout do código.
Configuração do Python 3.9.
Execução de testes com Pytest.
Login no Docker Hub.
Build e push da imagem seu_usuario/flask-cicd:latest.



Desafios Superados:

Configurei WSL2 no Windows para evitar problemas com comandos Linux (ex.: grep).
Resolvi erros de pipeline ajustando segredos no GitHub.

