# README — Aprendizado e Estrutura do Sistema Musical

O projeto **Sistema Musical** foi desenvolvido como uma interface *front-end* completa utilizando HTML5 e CSS3, estruturada para servir de base a um sistema web dinâmico de gestão de artistas e faixas musicais.

---

## 🎯 Objetivos de Aprendizagem

Esse projeto abordou a construção incremental de uma aplicação web, cobrindo os seguintes conceitos fundamentais:

* **HTML5 Semântico e Acessibilidade:** Uso de tags semânticas (`<head>`, `<body>`, `<form>`, `<table>`, `<label>`, `<select>`), configuração do *viewport*, tabelas acessíveis e atributos de auxílio aos utilizadores (`autocomplete`, `required`, `placeholder`, `target="_blank"`).
* **Arquitetura CSS Global e Variáveis:** Utilização de `:root` para centralização da paleta de cores e espaçamentos, regras de *reset* global (`box-sizing: border-box`), reutilização de estilos em múltiplas páginas através de um único ficheiro `styles.css`.
* **Layouts Modernos (Flexbox e CSS Grid):** Centralização absoluta no ecrã de *login*, grelhas responsivas com `repeat(auto-fit, minmax(...))` no menu principal e formulários divididos em duas colunas com `grid-template-columns`.
* **Formulários e Manipulação de Ficheiros:** Integração de tipos avançados de entrada (`url`, `password`, `file`), suporte a *upload* de imagens com `enctype="multipart/form-data"` e agrupamento visual de campos.
* **Componentização de UI:** Criação de botões reutilizáveis, cartões com efeito *hover*, miniaturas de imagem com *fallback* visual (`.no-image`), tabelas estilizadas e barras de filtro.



---

## 📁 Estrutura das Páginas e Conteúdos Aprendidos

* **Autenticação (`login.html`):** Construção de um cartão de entrada centralizado vertical e horizontalmente através do Flexbox. Demonstra o uso de formulários `POST`, campos de texto/palavra-passe obrigatórios e caixas de aviso com credenciais de teste.


* **Painel Principal (`index.html`):** Menu de navegação baseado em CSS Grid (`auto-fit`), permitindo um *layout* responsivo que ajusta automaticamente a quantidade de cartões por linha. Inclui barra superior (*topbar*) com botão de encerramento de sessão e cartões de acesso rápido.


* **Gestão de Artistas (`cadastro_artista.html`):** Estruturação de formulários em grelha de duas colunas, envio de ficheiros multimédia (fotos) com o atributo `enctype`, e listagem dos registos existentes com ações rápidas de edição, remoção e navegação.


* **Gestão de Músicas (`cadastro_musica.html`):** Formulário complexo com seleção de artista (`<select>`), hiperligação para o YouTube (`type="url"`), área de texto expansível para letras (`textarea`) ocupando a largura total (`grid-column: 1 / -1`) e tabela de faixas cadastradas.


* **Biblioteca Musical (`listagem_musicas.html`):** Implementação de uma área de pesquisa e filtragem (`GET`) com tabelas completas de dados, miniaturas de capas, botões de ação estilizados e abertura de vídeos externos em novo separador do navegador (`target="_blank"`).



---

## 🎨 Sistema de Estilos (`styles.css`)

O ficheiro CSS foi desenvolvido de forma modular e progressiva, dividido em 4 etapas de aprendizagem:

| Módulo / Aula | Conceitos Aplicados |
| --- | --- |
| **Aula 1: Base e Estrutura** | Variáveis CSS (`:root`), *reset* universal, estilo base de formulários, botões primários, página de *login* e grelha do menu principal. |
| **Aula 2: Componentes e Tabelas** | Tipografia (`h2`), barra de cabeçalho (`.page-header-bar`), variações de cores de botões (`.btn-edit`, `.btn-delete`, `.btn-youtube`), estilização de tabelas e zona de filtros. |
| **Aula 3: Formulários em Grelha** | Formulários em duas colunas (`.form-grid`), estilização de campos do tipo `file`, legendas assistivas (`small`), botão para músicas e pré-visualização de fotos. |
| **Aula 4: Campos Especiais e Ajustes** | Estilização de `textarea` e `input[type="url"]`, classe utilitária de largura total (`.form-group.full`) e regras de responsividade.

 |

---

## 🔮 Preparação para a Integração Back-end

A estrutura *front-end* desenvolvida inclui os requisitos necessários para integração com PHP e bases de dados relacionais:

* **Métodos HTTP:** Separação entre envios de dados e ficheiros via `method="post"` e envio de parâmetros de pesquisa/filtragem via `method="get"`.
* **Identificação de Campos:** Todos os elementos de formulário possuem o atributo `name` configurado de acordo com a nomenclatura da base de dados (ex.: `artista_id`, `youtube_link`, `letra`).
* **Estrutura de Tabelas:** As tabelas contêm marcas de posição (*placeholders*) prontas para serem substituídas por laços de repetição dinamizados por código *server-side*.
