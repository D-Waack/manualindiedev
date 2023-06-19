
# Capítulo 6: Versões Alfa
"O homem certo no lugar errado pode fazer toda a diferença no mundo." - G-man, "_Half Life 2_" (2004)

![Capítulo 6 capa](../Arquivos/Imagens/capa_06.jpg 'The right man in the wrong place can make all the difference in the world.')

## Introdução
_Este capítulo é direcionado para a equipe após a criação do protótipo 0._

Se você chegou aqui inteiro, isso é um ótimo sinal. A criação do protótipo 0 é um dos passos mais difíceis para um iniciante. Mas não se engane, a maior parte do trabalho virá nessa etapa de agora.

Você criou seu protótipo 0 e resolveu vários problemas no caminho. Provavelmente, o que você tem agora não é o ideal, mas já tem uma breve noção de como funcionará o seu jogo. Uma noção do que tem que ser mudado, do que tem que ser adicionado, e de que ainda há muito trabalho pela frente.

O mais importante é: Você consegue ver o seu jogo nesse protótipo? Consegue olhar para ele e reconhecer a base, mantendo em mente o que falta para completar sua ideia original? Se sua resposta é não, talvez valha a pena você voltar à fase do protótipo e trabalhar melhor nele. E se sua resposta é sim, está pronto para continuar o desenvolvimento.

Chegou a hora de envolver toda a sua equipe por inteiro no processo. 

Se você trabalha sozinho, seu ritmo não vai mudar muito, apenas o foco. Seu objetivo segue de forma similar ao protótipo 0: completar todos/a maioria das funções e mecânicas de seu jogo **primeiro**, e depois seguir com os outros aspectos como música, arte, e outros quando tiver avançado melhor. Mas não leve isso como uma lei. Caso você deseje ver o seu modelo/sprite na tela, ou precise criar um mapa para testar suas mecânicas, ou gostaria de criar uma música para verificar o tom do jogo, ou precise criar algum outro artefato em qualquer momento, sinta-se livre para fazê-lo.

Este foco nas mecânicas vem da minha experiência, pois minha competência principal é relacionada a lógica e programação, e as outras habilidades necessárias eu aprendi no caminho. Caso você seja um artista ou músico, trabalhar diretamente no que você domina melhor também é válido. Mas não se esqueça, você **não** terá um jogo se negligenciar o aspecto da programação/lógica. 

Para um grupo, cada membro deve seguir com o processo de acordo com o que se mostrar necessário. Sua ideia já deve ter amadurecido, e o retrabalho sobre o qual eu avisei nos primeiros capítulos não é tão provável (mas ainda possível). Dessa forma, esse é um bom momento para começar a trabalhar em versões aprimoradas de imagens de fundo, modelos, ou músicas. 

Lembro a vocês que o foco desse manual é principalmente para desenvolvedores e programadores, mas incluí capítulos voltados para várias das outras competências. Sugiro aos integrantes da equipe que leiam estes capítulos a partir de agora. Caso você esteja trabalhando sozinho, sinta-se livre para seguir com eles quando estiver pronto. 

Lembrando também que estas são as sugestões de um desenvolvedor que não tem um _background_ de arte, música, _design_, etc. Se você já trabalha com um destes itens e conhece métodos e _workflows_ melhores que os meus, sinta-se livre para segui-los.

Links para os capítulos:

- [Enredos/Narrativa](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo8.md)
- [Playtesting](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo7.md)
- [Arte/Modelagem](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo9.md)
- [Música/Sound Design](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo10.md)
- [Level Design](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo12.md)

### O Próximo Passo

De qualquer forma, agora é a hora de montar o seu jogo em si. Não se trata mais de um protótipo. Ao final da _build_ alfa você já deverá ter basicamente todos os blocos que juntos formarão o seu jogo final. A alfa, entretanto, não é a versão mais acabada do jogo.

Para a versão Alfa, o seu foco é similar ao foco da versão protótipo, mas mais espalhado. Para todos os sistemas de seu jogo, a intenção é que você se preocupe em deixá-los "bons o suficiente". Idealmente, você já trabalharia o suficiente para que cada sistema esteja completamente pronto, mas o foco em **apenas** ser bom o suficiente é para que você não fique completamente preso a um único sistema por um tempo indeterminado.

