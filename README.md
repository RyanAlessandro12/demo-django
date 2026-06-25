## 🛠️ Tecnologias utilizadas

<p align="center">
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django">
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
  <img src="https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
</p>


## 🖥️ Página inicial

<p align="center">
  <img src="imagen principal.png" alt="Página inicial" width="700">
</p>

<p align="center">
  <em>Página inicial do projeto com o tema visual modificado (gradiente em tons de esmeralda/teal).</em>
</p>

## 📝 Cadastro de mensagem no admin

<p align="center">
  <img src="prueba de mensaje.png" alt="Cadastro de mensagem" width="700">
</p>

<p align="center">
  <em>Formulário de cadastro de mensagem no painel administrativo, com o campo <code>autor</code> adicionado.</em>
</p>

## ℹ️ Página Sobre

<p align="center">
  <img src="sobre.png" alt="Página Sobre" width="700">
</p>

<p align="center">
  <em>Nova página <code>/sobre/</code> criada com informações sobre o projeto.</em>
</p>

## ▶️ Como executar o projeto

```bash
git clone 
cd demo-django
docker compose up --build
```

Acesse **http://localhost:8000** no navegador.

## 🔑 Acesso ao admin

Após criar o superusuário, acesse **http://localhost:8000/admin/** para gerenciar as mensagens.

## 📋 Funcionalidades implementadas

- **Página inicial** com listagem de mensagens do banco de dados SQLite
- **Tema visual** modificado com gradiente em tons de esmeralda/teal
- **Campo `autor`** adicionado ao modelo `Mensagem`
- **Página `/sobre/`** com informações estáticas sobre o projeto
- **Painel administrativo** do Django para gerenciar o conteúdo