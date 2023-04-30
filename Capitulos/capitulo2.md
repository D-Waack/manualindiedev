
# Capítulo 2: Preparação
"Um homem escolhe, um escravo obedece." - Andrew Ryan, "Bioshock" (2007)

![Capítulo 2 capa](../Arquivos/Imagens/capa_02.jpg 'A man chooses, a slave obeys.')

## Introdução

Após documentar o seu projeto, o próximo passo é começá-lo. Entretanto, existem inúmeros ambientes, linguagens, formatos e plataformas nas quais você pode desenvolver um jogo.

E você tem que escolher uma.

É claro, eu pretendo te ajudar com essa escolha. Mas ao final do dia, isso será decidido por você (ou o programador em sua equipe). E essa escolha vai mudar completamente como o desenvolvimento de seu jogo vai funcionar.

## Frameworks e Engines

Todo jogo é basicamente um conjunto de sistemas diferentes, sendo executados ao mesmo tempo e interagindo entre si. 

Por exemplo, quando eu clico no executável de _Minecraft_, aparece uma tela de menu principal (visual); ao mesmo tempo, uma música agradável começa a tocar (áudio); e se eu mexer o meu mouse e clicar em um botão, a tela vai reagir e fazer alguma coisa (_input_); se eu clicar em _multiplayer_, o jogo vai se conectar a internet e tentar se comunicar com um servidor (_networking_); se eu clicar em novo mundo, ele vai criar um (geração de mapas); e ao final, meu personagem será livre para interagir com esse mundo, onde várias coisas funcionam como o mundo real (simulação de mundo e física).

Tudo isso acontece simultâneamente e de maneira harmoniosa, mas no plano de fundo, vários processos diferentes são executados ao mesmo tempo para garantir que tudo aconteça na ordem e maneira correta.

No contexto de desenvolvimento, você vai encontrar cada uma dessas tarefas (_networking_, input, _display_ visual, gerenciamento de música, etc.) executada pelo que chamamos de uma "biblioteca" (_library_). Uma biblioteca para redes geralmente vai conter diversas funções necessárias para conectar diferentes computadores em um único jogo, enquanto uma biblioteca gráfica vai conter diferentes funções para mostrar coisas em sua tela.

Como cada biblioteca só se preocupa com uma tarefa, você não pode ter um jogo usando apenas uma. É aí que entram os _frameworks_.

Um _framework_ já fez o trabalho de juntar diversas bibliotecas para uso unificado. 

A melhor escolha para desenvolvimento costuma vir no formato de uma _Game Engine_ (motor de jogos), que são programas de computador que oferecem um ambiente quase completo para a construção de um jogo. Eles fazem a maior parte do trabalho, incluindo renderizar os gráficos, incluir áudio, gerenciar memória, simular física. Algumas vão até incluir editores de mapas e outras ferramentas úteis.

Para um desenvolvedor _indie_, partir de uma dessas é provavelmente a melhor escolha. Porém, existem casos onde uma _engine_ não oferece as ferramentas necessárias para que seu jogo seja criado da maneira que deseja. Neste caso, existem algumas opções: 
- tentar forçar que a _engine_ faça o que deseja (através de uma gambiarra, talvez);
- usar uma _engine_ diferente;
- criar sua prórpia _engine_;
- usar um _framework_.

Você vai perceber que muitos desenvolvedores AAA vão fazer seus jogos em uma _engine_ já estabelecida, ou aparecer com uma nova. Por exemplo, "Fortnite", um jogo bem popular atualmente, desenvolvido pela empresa _Epic Games_, foi criado usando a _engine_ Unreal. Enquanto "Resident Evil Village", um jogo que eu tenho jogado atualmente, foi desenvolvido pela empresa _Capcom_, usando sua própria _engine_ "RE ENGINE".



## Game Design Document (GDD)

Não existe um padrão exato para como o GDD deve ser criado. E se você procurar online, você vai encontrar dúzias de padrões e modelos/templates diferentes. Na hora de delimitar o formato do seu documento, é importante considerar quem verá o documento e quanto tempo você quer passar detalhando-o. Pessoalmente, eu tento ser curto e objetivo nos meus, tentando passar o máximo de informação no menor espaço possível.

