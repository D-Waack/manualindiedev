# Capítulo 13: Versões Beta, Finalizando Builds, Polishing
"A vós que labutas em vão. Sois tolo. Sois tolo. Sois tolo. Sois tolo." - Inscrição gravada na pedra no corredor sem fim, "_La Mulana_" (2006)

![Capítulo 13 capa](../Arquivos/Imagens/capa_12.png 'To the one who toils for naught. Thou art foolish. Thou art foolish. Thou art foolish. Thou art foolish.')

## Introdução
Se você já implementou todos os sistemas principais de seu jogo, seu _backlog_ não contém mudanças muito grandes, e você já consegue ver que o seu jogo está no caminho para ficar pronto. Podemos prosseguir com as versões beta.

Caso ainda tenha alguns sitemas simples para implementar, o processo pode seguir da mesma forma que a _alfa_. Entretanto, seu foco aqui vai ser dividido também em outras tarefas. Essas tarefas envolvem finalizar todo o trabalho que você deixou para trás nas outras etapas. Seu jogo pode estar próximo de sua versão final, mas ainda restam algumas pontas para atar.

## Finalizando sistemas da alfa
Parte do seu trabalho terá de ser voltar por tudo o que você fez e aprimorar cada sitema para que fique de acordo com o planejado. O "bom o suficiente" já não é mais bom o suficiente, agora seu objetivo é fazer com que estes sistemas fiquem **prontos**. Antes de considerar um sistema _terminado_, entretanto, interessa passar pelos diversos aspectos que descrevo no decorrer deste capítulo.

## Consertando Bugs Finais
A não ser que você estivesse focando em consertá-los antes, você deverá ter uma bela lista de várias coisas que não estão funcionando exatamente do jeito certo ao final da alfa. Agora é a hora de dar uma passada final por todos estes e deixar o seu jogo funcionando certinho.

A ordem pela qual você vai querer resolver estes _bugs_ pode ser importante. Às vezes, consertar um bug causa outro, às vezes, consertá-lo causa com que outros parem de acontecer. Se você souber que dois _bugs_ diferentes são parte do mesmo sistema, tente começar pelo mais "fundamental" entre os dois, e talvez você encontre uma surpresa agradável.

Lembre-se sempre de continuar com o _playtesting_ normalmente após consertar algo, para que os desdobramentos de suas mudanças sejam encontrados o mais rápido o possível.

No geral, eu costumo começar pelos problemas que _parecem_ mais simples, e costumo mover para outra resolução caso não consiga resolver algum problema em um tempo elevado. Isso fica ao critério do desenvolvedor, contanto que mantenha em mente o fato de que um erro pode influenciar no outro.

## Otimização
O processo de otimização envolve melhorar o seu código e outros aspectos do seu projeto para permitir com que o jogo execute _mais rápido_, ou seja, para evitar lentidão no seu jogo (_lag_). Geralmente, você vai encontrar três formas principais de lentidão: lentidão constante causada por um processo lento que ocorre todo frame; lentidão ocasional causada por processos intermitentes ou raros; e lentidão fora do _gameplay_, por exemplo no carregamento de um mapa ou menu.

Pode parecer um pouco tarde para introduzir um conceito tão importante quanto otimização no seu projeto, mas existe bons motivos para isso. 

Primeiramente, se você **não** encontra lentidão no seu jogo, você **não** precisa gastar seu tempo com otimização. Obviamente, se você deseja que seu jogo rode em máquinas com performance pior do que a sua, vale a pena testar por lentidão em uma dessas máquinas. O primeiro motivo é este: nem sempre a otimização se mostra necessária.

Outro motivo é o fato de que otimização é um trabalho complexo, e dependendo de seu projeto vai causar uma boa perda de tempo. Perder tempo aprimorando um projeto quase pronto é muito mais proveitoso do que perder tempo em um projeto que acabou de começar. Ainda outro motivo é que uma boa parte da necessidade para otimização é causada por desrespeitar boas práticas, o que espero que sua equipe esteja evitando.

