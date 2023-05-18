
# Capítulo 4: O Primeiro Ciclo - Rumo ao Protótipo 0
"Ciência não é sobre 'por que'. É sobre 'por que não'." - Cave Johnson, _Portal 2_ (2011)

<p align="center">
  <img src="../Arquivos/Imagens/capa_04.png" 'Science isn\'t about \'why\'. It's about \'why not\'.' />
</p>

## Introdução

O [capítulo anterior](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo3.md) ofereceu uma abordagem bem teórica sobre como funcionaria o ciclo de desenvolvimento, mas você provavelmente ainda tem várias dúvidas. De certa forma, o desenvolvimento é como um jogo de tabuleiro. Você pode ler as regras, mas só aprenderá realmente quando colocá-las na prática.

E, nesse sentido, a prática será os primeiros ciclos de desenvolvimento. Existem várias formas de separar as etapas da produção dos jogos, mas aqui a dividiremos da seguinte forma: **Protótipo 0** -> **Alfa** -> **Beta** -> **Produto final**

Se você joga, os termos _alfa_ e _beta_ não devem ser desconhecidos a você. Eles se referem a estados diferentes do desenvolvimento de um _software_. No contexto de jogos, isso é um pouco vago. Alguns vão definir a diferença entre _alfa_ e _beta_ como "um está bem incompleto e o outro está quase completo". Outros ainda vão dizer que versões beta são aquelas apresentáveis para a audiência, e que podem ser publicadas para teste.

Eu ainda incluo mais uma etapa, o Protótipo 0. Para o contexto deste manual, vou definir estas etapas da seguinte maneira:

- Protótipo 0: Primeira versão do jogo para testar a ideia, quase nada além da ideia central do jogo é implementada
- Alfa: Faltam diversos sistemas e funções a serem implementadas
- Beta: Sistemas e funções principais já foram todos implementados, resta poli-los e consertar _bugs_

Seguiremos esta ordem durante o manual. Logo, o primeiro passo é o Protótipo 0.

## O Protótipo 0

A ideia por trás do Protótipo 0 é destilar o conceito de seu jogo a um ponto que você tenha **apenas** sua essência, e implementar isto.

O que isso quer dizer na prática?

Sprites, modelos, música, mapas são todos desnecessários. Nada disso pertence ao protótipo 0. Na verdade, seu primeiro protótipo deve parecer muito mais como um jogo de _Atari_ do que um jogo moderno. Se fosse _Super Mario_, você poderia ter um quadrado correndo e pulando. Se fosse _Zelda_, talvez você teria um quadrado andando na tela e espetando inimigos (também quadrados) com um similar retângulo.

Esses exemplos são exageros, você não precisa se apegar ao minimalismo de tal maneira. Se você tem um artista no time, não precisa deixá-lo ocioso até o fim da criação deste protótipo, e se você já tem algo feito, não precisa evitar seu uso de propósito (apesar de ser uma opção). Se desejar ter algo visual em tela, pode interessar usar recursos grátis tirados, por exemplo, do site [Open Game Art](https://opengameart.org/). A intenção é apenas que você crie o protótipo para sentir sua ideia com as próprias mãos.

Dessa forma, se você trabalha sozinho, não se preocupe em criar nenhum artefato audiovisual. E se você trabalha em equipe, não se preocupe em incluir nenhum artefato audiovisual no projeto, por enquanto. Durante essa etapa, o trabalho principal vai ser entre designer e programador.

A intenção do protótipo 0 não é criar uma representação do seu jogo, é criar a base inicial dele. Como uma casa, você constrói uma fundação antes de começar a construir os cômodos. Se a fundação não estiver firme, a casa vai desmoronar.

Dessa forma, o seu primeiro passo é definir as mecânicas principais do seu jogo e implementá-las de maneira simples.

## Protótipo 0 - Exemplo 1
Na maioria dos casos, começamos qualquer projeto criando uma pasta para ele. Na minha _engine_ de escolha, isso pode ser feito no próprio editor. Aqui, vou descrever os passos para minha _engine_ de escolha, Godot. Mas independente do ambiente que escolher, você terá de seguir passos similares.

![Criando Projeto](../Arquivos/Imagens/04_01.png 'Criando Projeto')

Ao criar o projeto, somos apresentados ao menu principal da _engine_. Neste caso, já vemos o visualizador/editor de mapas imediatamente. Meu próximo passo sempre costuma ser criar as pastas de arquivos na estrutura que decidi anteriormente.

![Primeira Visão da Engine](../Arquivos/Imagens/04_02.png 'Primeira Visão da Engine')

![Pastas de Arquivos](../Arquivos/Imagens/04_03.png 'Pastas de Arquivos')

Em seguida, eu passo por algumas configurações que serão relevantes para a construção do jogo. No momento, estou preocupado apenas com o **nome do projeto** e o **tamanho da tela**. O tamanho dela é importante decidir cedo no desenvolvimento, pois isso vai afetar o seu jogo. Principalmente para questões de _câmera_ e quanto cabe em sua tela. Nesse caso, como trata-se de um jogo para celulares, optei por um tamanho padrão de 1080x720, mas talvez vá mudá-lo mais a frente. Essa resolução não é estática, e será mudada para se adequar à tela do celular do jogador, mas para isso, devo incluir também a opção de _stretch_.

![Configurações](../Arquivos/Imagens/04_04.png 'Configurações')

![Configurações2](../Arquivos/Imagens/04_05.png 'Configurações 2')

Após fazer essas mudanças, pressiono CONTROL + S para salvar meu projeto, e passo a trabalhar no protótipo em si.

Na _engine_ Godot, todos os elementos de um jogo são divididos em _cenas_. Cenas são um conceito comum para várias _engines_, e geralmente essas cenas são o elemento executável primário de um jogo. Ou seja, uma cena seria equivalente a um mapa ou fase. Ao rodar o seu jogo, a _engine_ partirá de uma cena específica, e poderá mudar para outras cenas durante a execução.

Essas cenas executáveis são então compostas de vários elementos. Por exemplo, de um mapa com colisões, um personagem controlável, e vários obstáculos. Já é possível enxergar uma fase com estes elementos.

TODO -> montar diagrama exemplo

No Godot, toda cena é uma estrutura de árvore. Dessa forma, 

## Protótipo 0 - Exemplo 2

## Quando parar


## Conclusão

O trabalho de criar esse protótipo inicial não é trivial. E esse é um passo muito importante. Se o seu time é inexperiente, ele vai naturalmente encontrar problemas e dúvidas durante o processo. 

No [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo5.md) discuto o que fazer quando você fica sem saber o que fazer durante a execução de etapas de programação.
