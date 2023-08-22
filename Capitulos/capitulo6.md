
# Capítulo 6: Versões Alfa
"O homem certo no lugar errado pode fazer toda a diferença no mundo." - G-man, _Half Life 2_ (2004)

![Capítulo 6 capa](../Arquivos/Imagens/capa_06.jpg 'The right man in the wrong place can make all the difference in the world.')

## Introdução
_Este capítulo é direcionado para a equipe após a criação do protótipo 0._

Se você chegou aqui inteiro, isso é um ótimo sinal. A criação do protótipo 0 é um dos passos mais difíceis para um iniciante. Mas não se engane, a maior parte do trabalho virá nessa etapa de agora.

Você criou seu protótipo 0 e resolveu vários problemas no caminho. Provavelmente, o que você tem agora não é o ideal, mas já tem uma breve noção de como funcionará o seu jogo. Uma noção do que tem que ser mudado, do que tem que ser adicionado, e de que ainda há muito trabalho pela frente.

O mais importante é: Você consegue ver o seu jogo nesse protótipo? Consegue olhar para ele e reconhecer a base, mantendo em mente o que falta para completar sua ideia original? Se sua resposta é não, talvez valha a pena você voltar à fase do protótipo e trabalhar melhor nele. E se sua resposta é sim, está pronto para continuar o desenvolvimento.

Chegou a hora de envolver toda a sua equipe por inteiro no processo. 

Se você trabalha sozinho, seu ritmo não vai mudar muito, apenas o foco. Seu objetivo segue de forma similar ao protótipo 0, mas agora para o jogo como um todo: completar todos/a maioria das funções e mecânicas de seu jogo **primeiro**, e depois seguir com os outros aspectos como música, arte, e outros quando tiver avançado melhor. Mas não leve isso como uma lei. Caso você deseje ver o seu modelo/sprite na tela, ou precise criar um mapa para testar suas mecânicas, ou gostaria de criar uma música para verificar o tom do jogo, ou precise criar algum outro artefato em qualquer momento, sinta-se livre para fazê-lo.

Este foco nas mecânicas vem da minha experiência, pois minha competência principal é relacionada a lógica e programação, e as outras habilidades necessárias eu aprendi no caminho. Caso você seja um artista ou músico, trabalhar diretamente no que você domina melhor também é válido. Mas não se esqueça, você **não** terá um jogo se negligenciar o aspecto da programação/lógica. 

Para um grupo, cada membro deve seguir com o processo de acordo com o que se mostrar necessário. Sua ideia já deve ter amadurecido, e o retrabalho sobre o qual eu avisei nos primeiros capítulos não é tão provável (mas ainda possível). Dessa forma, esse é um bom momento para começar a trabalhar em versões aprimoradas de imagens de fundo, modelos, ou músicas. 

Lembro a vocês que o foco desse manual é principalmente para desenvolvedores e programadores, mas incluí capítulos voltados para várias das outras competências. Sugiro aos integrantes da equipe que leiam estes capítulos a partir de agora, e avaliem se os métodos e recursos que ofereço vão ser proveitosos, ou se preferem seguir de outra forma. Caso você esteja trabalhando sozinho, sinta-se livre para seguir com eles quando estiver pronto. 

Lembrando também que estas são as sugestões de um desenvolvedor que não tem um _background_ de arte, música, _design_, etc. Se você já trabalha com um destes itens e conhece métodos e _workflows_ melhores que os que citei, sinta-se livre para segui-los.

Links para os capítulos:

- [Enredos/Narrativa - Capítulo 8](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo8.md)
- [Playtesting - Capítlo 7](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo7.md)
- [Arte/Modelagem - Capítulo 9](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo9.md)
- [Música/_Sound Design_ - Capítulo 10](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo10.md)
- [_Level Design_ - Capítulo 12](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo12.md)

### Daqui para frente

De qualquer forma, agora é a hora de montar o seu jogo em si. Não se trata mais de um protótipo. Ao final da _build_ alfa você já deverá ter basicamente todos ou quase todos os blocos que juntos formarão o seu jogo final. A alfa, entretanto, não é a versão mais acabada do jogo.

Para a versão Alfa, o seu foco é similar ao foco da versão protótipo, mas mais espalhado. Você vai listar todos os sistemas de seu jogo, e vai tentar dividir o desenvolvimento destes em tarefas menores e mais fáceis de executar. Para cada sistema, a intenção é que você se preocupe em deixá-lo "bom o suficiente". Idealmente, você já trabalharia o bastante para que cada sistema esteja completamente pronto, mas o foco em **apenas** ser bom o suficiente é para que você não fique completamente preso a um único sistema por um tempo indeterminado.