O motivo mais importante, porém, é que a princípio não haverão mudanças muito grandes no seu projeto. Dessa forma, você provavelmente não perderá tempo e esforço para otimizar um _script_ ou funcionamento que sofrerá mudanças grandes mais a frente no projeto. Ou seja, a intenção principal é poupar tempo e trabalho.

Inclusive, se você encontrou algo que deixa seu jogo muito lento durante o desenvolvimento da _alfa_, você provavelmente já procurou o motivo e trabalhou para consertar o problema antes de chegar aqui, mas é possível que seu jogo encontre lentidões com as quais você ainda não conseguiu lidar. É exatamente isso que a etapa de otimização objetiva consertar.

### Processo de otimização

A otmização de código é um processo que depende de vários fatores, inclusive do ambiente e linguagem de programação. O _debug_ neste caso não é muito diferente de como você faria para encontrar um erro ou consertar algo funcionando de maneira inesperada. Porém, esse tipo de análise costuma ser um pouco mais complexa do que as outras. Algumas _engines_ oferecem _Profilers_ e outras ferramentas que fazem uma análise da memória e tempo de execução do seu projeto, mas isso não é garantido. 

O processo que eu costumo seguir é o de criar uma cena de testes, e adicionar outros objetos aos poucos para encontrar qual está causando a lentidão. Em outros casos (como em casos de lentidão constante), é mais simples fazer o processo contrário, retirando elementos de sua cena até que a execução volte ao normal. 

Esse processo é bom para situações onde a mera presença de um objeto leva a lentidão, mas é simples tomar por regra de que quanto menos elementos houverem em uma cena, mais fácil será encontrar o elemento que está causando lentidão. E uma vez identificado o elemento causador da lentidão, é muito mais fácil buscar o problema e sua solução.

Se este causador for um único objeto, analise seu _script_. Tente encontrar alguma execução que parece ser mais complexa, remova partes e teste novamente pela lentidão, até que possa isolar o processo que está causando o problema. Uma vez isolado, tente entender o motivo e procure formas mais eficientes de fazer a mesma coisa.

### Exemplos comuns
Enquanto lentidão pode ser causada por inúmeros fatores, e depende da plataforma e máquina que executa o código, temos alguns casos universais que causam lentidão, tanto sozinhos quanto em conjunto:

- Criação/destruição de objetos
  
A criação e destruição de objetos (inimigos, NPCs, projéteis, objetos de cenário) em tempo de execução é muito custosa, e uma grande causa de lentidão na execução de um jogo. O melhor jeito de evitar esse problema é utilizar a técnica chamada _Object Pooling_.

Essa técnica consiste de inicializar/alocar as instâncias dos objetos que serão usados em uma cena todos em um único conjunto durante a inicialização dessa cena. Essas instâncias ficam desativadas e invisíveis até o momento que forem necessárias para a cena. O _script_ então pode simplesmente pegar um objeto desse conjunto e ativá-lo, e quando este não for mais necessário para a cena, pode desativá-lo e retorná-lo ao conjunto. Dessa forma, o custo da instância ocorre apenas durante o carregamento da cena.

Na maioria das _engines_, usar _Object Pooling_ pode melhorar bastante a performance do seu jogo, a não ser que seu projeto seja **bem** simples. Mesmo em _engines_ onde instanciar objetos não é tão custoso, como Godot, essa técnica ainda pode ser útil, por exemplo, ao pré-carregar objetos devido a um certo _bug_ do OpenGL que causa lentidão no primeiro carregamento de uma textura ou efeito.

- Objetos/efeitos demais
  
Todos os _scripts_ executando ao mesmo tempo em seu jogo concorrem pelos mesmos recursos. Um objeto rodando uma execução complexa pode não fazer diferença nenhuma na performance, mas se você tiver 200 cópias desse mesmo objeto, isso pode mudar facilmente. O mesmo se aplica para partículas, _shaders_ e outros efeitos que exigem cálculo a todo frame.

Nestes casos, você terá duas principais opções: simplificar o funcionamento destes objetos, ou diminuir a quantidade deles. Existem outras opções, mas estas seriam soluções complexas para um problema simples. Caso você _precise_ centenas de objetos em tela ao mesmo tempo, considere algumas outras formas de simplificar a execução destes, ou alguma espécie de execução condicional.

