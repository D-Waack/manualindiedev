
# Capítulo 11: Integrando Recursos Audiovisuais
"Mas o futuro se recusou a mudar." - "_Chrono Trigger_" (1995)

![Capítulo 11 capa](../Arquivos/Imagens/capa_11.jpg 'But the future refused to change.')

## Introdução
Pouco adianta criar recursos como _sprites_, modelos e temas musicais se você não souber como incluí-los em seu jogo. Esse capítulo vai discutir um pouco sobre técnicas para incluí-los e o que fazer com cada um deles.

## Recursos Visuais
Recursos visuais são extremamente importantes, mas também vêm em várias formas diferentes. Aqui, é importante fazer uma distinção entre recursos 2D, 3D e outros diversos formatos.

### Recursos 2D - Planos e camadas
Em grande parte, jogos 2D são compostos de diferentes camadas visuais. Em um jogo _sidescroller_, isso pode vir como diferentes camadas de objetos, um plano de fundo, e a camada principal onde existem os personagens. Em um jogo _topdown_ ou isométrico, nem sempre encontramos camadas de fundo, mas ainda assim temos a camada do mapa e pelo menos mais uma principal para os objetos e personagens.

O formato técnico de como essas camadas são mostradas em tela pouco importa para o nosso contexto. O que importa é a ordem de renderização, e as colisões. Cabe ao desenvolvedor montar essa ordem na hora da criação da cena no jogo. Porém, isso é um processo bem intuitivo.

Normalmente, encontramos a seguinte ordem: 
- Planos sem interação: plano de fundo (principal) -> objetos do plano de fundo (distantes) -> objetos no plano principal (próximos)
- Planos com interação (sidescroller): mapa (chão) -> objetos de cenário (interativos) -> personagens
- Planos com interação (topdown): mapa (chão) -> personagens -> objetos de cenário

Isso deve estar óbvio, mas a seta indica que o próximo objeto virá **à frente** do objeto anterior. Para jogos sidescroller, ter todas as 3 camadas que mencionei como uma só também é possível, ou apenas uma camada para objetos e mapa, com personagens no topo. 

Nem todos os projetos terão todas estas camadas, e alguns podem ter mais, mas no geral, seguir esse tipo de ordem costuma ser o caminho mais adequado.

### Recursos 2D - Colisões: camadas de objetos
As camadas principais para o funcionamento do seu jogo são as camadas de mapa, objetos e personagens.

Para jogos no estilo _sidescroller_ e similares, o **mapa em si** deve ser um objeto real com colisões. Afinal, se o seu personagem contem gravidade, ele precisa de um chão para impedir que ele caia infinitamente. Para mapas feitos com _tiles_ quadrados, costuma ser bem simples atribuir uma colisão quadrada diretamente a cada _tile_. A maioria das _engines_ permite isso, e programas como o _tiled_ e o _LDTK_ também oferecem a possibilidade de criação de mapas que já exportam com a colisão pronta para importação em uma _engine_ ou _framework_.

Para mapas que não são montados com _tiles_, como é o caso com o jogo Hollow Knight, é possível simplesmente criar colisões para eles manualmente. A mesma coisa também é possível com mapas de _tiles_, mas isso costuma ser um trabalho desnecessário. No meu projeto, tentei usar um pouco dos dois. 

Para mapas no estilo _topdown_ e similares, o mapa em si (o chão) não precisa ter colisões. A não ser em casos onde haja algum tipo de evento causado por andar no mapa. Mapas que contém buracos ou quedas vão conter colisão apenas em pontos onde existe essa queda, ou nos cantos. Ou ainda, terão colisões em áreas que não são acessíveis, como uma parede mais alta, ou uma área com água. O motivo pelo qual o chão navegável não costuma ter colisões é porque isso causaria conflitos com o movimento dos personagens. 

Objetos como pilares, árvores, alavancas, ou qualquer objeto de cenário vêm por cima da camada do chão, e estes costumam vir com colisões. Para um mapa sidescroller, o objeto interativo não _precisa_ ter uma colisão, até porque certos objetos vão causar com que o personagem jogável não consiga avançar no mapa. Ainda certos objetos vão conter apenas colisão que interage com a arma do jogador (por exemplo, objetos de cenário quebráveis). Certos objetos vão ter colisões apenas em certas situações. Em outros casos, se o objetivo é bloquear a passagem do personagem, é esperado que tenham a colisão.

Para jogos no estilo _topdown_, objetos de cenário sempre terão colisões. Porém, estes jogos tentam criar uma ilusão de 3D, e é interessante que contenham colisões somente na sua "base". Ou seja, o topo destes objetos costumam não conter colisões. Nesses casos, é interessante tentar criar um objeto em uma camada _acima_ do jogador (mais à frente), para que o mesmo não apareça no topo de um objeto erroneamente.

