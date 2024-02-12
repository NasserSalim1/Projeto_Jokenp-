# Jokenpô - Pedra, Papel e Tesoura

Este é um jogo simples de Pedra, Papel e Tesoura implementado em HTML, CSS e JavaScript. O jogo permite que o jogador jogue contra o computador e acompanhe o placar de pontos.

## Funcionalidades

- **Jogador vs Computador**: O jogador pode escolher entre Pedra, Papel ou Tesoura, e o computador também faz uma escolha.
- **Placar de Pontos**: O placar mostra a contagem de pontos do jogador e do computador.
- **Mensagens de Resultado**: O resultado de cada rodada é exibido em uma mensagem na tela.

## Estrutura do Código

### HTML (index.html)

O arquivo HTML contém a estrutura básica da página web e os elementos que compõem o jogo, como o título, placar de pontos, escolhas do jogador e do computador, e mensagens.

- **Elementos Importantes**:
  - `<div id="principal">`: Container principal que engloba todo o conteúdo do jogo.
  - `<h1 id="titulo">`: Título do jogo.
  - `<div id="placar">`: Contém o placar de pontos do jogador e do computador.
  - `<div id="jogador">` e `<div id="computador">`: Contêm as informações e escolhas do jogador e do computador, respectivamente.
  - `<div id="mensagem">`: Elemento para exibir mensagens de resultado.

### CSS (style.css)

O arquivo CSS define a aparência e o layout dos elementos na página, incluindo fontes, cores, tamanhos e posicionamento.

- **Estilização**:
  - Define o estilo para o contêiner principal, títulos, placar, escolhas do jogador e do computador, e mensagens.

### JavaScript (script.js)

O arquivo JavaScript adiciona interatividade ao jogo, controlando as ações do jogador e do computador, atualizando o placar e exibindo mensagens de resultado.

- **Variáveis Globais**:
  - `jogadorNome`: Armazena o nome do jogador.
  - `jogadorPontos`: Armazena a pontuação do jogador.
  - `jogadorEscolha`: Armazena a escolha do jogador (1 para Pedra, 2 para Papel, 3 para Tesoura).
  - `computadorEscolha`: Armazena a escolha aleatória do computador.
  - `computadorPontos`: Armazena a pontuação do computador.

- **Funções**:
  - `sortear(min, max)`: Gera números aleatórios entre `min` e `max`, inclusive.
  - `traduzirEscolha(numero)`: Traduz o número da escolha para uma palavra ('Pedra', 'Papel' ou 'Tesoura').
  - `selecionar(tipo, escolha)` e `deselecionar(tipo, escolha)`: Adicionam e removem a classe 'selecionado' às escolhas do jogador e do computador.
  - `mensagem(texto)`: Escreve uma mensagem na tela.
  - `definirJogadorNome(nome)`: Define o nome do jogador na interface.
  - `calcularEscolha(jogador, computador)`: Calcula e retorna o vencedor de cada rodada com base nas escolhas do jogador e do computador.
  - `somarPontoJogador()` e `somarPontoComputador()`: Incrementam os pontos do jogador e do computador, respectivamente.
  - `jogar(escolha)`: Controla o fluxo do jogo.
  - Event Listeners para as Escolhas do Jogador.

- **Inicialização do Jogo**:
  - Solicita ao jogador seu nome.
  - Define o nome do jogador na interface.
  - Exibe uma mensagem de boas-vindas.
