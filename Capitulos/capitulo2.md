
# Capítulo 2: Preparação
"Um homem escolhe, um escravo obedece." - Andrew Ryan, "Bioshock" (2007)

![Capítulo 2 capa](../Arquivos/Imagens/capa_02.jpg 'A man chooses, a slave obeys.')

## Introdução

Após documentar o seu projeto, o próximo passo seria começá-lo. Mas para fazer isso, você deve decidir _como_. 

Existem inúmeros ambientes, linguagens, formatos e plataformas por meio dos quais você pode desenvolver um jogo.

E você deve escolher entre eles.

Eu pretendo te ajudar com essa escolha. Mas, ao final do dia, isso será decidido por você (ou os desenvolvedores em sua equipe). E essa escolha vai mudar completamente como o desenvolvimento de seu jogo vai funcionar.

![Engines](../Arquivos/Imagens/02_04.jpg 'Engines')

## Frameworks e Engines

Sua escolha entre _Frameworks_ e _Engines_ vai depender de vários fatores. Para a maioria dos desenvolvedores _indie_, uma _engine_ é a escolha ideal, principalmente para quem deseja criar um jogo sem programar. Porém, é interessante entender um pouco sobre o tópico, porque isso vai influenciar sua escolha.

Todo jogo é basicamente um conjunto de sistemas diferentes, sendo executados ao mesmo tempo e interagindo entre si. 

Por exemplo, quando eu clico no executável de _Minecraft_, aparece uma tela de menu principal (visual); ao mesmo tempo, uma música agradável começa a tocar (áudio); e se eu mexer o meu mouse e clicar em um botão, a tela vai reagir e fazer alguma coisa (_input_); se eu clicar em _multiplayer_, o jogo vai se conectar à internet e tentar se comunicar com um servidor (_networking_); se eu clicar em novo mundo, ele vai criar um (geração de mapas); e ao final, meu personagem será livre para interagir com esse mundo, onde várias coisas funcionam como o mundo real (simulação de mundo e física).

![Menu Principal do Minecraft](../Arquivos/Imagens/02_03.png 'Minecraft title screen.')

Tudo isso acontece simultâneamente e de maneira harmoniosa, mas no plano de fundo, vários processos e cálculos diferentes são executados "ao mesmo tempo" para garantir que tudo aconteça na ordem e maneira correta.

No contexto de desenvolvimento, cada uma dessas tarefas (_networking_, input, _display_ visual, gerenciamento de música, etc.) costuma ser executada pelo que chamamos de uma "biblioteca" (_library_). Uma biblioteca para redes geralmente vai conter diversas funções necessárias para conectar diferentes computadores em um único jogo, enquanto uma biblioteca gráfica vai conter diferentes funções para mostrar coisas em sua tela. Estas bibliotecas geralmente vêm como código no formato de arquivos DLL, por exemplo em _Javascript_ ou _C++_. Alguns exemplos: FMOD (áudio), RakNet (_networking_), Box2D (física 2D), Assimp (importação de modelos 3D), entre várias outras.

![Página do FMOD](../Arquivos/Imagens/02_05.png 'FMOD Homepage.')

Como cada biblioteca só se preocupa com uma tarefa, você não pode criar um jogo usando apenas uma. É aí que entram os _frameworks_. Um _framework_ já fez o trabalho de juntar diversas bibliotecas em uma coleção para uso unificado. Utilizando um _framework_, você não precisa se preocupar com a maioria dessas tarefas simples, e apenas resta usar essas diversas funções como os componentes do que formará seu jogo. Alguns exemplos de _frameworks_ para jogos incluem: SFML, Phaser, OGRE, LibGDX e MonoGame.

![Página do Phaser](../Arquivos/Imagens/02_06.png 'Phaser Homepage.')