Colisões para objetos costumam ser _retângulos_ simples que englobam o objeto completamente. Para objetos redondos, talvez um círculo seja mais adequado. Para grande parte dos jogos, colisões simples assim costumam ser o mais adequado. Manter colisões com formatos primitivos também simplifica os cálculos de física, permitindo com que seu jogo execute melhor. Porém, em certos casos, colisões primitivas não vão ser boas o suficiente, e criar um polígono manualmente se mostra necessário. Tente evitar isso ao máximo, mas lembre-se que é uma opção.

[Ilustrando colisões nos dois estilos]

### Recursos 2D - Colisões: camadas de personagens
As camadas de personagens são as mais simples. Geralmente ficam no topo, como a camada mais aparente (com exceção de casos onde existem objetos que devem aparecer à frente destes). Em termos de colisões, costumamos seguir com o mesmo formato para objetos diversos. A colisão é um retângulo que engloba o personagem completamente. 

Em outros casos, um formato circular ou de cápsula pode ser bom também. Isso costuma ser útil para jogos _topdown_, onde o formato arredondado impede que o personagem interaja de maneira estranha com cantos (existem outros meios de evitar essa estranheza). Para jogos _sidescroller_ retângulos costumam ser o melhor formato para personagens que interagem com o chão.

O importante para personagens é que a colisão os englobe completamente, ou quase completamente. Além disso, é importante certificar-se de que as caixas de colisão _interagem_ com a colisão dos mapas e objetos. Em algumas _engines_, colisões são todas na mesma camada por padrão, mas na maioria dos casos você pode mudar manualmente quais camadas colidem com quais, e isso permite várias interações interessantes, mas exige cuidado para que as interações corretas aconteçam.

### Recursos 2D - Colisões vs Hitboxes
Um outro detalhe importante para personagens são as colisões de dano (ou o que chamamos de hitboxes e hurtboxes). Costumamos assumir que a área de dano de um personagem é a mesma que colide com o ambiente. Enquanto isso é verdade em alguns casos, na maioria deles não é.

[Exemplo hitbox touhou]

Uma _hitbox_ se refere a essa área de colisão responsável por registrar _dano_. Em alguns casos, o termo _hurtbox_ é usado para se referir a uma área responsável por **receber** dano, e _hitbox_ apenas para a área responsável por **realizar** dano. Eu usarei esses termos por questões de simplicidade, mas geralmente _hitbox_ se refere a ambos.

Hitboxes e Hurtboxes devem ser adaptadas ao contexto que se encontram. Geralmente, é comum criarmos uma hurtbox menor que a colisão para o player, e analogamente uma hurtbox maior que a colisão para inimigos. Isto deixa as coisas um pouquinho injustas, de modo que o jogo fica mais fácil. Mas essa inclinação para facilitar o jogo, quando aplicada, costuma passar despercebida pelo jogador. Da mesma forma, jogadores costumam se incomodar quando a mesma não é aplicada.

No Godot (a _engine_ que eu mais uso), eu costumo criar hitboxes como nós do tipo Area2D, para que eles não interajam fisicamente com objetos do cenário, e apenas reajam a outras hitboxes e hurtboxes. Essa é uma abordagem interessante, caso seja possível executá-la no seu ambiente de escolha.

No geral, hitboxes e hurtboxes vão ser projetadas caso a caso. Por exemplo, em _Super Mario Bros_, Mario tem uma hitbox somente no fundo de seus pés, enquanto o resto de seu corpo é uma hurtbox. Porém, quando o Mario coleta uma estrela, sua hurtbox é desativada e todo o seu corpo se torna uma hitbox. Da mesma forma, a hitbox dos inimigos é o corpo inteiro deles, e a hurtbox também.

Em um jogo como _Castlevania_, a hitbox do jogador é composta somente da arma do personagem (um chicote, ou uma espada, ou um projétil). Enquanto a hurtbox do jogador é sempre a mesma, composta de seu corpo inteiro.

### Recursos 2D - Planos de fundo e camadas secundárias
Enquanto não existe preocupação de colisões para planos de fundo em 2D, existem alguns detalhes interessantes. Isso se aplica principalmente a jogos do estilo _sidescroller_. Jogos _topdown_ em sua maioria são do estilo não contêm planos de fundo complexos.

### Recursos 2D - Efeitos e shaders

### Recursos 3D - Modelos e texturas

### Recursos 3D - Skyboxes, iluminação, efeitos e shaders

### Recursos Gerais - HUDs e interfaces

## Recursos Sonoros
Recursos sonoros são mais simples para inclusão do que os visuais, mas requerem alguns cuidados únicos.

