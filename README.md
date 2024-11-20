<p align="center">
  <a href="https://github.com/Edu-png">
    <img src="https://img.shields.io/badge/Autor-Eduardo%20Coqueiro-purple?style=flat&logo=github" alt="Autor">
  </a>
  <a href="mailto:eduardocoqueiro@gmail.com">
    <img src="https://img.shields.io/badge/Email-eduardocoqueiro%40gmail.com-purple?style=flat&logo=gmail" alt="Email">
  </a>
  <a href="https://linkedin.com/in/eduardocoqueiro/">
    <img src="https://img.shields.io/badge/LinkedIn-Eduardo%20Coqueiro-purple?style=flat&logo=linkedin" alt="LinkedIn">
  </a>
  <a href="https://kaggle.com/EduardoCoqueiro">
    <img src="https://img.shields.io/badge/Kaggle-Eduardo%20Coqueiro-blue?style=flat&logo=kaggle" alt="Kaggle">
  </a>
</p>

---
# 📝 Simple Sentiment Text Analysis: Análise de Sentimentos em Textos 📊

![CAPAS - PROJETOS (8)](https://github.com/user-attachments/assets/9e7cdc68-44ba-465a-9d22-248b753ffd14)

## 📋 Sumário
1. [Resumo 📄](#-resumo-)
2. [Introdução ☀](#-introdução-☀)
   - [Objetivo 🎯](#objetivo-)
3. [Pipeline do Projeto 🛠](#pipeline-do-projeto-)
4. [Metodologia 🧪](#metodologia-)
5. [Resultados e Conclusões 📊](#resultados-e-conclusões-)
   - [Resultados ✨](#resultados-✨)
   - [Conclusões 🚀](#conclusões-🚀)
6. [Considerações Finais 🚀](#considerações-finais-)
7. [Agradecimentos 🙏](#agradecimentos-🙏)
8. [Contato 📞](#-contato)

---

## Resumo 📄

Este projeto foi desenvolvido com o objetivo de realizar uma análise de sentimento simples em textos utilizando bibliotecas de Python como `TextBlob` e `newspaper3k`. A análise de sentimento permite identificar o tom emocional de um texto, classificando-o como positivo, negativo ou neutro.

Durante o projeto, foram abordadas as seguintes etapas:

- **Análise de textos obtidos online:** Um artigo da Wikipédia foi utilizado como exemplo de texto neutro.
- **Tradução e análise de textos personalizados:** Mensagens de autoria própria podem ser inseridas para identificar sua tonalidade emocional.
- **Medição de polaridade:** A polaridade de um texto varia de -1 (negativo) a 1 (positivo), permitindo a interpretação de sentimentos expressos no conteúdo.

Esse projeto demonstra como ferramentas de processamento de linguagem natural (NLP) podem ser utilizadas para entender melhor a intenção por trás de textos e mensagens.

## Introdução ☀

A análise de sentimento é uma técnica essencial no campo do Processamento de Linguagem Natural (NLP), amplamente utilizada em diversas áreas, como marketing, suporte ao cliente e análise de redes sociais. Essa técnica permite identificar e classificar as emoções expressas em um texto, determinando se o conteúdo é positivo, negativo ou neutro. Com isso, é possível obter insights valiosos sobre a percepção de consumidores, avaliar o tom de notícias, ou mesmo compreender as nuances emocionais em textos autorais.

Este projeto busca demonstrar, de forma prática e acessível, como realizar uma análise de sentimento utilizando o Python e bibliotecas como `TextBlob` e `newspaper3k`. A proposta inclui explorar artigos online e textos personalizados para calcular a polaridade do sentimento, fornecendo uma introdução direta e didática à aplicação de NLP.

### Objetivo 🎯

1. **Explorar o uso de técnicas de NLP em diferentes contextos:**
   - Analisar o sentimento de textos retirados de fontes online, como artigos da Wikipedia.
   - Avaliar textos autorais fornecidos pelo usuário, criando um ambiente prático e dinâmico.

2. **Demonstrar o uso de ferramentas práticas para análise de sentimento:**
   - Utilizar a biblioteca `TextBlob` para calcular a polaridade de sentimentos com base em textos em inglês.
   - Aplicar a `newspaper3k` para coletar e processar artigos diretamente da web, simplificando a extração de conteúdo.

3. **Facilitar o processamento de idiomas diversos:**
   - Traduzir textos em português para inglês utilizando o `TextBlob`, garantindo maior abrangência na análise de sentimentos.

4. **Promover o aprendizado e a replicação do projeto:**
   - Criar um pipeline intuitivo e funcional para iniciantes interessados em Processamento de Linguagem Natural e análise de sentimentos.
   - Oferecer um exemplo prático que possa ser adaptado para diferentes fontes e contextos de análise.

Com essas abordagens, o projeto apresenta uma introdução poderosa e amigável ao uso de ferramentas de NLP, mostrando como identificar a tonalidade emocional de textos e gerar insights práticos para aplicações reais.

## Pipeline do Projeto 🛠

O projeto foi estruturado em etapas bem definidas, desde a coleta e processamento dos dados até a análise e interpretação dos resultados. Abaixo está uma descrição detalhada de cada etapa:

---

### 1. **Configuração do Ambiente**
   - **Instalação de Dependências:**
     - Foram instaladas as bibliotecas essenciais para o projeto:
       - `nltk`: Biblioteca de processamento de linguagem natural.
       - `TextBlob`: Para análise de sentimento e tradução de texto.
       - `newspaper3k`: Para extração e processamento de artigos online.
   - **Configuração de Recursos do NLTK:**
     - Foi feito o download do recurso `punkt` do `nltk`, necessário para o tokenizador usado no `TextBlob`.

---

### 2. **Coleta de Dados**
   - **Fonte Online:**
     - Um artigo foi coletado diretamente da Wikipedia utilizando a biblioteca `newspaper3k`.
     - A URL do artigo foi fornecida como entrada, e o conteúdo textual foi extraído, processado e estruturado.
   - **Fonte Personalizada:**
     - O usuário pode fornecer um texto autoral, salvo em um arquivo chamado `mytext.txt`.
     - Esse texto é lido diretamente do arquivo para análise posterior.

---

### 3. **Processamento de Dados**
   - **Extração de Texto:**
     - Para artigos online:
       - O texto do artigo é baixado, parseado e tokenizado com as funcionalidades do `newspaper3k`.
     - Para textos autorais:
       - O texto é lido diretamente do arquivo e preparado para análise.
   - **Tradução:**
     - Textos em português são traduzidos para inglês utilizando o `TextBlob`. Isso garante que a análise de sentimento funcione corretamente, uma vez que a base de dados de polaridade do `TextBlob` está otimizada para textos em inglês.

---

### 4. **Análise de Sentimento**
   - **Criação de Objetos TextBlob:**
     - O texto processado é transformado em um objeto `TextBlob`, que permite calcular a polaridade do sentimento.
   - **Cálculo da Polaridade:**
     - O método `.sentiment.polarity` do `TextBlob` é utilizado para calcular a polaridade do texto, variando de `-1` (muito negativo) a `1` (muito positivo).
   - **Classificação do Sentimento:**
     - O valor de polaridade é interpretado:
       - Sentimento positivo: polaridade maior que 0.
       - Sentimento negativo: polaridade menor ou igual a 0.

---

### 5. **Interpretação dos Resultados**
   - **Classificação Final:**
     - Para textos autorais, uma mensagem personalizada é exibida ao usuário:
       - Caso o texto seja positivo: "Parece que sua mensagem é bastante positiva".
       - Caso o texto seja negativo: "Parece que sua mensagem tem um caráter negativo!".
   - **Discussão de Resultados:**
     - Para o artigo da Wikipedia, o sentimento foi classificado como quase neutro, destacando a objetividade do texto analisado.
     - Para textos autorais, os resultados podem variar de acordo com o tom e o conteúdo do texto fornecido.

---

### 6. **Melhorias e Expansões**
   - **Possibilidades Futuras:**
     - Suporte para mais idiomas sem a necessidade de tradução.
     - Análise de outros aspectos emocionais, como subjetividade e tom geral.
     - Integração com APIs de redes sociais para análise de grandes volumes de texto.
   - **Reutilização do Código:**
     - O pipeline foi projetado de forma modular, permitindo fácil adaptação para outros projetos ou fontes de texto.

## Metodologia 🧪

A metodologia adotada para este projeto seguiu uma abordagem sistemática e modular, garantindo que as análises fossem realizadas de maneira eficiente e precisa. Abaixo, descrevemos as etapas e métodos utilizados em cada fase do projeto:

---

### 1. **Configuração do Ambiente**
   - **Bibliotecas Utilizadas:**
     - `nltk`: Biblioteca de processamento de linguagem natural usada para tokenização.
     - `TextBlob`: Ferramenta principal para análise de sentimento e tradução automática de texto.
     - `newspaper3k`: Utilizada para extrair e processar textos de artigos online.
   - **Instalação e Configuração:**
     - Todas as bibliotecas foram instaladas via `pip`.
     - O recurso `punkt` foi baixado usando o `nltk` para suporte à tokenização.

---

### 2. **Coleta de Dados**
   - **Extração de Artigos Online:**
     - A biblioteca `newspaper3k` foi utilizada para baixar e processar um artigo da Wikipedia, usando a URL fornecida.
     - Funções como `download()`, `parse()` e `nlp()` foram aplicadas para estruturar o conteúdo.
   - **Entrada de Texto Personalizada:**
     - Um arquivo de texto chamado `mytext.txt` foi lido para incluir dados fornecidos diretamente pelo usuário.

---

### 3. **Processamento dos Dados**
   - **Transformação do Texto:**
     - Os textos coletados foram traduzidos do português para o inglês utilizando o método `.translate()` do `TextBlob`.
   - **Tokenização e Estruturação:**
     - O conteúdo dos textos foi tokenizado para facilitar a análise posterior.

---

### 4. **Análise de Sentimento**
   - **Criação de Objetos `TextBlob`:**
     - Os textos foram transformados em objetos `TextBlob`, que fornecem métodos para análise de sentimento.
   - **Cálculo de Polaridade:**
     - O método `.sentiment.polarity` foi utilizado para medir a polaridade dos textos, gerando valores entre `-1` (muito negativo) e `1` (muito positivo).
   - **Classificação Final:**
     - Os resultados foram categorizados como:
       - **Positivo:** Valores de polaridade maiores que 0.
       - **Negativo:** Valores de polaridade menores ou iguais a 0.

---

### 5. **Interpretação dos Resultados**
   - **Mensagem Personalizada para Textos Autorais:**
     - Um feedback direto foi gerado com base no valor de polaridade, indicando se o texto tinha um caráter positivo ou negativo.
   - **Discussão de Resultados:**
     - O texto da Wikipedia foi identificado como quase neutro, destacando sua objetividade.
     - Para textos autorais, os resultados variam de acordo com o conteúdo e o tom do texto.

---

### 6. **Visualização e Discussão**
   - **Discussão dos Insights:**
     - Os resultados da análise foram interpretados no contexto de cada texto.
   - **Identificação de Limitações:**
     - A necessidade de traduzir textos em português para inglês pode influenciar a precisão dos resultados.

---

### Ferramentas Utilizadas
- **Bibliotecas:** `nltk`, `TextBlob`, `newspaper3k`.
- **Funções Específicas:**
  - `download()` e `parse()` para extração de dados.
  - `.translate()` para tradução.
  - `.sentiment.polarity` para análise de sentimento.
- **Fonte de Dados:** Artigos da Wikipedia e texto autoral do usuário.

Com essa metodologia, o projeto aborda a análise de sentimento de maneira prática e eficiente, permitindo insights detalhados sobre diferentes tipos de textos.

## Resultados e Conclusões 📊

### Resultados ✨

Os resultados da análise de sentimento dos textos demonstraram a aplicabilidade prática de ferramentas de processamento de linguagem natural. Abaixo, apresentamos os principais achados organizados por tipos de entrada de dados:

---

### 1. **Análise do Artigo da Wikipedia**
   - **Texto Analisado:**
     - O artigo extraído da Wikipedia sobre "Matemática" foi processado para análise de sentimento.
   - **Resultados da Polaridade:**
     - **Polaridade:** Um valor de `0.02`, indicando um texto neutro, levemente inclinado para o positivo.
   - **Interpretação:**
     - Como esperado, o texto apresentou um tom predominantemente informativo e objetivo, típico de artigos enciclopédicos. A leve positividade pode ser atribuída ao uso de palavras que destacam a importância e as aplicações da matemática.

---

### 2. **Análise de Texto Autorado**
   - **Texto Analisado:**
     - Um texto fornecido pelo usuário, carregado do arquivo `mytext.txt`.
   - **Resultados da Polaridade:**
     - A polaridade variou dependendo do conteúdo e tom do texto autoral.
   - **Classificação:**
     - Mensagens personalizadas foram geradas:
       - **Positivo:** Para textos com polaridade acima de 0, indicando tom otimista ou encorajador.
       - **Negativo:** Para textos com polaridade abaixo ou igual a 0, indicando críticas, preocupações ou mensagens negativas.
   - **Interpretação:**
     - Textos autorais refletem os sentimentos e intenções do autor. A análise ajudou a identificar o tom geral da mensagem, possibilitando feedback imediato.

---

### 3. **Considerações sobre a Tradução**
   - **Impacto da Tradução:**
     - Os textos em português foram traduzidos para inglês antes da análise, o que pode introduzir pequenas variações nos resultados devido a nuances linguísticas.
   - **Desempenho da Ferramenta:**
     - O uso da API do `TextBlob` para tradução demonstrou eficiência, mas limitou a precisão da análise em alguns casos.

---

### Conclusões 🚀

#### 1. **Insights Obtidos**
   - **Artigos Informativos:**
     - Textos objetivos, como o artigo da Wikipedia, tendem a apresentar polaridade neutra, destacando a imparcialidade e informatividade.
   - **Textos Autorais:**
     - A ferramenta se mostrou útil para fornecer feedback rápido sobre o tom geral de mensagens pessoais, auxiliando na interpretação de sentimentos.

#### 2. **Limitações do Projeto**
   - **Dependência da Tradução:**
     - A necessidade de traduzir textos em português para inglês pode levar à perda de nuances e afeta diretamente a precisão da análise.
   - **Complexidade de Sentimentos:**
     - Textos que combinam sentimentos positivos e negativos em um mesmo contexto podem não ser avaliados com a devida granularidade.

#### 3. **Próximos Passos**
   - **Melhorar a Análise:**
     - Utilizar ferramentas de análise de sentimentos específicas para o idioma português, eliminando a etapa de tradução.
   - **Expandir o Escopo:**
     - Incluir visualizações gráficas para apresentar resultados de sentimento em forma de gráficos de barras ou nuvens de palavras.
   - **Avaliar Contextos:**
     - Desenvolver um modelo que avalie o sentimento em diferentes partes do texto separadamente, ao invés de uma análise geral.

#### 4. **Impacto Geral**
   - Este projeto demonstrou como ferramentas de processamento de linguagem natural podem ser aplicadas para avaliar sentimentos em textos de forma prática e acessível. Ele serve como base para projetos mais robustos e detalhados em análise de sentimentos.

## Considerações Finais 🚀

Este projeto demonstrou a aplicabilidade de ferramentas como `TextBlob` e `Newspaper3k` para análise de sentimentos em textos e artigos. Com foco em processamento de linguagem natural (NLP), foi possível explorar técnicas de tradução, extração e classificação de sentimentos, mostrando como essas tecnologias podem ser empregadas em cenários práticos e acessíveis.

---

### Pontos de Destaque:

1. **Análise de Sentimento:**
   - Textos informativos, como artigos enciclopédicos, tendem a apresentar polaridade neutra devido ao seu tom objetivo.
   - Textos autorais refletem sentimentos individuais, proporcionando feedback imediato sobre a intenção emocional do autor.

2. **Impacto da Tradução:**
   - O uso de tradução de textos em português para inglês introduziu pequenos desafios na precisão da análise, destacando a importância de ferramentas específicas para o idioma original.

3. **Feedback Rápido e Prático:**
   - A ferramenta provou ser útil para fornecer insights imediatos sobre o tom de mensagens, podendo ser aplicada em áreas como comunicação corporativa, análise de redes sociais e desenvolvimento de conteúdo.

---

### Limitações e Melhorias Futuras:

1. **Dependência de Tradução:**
   - A necessidade de tradução para inglês pode distorcer nuances do idioma original. O uso de ferramentas específicas para o português deve ser explorado em projetos futuros.

2. **Análise Limitada de Sentimentos:**
   - A polaridade de um texto inteiro não reflete nuances locais ou sentimentos mistos em diferentes partes do conteúdo. Um modelo mais granular é recomendado.

3. **Visualizações Gráficas:**
   - A inclusão de gráficos e representações visuais dos resultados pode facilitar ainda mais a interpretação dos dados e tornar o projeto mais interativo.

---

### Conclusão Geral:

Este projeto serviu como uma introdução prática à análise de sentimentos, utilizando ferramentas acessíveis e poderosas para NLP. Ele destaca a importância de entender o tom e a intenção emocional dos textos em um mundo cada vez mais digital. Apesar das limitações, os resultados obtidos são promissores e oferecem uma base sólida para expandir a análise para cenários mais complexos e abrangentes.

### Próximos Passos:
- Implementar ferramentas de análise de sentimentos nativas para o português.
- Expandir a análise para incluir visualizações gráficas.
- Explorar contextos mais diversificados e aplicações comerciais, como análise de feedback de clientes ou tendências de redes sociais.

## Agradecimentos 🙏

Gostaria de expressar minha sincera gratidão às seguintes contribuições e recursos que tornaram este projeto possível:

1. **Comunidade de Desenvolvedores de NLP:**
   - Pelas ferramentas incríveis como `TextBlob` e `Newspaper3k`, que proporcionaram a base técnica necessária para este projeto.

2. **Plataformas de Documentação e Tutoriais:**
   - Recursos online, como a documentação oficial das bibliotecas utilizadas, que forneceram orientações claras e detalhadas.

3. **Wikipedia:**
   - Por disponibilizar conteúdo aberto e acessível, que serviu como base para os testes e validações iniciais deste projeto.

4. **Mentores e Colaboradores:**
   - Agradeço às pessoas que compartilharam conhecimento e feedback ao longo do desenvolvimento, contribuindo para aprimorar minhas habilidades em análise de texto e processamento de linguagem natural.

Este projeto reflete a importância da colaboração, do aprendizado contínuo e do uso ético da tecnologia para promover a inovação e a compreensão. Agradeço a todos que, direta ou indiretamente, participaram desta jornada.

<div align="center">
  <img src="https://github.com/user-attachments/assets/54afb33c-97be-40b6-8c96-0f12852e946f" alt="thank-you" width="500">
</div>

## 📞 Contato
- **LinkedIn:** [Eduardo Coqueiro](https://www.linkedin.com/in/eduardocoqueiro/)
- **Site:** [Eduardo Coqueiro](https://dataguy.my.canva.site/eduardo-coqueiro)
- **Kaggle:** [Eduardo Coqueiro](https://www.kaggle.com/eduardocoqueiro)

