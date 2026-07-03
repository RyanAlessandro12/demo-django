## 🛠️ Tecnologias utilizadas

<p align="center">
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django">
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
  <img src="https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
</p>

## 🖥️ Página inicial

## 🏷️ Sistema de Categorias

Esta funcionalidade adiciona um sistema completo de **categorização de mensagens**, permitindo organizar, filtrar e identificar visualmente o tipo de cada mensagem.

<div align="center">

https://github.com/user-attachments/assets/0efbaeaa-e658-4e33-aae9-2c5f30eba948

</div>

### 📋 O que foi implementado

#### 1. Admin — Listagem de mensagens com coluna Categoria e filtro lateral
Após a `migration`, o painel administrativo passou a exibir:
- Uma nova coluna **Categoria** na listagem de mensagens;
- Um **filtro lateral** que permite filtrar as mensagens por categoria diretamente no admin.

#### 2. Admin — Cadastro de Categorias
Foi criada uma nova seção no painel admin para **criar e gerenciar categorias**, por exemplo:
- Aviso
- Dúvida
- Sugestão

#### 3. Página principal — Selos de categoria
Na página principal, cada mensagem agora exibe um **selo (badge) colorido** com o nome da sua categoria.

Mensagens sem categoria **não exibem o selo**, graças à proteção implementada no template:

```django
{% if m.categoria %}
  <span class="badge">{{ m.categoria }}</span>
{% endif %}
```

</br>

> 🎥 O vídeo acima demonstra o fluxo completo: cadastro de categoria no admin → associação com uma mensagem → exibição do selo colorido na página principal.