Em termos simples: cada sistema planejado deve ser trabalhado em um ciclo e testado. Se ao final do ciclo ele estiver bom o suficiente, você deve seguir para outro, e deixar o aprimoramento do sistema anterior para a _beta_. Caso este sistema **não** esteja bom o suficiente, é interessante mantê-lo para o próximo ciclo, mas você pode começar a trabalhar em outros também, lembrando que terá de voltar ao incompleto eventualmente.

Se tiverem mais de um programador na equipe, é possível que trabalhem em 2 sistemas diferentes ao mesmo tempo. Isso pode agilizar o processo, mas lembre-se sempre de que eles devem comunicar e entender o que o outro tem feito, mesmo que superficialmente. Porque todos os sistemas **vão interagir** de alguma forma.

## Outros aspectos
Para aqueles que trabalham em grupo, ou desenvolvedores _solo_ impacientes que já desenvolveram diferentes itens audiovisuais, mapas, etc. Já é interessante que, quando prontos, integrem esses diferentes artefatos no jogo, conforme trabalharem. Este costuma ser um processo simples, mas não trivial. E dependendo do caso, pode se tornar complexo. 

Quando for seguir com este processo, interessa a leitura do capítulo a seguir:

- [Integrando Diferentes Aspectos](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo11.md)

## Primeiros passos
Costumo recomendar como primeiro passo que faça uma revisão de seu protótipo 0, e siga com a expansão do projeto a partir dele. Quando fazendo o protótipo 0, a maior preocupação é ter um sistema funcionando para testar sua idiea. Agora, você vai precisar aprimorá-lo para que sirva como base do seu projeto inteiro.

Para isso, minha sugestão é que volte por todos os seus _scripts_ e configurações para certificar-se de que está seguindo as boas práticas de programação que vou listar a seguir. Além dessas, vou citar algumas práticas que se referem ao gerenciamento do projeto em si.

Junto com a revisão do protótipo, é interessante revisar também o _design_ e atualizar seu GDD não somente após essa revisão, mas também a cada novo ciclo.

### Boas Práticas - Gerenciamento do projeto
- Usar alguma forma de controle de versões

Admito que raramente tive a necessidade de voltar a uma versão anterior de meu projeto. Mas quando eu precisei, ter um controle de versões me poupou horas de estresse e trabalho. Além da possibilidade de retornar a versões anteriores, isso também auxilia na organização de seu projeto, e serve como um _backup_ caso algo aconteça. Eu costumo usar o Git/Github para fazer isso, mas você pode usar a ferramenta que preferir.

- Manter sua lista de tarefas atualizada

A "lista de tarefas" é literalmente uma lista com coisas que você tem que fazer/aprimorar no seu projeto. Eu usei o termo _backlog_ emprestado do Scrum como minha lista de tarefas. Na teoria, esses conceitos não são exatamente iguais, mas para o contexto em que estamos, vão servir como a mesma coisa. 

Minha política é de que **sempre** que eu penso em algo que deve ser feito, eu o anoto na minha lista de tarefas. Sugiro que você faça o mesmo. Se não, é muito provável que você esquecerá de algo importante.

Para muitos projetos, essa lista começa a ficar cada vez maior com o passar do tempo. Por isso, é interessante separar as tarefas em alguns tópicos diferentes. Alguns exemplos de tópicos que costumo utilizar são: _Sistemas_ (sistemas completos que ainda não implementei), _Bugs_ (algum funcionamento inesperado que deve ser concertado), _Ajustes_ (funcionamento é similar ao esperado, mas ainda não está perfeito).

- Usar alguma ferramenta de organização

Similar ao tópico anterior, utilizar uma ferramenta como o Trello ou JIRA pode ser interessante também. Especialmente se você trabalha em equipe. Trabalhando solo, eu geralmente me limito à minha lista manual, mas as interfaces destes programas podem ajudar a organizar seu trabalho de maneira mais eficiente também. 

### Boas Práticas - Programação
- 

## Revisitando o _Design_

## Priorização 
Após a revisão do seu protótipo 0, você pode partir para os outros aspectos. Mas por onde prosseguir?

Isso realmente fica a critério de cada desenvolvedor, e técnicamente você pode seguir com qualquer sistema em seu jogo, mas eu costumo seguir uma ordem específica:

- Gameplay First (gameplay primeiro):

Eu sempre começo com os diferentes aspectos do jogo em si. Em outras palavras, trabalho nas mecânicas primeiro. Dessa forma, coisas como menus, conexões de rede, aspectos audiovisuais gerais sempre ficam para depois. O meu foco no início é sempre criar o **jogo** em si.

Em certos casos isso vai envolver algum dos outros aspectos. Por exemplo, acho difícil você criar um RPG sem trabalhar nos diversos menus de inventário e equipamento, _crafting_, ou o que for. Porém, mesmo para um caso assim, eu trabalharia primeiro na matemática, no movimento, etc.

No geral, eu costumo seguir o seguinte _workflow_: 
1. Trabalhar no personagem jogável (inclui movimento, física, etc.);
2. Trabalhar em objetos e entidades que interagem com o personagem jogável;
3. Trabalhar no resto.

Você não precisa segui-lo, mas é um método organizado caso te interesse.

- Feel em Seguida:

Coisas como efeitos sonoros, _screen shakes_ (tela balançando), animações, movimento da câmera, etc. são os próximos aspectos que eu priorizo. Entretanto, aperfeiçoar esses diversos aspectos é mais relevante para versões beta.

Para a priorização destes diferentes aspectos, eu sugiro que se faça as seguintes perguntas:
1. Isso é completamente necessário para o funcionamento do meu jogo? (Se a resposta for sim, como uma ação que **deve** estar atrelada a uma animação, você deve trabalhar melhor nisso. Caso contrário, não tenha como prioridade.)
2. Isso vai atrasar o desenvolvimento de outros sistemas? (Se sim, talvez valha a pena deixar isso para depois).
3. Não completar isso vai impedir o desenvolvimento de outros sistemas? (Se a resposta for sim, isso cai na pergunta 1).

Caso conclua um "não" para estas perguntas, vale a pena seguir com o "bom o suficiente".

- Outros aspectos:

Coisas como menus principais e de pause, leaderboards, telas diversas caem todos como o último item na lista de prioridade. Isso é porque eles não são necessários para o funcionamento do jogo em si, e provavelmente serão mudados extensivamente nas versões _beta_. Entretanto, é bom trabalhar também neste aspecto, pois o desenvolvimento de interação entre menus não é tão simples quanto pode parecer.

Implementar a ideia por trás deles com arte provisória e afins é completamente válido. Inclusive, trabalhar em versões simples destes menus pode te dar ideias para como melhorá-los mais a frente. 

- Quando sozinho:

Quando você trabalha sozinho, eu sugiro seguir basicamente o mesmo processo que destaquei anteriormente. O que seria desenvolver o jogo próprio antes de se preocupar com outros aspectos. Porém, em certos casos você vai precisar criar um determinado recurso audiovisual por questões diversas. Nesse caso, um trabalho alternado entre programação e outro aspecto é válido, mas lembre-se sempre de manter o foco no sistema em que está trabalhando. 

## Builds Alfa
A esse ponto, você tem a opção de exportar o seu jogo completamente como um arquivo executável jogável, ou continuar testando sua execução diretamente na _engine_. 

A maioria das _engines_ vai te oferecer a opção de exportar um executável do jogo que construiu. Isso será ainda mais interessante se já tiver um menu simples pronto.

Essas builds serão muito úteis para _playtesting_, pois podem ser enviadas a terceiros sem que eles tenham acesso ao seu projeto completo. Entretanto, lembre-se de tomar cuidado. Cerfique-se de que confia em todas as pessoas a quem vai mandar essas builds, para que eles não o espalhem sem sua permissão.

Mais sobre isso no capítulo de [playtesting](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo7.md).

## Conclusão
Ao final deste capítulo, espero que você tenha uma ideia geral de como conduzir o desenvolvimento das versões alfa, e de algumas das melhores práticas de programação para manter em mente durante o desenvolvimento. 

Antes de completá-las, sugiro que dê uma lida nos capítulos seguintes pertinentes aos diferentes aspectos de desenvolvimento que não envolvem programação. Especialmente o [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo7.md), sobre _playtesting_. Nele, falamos mais sobre criação de builds, testes e _debugging_.