- Operações e estruturas custosas
  
Nem todas as linhas de código são criadas iguais. Certas operações são extremamente custosas e vão arruinar a performance do seu jogo, especialmente se forem executadas a todo _frame_. Certos casos como funções recursivas, certas operações entre vetores, cálculos contantes vão causar lentidão.

Nesses casos, é interessante limitar estas chamadas apenas para situações ocasionais, e evitar ao máximo fazer cálculos complexos com certas estruturas de dados. Eu mesmo cansei de me perguntar por que meu jogo estava travando enquanto tentava rodar um A* para vários personagens todo frame.

Outro tipo de operações que podem ser custosas são chamadas de certas funções de sua própria _engine_. Por exemplo, muitos processos físicos como colisões e _checks_ de colisão simultâneos podem causar lentidão. Nestes casos, pode interessar criar métodos alternativos para estas detecções que não dependem de chamadas da física da própria _engine_.
  
Uma forma de tentar evitar certos cálculos custosos contantes é utilizar uma _flag_ para atualização de certos elementos. Porém, isso só vale a pena se estes cálculos são mais custosos do que o _check_ para esta _flag_.

- No geral...
  
A maioria das necessidades de otimização vão estar diretamente ligadas ao funcionamento da _engine_ ou _framework_ que você está utilizando. Sempre vale à pena fazer uma busca específica sobre as particularidades de seu ambiente de programação.

## Usabilidade
O final de seu projeto é um ótimo momento para melhorar diversos aspectos do produto em si. Busque sempre dar _mais opções_ ao seu jogador. Por exemplo, permita que ele possa usar diferentes tipos de controles, se mais de um estiver disponível para a plataforma. Inclua opções para mudança de teclas e botões, ajuste de volumes para diferentes canais de áudio, diversas mudanças de resolução da tela e efeitos gráficos. Se possível e relevante, inclua diferentes opções e níveis para diversos efeitos gráficos, para que seu jogador possa buscar melhoria de performance em sua máquina.

## Mais _Playtesting_
Testar o seu jogo a cada mudança na beta se torna cada vez mais importante, tanto para os desenvolvedores quanto aos _playtesters_. Mantenha os _playtesters_ informados sobre mudanças e adições, e deixe com que sigam com o processo normalmente.

## _Polishing_
_Polishing_ se refere a melhorar o "acabamento" do jogo. Torná-lo mais agradável e limpo. Essa etapa se refere principalmente à estética e responsividade.

Se trata de coisas como melhorar a interface, melhorar responsividade de certas ações e do controle no geral. Incluir coisas desnecessárias que os jogadores podem apreciar. Melhorar o uso de cores, revisar o impacto e qualidade dos efeitos sonoros, incluir transições entre telas, entre várias outras melhorias pequenas.

Isso é um trabalho simples, mas que faz muita diferença para as versões finais de seu jogo.

## Preparação para o Lançamento
Quando estiver satisfeito com todos os elementos do seu jogo, uma última série de testes deve ser feita. Revise tudo o que fez, e tente comparar o seu produto final com a ideia inicial proposta no seu primeiro GDD.

O que mudou? O que ficou melhor? O que você teve que sacrificar? Sua visão foi realizada? Esta é a versão final de seu jogo. Tome o _feedback_ dos seus _playtesters_, e faça essa pergunta: "Meu jogo está realmente pronto?"

Essa última avaliação é importante, e tenha certeza de que a resposta é sim, a não ser que você queira começar lançá-lo como _Early Access_ ou uma _open beta_. Nas palavras de Miyamoto, "Um jogo bom só está atrasado até o momento de lançamento, um jogo ruim é ruim para sempre."

## Conclusão
Nesse capítulo descrevo o processo para o desenvolvimento e finalização da _beta_. Este processo não é muito diferente do que vimos com a _alfa_, exceto que o foco é diferente. Aqui, a questão principal é o acabamento e finalização do projeto, e não o desenvolvimento de funcionalidades novas. 

No [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo14.md), falarei sobre o passo final, a publicação, e a manutenção do jogo pós-lançamento.
