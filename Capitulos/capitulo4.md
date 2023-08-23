
# Capítulo 4: O Primeiro Ciclo - Rumo ao Protótipo 0
"Ciência não é sobre 'por que'. É sobre 'por que não'." - Cave Johnson, _Portal 2_ (2011)

<p align="center">
  <img src="../Arquivos/Imagens/capa_04.png" 'Science isn\'t about \'why\'. It's about \'why not\'.' />
</p>

## Introdução

O [capítulo anterior](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo3.md) ofereceu uma abordagem bem teórica sobre como funcionaria o ciclo de desenvolvimento, mas você provavelmente ainda tem várias dúvidas sobre o que fazer. De certa forma, o desenvolvimento é como um jogo de tabuleiro. Você pode ler as regras, mas só aprenderá realmente quando colocá-las na prática.

E, nesse sentido, a prática será os primeiros ciclos de desenvolvimento. Existem várias formas de separar as etapas da produção dos jogos, mas aqui a dividiremos da seguinte forma: **Protótipo 0** → **Alfa** → **Beta** → **Produto final**

Se você joga, os termos _alfa_ e _beta_ não devem ser desconhecidos a você. Eles se referem a estados diferentes do desenvolvimento de um _software_. No contexto de jogos, isso é um pouco vago. Alguns vão definir a diferença entre _alfa_ e _beta_ como "um está bem incompleto e o outro está quase completo". Outros ainda vão dizer que versões beta são aquelas apresentáveis para a audiência, e que podem ser publicadas para teste.

Eu ainda incluo mais uma etapa, o Protótipo 0. Para o contexto deste manual, vou definir estas etapas da seguinte maneira:

- Protótipo 0: Primeira versão do jogo para testar a ideia, quase nada além da ideia central do jogo é implementada
- Alfa: Faltam diversos sistemas e funções a serem implementadas
- Beta: Sistemas e funções principais já foram todos implementados, resta poli-los e consertar _bugs_

Seguiremos esta ordem durante o manual. Logo, o primeiro passo é o Protótipo 0.

## O Protótipo 0

A ideia por trás do Protótipo 0 é destilar o conceito de seu jogo a um ponto que você tenha **apenas** sua essência, e implementar isto.

O que isso quer dizer na prática?

_Sprites_, modelos, música, mapas são todos desnecessários. Nada disso pertence ao protótipo 0. Na verdade, seu primeiro protótipo deve parecer muito mais como um jogo de _Atari_ do que um jogo moderno. Se fosse _Super Mario_, você poderia ter um quadrado correndo e pulando. Se fosse _Zelda_, talvez você teria um quadrado andando na tela e espetando inimigos (também quadrados) com um similar retângulo.