Em termos simples: cada sistema planejado deve ser trabalhado em um ciclo e testado. Se ao final do ciclo ele estiver bom o suficiente, você pode seguir para outro, e deixar o aprimoramento do sistema anterior para a _beta_. Caso este sistema **não** esteja bom o suficiente, é interessante mantê-lo para o próximo ciclo, mas você também pode começar a trabalhar em outros, lembrando que terá de voltar ao incompleto eventualmente.

Se tiverem mais de um programador na equipe, é possível que trabalhem em 2 sistemas diferentes ao mesmo tempo. Isso pode agilizar o processo, mas lembre-se sempre de que eles devem comunicar e entender o que o outro tem feito, mesmo que superficialmente. Porque todos os sistemas **vão interagir** de alguma forma.

## Outros aspectos
Para aqueles que trabalham em grupo, ou desenvolvedores _solo_ impacientes que já desenvolveram diferentes itens audiovisuais, mapas, etc. Já é interessante que, quando prontos, integrem esses diferentes artefatos no jogo, conforme trabalharem. Este costuma ser um processo simples, mas não trivial. E dependendo do caso, pode se tornar complexo. 

Quando for seguir com este processo, interessa a leitura do capítulo a seguir:

- [Integrando Diferentes Aspectos - Capítulo 11](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo11.md)

## Primeiros passos
Costumo recomendar como primeiro passo que faça uma revisão de seu protótipo 0, e siga com a expansão do projeto a partir dele. Quando fazendo o protótipo 0, a maior preocupação é ter um sistema funcionando para testar sua idiea. Agora, você vai precisar aprimorá-lo para que sirva como base do seu projeto inteiro.

Para isso, minha sugestão é que volte por todos os seus _scripts_ e configurações para certificar-se de que está seguindo boas práticas de programação e desenvolvimento, algumas das quais vou listar a seguir. Além dessas, vou citar algumas práticas que se referem ao gerenciamento do projeto em si.

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

### Boas Práticas - Programação para jogos
- Use comentários e nomenclatura intuitiva

Sempre inclua comentários quando implementando algo não trivial. Não é necessário incluir um comentário para TODA linha de código, mas é importante incluí-los em trechos de entendimento complexo e certas funcionalidades. Em certos casos, para nomes de variáveis também interessa incluí-los.

Outro detalhe importante é a nomenclatura de suas variáveis e funções. Você é livre para dar o nome que quiser a estes, mas é sempre preferível que esse nome seja claro sobre a função deste objeto. Mesmo um nome simples pode aumentar imensamente a legibilidade de seu código.

Esses cuidados não são apenas para outros desenvolvedores que vão trabalhar no mesmo projeto, mas também para o desenvolvedor que escreveu o código. Certos projetos podem levar meses e até anos para serem finalizados, e a maioria das pessoas não tem a memória boa o suficiente para lembrar cada script de um projeto por meses.

- Separe códigos com objetivos diferentes

Organizar o seu código em trechos diferentes vai te ajudar toda vez que você tiver que fazer uma adição ou consertar algum erro. Estes trechos devem estar atrelados a função que o código implementa. Por exemplo, o código de animação do meu personagem não deve estar junto ao código de movimento do meu personagem, por mais que estas duas funções estejam relacionadas.

Isso gera maior complexidade na hora de criar e organizar o código e as condições, mas vale pela organização. Geralmente, eu faço essa separação por meio de funções. No _loop_ principal do meu jogo, uma função é responsável pelo código de movimento, outra pelas animações, outra para capturar _inputs_ diversos, etc.

- Não crie funções/métodos demais

Um erro que eu cometia muito era querer dividir **todos** os subprocessos dos subprocessos de meu jogo em suas próprias funções separadas. Isso deixava o código do _loop_ principal de cada _script_ bem limpo, mas também causava que o resto do _script_ ficasse uma bagunça com uma dúzia de funções curtas.

Nesse sentido, é importante ter bom senso. Funções são úteis para reutilização e organização, mas não as use como "gavetas" para qualquer trecho de código ao qual você _pode_ dar um nome separado. Se desejar, incluir um breve comentário para cada trecho é mais legível e organizado.

