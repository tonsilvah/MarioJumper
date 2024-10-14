# MarioJumper
 
Código desenvolvido para aprendizagem via tutorial do canal MANUAL DO DEV (https://www.youtube.com/watch?v=r9buAwVBDhA), com pequenas modicações que aperfeiçoaram a visibilidade e jogabilidade.

<b>Descrição Técnica do Jogo MarioJumper</b>

 Estrutura do Projeto: O projeto é composto por três arquivos principais: index.html, style.css e script.js, organizados de maneira a separar a estrutura, a apresentação e a lógica do jogo.
  
  HTML (index.html): O arquivo HTML define a estrutura básica da página e contém os elementos visuais do jogo:
        Tags: O jogo utiliza <img> para exibir imagens do Mario, do cano e do fundo de nuvens.
        Classes: As classes (.mario, .pipe, .clouds) são usadas para estilizar e manipular os elementos via CSS e JavaScript.
  CSS (style.css):
    Estilos Globais '(*)': Reseta as margens e o preenchimento de todos os elementos e define o box-sizing como border-box, facilitando o controle de largura e altura.
    game-board: Define o tamanho e a posição da área de jogo, com um fundo de gradiente e uma borda inferior representando o chão.
    pipe: Posiciona o cano na parte inferior da tela e aplica uma animação que o move da direita para a esquerda continuamente.
    mario: Posiciona Mario na parte inferior da tela com um tamanho fixo.
    jump: Aplica a animação de pulo ao Mario, que é definida na keyframe jump.
    clouds: Cria nuvens em movimento horizontal com uma animação contínua.
    
   @keyframes:
    pipe-animation: Define a animação do cano, movendo-o da direita para fora da tela.
    jump: Controla a animação de pulo do Mario, levando-o a uma altura de 180 pixels antes de retornar ao chão.
    clouds-animation: Move as nuvens da esquerda para a direita na tela.

4. JavaScript (script.js):

A lógica do jogo é implementada em JavaScript e inclui as seguintes funcionalidades:
Seleção de Elementos: Utiliza document.querySelector para selecionar os elementos do Mario e do cano.
Função de Pulo: A função jump() adiciona uma classe ao Mario para iniciar a animação de pulo, que dura 500 milissegundos.
Loop de Jogo: Um loop (setInterval) verifica constantemente a posição do cano e do Mario:
Detecção de Colisão: Se o cano se aproxima de Mario e eles colidem (verificando posições em pixels), a animação do cano é interrompida, e a imagem de Mario é substituída por uma imagem de game over.

Parada do Jogo: O loop é interrompido usando clearInterval(loop) após a colisão.

5. Interatividade:

Eventos: O jogo escuta eventos de teclado usando document.addEventListener, permitindo que o jogador ative o pulo de Mario ao pressionar qualquer tecla.

Tecnologias Utilizadas:
HTML5: Estrutura do jogo.
CSS3: Estilização e animação dos elementos.
JavaScript (ES6): Lógica de interação, detecção de colisões e animações.
