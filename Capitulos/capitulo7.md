
# Capítulo 7: Playtesting e Feedback
"Era estranho que Stanley ainda estivesse sentado no armário das vassouras. Ele nem sequer estava fazendo nada. Pelo menos se houvesse alguma coisa com que interagir ele estaria justificado de alguma forma." - Narrador, "_The Stanley Parable_" (2013)

![Capítulo 7 capa](../Arquivos/Imagens/capa_07.png 'It was baffling that Stanley was still just sitting in the broom closet. He wasn\'t even doing anything, at least if there was something to interact with he\'d be justified in some way.')

## Introdução
Se você já está trabalhando no seu jogo há certo tempo, você com certeza já encontrou algum _bug_ ou erro. Você entende todos os aspectos do seu jogo melhor que ninguém, e você sabe exatamente o que está errado.

Então por que precisa testar?

Porque você é cego. Ou melhor dizendo, porque você não tem uma visão completa do seu jogo. _Playtesters_ também não têm. Na verdade, eles entendem seu jogo menos que você (ao menos a princípio). Mas, sendo pessoas diferentes, com experiências e inclinações diferentes, eles **vão** agir de forma diferente. E encontrar possibilidades no seu jogo que você não conseguia sequer imaginar.

Quando você olhar para uma versão e falar "está pronta" pela primeira vez, você pode ter (quase) absoluta certeza de que ela ainda não está pronta. E você pode testar por si e encontrar de fato alguns problemas, mas os _playtesters_ são o melhor caminho para encontrar _bugs_ e acontecimentos inesperados. Ou interações que você sequer sabia que podiam acontecer. E até soluções em que você não havia pensado. 

Isso pode ser por vários motivos, mas no geral é simplesmente porque seu _playtester_ pensa e joga diferente de você. Por exemplo, em um dos meus projetos, eu havia incluído uma caixa de colisão no fundo de cada fase para que se o jogador encostasse nela, ele perderia imediatamente. (Ou seja, um buraco sem fundo). Entretanto, eu havia incluído uma condição em meu jogo onde caixas de colisão **não** interagiam com o personagem quando o mesmo havia sido atingido nos últimos 1.4 segundos. O resultado era que quando o meu _playtester_ levava dano de um inimigo e caía em um buraco **antes** que esse tempo acabasse, ele não morria, e não conseguia voltar, causando com que  personagem caísse eternamente. (Obviamente, isso não deveria acontecer). Nesse caso, eu era **cego** para esse problema. Porque eu já estava tão acostumado com o jogo que eu sequer levava dano no inimigo em questão, e nunca me deparei com essa situação. Felizmente, meu _playtester_ encontrou o problema e eu pude consertá-lo. 

Esse tipo de situação é muito mais comum do que parece. E é por isso que o papel do _playtester_ é tão importante.

## Quem deve testar?
Basicamente, você, sua equipe, e terceiros. Os testes que você fará virão naturalmente durante o desenvolvimento. Por exemplo, se eu criar um botão no meu jogo, eu vou testá-lo para ver o mesmo consegue ser pressionado, e se ele faz o que deveria quando pressionado.

Isso é óbvio e natural. Você pede testar diferentes maneiras de interagir com cada objeto. Se for um botão que reage a peso, o que acontece se eu colocar um objeto em cima dele? E se (...)? Tente testar todas as possibilidades e interagir de todas as formas que conseguir pensar. Esse é o tipo de teste que as pessoas que criaram o jogo devem fazer.

Um outro caso são outros membros de sua equipe. Estes vão ser menos informados sobre o funcionamento exato do seu jogo, mas eles podem ter uma vaga ideia de como ele _deveria_ funcionar. O que provavelmente vai resultar em interações similares, mas não completamente iguais as suas. Eles podem tomar ações inesperadas, e caso não o façam, você pode estimular que tentem. 

Por fim, os outros. Novamente, é importante que tome cuidado com _quem_ e _como_ você vai disponibilizar seu jogo para testes, para que não compartilhem seu jogo sem sua permissão. De qualquer forma, é normal esperar que a experiência desses jogadores vai ser consideravelmente diferente dos outros dois casos. É interessante que os _playtesters_ estejam relativamente familiares com o gênero de jogo, mas _input_ de jogadores não familiares pode ser valioso também.

## Como funciona o teste?
Isso vai depender das condições. O ideal seria _observar_ e _gravar_ como o jogador interage e reage ao jogo.

Não é interessante dar _input_ algum ao seu jogador sobre como interagir com o jogo, para que a experiência dele seja o mais pura o possível. Afinal, quando seu jogo for lançado, o seu jogador não terá um desenvolvedor ao lado para guiá-lo pelo jogo.

