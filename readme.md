# Projeto Integrador — Interface Web com HTML e CSS

## Tema: Confeitaria Doce Encanto — Confeitaria Artesanal desde 2015 (Pequeno Negócio Local)

### 1. Sobre o Projeto (Entrega 1 — Esqueleto Semântico)

Este repositório contém a **Entrega 1 (Bloco 2: HTML Estrutural)** do Projeto Integrador da disciplina de Interface Web com HTML e CSS. O projeto segue a sugestão de tema nº 2 (*Site de pequeno negócio local*) e consiste no site institucional, cardápio e canal de encomendas da **Confeitaria Doce Encanto**, localizada no bairro Jardim Europa, em São Paulo/SP.

Nesta primeira entrega (`branch`/`tag`: `entrega-1`), o projeto é composto exclusivamente por **HTML5 puro e semântico**, sem qualquer utilização de CSS, priorizando a arquitetura da informação, a semântica estrutural, a hierarquia de títulos, a navegação interna funcional e o checklist de acessibilidade.

---

### 2. Estrutura de Arquivos do Repositório

```text
├── index.html       # Página Inicial (Home): Boas-vindas, destaques da vitrine, diferenciais, depoimentos e especial sazonal
├── cardapio.html    # Cardápio e Catálogo: Bolos festivos, tortas, brigadeiros/doces finos, tabela de rendimento e alérgenos
├── sobre.html       # Sobre e Localização: História desde 2015, ingredientes, endereço, horários e sustentabilidade
├── contato.html     # Contato e Encomendas: Formulário com validação nativa HTML5, canais diretos e política de pedidos
└── README.md        # Documentação técnica do projeto e Registro de Uso de IA Generativa
```

---

### 3. Checklist Técnico Cumprido (Entrega 1)

* [x] **Mínimo de 4 páginas HTML distintas** conectadas por navegação interna coerente (`index.html`, `cardapio.html`, `sobre.html`, `contato.html`).
* [x] **HTML5 Puro (Sem CSS):** Ausência total de folhas de estilo externas, tags `<style>` ou atributos `style` inline.
* [x] **Landmarks Semânticos em todas as páginas:** Uso estruturado de `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>` e `<footer>`.
* [x] **Hierarquia Lógica de Headings:** Uso de `<h1>` único por página descrevendo o conteúdo principal, seguido por `<h2>` e `<h3>` sem saltos de nível.
* [x] **Checklist de Acessibilidade Aplicado:**
  * Declaração de idioma `<html lang="pt-BR">` em todas as páginas.
  * *Skip link* (`<a href="#conteudo-principal">Pular para o conteúdo principal</a>`) funcional logo após a abertura da tag `<body>`.
  * Atributos `aria-label`, `aria-labelledby` e `aria-current="page"` para orientar leitores de tela.
  * Imagens estruturadas com `<figure>`, `<figcaption>` e atributo `alt` descritivo.
  * Tabelas semânticas com `<caption>`, `<thead>`, `<tbody>` e `<th scope="col|row">`.
  * Formulário navegável via teclado (`Tab`) com `<label for="...">`, `<fieldset>`, `<legend>` e validação nativa do HTML5 (`required`, `type="email"`, `type="tel"`, `pattern`, `min`, `max`).

---

## 4. Registro de Uso de Inteligência Artificial Generativa (Entrega 1)

Em conformidade com a **Seção 5 (Política de Uso de Inteligência Artificial Generativa)** da especificação do Projeto Integrador, declara-se abaixo o mapeamento de uso, o prompt utilizado e a revisão técnica realizada pelo estudante.

### 4.1. Mapeamento de Uso

* **Desenvolvimento Autoral (Estudante):** Toda a codificação e estruturação em HTML5 puro das 4 páginas (`index.html`, `cardapio.html`, `sobre.html` e `contato.html`), incluindo a escolha e aplicação dos landmarks semânticos (`header`, `nav`, `main`, `section`, `article`, `aside`, `footer`), hierarquia de cabeçalhos (`h1` a `h3`), navegação interna, estruturação de tabelas e construção do formulário com validação nativa.
* **Apoio de IA Generativa:** Utilizado estritamente para a geração de conteúdo textual fictício (história da Confeitaria Doce Encanto, descrições gastronômicas dos doces, preços fictícios, endereço e horários) e sugestões de descrições visuais para imagens (`alt` e `figcaption`).

### 4.2. Prompts Utilizados

