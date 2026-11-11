# 🎨 Art & Criativa — E-commerce de Materiais Artísticos e Escolares

> Projeto prático e acadêmico desenvolvido para a disciplina de **Linguagem de Marcação / Desenvolvimento Web Frontend (LIMA)** — 2º Semestre.

---

## 📌 Sobre o Projeto

O **Art & Criativa** é uma vitrine e fluxo completo de e-commerce voltado para a venda de materiais de arte, pintura, artesanato e papelaria escolar.

O projeto foi dividido em duas grandes etapas:
1. **Parte 1 (Foco em Imagens e CSS3):** Criação da identidade visual, carrossel de promoções, categorias com fotos circulares e vitrine padronizada com filtros e efeitos de hover.
2. **Parte 2 (Expansão e Navegação Multi-Páginas):** Desenvolvimento de um fluxo real de compra com página de produto (galeria e especificações), carrinho de compras com tabela semântica e checkout/cadastro de cliente acessível.

---

## 🚀 Funcionalidades & Páginas

### 1. 🏠 Vitrine Principal (`index certo.html` / `index.html`)
- **Cabeçalho:** Logotipo da loja, barra superior de anúncio, menu de navegação e atalho para o carrinho.
- **Carrossel Promocional:** 3 banners com `<picture>` responsivo e rolagem suave via CSS puro (`scroll-snap-type: x mandatory`).
- **Categorias em Círculo:** 4 departamentos com imagens perfeitamente circulares (`border-radius: 50%`) e efeito `:hover` com borda destacada e leve zoom.
- **Vitrine de Produtos:** Cards semânticos (`<article>`, `<figure>`, `<figcaption>`) com `aspect-ratio: 1 / 1`, zoom suave e identificação de promoções (`-20%`, `-10%`, etc.) e itens esgotados (`filter: grayscale(100%)`).

### 2. 🔍 Página de Detalhes do Produto (`produto.html`)
- **Trilha de Navegação (Breadcrumb):** Mostra o caminho da página (*Início > Categoria > Produto*).
- **Galeria de Fotos:** Foto principal em alta resolução com 4 miniaturas interativas com efeito `:hover`.
- **Painel de Compra:** Título `<h1>`, avaliação com estrelas, preços com destaque de desconto, seletor de opções (`<select>`) e botão de ação para adicionar ao carrinho.
- **Tabela Semântica de Especificações:** Construída com `<table>`, `<tbody>` e `<th scope="row">`, estilizada com efeito zebrado (`:nth-child(even)`).

### 3. 🛒 Carrinho de Compras (`carrinho.html`)
- **Tabela Semântica Completa:** Desenvolvida com `<caption>`, `<thead>`, `<tbody>`, `<tfoot>` e cabeçalhos com `<th scope="col">`.
- **Lista de Produtos:** Exibe miniatura (64x64px), categoria, preço unitário, seletor numérico de quantidade (`<input type="number">`), subtotal e botão de remoção 🗑️.
- **Rodapé da Tabela (`<tfoot>`):** Utiliza `colspan` informando benefício de Frete Grátis acima de R$ 99,00.
- **Card de Resumo (`<aside>`):** Cálculo de subtotal, frete, campo de cupom de desconto com botão "Aplicar" e botão para seguir para o checkout.

### 4. 👤 Cadastro de Cliente & Checkout (`cadastro.html`)
- **Formulário Semântico Acessível:** Todos os campos `<input>` devidamente associados aos seus respectivos `<label for="...">`.
- **Blocos com `<fieldset>` e `<legend>`:**
  - **Bloco 1 (Dados Pessoais):** Nome, E-mail (`email`), CPF (`pattern`), Telefone (`tel`), Data de Nascimento (`date`), Senha (`password`) e upload opcional de avatar (`file`).
  - **Bloco 2 (Endereço de Entrega):** CEP, Rua, Número, Complemento, Bairro, Cidade e Estado com `<select>`.
  - **Bloco 3 (Pagamento):** Seleção via `<input type="radio">` com ícones visuais para PIX ⚡, Cartão de Crédito 💳 e Boleto 📄.
- **Validação e Pseudo-classes:**
  - `:focus`: Destaque com brilho lilás ao selecionar o campo.
  - `:focus:valid`: Borda verde suave indicando dado preenchido corretamente.
  - `:focus:invalid`: Borda vermelha suave sinalizando campo obrigatório pendente.
- **Termos de Uso:** Checkbox obrigatória antes do envio final.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5 Semântico:** `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<figcaption>`, `<table>`, `<fieldset>`, `<legend>`, `<aside>`, `<footer>`.
- **CSS3 Moderno:**
  - Layouts responsivos com **Flexbox** e **CSS Grid**;
  - Padronização e enquadramento de imagens com `aspect-ratio` e `object-fit: cover`;
  - Filtros visuais (`filter: grayscale()`, `opacity`);
  - Transições suaves e animações de hover (`transform: scale()`);
  - Rolagem por toque/snap (`scroll-snap-type`);
  - Pseudo-classes (`:hover`, `:focus`, `:valid`, `:invalid`, `:checked`, `:nth-child`).
- **MySQL (Banco de Dados):** Script relacional com criação de tabelas (`categoria`, `produto`), controle de estoque, status de promoção e consultas de verificação (`SELECT`).

---

## 📁 Estrutura de Arquivos

```text
E-commerce/
├── fotos/                       # Imagens de banners, produtos, logos e categorias
├── index certo.html             # Vitrine principal da loja
├── produto.html                 # Página de detalhes e especificações do produto
├── carrinho.html                # Tabela do carrinho e resumo do pedido
├── cadastro.html                # Formulário acessível de cadastro e checkout
├── style certo.css              # Folha de estilos unificada
├── ecommerce_artes.sql          # Script de banco de dados MySQL
└── README.md                    # Documentação do projeto
```
## 🌐 Links das Páginas Publicadas (GitHub Pages)
- 🏠 [Vitrine Principal (index.html)](https://isafrsilva.github.io/E-commerce-Isabela-Artes-/index.html)
- 🔍 [Detalhes do Produto (produto.html)](https://isafrsilva.github.io/E-commerce-Isabela-Artes-/produto.html)
- 🛍️ [Carrinho de Compras (carrinho.html)](https://isafrsilva.github.io/E-commerce-Isabela-Artes-/carrinho.html)
- 👤 [Cadastro e Checkout (cadastro.html)](https://isafrsilva.github.io/E-commerce-Isabela-Artes-/cadastro.html)

---

## ✅ Relatório de Conformidade W3C (Clique para Auditar em Tempo Real)

Todas as páginas deste repositório foram inspecionadas e validadas com **Zero Erros** nos validadores oficiais do consórcio W3C:


---

## 👩‍💻 Autora

- **Isabela** — Estudante de Desenvolvimento Web / 2º Semestre