Esses exemplos são exageros, você não precisa se apegar ao minimalismo de tal maneira. Se você tem um artista no time, não precisa deixá-lo ocioso até o fim da criação deste protótipo, e se você já tem algo feito, não precisa evitar seu uso de propósito (apesar de ser uma opção). Se desejar ter algo visual em tela, pode interessar usar recursos grátis tirados, por exemplo, do site [Open Game Art](https://opengameart.org/). A intenção é apenas que você crie o protótipo para sentir sua ideia com as próprias mãos.

Dessa forma, se você trabalha sozinho, não se preocupe em criar nenhum artefato audiovisual. E se você trabalha em equipe, não se preocupe em incluir nenhum artefato audiovisual no projeto, por enquanto. Durante essa etapa, o trabalho principal vai ser entre designer e programador.

A intenção do protótipo 0 não é criar uma representação do seu jogo, é criar a base inicial dele. Como uma casa, você constrói uma fundação antes de começar a construir os cômodos. Se a fundação não estiver firme, a casa vai desmoronar.

Assim, o seu primeiro passo é definir as mecânicas principais do seu jogo e implementá-las de maneira simples.

## Destilando sua Ideia
Como esse "destilar" deve ser feito? O primeiro passo é entender quais são os elementos que definem o seu jogo em si, qual é a identidade de seu jogo. Para um jogo de plataforma, isso seria o movimento e física do personagem jogável. Para um jogo de luta, isso seria dois personagens com apenas um jogável, com os quais você pode testar várias ações provisórias e combos simples (sem preocupação inicial com vida e outros sistemas). Para um jogo de corrida, um único veículo provisório em uma pista de testes. Para um RPG, talvez o sistema de batalhas ou o sistema de movimento em um mapa (o que for mais relevante). Enfim, acho que ilustrei a ideia com estes exemplos.

Caso haja alguma mecânica especial para o seu projeto, é interessante incluir pelo menos uma versão primitiva dela no seu protótipo também, como é o caso no meu protótipo que exemplifico abaixo.

Quanto mais complexo o seu projeto for, mais complexo este protótipo terá de ser para que você consiga realmente incluir uma base completa para seu projeto. Nesse ponto, você está livre para seguir com seu projeto, mas se esta é sua primeira vez criando um jogo, sugiro diminuir a complexidade do seu projeto tanto quanto possível, para evitar qualquer risco de que você e sua equipe não consigam completá-lo.

Uma vez selecionada a(s) mecânica(s) principais para o seu projeto, o próximo passo real é dividir estas em pedaços menores, cada vez mais simples. Da mesma forma que exemplifiquei no capítulo anterior, todo elemento e sistema de um jogo pode ser dividido em elementos e sistemas menores (o sistema de física dividido em movimento e colisão, por exemplo). 

Obviamente, para dividir um sistema ou mecânica em elementos menores, você precisa entender esse elemento ou mecânica. Procure jogos com mecânicas similares, tente entender como elas funcionam. Procure também vídeos analisando estas mecânicas e ideias. E quando tiver um bom entendimento de como ela funciona, faça essa quebra nos pedaços menores. Feito isso, vá a sua _engine_ ou ambiente de escolha e trabalhe para implementar estes pedaços menores até que consiga construir o todo.

Caso você não tenha ideia de como fazer essas implementações, ou fique sem saber como prosseguir em qualquer ponto do desenvolvimento do protótipo ou do projeto como um todo, use o [capítulo 5](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo5.md) como referência de como prosseguir.

## Protótipo 0 - Exemplificado
Na maioria dos casos, começamos qualquer projeto criando uma pasta para ele. Na minha _engine_ de escolha, isso pode ser feito no próprio editor. Aqui, vou descrever os passos para minha _engine_ de escolha, Godot. Mas independente do ambiente que escolher, essa descrição do processo pode servir como referência para o seu.

![Criando Projeto](../Arquivos/Imagens/04_01.png 'Criando Projeto')
<sup><sub> Criando o projeto </sup></sub>

Ao criar o projeto, somos apresentados ao menu principal da _engine_. Neste caso, já vemos o visualizador/editor de mapas imediatamente. Meu próximo passo sempre costuma ser criar as pastas de arquivos na estrutura que decidi anteriormente.

![Primeira Visão da Engine](../Arquivos/Imagens/04_02.png 'Primeira Visão da Engine')
<sup><sub> Editor de cena e mapas </sup></sub>

![Pastas de Arquivos](../Arquivos/Imagens/04_03.png 'Pastas de Arquivos')
<sup><sub> Explorador de arquivos </sup></sub>

Em seguida, eu passo por algumas configurações que serão relevantes para a construção do jogo. No momento, estou preocupado apenas com o **nome do projeto** e o **tamanho da tela**. O tamanho dela é importante decidir cedo no desenvolvimento, pois isso vai afetar o seu jogo. Principalmente para questões de _câmera_ e quanto cabe em sua tela. Nesse caso, como se trata de um jogo para celulares, optei por um tamanho padrão de 1080x720, mas provavelmente vou mudá-lo mais a frente por se tratar de um jogo _pixel art_. Essa resolução não é estática, e será mudada para se adequar à tela do celular do jogador, mas para isso, devo incluir também a opção de _stretch_.

![Configurações](../Arquivos/Imagens/04_04.png 'Configurações')
<sup><sub> Abrindo as configurações </sup></sub>

![Configurações2](../Arquivos/Imagens/04_05.png 'Configurações 2')
<sup><sub> Configurações do projeto </sup></sub>

![Configurações3](../Arquivos/Imagens/04_06.png 'Configurações 3')
<sup><sub> Configurações de janela </sup></sub>

Após fazer essas mudanças, pressiono CONTROL + S para salvar meu projeto, e passo a trabalhar no protótipo em si.

Na _engine_ Godot, todos os elementos de um jogo são divididos em _cenas_. Cenas são um conceito comum para várias _engines_, e geralmente essas cenas são o elemento executável primário de um jogo. Ou seja, uma cena seria equivalente a um mapa ou fase, ou um menu. Ao rodar o seu jogo, a _engine_ partirá de uma cena específica, e poderá mudar para outras cenas durante a execução.

Essas cenas executáveis são então compostas de vários elementos. Por exemplo, de um mapa com colisões, um personagem controlável, e vários obstáculos. Já é possível enxergar uma fase com estes elementos.

No Godot, toda cena é uma estrutura de árvore. Estruturas de árvore são compostas de um nó pai e vários nós filhos. Aqui, estes nós filhos representam diferentes objetos de cada cena. Por exemplo, um personagem que se move na tela seria um _CharacterBody_ ou _CharacterBody2D_. O mapa pode ser composto de vários objetos estáticos _StaticBody3D_/_StaticBody2D_, ou de um _Tilemap_ (mapa formado por _tiles_/blocos).

Aqui, para criar a primeira cena, eu escolho a opção "2D Scene", e em seguida eu dou um nome para esta cena. Para nomenclatura de cenas e nós, eu costumo usar o padrão CamelCase (palavras diferentes não são separadas por espaços, mas têm sua primeira letra em caixa alta). Eu faço isso para separar objetos instanciados de nomes de variáveis quando escrevo meus _scripts_. Mas você pode nomear suas cenas como preferir, ou como for o padrão em seu ambiente de desenvolvimento.

![Primeira Cena](../Arquivos/Imagens/04_07.png 'Primeira Cena')
<sup><sub> Visualizador de cena </sup></sub>

![Primeira Cena 2](../Arquivos/Imagens/04_08.png 'Primeira Cena 2')
<sup><sub> Nó raiz da primeira cena </sup></sub>

Em seguida, eu adiciono os elementos que vou precisar para a criação desse primeiro mapa teste. Ou seja, adiciono nós filhos. No caso, um nó para o mapa em si (_Tilemap_), um nó para a câmera (_Camera2D_), e um nó que representará o personagem jogável (_CharacterBody2D_). Por experiência, eu já sei exatamente quais são os nós que precisarei para isso, mas é normal que você precise pesquisar nas primeiras vezes.

![Adicionando nós filhos](../Arquivos/Imagens/04_09.png 'Adicionando nós filhos')
<sup><sub> Adicionando nós filhos </sup></sub>

![Procurando nós filhos](../Arquivos/Imagens/04_10.png 'Procurando nós filhos')
<sup><sub> Procurando o nó adequado </sup></sub>

![Nós filhos](../Arquivos/Imagens/04_11.png 'Nós filhos')
<sup><sub> Novos nós filhos </sup></sub>

Ao final, temos uma cena TestMap com alguns nós filhos. Esses são os **blocos principais** para o meu protótipo 0. Um personagem jogável, um mapa com o qual ele poderá interagir, e uma câmera para acompanhar o personagem durante o jogo.

Por enquanto, se executar essa cena, vou notar que ela não faz nada. Não há nada para executar nela, apenas uma câmera apontada para um espaço vazio. O próximo passo é incluir objetos nessa cena. Em qual objeto você trabalharia fica a seu critério. Eu começarei pelo mapa, pois não conseguirei testar o meu jogador sem ter um mapa onde ele possa andar.

Para isso, criei um simples _tileset_ com 2 _tiles_ diferentes. Em jogos 2D, _tilesets_ são imagens onde você cria diferentes "azulejos" que pode usar como blocos em suas fases. Esse tipo de construção era comumente usada em jogos até a quarta geração de consoles, por motivos de memória e simplicidade de montagem. Hoje em dia, ainda é usada em jogos justo pela simplicidade, ou para emular um estilo de jogo antigo.

Não é relevante me dar ao trabalho de criar um mapa finalizado para o protótipo 0. Criei um _tileset_ com 2 cores sólidas, cada um de 16x16 píxeis. Por questões de facilidade de divisão da tela e padronização de tamanhos, costumamos usar múltiplos de 16 para os tamanhos de _tiles_ (e.g. 16, 32, 64, 128, e, raramente, 8). Esse _print_ é da ferramenta _Aseprite_, que uso para criar _pixel art_:

![Tileset Básico](../Arquivos/Imagens/04_12.png 'Tileset Básico')
<sup><sub> Criando um _tileset_ no Aseprite </sup></sub>

Em seguida, adicionei o _tileset_ aos arquivos do meu projeto. Nesse caso, junto ao arquivo do mapa. No Godot, é possível fazer isso arrastando o arquivo para dentro do editor. Também é possível encontrar a pasta no seu explorador de arquivos e adicioná-lo manualmente.

![Adicionando arquivo ao editor](../Arquivos/Imagens/04_13.png 'Adicionando arquivo ao editor')
<sup><sub> Adicionando arquivo ao editor </sup></sub>

Agora, posso começar a criar o mapa, no outro canto da janela, opções de edição do nó selecionado aparecem. No campo Tile Set, adiciono um novo recurso do tipo _tileset_, e clico nele, para que o editor de _tileset_ apareça no canto inferior da tela. Arrastando o arquivo de imagem de meu _tileset_ para este editor, a _engine_ já separa os _tiles_ da maneira correta. (Isso acontece porque o tamanho padrão da _engine_ é 16x16 píxeis. Caso meu _tile_ tivesse um tamanho maior, seria necessário mudar essa configuração).

![Tileset](../Arquivos/Imagens/04_14.png 'Tileset')
<sup><sub> Configurando _tileset_ </sup></sub>

![Tileset 2](../Arquivos/Imagens/04_15.png 'Tileset 2')
<sup><sub> Procurando o arquivo do _tileset_ </sup></sub>

![Tileset 3](../Arquivos/Imagens/04_16.png 'Tileset 3')
<sup><sub> _Tileset_ configurado </sup></sub>

Agora, eu posso clicar em um _tile_ qualquer e desenhar o meu mapa como quiser.

![Desenhando Mapa](../Arquivos/Imagens/04_17.png 'Desenhando Mapa')
<sup><sub> Desenhando um mapa </sup></sub>

Eu sabia que isso aconteceria, mas o tamanho que escolhi para minha tela é grande demais para o tamanho dos _tiles_. Isso é algo que vou ter que corrigir depois. Por enquanto, anotarei isso no meu documento de _backlog_.

Se eu executar essa cena do jeito que está, vou encontrar o mapa que desenhei, mas nada acontece. O próximo passo é incluir algum tipo de interação. E o melhor jeito de seguir com isso é criar o jogador. 

![Cena em execução](../Arquivos/Imagens/04_18.png 'Cena em execução')
<sup><sub> Cena estática </sup></sub>

Um detalhe interessante sobre a estrutura de árvores, é que nós filhos podem ter seus próprios nós filhos. Talvez você tenha reparado que o nó do meu personagem tem um triângulo de aviso. Isso é porque nós do tipo "corpo" precisam de um formato de colisão para funcionarem normalmente. Nesse caso, basta incluir um nó de colisão como filho. 

![Incluir colisão](../Arquivos/Imagens/04_19.png 'Incluir colisão')
<sup><sub> Incluindo um nó de colisão </sup></sub>

Geralmente, quando existe alguma configuração faltante, o próprio editar vai me avisar. Aqui, ele reclama que é preciso incluir um formato para o nó de colisão, então eu o faço. Nesse caso, selecionei um simples formato de retângulo, que é provavelmente o que vou usar para o personagem de qualquer forma.

![Colisão 1](../Arquivos/Imagens/04_20.png 'Colisão 1')
<sup><sub> Configurando nó de colisão </sup></sub>

![Colisão 2](../Arquivos/Imagens/04_21.png 'Colisão 2')
<sup><sub> Colisão exibida no editor </sup></sub>

Agora, tenho um "personagem" com colisão, mas ele não é visível durante a execução. Isso é porque ele não contém nenhum nó visual. Por isso, incluo um nó "Sprite 2D" como filho. Eu já tenho um _sprite_ para o personagem, mas desenhei um provisório apenas por questões de ilustração. Da mesma forma, um quadrado sólido também serviria, mas tente fazer um quadrado de cor diferente do mapa para facilitar sua visualização.

![Sprite embaçado](../Arquivos/Imagens/04_22.png 'Sprite embaçado')
<sup><sub> _Sprite_ incluído aparece embaçado </sup></sub>

Adicionado o arquivo ao editor, e incluído como textura do sprite, percebo um problema com o meu desenho. Ele aparece um tanto embaçado no editor. Isso é porque a _engine_ tenta "filtrar" as imagens adicionadas para melhorar sua visualização. E isso costuma ser algo bom, mas para resoluções muito baixas (como 16x16 píxeis), isso não é desejável. Nesse caso, basta mudar a configuração de filtro, e o _sprite_ aparece da forma desejada.

![Configuração de filtro](../Arquivos/Imagens/04_23.png 'Configuração de filtro')
<sup><sub> Ajuste de filtro para o _sprite_ </sup></sub>

Se eu executar a cena agora, notamos que o personagem existe, mas ele não faz nada. Aqui, me incomodo novamente com a resolução e a diminuo novamente nas configurações do projeto. Agora, o tamanho da câmera é pequeno demais para mostrar o mapa que criei abaixo, porém mais importante é o fato de que o personagem permanece flutuando no ar.

![Flutuando](../Arquivos/Imagens/04_24.png 'Flutuando')
<sup><sub> Personagem flutuando no mapa </sup></sub>

![Flutuando 2](../Arquivos/Imagens/04_25.png 'Flutuando 2')
<sup><sub> Personagem flutuando no mapa 2 </sup></sub>

Para mudar isso, será necessário criar um _script_. Normalmente, _engines_ vão conter dois tipos de "corpos". Corpos 'rígidos' e 'cinemáticos'. Corpos rígidos têm sua física pré-programada, e são rígidos também no sentido de que o jeito que funcionam não é tão fácil de mudar. Corpos cinemáticos funcionam ao contrário, eles só funcionam se forem programados manualmente, mas é muito mais fácil mudá-los para que fiquem da maneira desejada. O corpo cinemático é mais adequado ao tipo de jogo que estou construindo.

Como mencionei antes, para dar funcionalidade a esse corpo será necessário incluir um _script_. Por ora, esse _script_ cuidará apenas de física e controle. Mas antes de fazer isso, é interessante tomar outro passo: salvar o jogador como uma cena diferente. Isso é outra funcionalidade muito útil do Godot. Eu posso salvar qualquer nó e seus filhos como uma cena separada, e reutilizar essa cena como nó filho em qualquer outra cena que precisar.

Eu simplesmente salvo o nó do jogador como uma cena diferente, na minha pasta de Entities/Player, chamando-o de _Player_. Agora é possível clicar no botão de edição para abrir a cena do jogador. Eu também renomeio o nó pai dessa cena para "Player". Tanto a nova cena quanto o nó filho na cena do mapa.

![Salvando como cena](../Arquivos/Imagens/04_26.png 'Salvando como cena')
<sup><sub> Salvando nó como cena </sup></sub>

![Salvando como cena 2](../Arquivos/Imagens/04_27.png 'Salvando como cena 2')
<sup><sub> Configurando o nome correto </sup></sub>

![Botão de edição](../Arquivos/Imagens/04_28.png 'Botão de edição')
<sup><sub> Botão de edição da cena </sup></sub>

![Renomeando](../Arquivos/Imagens/04_29.png 'Renomeando')
<sup><sub> Renomeando o nó raiz da cena </sup></sub>

![Renomeando 2](../Arquivos/Imagens/04_30.png 'Renomeando 2')
<sup><sub> Renomeando o nó na cena do mapa </sup></sub>

Teria sido melhor renomear o nó antes de salvá-lo como filho, mas sinceramente eu esqueci de fazer isso. Felizmente, também é possível fazer essa mudança após salvar a cena. De qualquer forma, agora é mais simples adicionar um _script_ a cena _Player_. Aproveitando a oportunidade, também levei o _sprite_ do jogador para a mesma pasta onde salvei a cena do _Player_.

![Ajuste de arquivos](../Arquivos/Imagens/04_32.png 'Ajuste de arquivos')
<sup><sub> Ajustando arquivos e pastas </sup></sub>

![Incluindo Script](../Arquivos/Imagens/04_31.png 'Incluindo Script')
<sup><sub> Incluindo _script_ </sup></sub>

Eu sempre salvo o _script_ com o mesmo nome e na mesma pasta que a cena. (Isso só é possível porque o _script_ e a cena têm extensões diferentes). Uma adição interessante ao Godot 4 é a desse _script_ padrão para o nó do tipo CharacterBody2D (corpo cinemático). 

![Nome do script](../Arquivos/Imagens/04_33.png 'Nome do script')
<sup><sub> Menu de adição de _script_ </sup></sub>

![Script padrão](../Arquivos/Imagens/04_34.png 'Script padrão')
<sup><sub> _Script_ padrão de corpo cinemático </sup></sub>

Esse _script_ já inclui controle lateral, pulo e gravidade. Se eu fosse escrever um _script_ do zero para essa mesma funcionalidade, ele seria bem similar a esse. Porém, se eu rodar a cena de teste nesse exato momento, notarei que o meu jogador apenas cai. Isso é porque a câmera não está configurada para seguir o jogador.

![Gif, Player caindo](../Arquivos/Imagens/04_35.gif "Player Caindo")
<sup><sub> Personagem cai </sup></sub>

Existem vários jeitos de consertar isso. O mais simples é simplesmente colocar a câmera como um nó filho do jogador. Enquanto eu não pretendo usar isso na versão final do jogo (pois quero ter diferentes funcionalidades para a câmera em diferentes momentos), para motivos do protótipo, isso vai servir. Incluo agora também no backlog o item "Ajustar funcionamento da câmera".

Na minha cena de teste, arrasto a câmera para que se torne nó filho do _Player_.

![Ajuste de câmera](../Arquivos/Imagens/04_36.png 'Ajuste de câmera')
<sup><sub> Ajuste de nós </sup></sub>

Agora, ao tentar executar a cena, a câmera segue o personagem como esperado, mas me deparo com outro problema. Eu não incluí colisão para o mapa que criei abaixo, e a gravidade faz com que o personagem caia diretamente através do chão.

![Gif, Player caindo 2](../Arquivos/Imagens/04_37.gif "Player Caindo 2")
<sup><sub> Caindo novamente </sup></sub>

Para esse caso, eu ainda não lembrava como configurar colisões em _Tilemaps_ para o Godot 4 (pois tenho mais experiência com a versão 3). Então tive que pesquisar sobre, e [este vídeo](https://www.youtube.com/watch?v=1Uk1yhGtnOo) me mostrou como fazê-lo. Segui os passos descritos, e incluí colisão para os dois _tiles_ que usei no _tileset_.

![Ajuste de colisão](../Arquivos/Imagens/04_38.png 'Ajuste de colisão')
<sup><sub> Ajuste de colisão  </sup></sub>

Agora, o personagem cai até encontrar o chão. E é possível controlá-lo com as setas e a barra de espaço. O movimento não é muito bom, e o personagem não é animado, nem sequer vira para o lado onde está andando, porque nenhuma dessas funções foi programada. 

![Gif, Movimento básico](../Arquivos/Imagens/04_39.gif "Movimento básico")
<sup><sub> Movimento básico do personagem </sup></sub>

Contudo, já temos os primeiros passos para o protótipo 0. Uma cena de testes, um personagem jogável, e um plano de ação. Antes de prosseguirmos, vamos entender o código que já temos.

### Desmistificando o código
Para alguém que acabou de começar sua jornada de desenvolvimento, isso pode parecer mágica. Mas não há mágica alguma em códigos, são apenas conjuntos de instruções, e entendendo as instruções você entenderá o funcionamento do código. Então, vamos observar o _script_ do jogador que temos até agora.

![Código Player](../Arquivos/Imagens/04_40.png 'Script Player')
<sup><sub> _Script_ do _Player_ </sup></sub>

Esse é um _script_ bem simples. Ele contém apenas uma função, e são apenas 29 linhas de código, incluindo linhas em branco.

![Linha 1](../Arquivos/Imagens/04_41.png 'Linha 1')
<sup><sub> _Script Player_ Linha 1 </sup></sub>

A primeira linha é padrão na maioria dos _scripts_ no Godot. "_Extends_" indica herança, que é um conceito de programação orientada a objetos. Em termos simples, quando um objeto herda de outro, ele recebe todos os atributos do objeto o qual ele herda. Nesse caso, nosso nó _Player_ herda de CharacterBody2D. Ou seja, ele herda todos os atributos e funções da classe CharacterBody2D, e pode fazer coisas como andar pela tela e colidir com outros objetos. Sempre que você quiser entender qual é o tipo de objeto no Godot, você pode procurar por essa linha.

![Linhas 4-8](../Arquivos/Imagens/04_42.png 'Linhas 4-8')
<sup><sub> _Script Player_ Linha 4-8 </sup></sub>

As linhas 4-8 são declarações de constantes e variáveis. Velocidade e velocidade de pulo **não mudarão** durante a execução do jogo, então declará-las como _constant_ é melhor (tanto em termos de organização quanto para a execução do jogo). Quanto ao que significam, SPEED é a velocidade com que o jogador anda horizontalmente, e JUMP_VELOCITY é a força com que o jogador pula quando o botão de pulo é pressionado. Além disso, temos a variável _gravity_, que herda um valor nas configurações, para que haja sincronia entre ela e corpos rígidos. No meu caso, eu não pretendo usar corpos rígidos por enquanto, mas posso decidir usá-los adiante, então vou manter essa linha assim.

Você pode editar estes valores e perceber como eles afetam o personagem. Diminuindo a gravidade, por exemplo, o personagem leva mais tempo para cair. E aumentando a velocidade, ele anda mais rápido através da tela.

![Mudando configurações](../Arquivos/Imagens/04_43.png 'Mudando configurações')
<sup><sub> Ajuste de configuração de gravidade </sup></sub>

![Linhas 11-28](../Arquivos/Imagens/04_44.png 'Linhas 11-28')
<sup><sub> _Script Player_ Linha 11-28 </sup></sub>

O próximo bloco de código é uma função. Funções são blocos de código que podem ser executados quando chamados em outras partes do código. No Godot, além de poder criar suas próprias funções, encontramos algumas funções comuns para quase todos os tipos de objetos. Estas são:

- Funções de inicialização: funções como _\_ready()_ e _\_init()_ são ótimas para incluir configurações importantes na hora que o seu nó entra em ação. Ambas rodam uma única vez em condições específicas. _Ready_ roda quando o objeto é criado em uma cena, e _init_ quando é instanciado como um objeto.
- Funções de execução: funções como _\_physics_process()_ e _\_process()_ rodam todo _frame_ (geralmente, 60 vezes por segundo), e são as funções de código primárias para seus objetos. A maioria das ações, _checks_ e mudanças são feitas nestas funções. É importante lembrar que muitos objetos ativos ao mesmo tempo, com muitas instruções nessas funções, vão causar com que a execução do seu jogo fique lenta.
- Funções _trigger_: Estas funções ficam separadas da execução dos processos, mas rodam como resposta a algum acontecimento. Geralmente, elas estão atreladas a _signals_(sinais), e vão rodar quando as condições necessárias forem verdadeiras. Por exemplo, quando o personagem jogável colidir com um espinho, um sinal vai indicar que ele rode a função que diminui seus pontos de vida por 1.

Para objetos submetidos a física como corpos, fazemos seu código por padrão na função _physics_process_, pois ela é a mais adequada para as operações deles. Ela recebe a variável _delta_, que indica o tempo entre a renderização do _frame_ anterior e o atual. Esse delta é usado para que o tempo de execução de certas ações seja o mesmo, independente do tempo de execução do computador. Nesse caso, o _delta_ vai permitir que o movimento do jogador não seja afetado por lentidão ou rapidez do computador.

A linha 13 verifica se o jogador está no chão (_is_on_floor_). Caso não esteja, gravidade é aplicada na linha 14. Essa gravidade é aplicada diretamente ao valor Y da posição do jogador. Isso demonstra outro aspecto do funcionamento da _engine_. Todos os objetos em tela tem uma **posição**, representada por um vetor com 2 valores, uma posição X e uma posição Y (para objetos 2D, os 3D também têm uma posição Z). Mover estes objetos é simplesmente uma questão de mudar o valor X,Y dessas posições. 

Para movimento de objetos físicos, Godot utiliza a função _move_and_slide_. Essa função usa uma variável _velocity_ (velocidade) e a aplica na posição do corpo que a invocou. Dessa forma, para movimentar um personagem em Godot 4, basta calcular sua velocidade, atribuí-la à variável _velocity_ e rodar a função _move_and_slide_, como é feito na linha 28.

Para o caso da gravidade, o movimento vai para baixo (Y positivo), logo, gravidade * delta é aplicado para o corpo a cada _frame_ quando não estiver tocando o chão.

Na linha 17, temos uma verificação de _input_. Caso pressione a tecla "ui_accept" (que se refere, por padrão, às teclas Enter e Barra de Espaço), e o personagem esteja no chão (pois ele não pode pular no ar), a velocidade Y é igualada a JUMP_VELOCITY, que é um valor negativo, causando com que o personagem mova-se para cima (Y negativo).

Após o cálculo do movimento vertical, é calculado o movimento horizontal. A linha 22 declara uma variável que verifica se as teclas direcionais estão pressionadas. Caso a tecla esquerda esteja pressionada, _direction_ é -1. Caso seja a direita, _direction_ é 1. Caso nenhuma ou ambas estejam pressionadas, _direction_ é 0. Isso indica qual direção o personagem deve se mover (-1 para esquerda, +1 para direita).

Em seguida, na linha 23, é verificado se essa direção é diferente de 0. Caso seja, o valor X de _velocity_ é alterado para que o personagem se mova na direção correta. Caso contrário, a velocidade do personagem é diminuída até chegar a 0 através da linha 26.

Por fim, move_and_slide é executado para que essas mudanças calculadas sejam atualizadas. Esse processo inteiro ocorre a cada frame, ou seja, geralmente em torno de 60 vezes por segundo.

Quebrando o código assim, linha por linha, fica muito mais fácil entender como ele funciona, e seguir com mudanças necessárias.

### Próximos Passos

Eu tenho um código para um personagem jogável de um plataforma. Mas isso não é o jogo que eu tinha planejado. Eu devo adaptar o código para seguir da forma que eu desejo. Primeiramente, isso se trata de um _auto runner_, então, a princípio, meu personagem deveria correr sozinho.

Meu primeiro passo foi virar o personagem para que encare a direção onde ele andará. Em seguida, mudei o código da seguinte maneira:

![Código Runner](../Arquivos/Imagens/04_45.png 'Código Runner')
<sup><sub> Ajuste do código do personagem </sup></sub>

Com essa mudança, o personagem não mais reage ao _input_ de direção do teclado, mas sempre segue em frente na direção para onde está olhando. Também incluí paredes nos cantos do mapa para que o personagem não caia no abismo.

![Pós Mudança](../Arquivos/Imagens/04_46.gif "Pós Mudança")
<sup><sub> _Player_ se move sozinho </sup></sub>

OK, a situação evoluiu um pouco, mas temos outro problema, o personagem continua tentando avançar para dentro da parede. Geralmente, em jogos desse estilo, encontrar um obstáculo significa o fim dessa jogada, ou esse tipo de obstáculo não existe. Para o caso do meu jogo, minha intenção é ter fases menores e mais fechadas, então precisarei de outro tipo de solução. 

A solução que pensei é que o personagem irá trocar de direção quando encostar em obstáculo que impede seu avanço. Para isso, fiz com que o personagem trocasse de direção toda vez que encontrar uma parede.

![Código Runner 2](../Arquivos/Imagens/04_48.png 'Código Runner 2')
<sup><sub> Ajuste para colisões com paredes </sup></sub>

![Vai e volta](../Arquivos/Imagens/04_47.gif "Vai e volta")
<sup><sub> Funcionamento após o ajuste </sup></sub>

Quanto ao botão de pulo, decidi mantê-lo por enquanto. Talvez eu faça pulos automáticos mais a frente no projeto, mas, por enquanto, usar a barra de espaço é o suficiente. Fiz também algumas mudanças ao mapa para testar o movimento.

Meu próximo passo foi tentar concretizar minha ideia de construir plataformas no mapa durante a execução do jogo. Para isso, criei um _script_ na cena do mapa em si, em vez da cena do _Player_. Dessa vez, essa não veio pronta para eu adaptar.

![Código Mapa](../Arquivos/Imagens/04_49.png 'Código Mapa')
<sup><sub> Novo _script_ para o mapa </sup></sub>

No _script padrão_, sempre temos duas funções: _ready_ e _process_. Eu poderia usar apenas uma, ambas ou nenhuma delas. Para este caso, não precisarei usar _ready_ por enquanto, mas _process_ será importante. 

Meu objetivo é fazer a seguinte ação: ao clicar em algum pedaço do mapa, eu gostaria que fosse criado um _tile_ no lugar onde cliquei. Eu posso dividir essa ideia em alguns aspectos diferentes:
- Reconhecer o input de clique
- Localizar a posição desse clique no mapa
- Interagir com o _tilemap_ para criar um novo _tile_ nessa posição

Felizmente, isso é tudo bem simples de fazer. A primeira coisa que eu checo em minha função _process_ é se houve um clique do mouse. Para isso, eu uso o _singleton_ _Input_. Um _singleton_, no contexto da _engine_ Godot, se refere a qualquer _script_ que pode ser invocado em qualquer outro _script_ durante a execução do jogo. Ou seja, um _script_ de acesso universal que fica carregado na memória o tempo todo.

_Input_, como o nome sugere, é um _singleton_ que captura qualquer input feito pelo jogador, seja através de um controle, mouse, teclado, ou qualquer outro método de _input_ reconhecido pela _engine_. Daí vem nossa primeira linha, uma condicional. Caso o botão esquerdo do mouse seja clicado, faremos algo:

![Código Mapa 2](../Arquivos/Imagens/04_50.png 'Código Mapa 2')
<sup><sub> Condicional com _input_ </sup></sub>

O que seria esse algo? O que descrevi acima. Primeiro, vamos descobrir a posição do ponteiro do mouse. Uma simples pesquisa no Google me retornou qual função deveria ser usada, _get_global_mouse_pos_.

![Pesquisa 1](../Arquivos/Imagens/04_51.png 'Pesquisa 1')
<sup><sub> Pesquisa para posição do mouse </sup></sub>

![Pesquisa 2](../Arquivos/Imagens/04_52.png 'Pesquisa 2')
<sup><sub> Resultado da pesquisa </sup></sub>

Além de saber a posição no mapa, eu também precisarei incluir essa posição no meu _tilemap_. Eu sei, por experiência, que o _tilemap_ trabalha com uma _grid_ quadriculada, e nela trabalha com coordenadas X,Y. Porém, eu não sabia como traduzir as posições globais para as coordenadas do _tilemap_. Por isso, procurei a documentação da _engine_ para _tilemaps_.

Convenientemente, Godot já deixa a maior parte da documentação disponível no próprio editor de _scripts_. Através do botão "Search Help", eu encontrei a documentação para o _tilemap_. Percebo que _tilemap_ tem muitas funções, então eu procuro por palavras-chave como "position" ou "coordinates". Não demora muito para encontrar o que eu preciso.

![Documentação 1](../Arquivos/Imagens/04_53.png 'Documentação 1')
<sup><sub> Documentação de _Tilemap_ </sup></sub>

A primeira função interessante é _local_to_map_. Ela retorna a posição em coordenadas do mapa para uma **posição local**. Entretanto, a posição adquirida do mouse é uma posição global. Eu sei que isso não vai fazer diferença nesse caso (porque o meu _tilemap_ está na origem, ou seja, a posição global será a mesma que a local), mas apenas por questões de boas práticas, vou incluir a função _to_local_ para passar essa posição global para local. Assim, mesmo que eu tire o mapa da origem global, não terei problemas com isso.

![Documentação 2](../Arquivos/Imagens/04_55.png 'Documentação 2')
<sup><sub> Função relevante </sup></sub>

Essas funções são as peças do quebra cabeça para montar o jogo que desejo ter. Primeiramente, para usar funções do _tilemap_ eu preciso de acesso a ele. Em Godot 4, acessar um nó pelo _script_ é simples, basta criar uma variável anotada como @onready, e apontar para seu nome na árvore com o símbolo $. Além disso, eu crio uma variável para salvar a posição do meu clique (mouse_position), e uma variável para salvar as coordenadas em posição local (tile_position).

![Código Mapa 3](../Arquivos/Imagens/04_56.png 'Código Mapa 3')
<sup><sub> Adicionando funções ao código do mapa </sup></sub>

Tendo feito isso tudo, o próximo passo é: reconhecer se não há nenhum bloco na posição clicada, incluir um bloco caso não tenha nada. Nesse caso, as funções relevantes são _get_cell_source_id_, que retorna o ID do _tile_ nesta coordenada, e -1 caso não haja nada. E a função _set_cell_, que insere determinado _tile_ na coordenada indicada.

![Documentação 3](../Arquivos/Imagens/04_54.png 'Documentação 3')
<sup><sub> Função para encontrar o ID do _tile_ </sup></sub>

![Documentação 4](../Arquivos/Imagens/04_57.png 'Documentação 4')
<sup><sub> Função para configurar um _tile_ </sup></sub>

Essas duas são as últimas peças necessárias para criar o que eu tenho em mente. Caso o ID para esta coordenada seja -1, sabemos que isso é um espaço vazio, logo, inserimos a célula 0 nessa posição.

![Código Mapa 4](../Arquivos/Imagens/04_58.png 'Código Mapa 4')
<sup><sub> Aplicando as funções ao código do mapa </sup></sub>

![Protótipo Novamente](../Arquivos/Imagens/04_59.gif "Protótipo Novamente")
<sup><sub> Resultado das adições ao protótipo </sup></sub>

Se você deu uma olhada no _gif_ acima, provavelmente notou um problema. É possível criar plataformas na mesma posição onde o personagem está, causando com que ele seja lançado para cima em alta velocidade. Não preciso dizer que isso não estava em minhas intenções. Outra coisa que eu notei foi que o personagem é rápido demais, o que dificulta o controle de onde você está incluindo blocos ou não. Por ora, decidi incluir também a opção de excluir blocos, apenas para teste.

A primeira coisa que fiz foi incluir ainda **outro** _tilemap_. Este outro _tilemap_ permite que eu construa um mapa que não pode ser deletado, mas que tudo aquilo que o jogador construir possa ser. Assim, não encontro o problema de o jogador destruir o mapa completamente (o que poderia ser interessante, mas não é minha intenção com esse jogo).

![Código Mapa 5](../Arquivos/Imagens/04_60.png 'Código Mapa 5')
<sup><sub> Adicionando deleção de _tiles_ </sup></sub>

Aqui, incluí também o _tilemap2_. Agora, a primeira verificação procura se existe um _tile_ nessa coordenada tanto para o _tilemap_ 1 quanto para o 2, e caso contrário o _tile_ é inserido no _tilemap2_. Em seguida, fiz um bloco de código similar ao anterior para o botão direito do mouse. Para o botão direito, se existe alguma coisa na coordenada clicada, esse _tile_ é deletado.

Também fiz uma mudança ao código do _Player_. Nele incluí um nó de "Area2D". Este nó tem algumas propriedades especiais para detecção de vários objetos, inclusive, verificação se o mouse está dentro de sua área, o que será útil para mim. Minha intenção aqui é que eu **não** consiga criar novos _tiles_ se o mouse estiver muito próximo do jogador.

![Mudança ao Player](../Arquivos/Imagens/04_61.png 'Mudança ao Player')
<sup><sub> Ajuste de colisões no _Player_ </sup></sub>

Por isso, criei essa área em volta do _Player_. Além disso, incluí os sinais relevantes no código. No menu na direita, existe uma opção "Node", onde você pode ver os diferentes _signals_ que cada nó possui. Estes _signals_ são ativados em reação a diferentes condições. Nesse caso, selecionei as condições "Mouse entered" e "Mouse exited" para a área 2D. 

![Signals](../Arquivos/Imagens/04_62.png 'Signals')
<sup><sub> _Signals_ </sup></sub>

Ao clicar duas vezes em qualquer _signal_, o mesmo cria um nome e pede para selecionar a qual nó este sinal será conectado. Essa conexão apenas ocorre quando um nó contém um script. Aqui a minha intenção é conectá-lo ao próprio _Player_.

![Signals 2](../Arquivos/Imagens/04_63.png 'Signals 2')
<sup><sub> Conectando _signal_ </sup></sub>

Neste exemplo, ele só pode ser conectado ao próprio _Player_. Porém, eu preciso que essa informação chegue ao _script_ do meu mapa. Eu poderia acessar o meu _Player_ através do _script_ do mapa. Mas, uma opção de melhor organização é emitir um novo sinal a partir do meu próprio _Player_. Esse sinal será criado manualmente, já que o sinal de Area2D não existe para um CharacterBody2D (que é o tipo do meu _Player_).

O primeiro passo é declarar o sinal no código. Em seguida, editar o código dos sinais abaixo para emiti-lo. Para cada um, emito o _signal_ como _true_ ou _false_, para que eu possa usar o mesmo sinal para os dois casos.

![Signals 3](../Arquivos/Imagens/04_64.png 'Signals 3')
<sup><sub> Declarando _signal_ por código </sup></sub>

![Signals 4](../Arquivos/Imagens/04_65.png 'Signals 4')
<sup><sub> Emitindo _signal_ por código </sup></sub>

Agora, posso pegar este _signal_ que criei no meu _Player_ e usá-lo no meu mapa principal. Uma vez conectado, eu crio uma variável _mouse_on_player_ e a configuro como _false_. Agora, toda vez que o mouse entrar ou sair da Area2D do meu _Player_, essa emitirá um _signal_ que causará com que o _Player_ emita o _signal_ com _true_ ou _false_, e esse valor será atribuído à variável _mouse_on_player_. 

![Signals 5](../Arquivos/Imagens/04_66.png 'Signals 5')
<sup><sub> Conectando _signal_ ao mapa </sup></sub>

![Signals 6](../Arquivos/Imagens/04_67.png 'Signals 6')
<sup><sub> Nova função atrelada ao _signal_ </sup></sub>

Por fim, eu incluo uma última alteração no código do meu mapa. Nas linhas 13 e 14, caso o meu mouse esteja na área delimitada pelo Area2D, o jogador não conseguirá incluir blocos novos nessa posição, pois o comando retorna, interrompendo a execução da função neste frame. Isso não acontece para o caso de deleção. Ou seja, o jogador consegue destruir blocos próximos a ele, mas não consegue criar novos.

![Signals 7](../Arquivos/Imagens/04_68.png 'Signals 7')
<sup><sub> Ajuste no código do mapa </sup></sub>

![Execução pós mudança](../Arquivos/Imagens/04_69.gif "Execução pós mudança")
<sup><sub> Execução após os ajustes </sup></sub>

Agora é possível notar que eu exagerei um pouco no tamanho da minha área, principalmente para baixo, e eu mudei o tamanho da área mais a frente para não incluir o espaço logo abaixo do personagem. De qualquer forma, a deleção e bloqueio pela área estão funcionando normalmente. 

![Ajuste de área](../Arquivos/Imagens/04_70.png "Ajuste de área")
<sup><sub> Ajuste de área </sup></sub>

Após fazer tudo isso, eu subi o progresso para o _github_, para salvar essa versão em algum outro lugar.

### Um pequeno problema

Ao continuar brincando com este protótipo, eu notei que ele não era muito o que eu tinha em mente. Enquanto eu consegui criar o que havia imaginado, isto não era muito divertido. 

Talvez você desenvolva o seu projeto e consiga ver nele a semente para sua visão original do jogo. Neste caso, siga em frente. Porém, é provável que você se encontre na mesma situação que eu. As coisas não estão se realizando da forma que você esperava. Neste caso, vale a pena revisar o seu _design_ para o jogo, e melhorá-lo aos poucos para que a ideia que sua ideia se concretize da melhor forma possível.

Após pensar muito sobre isso, e testar diferentes velocidades e ideias, cheguei à conclusão de mudar um pouco a ideia do jogo. Mas como minha ideia evoluiu?

A primeira coisa que fiz foi analisar outros jogos de plataforma. Não consegui encontrar um jogo com uma ideia similar, onde você mesmo constrói o mapa em tempo real. Mas construir o mapa em si é uma ideia que já existe em jogos como _Mario Maker_. Neste jogo, você constrói sua fase _antes_ e a joga em seguida, podendo compartilhá-la com outros jogadores. 

Minha intenção não é criar um jogo como _Mario Maker_, mas isso me deu uma ideia interessante. E se toda a edição da fase fosse feita _antes_ que ela começasse? Assim, você ainda é responsável por arranjar o mapa, mas também tem que navegá-lo, e o problema de ter que criar blocos mais rápido do que você pode raciocinar é resolvido. Porém, isso tira o foco no _gameplay_ rápido que eu queria inicialmente. Para manter esse _gameplay_, pensei em outro elemento interativo, o arco e flecha que meu personagem Sleepy costuma usar em outros jogos.

Logo, o design revisado do meu jogo é o seguinte: ao início de cada fase, você é apresentado uma fase com diversos objetos que podem ser rearranjados. Em um primeiro momento, você os rearranja da maneira que achar melhor. Em seguida, você terá um botão de _play_ que iniciará a execução da fase, onde você deve controlar os pulos e o arco e flecha de Sleepy para alcançar o final da fase.

### Protótipo 0 v2

Imediatamente eu me ponho a trabalhar nesta segunda versão do meu protótipo. Primeiramente, após certificar-me que o meu backup estava disponível no _github_, desfiz todo o meu _script_ na cena do mapa. Para o meu _Player_, excluí a Area2D e as funções para os dois sinais, além do sinal que declarei. 

Além disso, no mapa original, mudei a posição de meu _Player_ para que ele comece a execução caindo. Um detalhe importante sobre essa nova ideia é de que, a princípio, mais do mapa deve estar visível a todo o tempo. Por isso, aumentei a resolução da tela novamente. Também adicionei um novo nó à cena de meu mapa, e o renomeei para "Objects". Este nó vai servir como um _container_ para todos os objetos que incluirei em cada fase.

![Ajustes Mapa](../Arquivos/Imagens/04_71.png 'Ajustes Mapa')
<sup><sub> Ajustes no mapa </sup></sub>

Por agora, criei estes objetos como instâncias do _StaticBody2D_, usando a imagem de meu _tileset_ como textura para eles. Estes objetos também são corpos como os rígidos e cinemáticos, mas eles são estáticos, e não são feitos para serem movidos em conjunto com atualizações de _frames_ de física. Estes serão os objetos de teste. 

![Novos objetos](../Arquivos/Imagens/04_72.png 'Novos objetos')
<sup><sub> Novos objetos </sup></sub>

Agora, eu preciso fazer com que seja possível arrastá-los antes do jogo começar. Além disso, preciso fazer com que o jogador **não** comece a andar antes que eu permita que isso aconteça. Para isso, incluirei um botão de _play_ no canto da tela. Até que esse botão seja pressionado, meu jogador permanecerá desativado. Para isso, incluí um nó _Control_, que servirá como _container_ para nós de interface, e um _TextureButton_, que será o botão de _play_ ao qual me referi.

![Nós de controle](../Arquivos/Imagens/04_73.png 'Nós de controle')
<sup><sub> Nós de controle </sup></sub>  

Criei uma simples textura para este botão e a incluí como a textura do nó relevante. Além disso, incluí a função _ready_ no _script_ do _Player_, para que seu processo físico seja desativado antes de iniciar a execução do jogo, e ele não se jogue da plataforma imediatamente.

![Script player stop](../Arquivos/Imagens/04_74.png 'Script player stop')
<sup><sub> Ajuste em função _ready_ </sup></sub>

Tratando-se dos objetos que devem ser arrastados, ativei a opção _pickable_ em suas abas de _Input_. Esta opção permite com que eles sejam clicáveis e arrastáveis. Por enquanto, porém, botão de _play_ não faz nada.

![Opção de arrasto](../Arquivos/Imagens/04_75.png 'Opção de arrasto')
<sup><sub> Opção de arrasto </sup></sub>

Antes de poder testar se o que fiz funcionou, percebo que não consigo ver os objetos, pois a câmera continua centrada no _Player_, e sequer posso mexê-lo. Por isso, passei a trabalhar na câmera. No próprio _script_ do mapa, na função _ready_, incluo um limite de fundo e de esquerda para a câmera. Esse limite impede que a câmera caia além do fundo da tela, ou vá além do início do mapa. 

![Câmera inadequada](../Arquivos/Imagens/04_76.png 'Câmera inadequada')
<sup><sub> Câmera inadequada </sup></sub>

Além disso, incluí no processo um update para que a posição da câmera seja sempre atualizada para a posição do _Player_ (respeitando os limites configurados).

![Configurando câmera](../Arquivos/Imagens/04_77.png 'Configurando câmera')
<sup><sub> _Script_ da câmera </sup></sub>

Ao tentar rodar isso, percebo que os objetos ainda não são arrastáveis. A opção _pickable_ não fez exatamente o que eu esperava. Sem problemas, a gente descobre um jeito. Dessa vez, encontrei uma forma de atualizar a posição do objeto. Nesse caso, tive que atrelar um _script_ diretamente ao objeto arrastável. 

![Script para objetos arrastáveis](../Arquivos/Imagens/04_78.png 'Script para objetos arrastáveis')
<sup><sub> _Script_ para objetos arrastáveis </sup></sub>

Criei algumas cópias deles, e as incluí na tela. Agora, sim, conseguimos arrastar os objetos. Porém, permanece um problema: conseguimos arrastar objetos para dentro de outros. Terei que lidar com isso eventualmente.

![Gif, Objetos arrastáveis](../Arquivos/Imagens/04_79.gif "Gif, Objetos arrastáveis")
<sup><sub> Objetos arrastáveis </sup></sub>

Outra coisa que eu gostaria de poder arrastar é a câmera, como em um arrasto (_scroll_) de celular. Isso não é tão simples de implementar, pois não desejo que isso aconteça durante a execução do jogo em si, apenas na etapa de preparação da fase. Para isso, utilizarei um conceito muito importante para o desenvolvimento de jogos, o das máquinas de estado.

Primeiramente, preciso decidir como isso vai funcionar. Minha intenção é que, por padrão, arrastar o clique na tela causará com que ocorra o scroll da câmera. Por esse motivo, arrastar objetos deve tomar outro formato. A solução que pensei foi que, caso o jogador pressione/clique a posição do objeto por certo tempo, este irá entrar no modo de arrasto, e a câmera não mudará de posição. Mais a frente, interessa fazer um scroll seletivo da tela (por exemplo, quando o objeto está no canto).

![Máquina de estados](../Arquivos/Imagens/04_80.png 'Máquina de estados')
<sup><sub> Máquina de estados </sup></sub>

Dividi a execução da cena em três estados: _Prepare_, _Select_, _Run_. _Prepare_ é o estado padrão, onde você pode fazer o scroll da tela e selecionar objetos. _Select_ é o estado onde você está selecionando um objeto. E _Run_ é o estado para iniciar a execução de cada fase. Mudei o processo para seguir com esses estados, e ali ele se refere a dois novos _scripts_. Um para a câmera, e outro para o _container_ de objetos.

Primeiramente, alterei o _script_ dos objetos para _apenas_ selecioná-los quando o jogador segura o clique por 0.15 segundos. Isso evita atrapalhar o jogador, selecionando um objeto quando ele deseja apenas fazer o _scroll_ da tela.

![Script de objetos arrastáveis novo](../Arquivos/Imagens/04_81.png 'Script de objetos arrastáveis novo')
<sup><sub> _Script_ de objetos arrastáveis </sup></sub>

Se o jogador mover o toque antes do timer acabar, o objeto não é selecionado, e o _scroll_ normal da tela segue. Caso contrário, o objeto é selecionado e arrastado. Em seguida, adicionei um _script_ ao _container_ de objetos. Este simplesmente verifica se algum dos objetos está selecionado. Caso haja algum, marca uma variável como verdadeiro. E caso contrário, esta é marcada como falso.

![Script de objetos arrastáveis novo](../Arquivos/Imagens/04_82.png 'Script de objetos arrastáveis novo')
<sup><sub> Script de objetos arrastáveis novo </sup></sub>

De volta em nosso _script_ com a máquina de estados. Nossa condição de mudança de estados é o _script_ acima. Quando algum objeto está selecionado, nosso estado é o de seleção. Caso contrário, vamos ao estado padrão de preparação. A condição para o estado de início ainda não existe.

![Máquina de estados 2](../Arquivos/Imagens/04_83.png 'Máquina de estados 2')
<sup><sub> Máquina de estados 2 </sup></sub>

Dependendo de qual for esse estado, permitimos ou não que a câmera seja arrastada com a variável _can_drag_ do script da câmera. 

![Máquina de estados 3](../Arquivos/Imagens/04_84.png 'Máquina de estados 3')
<sup><sub> Máquina de estados 3 </sup></sub>

E por fim, o _script_ da câmera é bem simples: caso a variável _can_drag_ seja verdadeira, fazemos o scroll da tela para o lado onde ela for deslizada. O _gif_ abaixo ilustra os resultados:

![Camera Script](../Arquivos/Imagens/04_85.png 'Camera Script')
<sup><sub> Script da câmera </sup></sub>

![Gif, Arrasto e Scroll](../Arquivos/Imagens/04_86.gif "Gif, Arrasto e Scroll")
<sup><sub> Arrasto e scroll </sup></sub>

Agora, resta trabalhar na execução em si. Incluí o botão de _play_ embaixo de um nó _CanvasLayer_, que faz que os objetos abaixo dele sempre estejam presentes na tela. Em seguida, conectei o sinal de clique do botão ao nó de controle principal, e esse ao nó pai do mapa. Ao clicar no botão, a cadeia de _signals_muda o estado no _script_ principal, e permite que o jogo se inicie.

Beleza, minha ideia funcionou. É claro, isso ainda não é um jogo. Temos algumas coisas a considerar: problemas de colisão, um _highlight_ para objetos selecionados, velocidade, _scroll_ da tela, condições de vitória e derrota. E, olhando melhor, percebo que ainda é possível arrastar os objetos durante a execução. Ainda falta bastante para termos um protótipo 0 completo. Mas já temos uma ideia de como esse jogo será.

![Execução completa](../Arquivos/Imagens/04_87.gif "Execução completa")
<sup><sub> Execução do protótipo </sup></sub>

Primeiramente, conserto o problema que mencionei acima, para que o jogador não possa arrastar objetos ou deslizar a tela durante a execução da fase. Além disso, incluí um _shader_ de contorno nos objetos quando selecionados, adaptado a partir [deste _shader_](https://godotshaders.com/shader/2d-outline-inline/). Lembrando-me de incluir a opção _local_to_scene_ para que o mesmo _shader_ não se aplique a todas as cópias do mesmo objeto em tela.

![Condicionais de arrasto](../Arquivos/Imagens/04_89.png 'Condicionais de arrasto')
<sup><sub> Condicionais para o arrasto </sup></sub>

![Shader de outline](../Arquivos/Imagens/04_88.png 'Shader de outline')
<sup><sub> _Shader_ de cotorno </sup></sub>

Decidi incluir também uma condição de derrota, já que eu estou caindo várias vezes no buraco em meus testes, e tenho que reiniciar o jogo toda vez. No fundo do mapa, incluí um nó do tipo _Marker2D_, que eu nomeei BottomBoundary, e que basicamente marca uma posição. Além disso, incluí uma condição na função _process_, que roda uma função _kill_ do _Player_ caso sua posição Y seja maior do que a posição Y do _Marker2D_.

![Marker2D](../Arquivos/Imagens/04_90.png 'Marker2D')
<sup><sub> Configurando limites </sup></sub>

![Kill caso abaixo do marker](../Arquivos/Imagens/04_91.png 'Kill caso abaixo do marker')
<sup><sub> _Kill_ caso abaixo do fundo da tela </sup></sub>

No _Player_, a função _kill_ simplesmente desativa seu processo físico, e emite um _signal_ que será reconhecido pelo _script_ do mapa. Você pode pensar que é redundante que o mapa invoque uma função que simplesmente irá emitir um _signal_ para ele mesmo. Mas eu faço isso porque este não será o único meio pelo qual o _Player_ morrerá, então este será interessante para outras situações.

![Função kill](../Arquivos/Imagens/04_92.png 'Função kill')
<sup><sub> Função _Kill_ </sup></sub>

Minha intenção é que, após o jogador morrer, o jogo imediatamente volte ao estado em que estava antes que isso acontecesse. Ou seja, que o mapa permaneça da maneira que estava para que o jogador possa testar uma iteração nova a partir da anterior. Dessa forma, não faz sentido reiniciar a cena inteira, pois as posições dos objetos seriam reiniciadas. O que preciso fazer é retornar apenas o jogador (e quaisquer coletáveis) para a posição original deles, e voltar ao estado de edição da fase.

Para isso, incluí uma variável que salva a posição inicial do jogador configurada no editor do mapa. Além disso, uma função que retorna o personagem para o lugar original. Não incluirei a câmera, porque provavelmente o ponto de interesse de edição para o jogador será onde ele morreu. Além disso, incluirei um marcador de mortes mais a frente no desenvolvimento. Também mudei o funcionamento da função _block_grabbing_ para levar uma condição _true_ ou _false_, para que eu possa reativá-los quando necessário.

![Salvando posição do Player](../Arquivos/Imagens/04_93.png 'Salvando posição do Player')
<sup><sub> Salvando posição incial </sup></sub>

![Soft reset](../Arquivos/Imagens/04_94.png 'Soft reset')
<sup><sub> Função de reset </sup></sub>

Pensando bem, talvez seja interessante fazer com que a câmera volte à posição inicial antes que o personagem passe a se mover. Também vou considerar usar um animador _tween_ para fazer isso mais adiante. Por agora, quero fazer com que objetos não consigam sobrepor um ao outro. E isso causou bastante trabalho e dificuldade, e ainda não está perfeito. Também fiz com que a câmera fizesse o scroll durante a seleção, o que foi bem simples. 

Mais importante que qualquer coisa, falta algo fundamental para que isso se torne um jogo. Nós temos uma condição de derrota, mas não uma de vitória. Fiz um objeto para representar a vitória do jogador. Eu mudo o formato da fase e incluo o objeto _goal_. E dou ao meu _Player_ um nome de classe. Por fim, _Goal_ recebe um _script_ simples. Caso entre um corpo da classe _Player_, emita um _signal_ de vitória.

![Novo Mapa](../Arquivos/Imagens/04_95.png 'Novo Mapa')
<sup><sub> Novo mapa </sup></sub>

![Classe do Player](../Arquivos/Imagens/04_96.png 'Classe do Player')
<sup><sub> Classe do _Player_ </sup></sub>

![Goal script](../Arquivos/Imagens/04_97.png 'Goal script')
<sup><sub> Script da bandeira </sup></sub>

![Tela de vitória](../Arquivos/Imagens/04_98.png 'Tela de vitória')
<sup><sub> Função da tela de vitória </sup></sub>

Ao final disso, quando meu _Player_ encostar na bandeia _goal_, a função fará com que o novo painel (ColorRect) que adicionei apareça com a mensagem de vitória. Agora, podemos chamar isso de um jogo. Não é um jogo bom, e não é um jogo completo, mas é um jogo, como pode ver no _gif_ abaixo:

![Protótipo 0](../Arquivos/Imagens/04_99.gif "Protótipo 0")
<sup><sub> Protótipo 0 </sup></sub>

E eu vou fechar meu protótipo 0 por aqui. Ainda há muita coisa para fazer, como o documento de _backlog_ indica. E isso é só o que eu pensei por agora. Mas o _core_ do jogo em si foi criado. A partir do capítulo da versão _alfa_, vou focar menos na execução da programação em si, e em boas práticas de programação geral. 

## Quando parar

O objetivo de seu protótipo 0 é testar sua ideia de forma mais concreta do que só na sua imaginação. Os básicos de controle, física e funcionamento deverão ser o seu foco. No meu projeto exemplo, eu sequer implementei a maioria das mecânicas, apenas incluí o mínimo para ver que a ideia de meu jogo era viável e divertida. Com isso feito, já me senti preparado para partir para a próxima etapa, a versão alfa.

## Conclusão

Ao final desse capítulo, espero que tenha uma certa ideia de como planejar e executar a criação de seu protótipo 0. Isso não deve ser algo muito formal, e eu não me preocupei muito com boas práticas ou com um processo tão organizado. Meu único objetivo era completar uma simples versão jogável de minha ideia, e o seu deve ser similar a isso.

É claro, isso também se deve ao fato de que o meu é um projeto simples. Se o seu objetivo é criar um MMO RPG, ou um jogo com dúzias de menus, cálculos e opções diferentes, o seu protótipo 0 seria um projeto maior. Mas tente sempre focar apenas nos aspectos fundamentais. Se é um jogo de carta, preocupe-se com fazer os cálculos funcionarem e os objetos interagirem, não em como as cartas se encaixam na tela, ou nos efeitos. Da mesma forma, se o seu RPG tem foco em combate, tente montar uma versão simples desse combate. Etc.

O trabalho de criar esse protótipo inicial não é trivial. E esse é um passo muito importante. Se o seu time é inexperiente, ele vai naturalmente encontrar problemas e dúvidas durante o processo. 

No [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo5.md) discuto o que fazer quando você fica sem saber o que fazer durante a execução de etapas de programação. E no [capítulo seguinte a ele](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo6.md), começo a falar das versões _alfa_ de seu projeto.
