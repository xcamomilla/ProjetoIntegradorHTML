## Registro de Uso de Inteligência Artificial Generativa (Entrega 1)

Em conformidade com a Seção 5 da especificação do Projeto Integrador, apresenta-se abaixo o mapeamento de uso, o prompt utilizado e a revisão técnica realizada pelo estudante.

### 1. Mapeamento de Uso
* **Desenvolvimento Autoral (Estudante):** Toda a codificação e estruturação em HTML5 puro das 4 páginas (`index.html`, `cardapio.html`, `sobre.html` e `contato.html`), incluindo a definição dos landmarks semânticos (`header`, `nav`, `main`, `section`, `article`, `aside`, `footer`), hierarquia de cabeçalhos (`h1` a `h3`), navegação interna, tabelas e formulário com validação nativa.
* **Apoio de IA Generativa:** Utilizado estritamente para a geração de conteúdo textual fictício (história da Confeitaria Doce Encanto, descrições gastronômicas dos doces, preços, endereço e horários) e sugestões de descrições visuais para imagens (`alt` e `figcaption`).

### 2. Prompts Utilizados

**Prompt Único:**
> "Estou desenvolvendo do zero o código em HTML5 semântico para o meu Projeto Integrador da faculdade sobre uma confeitaria chamada 'Confeitaria Doce Encanto — Confeitaria Artesanal desde 2015', localizada no bairro Jardim Europa, em São Paulo/SP. Eu mesmo vou programar toda a estrutura HTML das 4 páginas (Início, Cardápio, Sobre e Localização, e Contato e Encomendas), portanto NÃO gere código HTML. Preciso que você crie apenas os textos fictícios e as referências de imagens para eu inserir nas minhas tags:
> 1. Para a página 'Início': texto de boas-vindas, 3 destaques da vitrine com descrição e preço, 3 diferenciais da confeitaria, 2 depoimentos de clientes e uma nota de especial sazonal do mês.
> 2. Para a página 'Cardápio': descrições gastronômicas e preços divididos em Bolos Festivos, Tortas Clássicas e Brigadeiros/Doces Finos, além dos dados textuais para uma tabela de tamanhos, pesos, rendimento em fatias e antecedência mínima, mais um aviso sobre alérgenos.
> 3. Para a página 'Sobre e Localização': a história da Confeitaria Doce Encanto nascida em 2015 a partir do caderno de receitas de Dona Helena (avó da chef confeiteira Clara Mendes), nosso compromisso com ingredientes naturais (fava de baunilha, caramelo no tacho de cobre e morangos do interior paulista), endereço na Rua das Magnólias, 245 (Jardim Europa, São Paulo/SP), horários de atendimento de terça a domingo, e 3 práticas de sustentabilidade (embalagens FSC biodegradáveis, ovos de galinhas livres de gaiolas e compostagem).
> 4. Para a página 'Contato e Encomendas': textos de apoio com os campos necessários para um formulário de orçamento/reserva, canais de atendimento rápido — telefone (11) 99876-5432 e e-mail atendimento@doceencanto.com.br — e regras de encomenda.
> 5. Imagens: para cada produto do catálogo e foto do ateliê, sugira um nome de arquivo (.jpg), uma frase curta de legenda (para <figcaption>) e uma descrição visual detalhada da cena (para o atributo alt de acessibilidade)."

### 3. Revisão Técnica (Modificações Realizadas pelo Estudante)

#### Alteração 1: Refinamento dos textos alternativos (`alt`) para acessibilidade em leitores de tela
* **O que a IA gerou:** Descrições visuais iniciadas por termos redundantes, como *"Foto da cozinha do ateliê da Confeitaria Doce Encanto no Jardim Europa..."* e *"Imagem de uma fatia de bolo Red Velvet..."*.
* **O que foi alterado:** Remoção das expressões *"Foto de"* e *"Imagem de"* ao passar os textos para o atributo `alt` das tags `<img>`, descrevendo diretamente o conteúdo visual e reservando o contexto complementar para a tag `<figcaption>` (ex.: `<figcaption>Preparo diário na cozinha do nosso ateliê no Jardim Europa.</figcaption>`).
* **Por que foi alterado:** Leitores de tela já anunciam nativamente a tag `<img>` como "imagem" ou "gráfico". Manter a palavra "Foto" ou "Imagem" no `alt` causa repetição desnecessária para usuários com deficiência visual e descumpre o checklist de acessibilidade.

#### Alteração 2: Marcação semântica de endereço, contatos e horários na página Sobre (`sobre.html`)
* **O que a IA gerou:** O endereço (Rua das Magnólias, 245 — Jardim Europa, São Paulo/SP), telefone `(11) 99876-5432`, e-mail `atendimento@doceencanto.com.br` e a lista de horários de funcionamento em formato de texto simples.
* **O que foi alterado:** Envolvimento dos dados de localização e contato na tag semântica `<address>`, conversão do telefone e e-mail em links acionáveis (`href="tel:+5511998765432"` e `href="mailto:atendimento@doceencanto.com.br"`), e estruturação da seção "Sustentabilidade e Comunidade Local" dentro de um landmark `<aside>`.
* **Por que foi alterado:** O uso de `<address>` e protocolos `tel:`/`mailto:` fornece significado semântico real para navegadores e tecnologias assistivas, enquanto o uso de `<aside>` separa corretamente o conteúdo complementar de sustentabilidade da narrativa histórica principal dentro de `<main>`.

#### Alteração 3: Conversão das perguntas de encomenda em controles de formulário com validação HTML5 nativa (`contato.html`)
* **O que a IA gerou:** Uma relação textual simples das informações necessárias para encomendar doces ou reservar mesa (nome, e-mail, WhatsApp, data, horário, produto e restrições alimentares).
* **O que foi alterado:** Criação da estrutura de formulário dividida em blocos `<fieldset>` e `<legend>`, associação explícita entre `<label for="...">` e `id`, e adição de restrições nativas do HTML5 (`required`, `type="email"`, `type="tel"` com atributo `pattern`, `type="date"` e `type="time"` com limites `min` e `max` compatíveis com o horário de atendimento da loja).
* **Por que foi alterado:** Para atender ao requisito obrigatório de formulário funcional sem uso de JavaScript, garantindo validação automática pelo navegador e navegação completa via teclado (tecla `Tab`).