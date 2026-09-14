# 🌐 Semântica Web & Validações Nativas em HTML5

Projeto prático focado na aplicação das melhores práticas de **HTML5 Semântico**, **Acessibilidade Web (a11y)**, estruturação moderna e **Validações Nativas de Formulários** sem dependência inicial de bibliotecas externas ou scripts adicionais.

---

## 📌 Sumário

- [Sobre o Projeto](#-sobre-o-projeto)
- [Estrutura de Arquivos](#-estrutura-de-arquivos)
- [Páginas do Projeto](#-páginas-do-projeto)
  - [1. Página Institucional (`index.html`)](#1-página-institucional-indexhtml)
  - [2. Formulário com Validações Nativas (`formulario.html`)](#2-formulário-com-validações-nativas-formulariohtml)
- [Conceitos e Recursos Demonstrados](#-conceitos-e-recursos-demonstrados)
  - [Tags Semânticas Utilizadas](#tags-semânticas-utilizadas)
  - [Validações e Atributos de Entrada](#validações-e-atributos-de-entrada)
  - [Acessibilidade e SEO](#acessibilidade-e-seo)
- [Como Executar o Projeto](#-como-executar-o-projeto)
- [Autor](#-autor)

---

## 📖 Sobre o Projeto

O objetivo deste repositório é servir como referência sólida sobre:
1. Como estruturar uma página corporativa moderna utilizando exclusivamente tags semânticas da especificação HTML5, promovendo clareza para mecanismos de busca (SEO) e leitores de tela.
2. Como implementar formulários completos e robustos aproveitando os recursos nativos do navegador para validação client-side (como padrões regex com `pattern`, restrições de tamanho com `minlength`/`maxlength`, intervalos com `min`/`max`, e tipos semânticos de entrada).

---

## 📂 Estrutura de Arquivos

```text
Semantica/
├── index.html        # Página institucional completa da empresa fictícia "TechInova Soluções"
├── formulario.html   # Página com formulário avançado e testes de validações nativas do HTML5
└── README.md         # Documentação completa do projeto
```

---

## 📄 Páginas do Projeto

### 1. Página Institucional (`index.html`)
Representa o portal web da **TechInova Soluções Tecnológicas**, contendo:
- **Cabeçalho (`<header>`):** Identificação e menu de navegação (`<nav>`) com âncoras para seções internas e link para o exercício de formulário.
- **Seção Hero (`<section id="inicio">`):** Apresentação do propósito da empresa e CTA (Call to Action).
- **Sobre Nós (`<section id="sobre">`):** Linha do tempo (`<time>`), missão, visão e valores, além de imagem com legenda semântica (`<figure>` e `<figcaption>`).
- **Serviços (`<section id="servicos">`):** Artigos independentes (`<article>`) para cada especialidade (Desenvolvimento sob medida, Cloud/DevOps e Segurança da Informação).
- **Diferenciais (`<section id="diferenciais">`):** Lista ordenada com os pontos fortes do negócio.
- **Depoimentos (`<section id="depoimentos">`):** Citações e depoimentos de clientes utilizando `<blockquote>` e `<cite>`.
- **Formulário de Contato (`<section id="contato">`):** Formulário completo para solicitação de propostas e orçamento.
- **Barra Lateral (`<aside>`):** Horários de funcionamento e certificações da empresa.
- **Rodapé (`<footer>`):** Dados cadastrais e de contato delimitados por `<address>` e nota de copyright.

### 2. Formulário com Validações Nativas (`formulario.html`)
Página de exercícios e testes práticos dedicada a explorar as capacidades nativas do HTML5:
- **1. Dados Pessoais:**
  - Nome completo com restrição de caracteres (`minlength="3"`, `maxlength="60"`).
  - Data de nascimento (`type="date"`) com controle de datas mínima e máxima (`min="1920-01-01"`, `max="2010-12-31"`).
  - CPF com máscara e validação por regex (`pattern="\d{3}\.\d{3}\.\d{3}-\d{2}|\d{11}"`).
  - Seleção de gênero via botões de rádio (`type="radio"`).
- **2. Dados de Contato e Acesso:**
  - E-mail com validação de formato (`type="email"`).
  - Celular (`type="tel"`) com regex para 10 ou 11 dígitos.
  - Senha forte (`type="password"`) com validação via regex (`(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}`) exigindo no mínimo 8 caracteres, uma letra maiúscula, uma minúscula e um número.
- **3. Interesses e Mensagem:**
  - Dropdown com seleção obrigatória (`<select required>`).
  - Campo numérico (`type="number"`) com `min="0"`, `max="50"` e `step="1"`.
  - Área de texto (`<textarea>`) com limites de caracteres (`minlength="15"`, `maxlength="500"`).
- **4. Termos e Confirmação:**
  - Checkboxes obrigatórios e opcionais (concordância com termos de uso/LGPD e recebimento de novidades).
- **Ações:**
  - Botões semânticos para envio (`type="submit"`) e redefinição (`type="reset"`).

---

## 💡 Conceitos e Recursos Demonstrados

### Tags Semânticas Utilizadas
| Tag | Finalidade |
|---|---|
| `<header>` | Cabeçalho introdutório da página ou de seções |
| `<nav>` | Conjunto de links para navegação principal ou secundária |
| `<main>` | Conteúdo principal e exclusivo do documento |
| `<section>` | Seções temáticas e agrupamentos lógicos de conteúdo |
| `<article>` | Conteúdo autossuficiente e distribuível |
| `<aside>` | Informações tangenciais ou complementares ao conteúdo principal |
| `<figure>` / `<figcaption>` | Ilustrações, diagramas ou fotos com suas respectivas legendas |
| `<blockquote>` / `<cite>` | Citações diretas e referência/autoria da fonte |
| `<time>` | Representação semântica de datas e horários legíveis por máquinas |
| `<address>` | Informações de contato do autor ou organização |
| `<fieldset>` / `<legend>` | Agrupamento visual e semântico de campos de formulário |
| `<footer>` | Rodapé com créditos, termos e dados institucionais |

### Validações e Atributos de Entrada
- `required`: Torna o preenchimento do campo obrigatório antes da submissão.
- `pattern`: Aplica expressões regulares (Regex) para validação client-side nativa.
- `min` / `max`: Delimita valores mínimos e máximos permitidos para datas e números.
- `minlength` / `maxlength`: Controla a extensão textual mínima e máxima permitida.
- `autocomplete`: Auxilia no preenchimento automático pelo navegador (e.g. `name`, `email`, `tel`).
- `placeholder`: Dica contextual sobre o formato esperado do dado.
- `title`: Mensagem de auxílio exibida em caso de inconsistência com a validação.

### Acessibilidade e SEO
- Associação explícita entre rótulos e controles através de `<label for="...">` e `id="..."`.
- Marcação de landmarks para navegadores e leitores de tela com `aria-label`.
- Hierarquia lógica de títulos (`<h1>` a `<h3>`) sem pular níveis de conteúdo.
- Textos alternativos (`alt`) descritivos em elementos visuais.

---

## 🚀 Como Executar o Projeto

Como este é um projeto baseado em HTML5 nativo, nenhuma instalação de dependências ou build é necessária:

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/Luizssj21/Semantica.git
   ```
2. **Acesse a pasta do projeto:**
   ```bash
   cd Semantica
   ```
3. **Abra os arquivos no navegador:**
   - Dê um duplo clique diretamente em `index.html` ou `formulario.html`.
   - Ou utilize a extensão **Live Server** no VS Code para recarregamento automático durante a edição.

---

## 👤 Autor

Desenvolvido por **[Luiz Fernando](https://github.com/Luizssj21)**.