Partindo de _frameworks_, quando subimos um pouco mais o nível de sofisticação e facilidade de uso, chegamos às _Game Engines_ (motores de jogos). Estas oferecem o mesmo conjunto de bibliotecas para gráficos, áudio, memória, _networking_, física, etc., além de diversas outras ferramentas úteis no desenvolvimento. Diferente dos _frameworks_, _Engines_ costumam ser ambientes completos, com uma interface gráfica amigável acoplada de um editor de mapas/fases onde se pode visualizar e modificar o jogo em tempo real.

![Interface do Unity](../Arquivos/Imagens/02_07.jpg 'Unity Interface.')

_Engines_ facilitam muito o processo de desenvolvimento. Algumas oferecem a possibilidade de criar jogos sem programação alguma, mas programação ainda é uma necessidade na grande maioria delas. No geral, a maior diferença entre _engines_ e _frameworks_ está no editor de mapas, e no visualizador de cenas. Porém, existem vários casos onde essa diferença não é tão acentuada.

Como eu comentei antes, a melhor escolha para um desenvolvedor _indie_ costuma ser uma _engine_. Por questões de facilidade de uso e praticidade. Mesmo que não seja minha recomendação, sinta-se livre para pegar um _framework_ se este for o seu desejo. O manual vai assumir que você está usando uma _engine_, mas as tarefas para desenvolvimento serão as mesmas.

Na verdade, nem sempre uma _engine_ será a escolha ideal para se o projeto. O fato de que a _engine_ já deixa vários componentes prontos para uso pode significar que há pouca flexibilidade para fazer algo além do que foi projetado por seu criador. Algumas _engines_ como Godot vão permitir que edite seu código fonte, e várias delas permitem a criação de _plugins_ para complementar onde faltam, mas nenhuma dessas soluções é simples de programar. Lembre-se sempre: **Você sacrifica flexibilidade em busca de maior praticidade.**

Na grande maioria dos casos, uma _engine_ vai oferecer exatamente o que você precisa para a criação de seu jogo. Talvez não _qualquer_ engine, e isso é algo que discutimos mais a frente neste capítulo. Mas é muito provável que exista uma ótima _engine_ para a criação do seu projeto. 

Caso você se depare com uma necessidade que sua _engine_ não consegue suprir, existem as seguintes possibilidades: 
- tentar forçar que a _engine_ faça o que deseja (através de um plugin, ou uma gambiarra, talvez);
- usar uma _engine_ diferente;
- usar um _framework_;
- criar sua prórpia "_engine_" a partir de um _framework_;
- criar sua própria "_engine_" do zero.

A última possibilidade, criar uma _engine_ a partir do nada, é algo que eu desaprovo completamente para o contexto _indie_. Essencialmente, você estaria perdendo um tempo enorme reinventando a roda e provavelmente chegaria a resultados inferiores do que se tivesse apenas utilizado uma _engine_ pronta. É claro, é um ótimo jeito de aprender programação para jogos a fundo. Caso seu objetivo seja a criação de uma _engine_ do zero, então vá em frente, mas provavelmente levará um bom tempo até que o manual que está lendo agora seja de utilidade para você.

Na indústria como um todo, você vai perceber que muitos desenvolvedores AAA vão fazer seus jogos em uma _engine_ já estabelecida, ou criar uma nova. Por exemplo, "Fortnite", um jogo bem popular atualmente, desenvolvido pela empresa _Epic Games_, foi criado usando a _engine_ Unreal. Enquanto "Resident Evil Village", um jogo que eu tenho jogado atualmente, foi desenvolvido pela empresa _Capcom_, usando sua própria _engine_ "RE ENGINE".

![Fornite](../Arquivos/Imagens/02_08.jpg 'Fortnite.')

![RE Village](../Arquivos/Imagens/02_09.jpg 'RE Village.')

No contexto _indie_, _engines_ como Unity, Unreal, Godot, Game Maker, entre várias outras são a forma mais popular para desenvolvimento dos jogos.

## Escolhendo sua Engine