**Prompt Único:**
> "Estou desenvolvendo do zero o código em HTML5 semântico para o meu Projeto Integrador da faculdade sobre uma confeitaria chamada 'Confeitaria Doce Encanto — Confeitaria Artesanal desde 2015', localizada no bairro Jardim Europa, em São Paulo/SP. Eu mesmo vou programar toda a estrutura HTML das 4 páginas (Início, Cardápio, Sobre e Localização, e Contato e Encomendas), portanto NÃO gere código HTML. Preciso que você crie apenas os textos fictícios e as referências de imagens para eu inserir nas minhas tags:
> 1. Para a página 'Início': texto de boas-vindas, 3 destaques da vitrine com descrição e preço, 3 diferenciais da confeitaria, 2 depoimentos de clientes e uma nota de especial sazonal do mês.
> 2. Para a página 'Cardápio': descrições gastronômicas e preços divididos em Bolos Festivos, Tortas Clássicas e Brigadeiros/Doces Finos, além dos dados textuais para uma tabela de tamanhos, pesos, rendimento em fatias e antecedência mínima, mais um aviso sobre alérgenos.
> 3. Para a página 'Sobre e Localização': a história da Confeitaria Doce Encanto nascida em 2015 a partir do caderno de receitas de Dona Helena (avó da chef confeiteira Clara Mendes), nosso compromisso com ingredientes naturais (fava de baunilha, caramelo no tacho de cobre e morangos do interior paulista), endereço na Rua das Magnólias, 245 (Jardim Europa, São Paulo/SP), horários de atendimento de terça a domingo, e 3 práticas de sustentabilidade (embalagens FSC biodegradáveis, ovos de galinhas livres de gaiolas e compostagem).
> 4. Para a página 'Contato e Encomendas': textos de apoio com os campos necessários para um formulário de orçamento/reserva, canais de atendimento rápido — telefone (11) 99876-5432 e e-mail atendimento@doceencanto.com.br — e regras de encomenda.
> 5. Imagens: para cada produto do catálogo e foto do ateliê, sugira um nome de arquivo (.jpg), uma frase curta de legenda (para `<figcaption>`) e uma descrição visual detalhada da cena (para o atributo `alt` de acessibilidade)."
### 4.3. Revisão Técnica (Modificações Realizadas pelo Estudante)

#### Alteração 1: Refinamento dos textos alternativos (`alt`) para acessibilidade em leitores de tela
* **O que a IA gerou:** Descrições visuais iniciadas por termos redundantes, como *"Foto da cozinha do ateliê da Confeitaria Doce Encanto no Jardim Europa..."* e *"Imagem de uma fatia de bolo Red Velvet..."*.
* **O que foi alterado:** Remoção das expressões *"Foto de"* e *"Imagem de"* ao passar os textos para o atributo `alt` das tags `<img>`, descrevendo diretamente o conteúdo visual e reservando o contexto complementar para a tag `<figcaption>` (ex.: `<figcaption>Preparo diário na cozinha do nosso ateliê no Jardim Europa.</figcaption>`).
* **Por que foi alterado (Justificativa Técnica):** Leitores de tela já anunciam nativamente a tag `<img>` como "imagem" ou "gráfico". Manter a palavra "Foto" ou "Imagem" no atributo `alt` causa repetição auditiva desnecessária para usuários com deficiência visual e descumpre o checklist de acessibilidade (WCAG).

#### Alteração 2: Marcação semântica de endereço, contatos e seção lateral na página Sobre (`sobre.html`)
* **O que a IA gerou:** O endereço (*Rua das Magnólias, 245 — Bairro Jardim Europa, São Paulo/SP*), telefone *(11) 99876-5432*, e-mail *atendimento@doceencanto.com.br* e a lista de práticas de sustentabilidade entregues como texto corrido comum.
* **O que foi alterado:** Envolvimento dos dados de localização e contato na tag semântica `<address>`, conversão do telefone e e-mail em links acionáveis (`href="tel:+5511998765432"` e `href="mailto:atendimento@doceencanto.com.br"`), e estruturação do bloco "Sustentabilidade e Comunidade Local" dentro de um landmark `<aside>`.
* **Por que foi alterado (Justificativa Técnica):** O uso de `<address>` e protocolos `tel:`/`mailto:` fornece significado semântico real para navegadores e tecnologias assistivas, enquanto o uso de `<aside>` separa corretamente o conteúdo complementar de sustentabilidade da narrativa histórica principal dentro de `<main>`.

#### Alteração 3: Conversão dos itens de pedido em formulário estruturado com validação HTML5 nativa (`contato.html`)
* **O que a IA gerou:** Uma relação textual simples das informações necessárias para encomendar doces ou reservar mesa (nome, e-mail, WhatsApp, data, horário, produto e restrições alimentares).
* **O que foi alterado:** Criação da estrutura de formulário dividida em blocos `<fieldset>` e `<legend>`, associação explícita entre `<label for="...">` e `id`, e adição de restrições nativas do HTML5 (`required`, `type="email"`, `type="tel"` com atributo `pattern`, `type="date"` e `type="time"` com limites `min` e `max` compatíveis com o horário de atendimento da loja).
* **Por que foi alterado (Justificativa Técnica):** Para atender ao requisito obrigatório de formulário funcional sem uso de JavaScript, garantindo validação automática de formato pelo próprio navegador e navegação completa via teclado (tecla `Tab`).

---

### 5. Como Visualizar o Projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git
   ```
2. Acesse a branch ou tag correspondente à primeira entrega:
   ```bash
   git checkout entrega-1
   ```
3. Abra o arquivo `index.html` diretamente em qualquer navegador web.