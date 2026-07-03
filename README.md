## 🛠️ Tecnologias utilizadas

<p align="center">
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django">
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
  <img src="https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
</p>

## 🏷️ Sistema de Categorias e Tags

Esta funcionalidade expande o sistema de categorização de mensagens, adicionando um gerenciamento completo de **tags**, permitindo organizar, filtrar e identificar visualmente cada mensagem de forma ainda mais flexível.

<div align="center">

https://github.com/user-attachments/assets/502d00e4-905e-4236-9239-394ab7313d71

</div>

### 📋 O que foi implementado

#### 1. Admin — Seleção de tags com `filter_horizontal`
O painel administrativo agora utiliza o widget **`filter_horizontal`** para o campo de tags.

Em vez do `<select multiple>` padrão, o Django exibe dois painéis lado a lado:

- **Disponíveis**
- **Escolhidas**

Esse componente facilita a seleção de múltiplas tags, tornando o cadastro das mensagens muito mais intuitivo.

---

#### 2. Admin — Listagem de mensagens com filtro por tags
A listagem de mensagens no painel administrativo foi ampliada e agora permite filtrar registros por:

- **Categoria**
- **Tags**

O filtro lateral exibe todas as tags cadastradas, permitindo localizar rapidamente mensagens relacionadas a um determinado assunto.

---

#### 3. Página principal — Hashtags
Cada mensagem agora exibe suas tags em formato de **hashtags**, por exemplo:

`#aviso` `#específico` `#geral`

Caso a mensagem não possua nenhuma tag, o bloco não é renderizado graças à proteção implementada no template:

```django
{% if m.tags.all %}
    {% for tag in m.tags.all %}
        #{{ tag.slug }}
    {% endfor %}
{% endif %}
```

---

### 📚 Conceitos abordados neste roteiro

- Diferença entre **ForeignKey (1:N)** e **ManyToManyField (N:N)**;
- Utilização de **SlugField** como identificador textual amigável;
- Criação automática da tabela de junção pelo **Django ORM**;
- Uso de `blank=True` em `ManyToManyField` (e por que não utilizar `null=True`);
- Configuração do widget `filter_horizontal` no Django Admin;
- Iteração sobre relacionamentos N:N utilizando:

```django
{% for tag in m.tags.all %}
```

- Inserção idempotente de dados utilizando `get_or_create`;
- Navegação da relação em ambos os sentidos com `related_name`;
- Inspeção da estrutura do banco utilizando `dbshell` e comandos SQLite.

</br>

> 🎥 O vídeo acima demonstra todo o fluxo: cadastro de tags → seleção com `filter_horizontal` → associação às mensagens → filtros no painel administrativo → exibição das hashtags na página principal.
