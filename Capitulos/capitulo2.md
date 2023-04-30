
# Capítulo 2: Preparação
"Um homem escolhe, um escravo obedece." - Andrew Ryan, "Bioshock" (2007)

![Capítulo 2 capa](../Arquivos/Imagens/capa_02.jpg 'A man chooses, a slave obeys.')

## Introdução

Após documentar o seu projeto, o próximo passo é começá-lo. Entretanto, existem inúmeros ambientes, linguagens, formatos e plataformas nas quais você pode desenvolver um jogo.

E você tem que escolher uma.

É claro, eu pretendo te ajudar com essa escolha. Mas ao final do dia, isso será decidido por você (ou o programador em sua equipe). E essa escolha vai mudar completamente como o desenvolvimento de seu jogo vai funcionar.

## Frameworks e Engines

Sua escolha entre _Frameworks_ e _Engines_ vai depender de vários fatores. Para a maioria dos desenvolvedores _indie_, uma _engine_ é a escolha ideal, principalmente para quem deseja criar um jogo sem programar. Porém, é interessante entender um pouco sobre o tópico para melhor entendimento na hora de sua escolha.

Todo jogo é basicamente um conjunto de sistemas diferentes, sendo executados ao mesmo tempo e interagindo entre si. 

Por exemplo, quando eu clico no executável de _Minecraft_, aparece uma tela de menu principal (visual); ao mesmo tempo, uma música agradável começa a tocar (áudio); e se eu mexer o meu mouse e clicar em um botão, a tela vai reagir e fazer alguma coisa (_input_); se eu clicar em _multiplayer_, o jogo vai se conectar a internet e tentar se comunicar com um servidor (_networking_); se eu clicar em novo mundo, ele vai criar um (geração de mapas); e ao final, meu personagem será livre para interagir com esse mundo, onde várias coisas funcionam como o mundo real (simulação de mundo e física).

Tudo isso acontece simultâneamente e de maneira harmoniosa, mas no plano de fundo, vários processos diferentes são executados ao mesmo tempo para garantir que tudo aconteça na ordem e maneira correta.

No contexto de desenvolvimento, cada uma dessas tarefas (_networking_, input, _display_ visual, gerenciamento de música, etc.) costuma ser executada pelo que chamamos de uma "biblioteca" (_library_). Uma biblioteca para redes geralmente vai conter diversas funções necessárias para conectar diferentes computadores em um único jogo, enquanto uma biblioteca gráfica vai conter diferentes funções para mostrar coisas em sua tela. Estas bibliotecas geralmente vêm como código no formato de arquivos DLL, por exemplo em _Javascript_ ou _C++_. Alguns exemplos: FMOD, RakNet, Box2D, Assimp, entre várias outras.

Como cada biblioteca só se preocupa com uma tarefa, você não pode criar um jogo usando apenas uma. É aí que entram os _frameworks_. Um _framework_ já fez o trabalho de juntar diversas bibliotecas em uma coleção para uso unificado. Utilizando um _framework_, você não precisa se preocupar com a maioria dessas tarefas simples, e apenas resta usar essas diversas funções como os componentes do que formará seu jogo. Alguns exemplos de _frameworks_ para jogos incluem: SFML, Phaser, OGRE, LibGDX and MonoGame.

Partindo de _frameworks_, quando subimos um pouco mais o nível de sofisticação e facilidade de uso, chegamos às _Game Engines_ (motores de jogos). Oferecendo o mesmo conjunto de bibliotecas para gráficos, áudio, memória, _networking_, física, etc., além de diversas outras ferramentas úteis no desenvolvimento. Diferente dos _frameworks_, _Engines_ costumam ser ambientes completos, com uma interface gráfica amigável acoplada de um editor de mapas/fases onde se pode ver e editar o jogo em tempo real.

_Engines_ facilitam muito o processo de desenvolvimento. Algumas _engines_ oferecem a possibilidade de criar jogos sem programação alguma, mas programação ainda é uma necessidade na grande maioria delas. No geral, a maior diferença entre _engines_ e _frameworks_ está no editor de mapas, e no visualizador de cenas. Mas muitos entre eles não são tão distantes quanto parece.

Como eu comentei antes, a melhor escolha para um desenvolvedor _indie_ costuma ser uma _engine_. Mesmo que não seja minha recomendação, sinta-se livre para pegar um _framework_ se este for o seu desejo.

De fato, nem sempre uma _engine_ será a escolha ideal para se o projeto. O fato de que a _engine_ já deixa vários componentes prontos para uso pode significar que há muita pouca flexibilidade para fazer algo além do que foi projetado pelo criador da _engine_. Algumas _engines_ como Godot vão permitir que edite seu código fonte, e várias delas permitem a criação de _plugins_ para complementar onde faltam, mas nenhuma dessas soluções é simples de programar. Lembre-se sempre: **Você sacrifica flexibilidade em busca de maior praticidade.**

Na grande maioria dos casos, uma _engine_ vai oferecer exatamente o que você precisa para a criação de seu jogo. Talvez não _qualquer_ engine, e isso é algo que discutimos mais a frente neste capítulo. Mas é muito provável que exista uma ótima _engine_ para a criação do seu projeto. 

Caso você se depare com uma necessidade que sua _engine_ não consegue suprir, existem as seguintes possibilidades: 
- tentar forçar que a _engine_ faça o que deseja (através de uma gambiarra, talvez);
- usar uma _engine_ diferente;
- usar um _framework_;
- criar sua prórpia _engine_ (talvez a partir de um _framework_).

A última possibilidade, criar uma _engine_, ou até mesmo criar um _framework_, é algo que eu desaprovo completamente para o contexto _indie_. Essencialmente, você estaria perdendo um tempo enorme reinventando a roda e provavelmente chegaria a resultados inferiores do que se tivesse apenas utilizado uma _engine_ pronta. Caso seu objetivo seja a criação de uma _engine_ do zero, então vá em frente, mas provavelmente levará um bom tempo até que o manual que está lendo seja de utilidade para você.

Na indústria como um todo, você vai perceber que muitos desenvolvedores AAA vão fazer seus jogos em uma _engine_ já estabelecida, ou criar uma nova. Por exemplo, "Fortnite", um jogo bem popular atualmente, desenvolvido pela empresa _Epic Games_, foi criado usando a _engine_ Unreal. Enquanto "Resident Evil Village", um jogo que eu tenho jogado atualmente, foi desenvolvido pela empresa _Capcom_, usando sua própria _engine_ "RE ENGINE".

No contexto _indie_, _engines_ como Unity, Unreal, Godot, Game Maker, entre várias outras são a forma mais popular para desenvolvimento dos jogos.

## Escolhendo sua Engine


## Conclusão
Ao final desse capítulo, você deveria ter um entendimento básico sobre as diferentes opções para desenvolvimento de jogos. Idealmente, também já teria alguma ideia de qual _engine_ ou _framework_ usará para seu projeto. Além disso, esperamos que tenha decidido como organizar seus arquivos, ou já estava considerando qual formato funcionará melhor para sua organização.

No próximo capítulo vamos entrar no mérito do "Ciclo de Desenvolvimento", onde vou explicar como funcionará o desenvolvimento em si, abordando temas como planejamento, prazos, priorização de tarefas, entre vários outros aspectos importantes.