O seu GDD pode estar em qualquer lugar entre um documento simples de 3 ou 4 páginas, até um enorme documento descrevendo cada detalhe do funcionamento de seu jogo como a [_Doom Bible_](https://5years.doomworld.com/doombible/doombible.pdf) (GDD do jogo Doom de 1993). Como o seu projeto acabou de começar, meu conselho é seguir a primeira opção. Porém, durante o desenvolvimento do seu projeto, é esperado que o documento cresça consideravalmente, então sinta-se à vontade para colocar quanto detalhe achar interessante no futuro.

Eu criei um template bem simples que costumo usar para a proposta inicial do jogo, e vou usá-lo aqui para exemplificar um preenchimento inicial. Se desejar usá-lo: 
- [Versão Word](/Arquivos/modelo_GDDv1.2.docx) 
- [Versão LibreOffice](/Arquivos/modelo_GDDv1.2.odt)

Se procura por inspiração, vários exemplos notáveis de GDDs podem ser encontrados no seguinte repositório no Github: [Awesome GDDs](https://github.com/Roobyx/awesome-game-design). Note que a maioria destes vão ser muito maiores e mais complexos do que a especificação do seu projeto. Isso é esperado. Outra coisa interessante é que, se você observar, vários desses documentos são bem diferentes do que o jogo final se tornou. Isso também pode acontecer com o seu projeto, e pode ser algo bom ou ruim.

Enquanto eu deixei várias notas no modelo do documento, achei relevante falar brevemente sobre cada campo aqui. Você pode encontrar o GDD inicial para os 2 projetos desenvolvidos em conjunto com o manual nos seguintes links: [Sleepy Runner], [Topdown Space Shooter]

### Conceito
A primeiro seção, "Conceito", tem o objetivo de explicar a ideia por trás do jogo de maneira simples e sucinta.  
O "título provisório" é exatamente o que o nome implica. Talvez te interesse incluir um título de projeto. Não se preocupe muito em decidi-lo, o título final do jogo em si pode ser decidido mais a frente no projeto.  
O "conceito inicial" é uma explicação de qual é a ideia geral para o jogo. Explique a ideia do jogo, e porque ela é interessante.  
"Gêneros" se refere a classificação do jogo: É um shooter como _Call of Duty_? Ou um jogo de plataforma como _Super Mario Odyssey_? Talvez seja um jogo de corrida, ou um _metroidvania_. Qual é o estilo da arte? O estilo da câmera? Pense em outros gêneros também. Gêneros geralmente serão usados no _marketing_ de seu jogo.  
A intenção de "detalhes interessantes" é dar um destaque aos atributos únicos ou de maior interesse no seu jogo. Isso pode ser parte do que descreveu no conceito inicial.  
O "público alvo" é também bem óbvio. Para qual público este jogo é criado? Ou seja, que tipo de jogador você deseja interessar com seu projeto?

### Conceito Exemplificado 1
Título Provisório: Sleepy Runner  
Conceito Inicial: Um jogo sobre um pequeno espírito da névoa correndo através da terra. Sleepy foi forçado a vestir as botas dos pés inquietos, tornando-o incapaz de parar de correr. Este é um jogo onde o personagem corre automaticamente, e o jogador deve tocar na tela e interagir com diversos objetos para livrá-lo de todos os perigos em seu caminho.  
Gêneros: Plataforma, Puzzle, Autorunner, Sidescroller, Pixelart, Mobile  
Detalhes Interessantes: O jogo toma um formato diferente do habitual. Geralmente, jogos do gênero “autorunner” (corredor autmático) contêm mapas infinitos (endless runners), onde o jogador deve reagir a diferentes obstáculos escolhidos pseudo-aleatoriamente que vêm cada vez mais rápido (e.g. Subway Surfer, Temple Run, entre outros). A ideia desse jogo não é essa, nesse sentido, ele é mais parecido com um jogo puzzle, tendo fases curtas onde o jogador deve descobrir a melhor forma de alcançar determinado objetivo, controlando objetos da fase como plataformas e objetos do cenário.  
Público Alvo: O público-alvo são os jogadores de celular casuais. O jogo será simples e fácil de entender, com uma estética agradável.  

### Detalhes Técnicos
A segunda seção, "Detalhes Técnicos" se refere a vários aspectos que serão importantes durante a construção do jogo. Caso não saiba como responder um, não se preocupe, isso ficará melhor definido conforme seu projeto evoluir.  
A "plataforma" é, como o nome sugere, a plataforma onde seu jogo será executado. Podem ser computadores, celulares, navegadores, consoles de jogos, entre outros. E qualquer combinação destes. Lembre-se que fazer uma versão para um ambiente diferente (port) pode não ser um processo tão simples. Certas ferramentas e motores vão facilitar muito esse processo, para outros casos será impossível. O mesmo pode acontecer entre diferentes sistemas operacionais de computador. A plataforma em que deseja que seu jogo rode deve influenciar a escolha do ambiente de desenvolvimento.  
As "tencologias" estão intimamente relacionadas ao tópico anterior. Nós entraremos no mérito de como preencher esse tópico no capítulo seguinte. Porém, basicamente, se referem a o que você vai usar para criar o seu jogo. Por exemplo, motores como Unity, Unreal e Godot, ou _frameworks_ como Spritekit, Phaser e Starling. Talvez algo mais específico como RPG Maker, ou algo mais fácil de usar como o Game Maker. Qual linguagem será usada? Talvez javascript ou C++? Ou quem sabe usará uma ferramenta em que não há necessidade de programar em uma linguagem? Novamente, será mais interessante preencher isto no próximo capítulo, a não ser que já tenha alguma preferência.
A "interação" se refere às interfaces com as quais o seu jogador vai interagir com o jogo em si. Seja através de _touchscreen_, controles, mouses/teclados ou algum outro tipo de dispositivo de _input_. Também vale incluir situações especiais como controle por movimento/giroscópio. No caso de controles de console, é interessante incluir se existe vibração e outras reações do controle também.  
A "monetização" se refere a como você pretende ganhar dinheiro com o jogo. Se pretende vendê-lo como um jogo separado. Ou se será free 2 play com microstransações para diferentes personagens, cosméticos, etc. Quem sabe seu jogo é completamente grátis e não pretende ganhar dinheiro algum com ele? Qualquer que seja sua ideia, aqui é o lugar onde pode incluí-la.
As "ferramentas de desenvolvimento" são uma lista de ferramentas que serão utilizadas para a criação de recursos diversos como música, arte, modelos 3D, mapas, entre vários outros.

### Detalhes Técnicos Exeplificados 1

### Detalhes Conceituais
A terceira seção, "Detalhes Conceituais", começa a lidar com alguns aspectos mais abstratos, relacionados à narrativa. É possível que seu jogo não tenha um enredo, personagens ou um cenário específico. Por exemplo, um jogo _Candy Crush_ ou algo como Xadrez dificilmente vai ter uma história. Neste caso, pode pular os tópicos que achar desnecessários.
O "cenário" se refere ao mundo onde o jogo acontece. Deve ser descrito o tipo de ambiente onde a história aconteceria. Pode ser simplesmente descrito como um mundo _steampunk_ ou _cyberpunk_, ou um mundo fantástico, ou um mundo igual ao mundo real. Ou você pode dar mais detalhes. O importante é que um leitor potencial (e você mesmo) consiga imaginar o mundo onde a história do jogo acontece.  
Os "personagens" são os diversos personagens que aparecerão no seu jogo. Protagonistas, NPCs, inimigos, vilões todos podem ser considerados personagens. Caso tenha algum rascunho da aparência de cada um, seria interessante incluí-los aqui também. Mas isso pode ser feito mais adiante, caso ainda não tenha nenhum.  
O "enredo" se refere a história do jogo em si, a narrativa que será contada durante o decorrer do jogo. Não é necessário entrar em detalhes minuciosos sobre cada acontecimento no primeiro momento, mas, se preferir, pode ser feito. Lembre-se que durante o desenvolvimento você e seu time podem fazer várias decisões de mudança na história, então talvez poupe o seu tempo descrever de maneira bem simples até que o projeto esteja mais avançado. Criar uma _storyboard_ demonstrando a história eventualmente também deve estar nos seus planos, mas isso também pode esperar até que tenha um design definido para os personagens.  
O "contexto" engloba qualquer detalhe do enredo que não encaixe nos tópicos anteriores. Por exemplo, se isso é uma sequência, e o que ocorreu antes. Ou se existem acontecimentos paralelos que afetam a história do jogo, mas não são mostrados durante a narrativa.  
Os "temas" são palavras-chave que definirão o estilo do enredo que tem em mente.
O "formato da narrativa" se refere a como a história será contada. Serão _cutscenes_ cinematográficas, ou algo mais simples como caixas de diálogo, animações simples, etc.?

### Detalhes Conceituais Exemplificados 1

### Detalhes de Gameplay
A quarta seção, "Detalhes de Gameplay" se refere mais especificamente a como o jogo vai funcionar. Aqui, o conceito de mecânica é muito importante. Uma mecânica é uma regra ou conjunto de regras que define como o jogo vai funcionar e como o jogador vai interagir com ele.  
As "mecânicas primárias" são as mecânicas que definem o seu jogo e o seu estilo. Por exemplo, para o jogo Super Mario Bros. seria pular e correr. Para o jogo _Call of Duty_, isso seria correr, mirar e atirar. Elas se referem especificamente ao _core loop_, ou seja, as ações principais que o seu jogador fará durante o seu tempo jogando. Podem ser poucas como em Super Mario, ou muitas como em jogos de sobrevivência.
As "mecânicas secundárias" são qualquer mecânica ou regra que não seja principal ao _core loop_ do jogo. Por exemplo, o funcionamento de menus, como funciona a loja de itens em um jogo, como os pontos serão contados, etc...  
O tópico "world/level design" se refere a como as fases, mapas ou mundo em um jogo serão construídos para que o jogo funcione da maneira esperada. Por exemplo, eu poderia colocar o sonic e sua física em uma fase do jogo super mario. Porém, os mapas do Super Mario não são próprios para o tipo de jogo que é o Sonic, onde o objetivo é atingir grandes velocidades e encontrar o melhor caminho. Da mesma forma, Mario não teria como navegar a maioria das fases do Sonic.  
Os "objetivos/condições de vitória" são o que o jogador deve conseguir para atingir vitória no jogo. Seja navegar ao final de uma fase, coletar itens, resolver um enigma, derrotar um inimigo, ou uma combinação de todos esses. Sinta-se livre para descrever como o seu jogo decorre, e como uma condição de vitória pode levar a outra.  
Analogamente, as "condições de derrota" se referem a o que leva a derrota do jogador. Isso pode ser em termos de vidas, tempo, energia, entre vários outros. Em certos casos, pode haver mais de uma condição de derrota, e em muitos jogos, existem vários graus diferentes de derrota. Em _castlevania_, cair em um buraco sem fundo ou levar dano de um inimigo leva a uma derrota temporária, ou uma derrota de grau menor, a morte do personagem. Entretanto, caso o jogador morra várias vezes sem coletar vidas novas, ele alcança o estado "game over", ou seja, a derrota final.  
O "desafio" é tudo aquilo que se coloca entre o jogador e sua condição de vitória. Um desafio muito baixo e seu jogo pode ficar sem graça, um desafio muito alto e seu jogo pode ficar injusto. Na maioria dos jogos, é preferível que exista uma cruva de dificuldade, onde o jogo começa fácil e fica mais desafiador a medida que o jogador começa a dominar melhor suas mecânicas.  
O "sistema de recompensa" envolve o que o seu jogador ganhará ao completar determinado desafio. Isso pode vir em forma de powerups, itens colecionáveis, ugprades ao personagem, equipamento/armas alternativas, skins diferentes, novas habilidades, o nome do jogador em um _ranking_, entre vários outros. Isso é um tópico importante se deseja manter seu jogador engajado continuamente.

### Detalhes Audiovisuais
A quinta seção, "Detalhes Áudiovisuais", diz respeito aos estilos planejados para aspectos visuais e auditórios.  
Não há muito o que explicar para estes casos. "Estilo visual" é sobre como o jogo será visualmente (pixel art, voxel, vector, 3D realista, 3D fantástico, etc.). "Estilo musical" diz respeito ao tipo de música que tocará no fundo do seu jogo (música orquestral, _chiptune_, rock progressivo, música de elevador, vários tipos diferentes, etc.). Os "efeitos sonoros" se refere ao estilo do _sound design_ no geral, se tenta ser realista ou fantástico, se atmosférico ou satisfatório, ou qualquer outra categoria que tiver em mente. O "estilo da interface" tem a ver com os menus e telas que o jogador verá durante o jogo (se existem informações em tela como HUDs, contadores de itens/vidas/pontos, entre outros elementos. 

### Objetos e Assets de Jogo
A sexta seção, "Objetos e Assets de Jogo" será preenchida principalmente no decorrer do projeto conforme suas ideias forem evoluindo. Aqui você vai listar artefatos que serão criados e usados no decorrer do jogo, como entidades e objetos de cenário, e cada uma de suas respectivas representações visuais/sonoras.  
O tópico "entidades" se refere a qualquer personagem que aparecerá no jogo. Este tópico é análogo aos "sersonagens" na seção de detalhes conceituais, mas tem um foco mais focado em simplesmente listar os personagens/vilões para referência.  
O tópico "objetos" deve conter qualquer objeto que não encaixe na categoria de "entidade". Isso geralmente vai incluir objetos interativos que não são simplesmente parte do cenário (eles podem ser "parte" do cenário, mas que geralmente seriam objetos criados separadamente para que possa haver interação com eles).  
O tópico "texturas/modelos/sons/etc." se refere a todo tipo de recurso audiovisual que será necessário durante o jogo, como _sprites_ ou modelos de personagens (e suas texturas), planos de fundo, _skyboxes_ (planos de fundo para o céu), mapas/fases do jogo (sejam imagens ou modelos), músicas de fundo, efeitos sonoros, e quaisquer outros artefatos necessários.

### Planos
A última seção, "Planos", possui apenas um tópico, "wishlist", que é um lugar que eu reservo para listar ideias que eu tive sobre o jogo durante o desenvolvimento, e que não decidi se implementarei ou não ainda. É apenas uma seção para anotações, e não precisa ser preenchida se não for relevante.

## Conclusão
Ao final desse capítulo, você deveria ter uma ideia de como começar a criar seu GDD, ou idealmente já o tenha preenchido conforme lia o capítulo.

No próximo capítulo vamos lidar com a etapa de "Preparação", onde vamos decidir alguns detalhes importantes como o ambiente de desenvolvimento (engine/framework/linguagem) e como organizaremos os arquivos do projeto.