- Use tempo _delta_

Fazer _updates_ de posições e valores a cada _frame_ vai causar com que a velocidade de objetos em seu jogo fique dependente da velocidade da máquina, causando inconsistência nessas velocidades para máquinas mais velozes ou mais lentas. Usar o tempo _delta_ permite que você mantenha uma velocidade de _gameplay_ consistente  mesmo que o tempo de execução mude.

- Remova recursos inutilizados

Isso é algo com o qual eu também peco, pois gosto de incluir diversos _sprites_ e modelos de testes em meus projetos. É importante deletar recursos que não estão sendo utilizados para que não criem dificuldade para navegação do seu projeto, e não inflem o tempo de _build_ do seu jogo desnecessariamente.

É claro, tirá-los do projeto vai impedir que data-miners encontrem os recursos aleatórios e especulem sobre versões antigas do jogo, o que pode ser interessante.

- Use _switch cases_ em vez de _else, if_

O formato do _switch_ é muito mais fácil de ler, modificar e expandir do que uma longa sequência de _ifs_. Se você sabe que só terá duas condições, ou se está usando algum padrão com _returns_ diversos, _ifs_ são perfeitamente aceitáveis, mas uma enorme sequência de _elses_ inevitavelmente se tornará um pesadelo de organização.

- Use máquinas de estado

Máquinas de estado são _ótimas_ para desenvolvimento de jogos. Em muitos casos, você terá uma mesma entidade ou objeto com diversos possíveis modos onde sua execução deverá funcionar de maneira diferente. Usar uma máquina de estados é o jeito mais simples para implementar esse tipo de variabilidade.

- Cuidado com variáveis globais e de _script_

Enquanto variáveis globais e de _script_ são extremamente úteis, deve-se sempre tomar cuidado quando atribuindo diferentes valores a elas. É comum encontrar comportamentos inesperados diversos porque a variável foi mudada de uma maneira que não havia sido considerada. 

- Não procure por _strings_ ou IDs

Comparações de _strings_ ou IDs de objetos devem ser evitadas, tanto em termos de performance quanto em termos de organização. Usar comparações por classes para identificar instâncias e filtrar objetos é preferível. Isso, porém, exige que haja a orientação a objetos de alguma forma no seu ambiente de desenvolvimento.

- Não exagere com _Singletons_ e variáveis globais

_Singletons_ são ótimos pelo fato de que podem ser acessados em qualquer _script_ no seu projeto. Gerenciadores de diversas funções universais e variáveis que devem comunicar entre cenas diferentes são bons usos para _singletons_, mas vão causar maior complexidade na análise do seu código, além de certo custo na memória. Em casos onde o sistema não é universal, é preferível usar classes e funções estáticas.

No geral, é preferível evitar o uso de variáveis e funções globais o máximo o possível, pois geram dependências e complexidade no código que são em muitos casos desnecessárias. Porém, são úteis para muitos casos.

- Não inclua objetos/entidades demais

Encher a sua tela de objetos diversos é um ótimo jeito de destruir a performance do seu jogo. Alguns gêneros de jogos, entretanto, precisam que hajam inúmeros objetos em tela, mas isso gerará maior trabalho de otimização mais a frente.

## Revisitando o _Design_
Durante o desenvolvimento do protótipo 0 e da _alfa_, é provavel que você tenha novas ideias para o jogo, ou que chegue a conclusões que ideias que teve anteriormente não serão adequadas ou boas. Nestes casos, você sempre tem a opção de alterar as ideias planejadas no _design_, sejam mecânicas diferentes ou novas, sejam mudanças no cenário, ou quaisquer outras mudanças.

É importante ressaltar que quanto mais cedo estas mudanças foram feitas, menor será o seu trabalho para readaptar o projeto a elas. Mantenha em mente que após certo ponto no tempo de desenvolvimento, e se as suas mudanças forem muito radicais comparado ao estado atual do projeto, é possível que começar um novo projeto para essa ideia seja uma opção melhor. Porém, começar um novo projeto no meio de outro não é uma boa prática (não que eu nunca tenha cometido esse erro). 

## Priorização 
Após a revisão do seu protótipo 0, você pode partir para os outros aspectos. Aqui, você seguirá implementando diferentes sistemas do jogo da mesma maneira que fez no protótipo, mas por onde prosseguir?

Isso realmente fica a critério de cada desenvolvedor, e técnicamente você pode seguir com qualquer sistema em seu jogo, mas eu costumo seguir uma ordem específica:

- Gameplay First (gameplay primeiro):

Eu sempre começo com os diferentes aspectos do **jogo** em si. Em outras palavras, trabalho nas mecânicas primeiro. Dessa forma, coisas como menus, conexões de rede, aspectos audiovisuais gerais sempre ficam para depois. O meu foco no início é sempre criar o **jogo** em si.

Em certos casos isso vai envolver algum dos outros aspectos. Por exemplo, acho difícil você criar um RPG sem trabalhar nos diversos menus de inventário e equipamento, _crafting_, ou o que for. Porém, mesmo para um caso assim, eu trabalharia primeiro na matemática, no movimento, etc.

No geral, eu costumo seguir o seguinte _workflow_: 
1. Trabalhar no personagem jogável (incluir movimento, física, etc.);
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

Quando você trabalha sozinho, eu sugiro o mesmo processo que destaquei anteriormente. O que seria desenvolver o jogo próprio antes de se preocupar com outros aspectos. Porém, em certos casos você vai precisar criar um determinado recurso audiovisual por questões diversas. Nesse caso, um trabalho alternado entre programação e outro aspecto é válido, mas lembre-se sempre de manter o foco no sistema em que está trabalhando. 

## Builds Alfa
A esse ponto, você tem a opção de exportar o seu jogo completamente como um arquivo executável jogável, ou continuar testando sua execução diretamente na _engine_. 

A maioria das _engines_ vai te oferecer a opção de exportar um executável do jogo que construiu. Isso será ainda mais interessante se já tiver um menu simples pronto.

Essas builds serão muito úteis para _playtesting_, pois podem ser enviadas a terceiros sem que eles tenham acesso ao seu projeto completo. Entretanto, lembre-se de tomar cuidado. Cerfique-se de que confia em todas as pessoas a quem vai mandar essas builds, para que eles não o espalhem sem sua permissão.

Mais sobre isso no capítulo de [playtesting](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo7.md).

## Processo de alfa exemplificado
Eu comecei o processo da minha alfa com uma breve lista de funções para adicionar ao jogo: menu principal, menu de seleção de fases, _player completo_ (+ arco e flecha, animações, walljumps), mapas, botões diversos na cena do mapa, marcadores de morte, coletáveis, obstáculos, funcionamento do _ranking_, save/load.

Aqui eu descrevo os passos que tomei para desenvolvimento das diferentes versões alfa. Durante o caminho, recebi _feedback_ de 2 _playtesters_ que me auxiliaram na detecção de _bugs_ e planejamento de ajustes.

- 1: comecei revisando o código do protótipo 0, adicionando comentários e revisando variáveis e valores, e fiz os ajustes de pastas para alguns arquivos
- 2: criei um novo mapa de testes, além de novas _tiles_, uma imagem para o marcador de mortes
- 3: fiz um update no funcionamento das plataformas, além da cena de mapa principal, e diversos ajustes de colisão
- 4: adicionei objetos coletáveis, fiz novos ajustes no _setup_ do mapa principal
- 5: criei outro mapa de testes, fiz ajustes no mapa, incluindo também um plano de fundo
- 6: adicionei novos coletáveis, e criei um novo obstáculo (espinhos)
- 7: fiz um update na tela de vitória para que inclua elementos coletados (e _rankings_), fiz ajustes no script das plataformas para incluir funcionamento de obstáculos, incluí um plano de fundo melhor
- 8: fiz um update para diferentes painéis, além de incluir uma nova plataforma e fazer um ajuste no mapa de testes
- 9: adicionei a função de _walljump_, fiz um ajuste no coletável _puzzle_, adicionei uma função de retorno da câmera a sua posição inicial, fiz um ajuste provisório para um problema de movimento
- 10: incluí texturas e funcionalidades para os botões em tela, adicionei um novo botão de pulo
- 11: criei a cena do marcador de morte, adicionei variáveis para controle de itens coletados, fiz ajustes na cena de mapa
- 12: adicionei cenas provisórias e recursos iniciais para o menu principal e sistema de _save/load_
- 13: adicionei _sprite_ final e animações para o _player_, adicionei funcionalidade à cena de seleção de fases, além de ajustes menores
- 14: adicionei cena de ícone de fase para a tela de seleção, adicionei fontes e texturas para o menu principal, além de fazer ajustes para animar o _player_ nesta tela
- 15: adicionei um _singleton_ responsável pelo sistema de _save/load_, adicionei funcionamento de _load_ quando o jogo é iniciado, adicionei funcionamento à cena de seleção de fases para que receba as informações do _save_
- 16: fiz diversos ajustes na tela de seleção de fases e incluí a função para salvamento das informações após o jogador completar uma fase, removi funções print diversas de _debug_ e fiz outros ajustes menores
- 17: fiz um ajuste para o primeiro mapa, reorganizei as pastas e criei um novo mapa para testes, além de fazer alguns ajustes na cena de seleção de fases
- 18: adicionei ao personagem jogável o arco e flecha, ajustei o _script_ do player para conter uma máquina de estados para uso do arco e flecha, adicionei funcionalidade da flecha e fiz diversos ajustes de colisão
- 19: adicionei novo obstáculo, paredes que só desaparecem após um cristal ser quebrado por uma flecha, ajustei mapas para teste e adicionei _sprites_ inimigos
- 20: fiz alguns ajustes da cena do mapa principal, além de ajustes de pastas e de um _script_ para gerenciamento dos inimigos, adicionei um novo mapa de testes
- 21: fiz um update para o cálculo dos _rankings_ ao final de cada fase, mudei o funcionamento do marcador de morte para mostrar apenas a morte mais recente, fiz com que itens coletados fossem resetados após uma morte sem que a fase inteira fosse resetada
- 22: adicionei um novo botão à cena de seleção de fases, e ajustei o funcionamento dela com os rankings