### Música de fundo
Em questões de música, a abordagem principal é atrelar uma música a um _local_, uma _fase_, ou um _evento_. Nem todos os jogos seguem essa ideia. Alguns jogos como _The Legend of Zelda: Breath of the Wild_ vão oferecer música somente em _cutscenes_, e outras músicas atmosféricas aleatoriamente durante o decorrer do jogo. Alguns jogos como _Nier: Automata_ vão oferecer variações da mesma música para momentos diferentes em uma área (citaria um exemplo, mas não quero dar nenhum _spoiler_ da história do jogo).

Dessa forma, sua preocupação primária com a música é decidir quando e onde ela tocará. Para um _approach_ de áreas, isso costuma ser bem fácil. Qualquer que seja o _script_ responsável pela manutenção dessa área pode iniciar a música quando ele inicializa. Ou, ainda outro _approach_ é ter um gerenciador de músicas global que checa ou reage a uma mudança de área e troca a música quando necessário. A primeira opção é geralmente a mais simples, mas cada uma tem suas vantagens.

Esse mesmo conceito pode ser aplicado para _cutscenes_ e outros eventos similares. Para um jogo de mapa aberto, uma área maior que detecta a presença do personagem jogável pode ser responsável por uma troca de músicas.

Caso queira músicas adaptáveis a certas ações (por exemplo, um mesmo tema muda dependendo de onde você está no mapa, ou se você está segurando uma arma ou não), eu costumo criar um arquivo musical com o mesmo tempo e melodia, apenas com as harmonias diferentes, e fazer uma transição de um por outro por tempo passado, usando as funções da própria _engine_. Talvez outro método seja melhor para o seu caso.

Enfim, para músicas que acontecem "aleatoriamente", isso deve ser algo que você deve pensar por si próprio. Se ficam atreladas a um _timer_ global, ou se existe um _check_ de RNG a cada tantos minutos, ou se existem _triggers_ que causam que uma música comece.

### Efeitos sonoros
Para efeitos sonoros, a preocupação costuma ser outra. Efeitos sonoros vêm em vários tipos: sons atrelados a ações, sons atrelados a não-ações, sons atrelados ao ambiente, sons reativos do ambiente, entre outros.

No geral, minha abordagem para efeitos sonoros é a de que cada entidade responsável pelos sons faz a chamada à função responsável por tocar este som. Talvez, essa chamada seja executada no próprio script dessa entidade, talvez haja um gerenciador de sons global que fica responsável por cuidar disso. Independentemente, a chamada fica por parte da entidade geradora do som.

Por exemplo, cada ação do personagem jogável chama o seu som correspondente (ao tirar a espada da bainha, um som metálico soa, ao iniciar a animação de ataque, o personagem faz o "huh" atrelado ao seu ataque). Alguns sons serão reativos, estes podem ser atrelados ao objeto que recebe a ação ou ao objeto que pratica a ação (ao andar no chão de terra, um som soa, e ao andar num chão de mármore, outro; ou ao atacar uma rocha com uma espada, um som de colisão metálica soa, enquanto ao atacar uma grama, um som de corte soa).

A maneira mais simples de fazer com que os efeitos sonoros façam sentido no contexto de um jogo é atrelá-los diretamente a essas ações e reações. Seja uma colisão, seja uma ação, seja uma animação de ação ou _idle_, esta execução pode estar responsável por chamar a execução do áudio.

### Canais de áudio
Talvez você tenha um problema com diferentes ações afogando o sem de outras. Algumas _engines_ e ambientes vão te oferecer diferentes canais de áudio que podem acontecer simultaneamente. Separar diferentes tipos de sons para diferentes canais pode te ajudar a gerenciar volumes e quais áudios devem sobrepor os outros.

Por exemplo, a fala de um personagem deve ser mais alta que a música de fundo, para que os jogadores possam ouvi-lo. Da mesma forma, efeitos sonoros no geral devem ser mais altos que a BGM, já que sinalizam algo mais importante.

Outro caso é de ações repetitivas. Por exemplo, se eu posso atirar um laser várias vezes por segundo, é importante tomar cuidado de que o som não seja cortado para tocar novamente, e que este som não toque inúmeras vezes em um segundo, ao ponto que seja irreconhecível.

Isso dá trabalho, mas também é importante se assegurar de que todos os sons similares estão no mesmo volume geral. Sons de ação similares devem estar na mesma faixa de volume para mantera a coesão do mundo de seu jogo. Por exemplo, se o efeito sonoro para pulo é 3 vezes maior do que o efeito sonoro para o ataque, isso vai incomodar o seu jogador.

Às vezes, sons vão acontecer simultânameamente, e é importante reconhecer se um vai ser cancelado, ou se um vai se sobrepor ao outro, ou se simplesmente vão acontecer ao mesmo tempo.

Estes são os principais cuidados que você deve tomar com os sons de seu jogo. Esse processo é mais _chato_ do que _complicado_ em si. Lembre-se sempre de testar o jogo várias vezes para certificar-se de que os sons estão funcionando da maneira que deseja.

## Conclusão
