<br>
<br>

# Introdução:

O texto a seguir é um manual para desenvolvimento de jogos *indie*, ou seja, jogos criados em um contexto amador, de maneira independente. O foco desse material é principalmente prático, com um pouco de teoria quando se mostrar necessário. Durante o decorrer do manual, dois projetos de jogos serão criados, e o código fonte deles pode ser visualizado e baixado na página do github a seguir: (pag a criar) !!TODO

É um erro comum de pessoas que aspiram tornarem-se criadores de jogos se ocuparem com livros, vídeos de análise e *design*, gravações de GDCs (Game Development Conferences), comentários e entrevistas de desenvolvedores, entre várias outras categorias de vídeos educativos sobre jogos. Eu mesmo passo boa parte do meu tempo livre estudando estes diversos recursos online.

![GDC - Workshop de Level Design: Projetando Celeste](https://i.imgur.com/IT5UV3h.jpg "GDC - Workshop de Level Design: Projetando Celeste")
<sup><sub> Imagem de GDC: "Workshop de Level Design: Projetando Celeste", de Matt Thorson, desenvolvedor líder do jogo Celeste, apresentado em 2017 e publicado em 2018. Link: https://www.youtube.com/watch?v=4RlpMhBKNr0 </sup></sub>

Enquanto todos estes são ótimas fontes de aprendizado, uma coisa deve ficar clara a você: Você não vai realmente aprender a fazer um jogo até o momento em que colocar essa teoria na prática. Dessa forma, a melhor maneira de começar a sua jornada de criação de jogos é "aprender fazendo", com uma boa base de instruções para que você e sua equipe não se percam no caminho.

Existem vários outros manuais, artigos, guias e livros que propõem esta mesma ideia. Porém, os mesmos costumam ser focados em um gênero de jogos específico, ou atrelados completamente a um ambiente de desenvolvimento, ou simples/vagos demais. Enquanto os livros e artigos acadêmicos sobre o assunto costumam ter uma boa base em teorias de _design_, engenharia de _software_ e padrões de desenvolvimento, a maioria dos outros materiais costumam faltar nesse aspecto. Por outro lado, muitos dos livros e artigos exigem entendimento teórico, e um grande investimento de tempo para entender seu conteúdo, enquanto os demais formatos exigem um investimento menor, e costumam ser mais práticos, tornando sua aplicação mais fácil.

Minha intenção com esse manual é oferecer um conteúdo diferente, tentando ao máximo casar a praticidade e simplicidade dos guias informais com a base teórica encontrada nos livros e artigos. Minha esperança é que ao final da leitura você seja capaz de planejar e executar o projeto da criação de um jogo em qualquer gênero ou ambiente. 

O manual é direcionado a qualquer pessoa buscando criar jogos em um contexto amador. Sejam jogos para celular, consoles ou computador, sejam jogos 3D ou 2D. Vou assumir que você entende certos termos de informática, e não me preocuparei muito em explicar minúcias, salvo quando necessário para realização de uma tarefa prática.

Não pense por um momento que o processo de criação de um jogo será simples, rápido ou fácil. Porém, meu objetivo é guiá-lo de maneira que ele seja mais eficiente o possível, evitando ao máximo atrasos, retrabalhos e outros problemas. 

Talvez você já tenha tentado criar um jogo e falhado algumas vezes, ou talvez seja a sua primeira tentativa. A experiência ajuda, mas o fator mais importante é que tenha o empenho e ânimo para levar seu projeto do zero ao sucesso. Eu mesmo passei pela experiência de falhar em vários projetos até aperfeiçoar uma maneira ideal para a construção de jogos que funcionava para mim, com o apoio da Engenharia de Software, de muito estudo, da opinião de outros desenvolvedores, e de muito empenho.

Obviamente, isso não quer dizer que o meu método vai funcionar para qualquer um. E eu não tenho a arrogância de dizer que você deve seguir os meus passos para alcançar o sucesso.  
Enquanto eu ofereço orientações específicas, em vários momentos deste manual você vai encontrar instruções e prazos flexíveis, ou várias opções diferentes para executar uma única tarefa. Descrevo estas várias opções na esperança de que você possa adaptar ao máximo o projeto ao seu ritmo de trabalho, e da sua equipe.

Lembre-se, os responsáveis pelo seu projeto são você e seu time. Enquanto descrevo aqui uma sequência de orientações para que seu projeto siga em frente, todo o esforço e tempo gasto será seu/de vocês. Da mesma forma, o mérito do produto final será completamente seu e do seu time. Te desejo sucesso nessa jornada!

![Painel, Falling Dream Shards](https://img.itch.zone/aW1nLzEwNzg1OTQzLmdpZg==/original/s411yZ.gif "Falling Dream Shards - Daniel Waack")
<sup><sub> Pixel art criada por mim para a _intro_ de um jogo. </sup></sub>

<br>
<br>

## Conteúdo do Manual:
Um detalhe importante sobre o conteúdo deste manual é que ele está muito preocupado com *o que* você vai fazer, e não tanto com *como* você vai fazê-lo.  

Como assim?  
Se eu sentasse e decidisse criar um tutorial para a construção de todos os possíveis algorítmos e funções de jogos, em todas as possíveis plataformas de desenvolvimento, eu ficaria aqui por duas vidas e não terminaria.  
E eu não preciso fazer isso, pois já existem diversos recursos de todos os tipos que exploram estes méritos, e procurá-los será invevitvalmente parte do seu trabalho, ou de alguém na equipe. Como procurá-los, filtrá-los, entendê-los e usá-los será mais relevante para este manual. Até porque se você sabe exatamente o que procurar, você já avançou considervalemnte.  
A pergunta fundamental que exemplifica o foco desse manual é a seguinte:

<br>

**O que devo fazer para criar um jogo?**

<br>

Em outras palavras: "Qual é a sequência de ações que devo tomar para a criação de um jogo?" Ou ainda, "Por onde eu começo?" É com esse tipo de pergunta muito mais fundamental que as pessoas costumam encontrar problemas.  

Enquanto eu ocasionalmente vou entrar no mérito de alguns tipos de desenvolvimento, e vou exemplificar com um projeto de jogo de plataforma 2D e um *topdown shooter* 3D, é importante entender que o meu objetivo não é explicar especificamente como criar um *tipo* de jogo, mas sim descrever um processo de desenvolvimento e organização que servirá para qualquer jogo.

E se você pretende fazer um jogo em um desses dois estilos, melhor ainda, você pode usar o meu processo como exemplo. Para o jogo de plataforma, usarei a *engine* Unity, e para o 3D, usarei a *engine* Godot. A escolha dos ambientes deste projeto não foi aleatória. Unity por ser uma das *engines* grátis (com algumas restrições) mais populares, tendo uma quantidade enorme de material de apoio focado nela. E Godot por ser a minha *engine* de escolha para desenvolvimento, e por sua estrutura de árvores que eu considero mais amigável para novos usuários. De qualquer forma, sinta-se livre para fazer o seu projeto em seu ambiente de escolha. Mais sobre isso nos capítulos 1 e 2.

<br>
<br>

## Detalhes Importantes:
Antes de entrar no manual em si, alguns detalhes podem te interessar.  
O *approach* sugerido nesse manual vai se ramificar dependendo de alguns fatores. Toda vez que isso for relevante, apontarei o fato. Entretanto, é importante que você os tenha em mente desde já.  
Os fatores são:

<br>
<br>

1. Se você trabalha em equipe ou sozinho:

Isso é muito importante para o seu ritmo e organização de trabalho. Um grupo trabalha melhor do que um indivíduo. Porém, sozinho você terá liberdade criativa maior do que em um grupo.  
Outras vantagens do desenvolvimento em grupo são poder trabalhar em diferentes frentes ao mesmo tempo, apoio entre os membros, maior facilidade em testes e discussões de melhorias, entre vários outros. É claro, nem sempre o trabalho em grupo é uma opção. Eu mesmo trabalhei na maioria de meus projetos sozinho, por vários motivos, com o apoio ocasional de terceiros, principalmente para fins de testes. Mas isso causou diversas dificuldades no meu caminho, e eu tive que aprender a fazer o trabalho de várias pessoas.

Entenda que, no contexto *indie*, um grupo de 3-5 pessoas provavelmente oferece o melhor equilíbrio entre trabalho em equipe, poder de decisão e facilidade de gerenciamento da equipe.  
Esse manual vai, no geral, assumir que você esteja sozinho ou em um grupo pequeno. Quando relevante, apontaremos diferenças entre o trabalho *solo* e e o trabalho em equipe. Porém, as ideias e orientações descritas aqui podem ser aplicadas independente da quantidade de integrantes na equipe.

<br>
<br>

2. Quais competências estão disponíveis na equipe:

A criação de um jogo envolve várias competências. Neste manual, eu as dividi em alguns tópicos: *Design*, Programação e Lógica, Arte (conceitual, de fundo, 2D, 3D, de interface, etc.), Modelagem, Animação, Música (*BGM* e *sound design*), *Playtesting*.  
Para certos projetos, algumas dessas competências são irrelevantes. Ainda para outros projetos, algumas podem ser mais importantes que as outras. 

Por exemplo, modelagem não é necessária em jogos 2D. 

[comment]: <(![Exemplo, Jogo 2D](files://C:/Users/55619/Documents/Dev/TCC/Hollow-Knight-Gameplay.jpg "Hollow Knight - Exemplo 2D"))>

![Exemplo, Jogo 2D](https://www.ubuntufree.com/wp-content/uploads/2017/05/Hollow-Knight-Gameplay.jpg "Hollow Knight - Exemplo 2D")

Feito na *engine* híbrida Unity, **Hollow Knight** é um jogo 2D. Dessa forma, a arte é toda feita em planos 2D, e modelagem não foi necessária.

<br>

Outro exemplo, para um jogo musical ou de ritmo, o *sound design* e música geralmente serão mais importantes do que a arte.  

![Exemplo, Jogo de Ritmo](https://i.imgur.com/JOhEaHf.jpg "Deemo - Exemplo Ritmo")

Deemo tem uma arte bonita, mas ela não é particularmente detalhada ou feita para ser um ponto focal do jogo. Afinal, o aspecto de maior importância neste jogo é a música e som.

<br>

Enquanto é preferível que o seu time contenha integrantes que cubram todas as competências necessárias para a criação do jogo, a falta delas não significa que o seu projeto não pode ser criado. Existem alternativas para todos os casos, como ambientes onde programação não é necessária, recursos audiovisuais grátis, ou até a possibilidade de contratar artistas, programadores e músicos para auxiliar no processo.  
É claro, isso tudo depende da habilidade e orçamento do seu time. Porém, o objetivo deste manual é sempre apresentar diversas opções, buscando sempre opções sem custo, ou o melhor equilíbrio entre preço baixo e qualidade do produto final.

<br>
<br>

3. Quanto tempo você pode dedicar ao projeto.

A quantidade de tempo em que você pode trabalhar no projeto vai refletir no produto final, ou no tempo que você vai demorar até alcançar o que idealizou para o seu projeto. 
Não é incomum que jogos grandes levem anos para serem construídos. O mesmo acontece para certos jogos pequenos, mesmo com equipes maiores. Isso depende de vários fatores, como o escopo e a organização do seu projeto.  
Durante o manual, haverá uma sequência de períodos onde a equipe deverá desenvolver determinados aspectos do jogo (*sprints*). É sempre possível aumentar estes períodos, a custo de demorar mais tempo para desenvolver o seu projeto. Caso o tempo livre de sua equipe seja limitado, existe flexibilidade para determinar os períodos de ação. Isso fica a critério de você(s).

<br>

Com todas estas considerações em mente, sem mais delongas, vamos ao conteúdo real do manual:

[Capítulo 1: Design](capitulo1.md) 