A _engine_ ideal para o seu projeto pode não ser a _engine_ ideal para o meu projeto. E cabe ao desenvolvedor escolher o que encaixa melhor para seu jogo e para seu formato de trabalho. Por exemplo, enquanto eu acho Unreal uma ótima engine para desenvolvimento 3D, eu não a recomendaria para desenvolvimento 2D.

Entre _engines_, você vai encontrar diferenças diversas:
- linguagens de programação usadas;
- tipo de ambiente (focado em jogos 2D, 3D ou híbridos);
- disponibilidade de ferramentas e _plugins_ para auxílio;
- lojas com recursos e _assets_ para uso e reuso;
- tempo de _building_ (criação do executável do jogo);
- plataformas de exportação (se pode facilmente exportar para PC, consoles, web ou mobile);
- especialidade (se geral, se focado em algum gênero de jogo);
- entre outros...

Não só isso, mas uma simples pesquisa vai revelar que existem dúzias e dúzias de opções diferentes. E com isso em mente, não é difícil ficar indeciso quanto a qual _engine_ usar. Hoje, após muita experiência, eu tenho uma boa ideia de quais _engines_ e ferramentas usarei para qualquer projeto que começar, mas já passei muito tempo testando várias opções diferentes até chegar nesse ponto.

Enquanto eu não posso decidir por você, e acho bom que faça sua própria pesquisa sobre o assunto, vou te dar algumas dicas e opções para auxiliar sua decisão. (Lembrando que este manual está sendo escrito em 2023, e novas tecnologias e opções melhores podem ter aparecido se estiver lendo isso em um futuro não tão distante). Se existe um programador em sua equipe, dele(a) deve ser a opinião principal neste tema.

### Fator 1: Programar ou Não Programar (Eis a questão?)

A programação é um detalhe que requer atenção, pois, na maioria dos casos, vai ser o aspecto mais importante do seu projeto. Cada _engine_ tem a sua prórpria abordagem para como as coisas devem ser programadas. Geralmente, isso é demonstrado em formas de linguagens diferentes. 

Para um programador experiente que entende de lógica, pular de uma linguagem para outra exige um pouco de estudo, mas não é uma mudança impossível. Seu programador pode ser familiar com uma linguagem como C++, e talvez seja interessante escolher uma _engine_ como Unity ou Unreal, onde é possível utilizá-la. Entretanto, caso escolham uma _engine_ com uma outra linguagem, é possível que o programador consiga se adaptar à nova linguagem (isso pode levar certo tempo, dependendo do conhecimento dele.)

Entretanto, caso você não tenha um programador em sua equipe, a questão se torna um pouco mais complexa. Neste caso, você teria algumas opções:
- Utilizar uma _engine_ que não exige programação;
- Escolher alguém da equipe para aprender programação;
- Recrutar um programador para a equipe.

Pessoalmente, acredito que ter uma pessoa familiar com programação em sua equipe é importante. Isso é porque programação permite uma flexibilidade e usabilidade maior do que as alternativas. É claro, isso também exige mais conhecimento e treino. Aprender programação não é algo trivial, mas existe uma infinidade de cursos e material _online_ grátis cujo objetivo é te ensinar exatamente isso. Caso esteja disposto, é uma boa opção. Caso decida recrutar um programador, seja um novo membro ou uma pessoa contratada, lembre-se dos pros e cons de trabalhar com mais uma pessoa na equipe.

Entretanto, a escolha continua sendo sua, algumas opções de _engines_ que permitem criação de jogos sem uso de programação são: **Gdevelop**, **Game Maker Studio 2**, **Unity Visual**, **Scratch**, **Soba**.

![Interface do GDevelop](../Arquivos/Imagens/02_10.jpg 'GDevelop Interface.')

### Fator 2: Plataforma Alvo