É ideal que você tenha uma gravação da voz e da tela do seu _playtester_. Entretanto, isso nem sempre é possível. Enquanto menos confiável, é sempre possível esperar que seus _playtesters_ descrevam quaisquer problemas e inconsistências que encontrarem no jogo. Isso acontece muitas vezes com _betas_ abertas, onde jogadores podem contribuir com a caça por _bugs_ através de fóruns e formulários.

## Builds de teste
A maioria das _engines_ e ambientes de programação vai permitir que você crie uma versão executável do seu jogo. Você pode criar uma para distribuir entre diferentes jogadores.

Enquanto não existem regras para como criar uma _build_ para testes, alguns detalhes são importantes:

- Não inclua todo o conteúdo disponível em uma build de testes:

Em certos casos, é possível usar certas técnicas para desconstruir o executável de seu jogo, dando acesso aos arquivos disponíveis na criação da _build_ para o jogador. Enquanto isso não é um problema com uma pessoa em que você confia, pode ser ruim para _betas_ abertas ao público e casos similares.

- Crie uma interface simples:

Caso ainda não tenha criado um menu final para o seu jogo, deixe um menu rudimentar para o acesso de seus _playtesters_. Pelo menos com uma opção de "Iniciar" e uma de "Sair".

- Inclua anotações caso necessário:

Se estiver disponibilizando uma nova versão a alguém que já testou a versão antiga, inclua anotações de problemas que foram consertados e mudanças que foram feitas. Interessa ao seu _playtester_ conferir o que mudou, e se o que consertou realmente funciona da maneira correta agora.

## Interpretando e Integrando _Feedback_
Os diferentes meios como o _feedback_ pode chegar vão resultar em diferentes métodos para interpretá-los e considerá-los. Além disso, esse _feedback_ pode apontar diversas coisas como: erros e _bugs_ na execução, deficiências no _design_, dificuldade inadequada, entre vários outros detalhes. 

### Erros e _bugs_

Para o caso de **textos**, não há muito o que fazer além de lê-los e tentar entender o problema ou sugestão. Nem sempre isso será o suficiente para entender e reproduzir o problema. E certas vezes o texto estará bem claro, mas você simplesmente não conseguirá reproduzir o caso. Isso pode acontecer. Particularidades do sistema operacional, execução simultânea a outros programas, problemas físicos e outros casos diversos podem causar diferenças de execução entre duas máquinas, criando erros que não podem ser facilmente reproduzidos.

De qualquer forma, conseguir entender e reproduzir algum problema é o primeiro passo para encontrar o que está causando-o. E se você chegou até aqui neste manual, provavelmente já tem uma boa ideia de como prosseguir com isso.

Para o caso de **vídeo e áudio**, ou somente vídeo, você pode ver diretamente o que causou o erro em tempo real, e pode tentar seguir os passos diretamente, ou usar o próprio vídeo para seguir com sua análise. Da mesma forma, você pode se ver incapaz de reproduzir o problema, mas nestes casos é muito mais fácil entender a situação.

### Feedback geral

Feedback positivo/negativo em formatos de texto também pode ser considerado. Apesar de se tratar de um _feedback_ baseado em opinião, uma _review_ sensível pode ser muito útil para o processo de análise do jogo.

Para o caso de vídeos, é interessante ver onde o seu jogador encontra dificuldades, se ele entendeu o que deveria ser feito, se o _design_ da fase apresenta as informações necessárias, se será preciso fazer algum ajuste para facilitar o entendimento e _gameplay_.

Existe ainda a possibilidade de conduzir **entrevistas** com os _playtesters_. Após o processo de _playtesting_, você pode conduzir uma entrevista diretamente com o jogador, perguntando sobre a experiência, problemas encontrados, o que gostou e o que não gostou, etc. Esse tipo de entrevista pode ser muito útil, mas tome sempre cuidado para não mudar sua visão do jogo para acatar aos desejos de _cada_ _playtester_.

Lembre-se sempre, não há como agradar a todos.

Entendendo os erros, problemas e coisas que não funcioname como deveriam, você deve decidir como irá lidar com eles. Se vai incluir suas soluções no próximo ciclo de desenvolvimento, ou se vai deixar no _backlog_ para tentar resolvê-los mais tarde. Ambas são opções, mas lembre-se sempre de anotar todos os problemas que merecem sua atenção.

## Conclusão
Ao final desse capítulo, esperamos que você tenha certo entendimento quanto a como seguir com o processo de _playtesting_, e de sua importância para o desenvolvimento de jogos.

No [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo8.md), vou falar um pouco sobre enredos e narrativas em jogos.