Para este projeto, eu estava fazendo ciclos bem curtos para terminá-lo rapidamente, mas creio que o processo e a priorização que citei anteriormente ficam evidentes no decorrer dos itens que descrevi acima. Primeiramente eu revisei o código do protótipo 0, e em seguida fiz mudanças no funcionamento das plataformas, até que este ficasse bom o suficiente. Em seguida, passei a adicionar outros objetos importantes ao _gameplay_ como obstáculos e coletáveis, bem como uma informação de _ranking_ com os itens coletados no painel de vitória das fases, incluindo elementos gráficos quando julguei importante para visualização nos testes. Então, voltei ao _script_ do personagem jogável para finalizar algumas das mecânicas que restavam (estas mecânicas dependiam do desenvolvimento dos coletáveis e plataformas, por isso vieram depois de trabalhar nestes aspectos). 

Trabalhei então no resto da tela do que havia planjeado para o _gameplay_, com os botões de ações, a adição de um marcador de mortes, e o funcionamento para controle de itens coletados durante a fase (este não foi terminado por ora). Comecei a trabalhar no sistema de save/load e no menu principal, mas isso se tornou complexo, e voltei ao _player_ para incluir seu sprite e animações. Agora julguei ser uma boa hora de trabalhar nas outras cenas que não a do _gameplay_, seleção de fases e menu principal, adicionando uma nova fonte e texturas quando necessário. Como o sistema de save/load estava ligado ao menu principal, voltei a trabalhar nele até que ficasse bom o suficiente.

Atualizei mais uma vez a tela de seleção de fases, para que fizesse uso das novas funções de save/load. E fiz o mesmo para a tela de _gameplay_ geral. Após fazer alguns ajustes gerais, voltei a trabalhar na última mecânica do personagem jogável, seu arco e flecha. Fiz diversos ajustes para o funcionamento dessa mecânica, e adicionei um novo obstáculo para testes que dependia dela (a parede com o cristal que deve ser destruído para que ela saia do caminho). Adicionei então novas cenas para inimigos que também dependeriam da nova mecânica de arco e flecha. Por fim, fiz alguns ajustes no funcionamento dos _rankings_ ao final de cada fase, um ajuste no funcionamento do marcador de mortes, e um ajuste no funcionamento da fase após a morte do jogador, deixando a cena de mapas boa o suficiente. Com o último ajuste na tela de seleção, encerrei a etapa da _alfa_.

## Conclusão
Ao final deste capítulo, espero que você tenha uma ideia geral de como conduzir o desenvolvimento das versões alfa, e de algumas das melhores práticas de programação para manter em mente durante o desenvolvimento. 

Durante o desenvolvimento, sugiro que dê uma lida nos capítulos seguintes pertinentes aos diferentes aspectos de desenvolvimento que não envolvem programação. Especialmente o [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo7.md), sobre _playtesting_. Nele, falamos mais sobre criação de builds, testes e _debugging_.