Um detalhe muito importante é para onde você deseja exportar o seu jogo. Certas _engines_ não podem exportar para _mobile_, outras não exportam muito bem para _Mac_ e _Linux_. Na hora de escolher sua _engine_, você deve procurar sobre a possibilidade de exportar para sua plataforma desejada.

![Consoles de Jogos](../Arquivos/Imagens/02_11.jpg 'Gaming Consoles')

### Fator 3: Estilo do Jogo

Certas _engines_ vão servir apenas para jogos 2D ou 3D, enquanto várias delas são híbridas.

Dependendo do gênero do seu jogo, você pode querer usar uma _engine_ específica voltada para ele. A maioria das _engines_ são feitas para usos gerais, e vão conseguir criar qualquer tipo de jogo, mas uma pode ser melhor do que a outra em determinada tarefa, e isso você deve considerar. 

Em alguns casos, temos _engines_ feitas especificamente para um estilo de jogo. Por exemplo, a série de _engines_ _RPG Maker_ vêm com todo o formato necessário para criação de um jogo no estilo de JRPGs antigos como os _Final Fantasy I-V_, _Dragon Quest_, etc... A _engine_ _Renpy_ é ótima para criar jogos no estilo _Visual Novel_, entre outros exemplos.

É sempre possível criar o mesmo estilo de jogo em outras _engines_ gerais, mas se o seu objetivo é criar algo específico, talvez seja mais fácil usar uma _engine_ especializada.

![Interface do RPG Maker VX](../Arquivos/Imagens/02_12.png 'RPG MAKER VX interface')

### Fator 4: Recursos e Material

Outro fator muito importante é a disponibilidade de recursos e materiais para a _engine_ relevante. Geralmente, quanto mais material educativo está disponível para sua _engine_, mais fácil será o processo de desenvolvimento. 

Como assim?

Muitas vezes o desenvolvedor de seu jogo vai ficar sem saber como implementar determinada ideia. Nesse caso, uma simples pesquisa no Google pode ser a solução para esse problema. Isto é, se a _engine_ for popular e tiver fóruns de dúvidas, tutoriais e afins. Não é esperado que você encontre isso para _engines_ novas e obscuras, o que vai implicar em mais tempo lendo documentações ou fazendo posts em fóruns.

Para _engines_ populares como _Unity_, por exemplo, é muito mais fácil encontrar uma solução para o seu problema imediatamente, e adaptá-la para seu projeto se torna muito mais rápido e prático.

![Godot Tutorials](../Arquivos/Imagens/02_13.png 'Godot Tutorials')

### Sugestões:

Mesmo com todos esses fatores em mente, às vezes continua sendo difícil encontrar a _engine_ perfeita. Então eu deixarei minhas próprias recomendações aqui:

Se não deseja programar, as opções acima são a solução: **Gdevelop**, **Game Maker Studio 2**, **Unity Visual**, **Scratch**, **Soba**.

Se o seu jogo é 3D, Unity ou Unreal são as opções mais completas. (Um adendo, acredito que criar um complexo jogo 3D em um contexto _indie_ seja uma má ideia).

Se o seu jogo é um RPG 2D ou uma visual novel, talvez te interessem _engines_ como RPG Maker, ou Renpy.

Para jogos 2D como jogos de plataforma, _metroidvanias_ e outros jogos do tipo, recomendo Unity ou Godot.

Para o caso dos projetos que montarei durante a criação do manual, tive certa dificuldade em decidir entre Godot e Unity. Ao final, decidi usar Godot para as duas, pois é a _engine_ com a qual eu estou mais familiar, e acho seu formato de árvores e nós mais simples de entender que o formato de cenas no Unity. Godot tem bastante material para desenvolvimento 2D, enquanto para o 3D ainda não há tanto. Entretanto, a quantidade de material não é tão grande quanto para Unity.

Para o seu caso, sinta-se livre para escolher a que achar mais adequada. De qualquer forma, Unity será minha recomendação geral para a maioria dos projetos, com Godot vindo perto em segundo. Após escolher sua _engine_, não esqueça de preenchê-la no seu GDD! Sugiro que salve como uma nova versão, e não por cima do documento atual. Será interessante comparar as diferentes versões no final de seu projeto.

[Sleepy Runner - GDD Cap 2](https://github.com/D-Waack/sleepy-runner-godot4/blob/main/Docs/Sleepy_GDD_cap2.pdf)

[Vortex Tautology - GDD Cap 2](https://github.com/D-Waack/vortex-tautology-demo/blob/main/Docs/VortexTautology_GDD_cap2.pdf)

## Organização de Arquivos

Com uma _engine_ em mente, outro detalhe importante é como organizará seus arquivos. Isso não é um detalhe trivial. É de **extrema importância**. 

Muitas coisas em seu projeto serão arquivos. Por exemplo, imagens de fundo, _sprites_ de personagens, modelos 3D e suas texturas, músicas e sons diversos, mapas, _scripts_. Todos estes arquivos estarão dentro da pasta de seu projeto. E eles são os principais responsáveis pelo "peso" dos jogos que você baixa.

Algumas _engines_ vão tirar essa opção das suas mãos, seguindo sua própria estrutura de arquivos, e cabe a você colocá-los no lugar certo. Entretanto, na maioria dos casos a estrutura de arquivos fica completamente a critério do desenvolvedor.

Para a manutenção de seu projeto é importante ter em mente como organizá-los. Pois quanto mais complexo ele ficar, mais difícil vai ser encontrar seus arquivos. Saber exatamente onde encontrar cada arquivo se torna indispensável à medida que os mesmos vão se amontoando na pasta de seu jogo.

Não existe um jeito "certo" de organizar seus arquivos. Mas existem jeitos melhores e piores. 

Pessoalmente, eu costumava separá-los no seguinte formato, tentando seguir certa noção de orientação a objetos: **Entities**, **Managing**, **Persistent**, **Resources**, **UI** e **World**

![Arquivos 1](../Arquivos/Imagens/02_01.png 'Arquivos 1')

Esse formato é compreensível e útil, mas deixa muito a desejar. Os "recursos" eram todo o tipo de arquivo que não era um _script_. Ou seja, texturas, _sprites_, e música todos ficavam em uma mesma pasta, enquanto todo o resto ficava espalhado. É fácil imaginar a frustração de ter que passar por uma dúzia de pastas completamente separadas ao meu objeto para encontrar uma textura específcia toda vez que quero mudar seu visual.

Percebendo que isso não era tão prático, mudei para um novo jeito de organizar as pastas:

![Arquivos 2](../Arquivos/Imagens/02_02.png 'Arquivos 2')

Objetos, seus _scripts_, modelos, texturas e sons ficam todos juntos na mesma pasta. Caso um artefato seja usado em mais de um objeto, o mesmo fica em uma pasta "common". Dessa forma, evito o problema que ocorria antes. É claro, dependendo do projeto, essa estrutura pode não ser ideal.

Minha sugestão fica para o formato que uso atualmente, mas sinta-se livre para usar sua própria estrutura. Apenas lembre-se de mantê-la consistente e organizada sempre, para evitar futuros transtornos. Anote-o em algum lugar, mesmo no GDD se quiser.

## Conclusão
Ao final desse capítulo, você deveria ter um entendimento básico sobre as diferentes opções para desenvolvimento de jogos. Idealmente, também já teria alguma ideia de qual _engine_ ou _framework_ usará para seu projeto. Além disso, esperamos que tenha decidido como organizar seus arquivos, ou já esteja considerando qual estrutura funcionará melhor para sua organização.

No [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo3.md) vamos entrar no mérito do "Ciclo de Desenvolvimento", onde vou explicar como funcionará o desenvolvimento em si, abordando temas como planejamento, prazos, priorização de tarefas, entre vários outros aspectos importantes.
