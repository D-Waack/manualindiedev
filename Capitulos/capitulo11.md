
# Capítulo 11: Integrando Recursos Audiovisuais
"Mas o futuro se recusou a mudar." - "_Chrono Trigger_" (1995)

![Capítulo 11 capa](../Arquivos/Imagens/capa_11.jpg 'But the future refused to change.')

## Introdução
Pouco adianta criar recursos como _sprites_, modelos e temas musicais se você não souber como incluí-los em seu jogo. Esse capítulo vai discutir brevemente sobre algumas particularidades da inclusão de cada um deles.

## Recursos Visuais
Recursos visuais vêm em vários formatos, e cada formato diferente vai influenciar no jeito que ele será integrado ao jogo.

### Recursos 2D - Planos e camadas
Em grande parte, jogos 2D são visualmente compostos de várias camadas visuais diferentes, uma "por cima" da outra. Você pode criar um jogo 2D em uma única camada visual, mas perderia a oportunidade de criar diversos efeitos interessantes. Em um jogo _sidescroller_, isso pode vir como diferentes camadas de objetos, um plano de fundo, e a camada principal onde existem os personagens. Em um jogo _topdown_ ou isométrico, nem sempre encontramos camadas de fundo, mas ainda assim temos a camada do mapa e pelo menos mais uma principal para os objetos e personagens.

O formato técnico de como essas camadas são mostradas em tela pouco importa para o nosso contexto. O que importa é a ordem de renderização, e as colisões. Cabe ao desenvolvedor montar essa ordem na hora da criação da cena no jogo. Porém, isso é um processo bem intuitivo.

Normalmente, encontramos a seguinte ordem: 
- Planos sem interação: plano de fundo (principal) -> objetos do plano de fundo (distantes) -> objetos no plano principal (próximos)
- Planos com interação (sidescroller): mapa (chão) -> objetos de cenário (interativos) -> personagens
- Planos com interação (topdown): mapa (chão) -> personagens -> objetos de cenário

Isso deve estar óbvio, mas a seta indica que o próximo objeto virá **à frente** do objeto anterior. Para jogos sidescroller, ter todas as 3 camadas que mencionei como uma só também é possível, ou apenas uma camada para objetos e mapa, com personagens no topo. 

Nem todos os projetos terão todas estas camadas, e alguns podem ter mais, mas no geral, seguir esse tipo de ordem costuma ser o caminho mais adequado.

### Recursos 2D - Colisões: camadas de objetos
As camadas de colisão principais para o funcionamento do seu jogo são as camadas de mapa, objetos e personagens.

Para jogos no estilo _sidescroller_ e similares, o **mapa em si** deve ser um objeto real com colisões. Afinal, se o seu personagem é afetado pela gravidade, ele precisa de um chão para impedir que caia infinitamente. Para mapas feitos com _tiles_ quadrados, costuma ser bem simples atribuir uma colisão quadrada diretamente a cada _tile_. A maioria das _engines_ permite isso, e programas como o _tiled_ e o _LDTK_ também oferecem a possibilidade de criação de mapas que já exportam com a colisão pronta para importação em uma _engine_ ou _framework_.

Para mapas que não são montados com _tiles_, como é o caso do jogo Hollow Knight, é possível simplesmente criar colisões para eles manualmente. A mesma coisa também é possível com mapas de _tiles_, mas isso costuma ser um trabalho desnecessário. No meu projeto, tentei usar um pouco dos dois. 

Para mapas no estilo _topdown_ e similares, o mapa em si (o chão) não precisa ter colisões. A não ser em casos onde haja algum tipo de evento causado por andar no mapa. Mapas que contém buracos ou quedas vão conter colisões apenas em pontos onde existe essa queda, ou nos cantos. Ou ainda, terão colisões em áreas que não são acessíveis, como uma parede mais alta, ou uma área com água. O motivo pelo qual o chão navegável não costuma ter colisões é porque isso causaria conflitos com o movimento dos personagens. 

Objetos como pilares, árvores, alavancas, ou qualquer objeto de cenário vêm por cima da camada do chão, e estes costumam vir com colisões. Para um mapa sidescroller, o objeto interativo não _precisa_ ter uma colisão, até porque certos objetos vão causar com que o personagem jogável não consiga avançar no mapa. Ainda certos objetos vão conter apenas uma colisão que interage com a arma do jogador (por exemplo, objetos de cenário quebráveis). Certos objetos vão ter colisões apenas em certas situações. E é claro, se o objetivo do objeto é bloquear a passagem do personagem, é esperado que tenham colisão.

Para jogos no estilo _topdown_, objetos de cenário sempre terão colisões. Porém, estes jogos tentam criar uma ilusão de 3D, e é interessante que contenham colisões somente na sua "base". Ou seja, o topo destes objetos costumam não conter colisões. Nesses casos, é interessante tentar criar um objeto em uma camada _acima_ do jogador (mais à frente), para que o mesmo não apareça no topo deste erroneamente.

![Exemplos Colisão Topdown](../Arquivos/Imagens/11_01.png 'Exemplos Colisão Topdown')

Colisões para objetos costumam ser _retângulos_ simples que englobam o objeto completamente. Para objetos redondos, talvez um círculo seja mais adequado. Para grande parte dos jogos, colisões simples assim costumam ser o mais adequado. Manter colisões com formatos primitivos também simplifica os cálculos de física, permitindo com que seu jogo execute melhor. Porém, em certos casos, colisões primitivas não vão ser boas o suficiente, e criar um polígono manualmente se mostra necessário. Tente evitar isso ao máximo, mas lembre-se que é uma opção.

![Exemplos Colisão Sidescroller](../Arquivos/Imagens/11_02.png 'Exemplos Colisão Sidescroller')

### Recursos 2D - Colisões: camadas de personagens
As camadas de personagens são as mais simples. Geralmente, sprites de personagens ficam no topo, como a camada mais aparente (com exceção de casos onde existem objetos que devem aparecer à frente destes). Em termos de colisões, costumamos seguir com o mesmo formato para objetos diversos. A colisão é um retângulo que engloba o personagem completa ou parcialmente. 

Em outros casos, um formato circular ou de cápsula pode ser bom também. Isso costuma ser útil para jogos _topdown_, onde o formato arredondado impede que o personagem interaja de maneira estranha com cantos (existem outros meios de evitar essa estranheza). Para jogos _sidescroller_ retângulos costumam ser o melhor formato para personagens que interagem com o chão.

Geralmente é esperado que, para personagens, a colisão os englobe completa, ou quase completamente. Mas nem sempre isso é o caso, ou a melhor opção. É importante certificar-se de que as caixas de colisão _interagem_ com a colisão dos mapas e objetos. Em algumas _engines_, colisões são todas na mesma camada por padrão, mas na maioria dos casos você pode mudar manualmente quais camadas colidem com quais, e isso permite várias interações interessantes, mas exige cuidado para que as interações corretas aconteçam.

### Recursos 2D - Colisões vs Hitboxes
Um outro detalhe importante para personagens são as colisões de dano (ou o que chamamos de hitboxes e hurtboxes). Costumamos assumir que a área de dano de um personagem é a mesma que colide com o ambiente. Enquanto isso é verdade em alguns casos, na maioria deles não é.

![Exemplo Hitbox Touhou](../Arquivos/Imagens/11_03.png 'Exemplo Hitbox Touhou')

Uma _hitbox_ se refere a essa área de colisão responsável por registrar _dano_. Em alguns casos, o termo _hurtbox_ é usado para se referir a uma área responsável por **receber** dano, e _hitbox_ apenas para a área responsável por **realizar** dano. Eu usarei esses termos por questões de simplicidade, mas geralmente _hitbox_ se refere a ambos.

Hitboxes e Hurtboxes devem ser adaptadas ao contexto que se encontram. Geralmente, é comum criarmos uma hurtbox menor que a colisão para o player, e analogamente uma hurtbox maior que a colisão para inimigos. Isto deixa as coisas um pouquinho injustas, de modo que o jogo fica mais fácil. Mas essa inclinação para facilitar o jogo, quando aplicada, costuma passar despercebida pelo jogador. Da mesma forma, jogadores costumam se incomodar quando a mesma não é aplicada.

No Godot, eu costumo criar hitboxes e hurtboxes como nós do tipo Area2D, para que eles não interajam fisicamente com objetos do cenário, e apenas reajam a outras hitboxes e hurtboxes. Essa é uma abordagem interessante, caso seja possível executá-la no seu ambiente de escolha.

No geral, hitboxes e hurtboxes vão ser projetadas caso a caso. Por exemplo, uma forma de implementar o jogo _Super Mario Bros_, poderia ser criar o Mario com uma hitbox somente no fundo de seus pés, enquanto o resto de seu corpo é uma hurtbox. Porém, quando o Mario coleta uma estrela, sua hurtbox é desativada e todo o seu corpo se torna uma hitbox. Da mesma forma, a hitbox dos inimigos é o corpo inteiro deles, e a hurtbox também.

Em um jogo como _Castlevania_, a hitbox do jogador é composta somente da arma do personagem (um chicote, uma espada, ou um projétil). Enquanto a hurtbox do jogador é sempre a mesma, composta de seu corpo inteiro.

### Recursos 2D - Planos de fundo e camadas secundárias
Enquanto não existe preocupação de colisões para planos de fundo em 2D, existem alguns detalhes interessantes. Isso se aplica principalmente a jogos do estilo _sidescroller_. Jogos _topdown_ em sua maioria não contêm planos de fundo complexos.

Em muitos casos, jogos _sidescroller_ vão ter fundos de paisagens distantes. Neles, existe uma técnica de arrasto do fundo chamada _parallax scrolling_. Esta técnica consiste de fazer com que, junto ao movimento da câmera, diferentes camadas do plano de fundo se arrastem em velocidades diferentes, de maneira a dar a impressão de um movimento mais realista.

Algumas _engines_ oferecem isso por padrão, em outras, esse cálculo deve ser feito manualmente.

### Recursos 2D - Animações
O tratamento de animações pode ser feito de várias formas dependendo do seu ambiente. 

Para um _tile_ animado (por exemplo de um rio) que funciona sozinho, simplesmente soltar um _gif_ no seu projeto pode ser a solução perfeita. 

Para personagens, inimigos, objetos animados, etc., você precisará atrelar essas animações às ações do personagem de alguma forma através de um script. Para _sprites_, o método mais comum é criar um _spritesheet_, um arquivo de imagem com a sequência de todas as variações do sprite igualmente espeçadas. Estas variações se tornam os frames da animação.

![Exemplo Spritesheet Momodora](../Arquivos/Imagens/11_04.png 'Exemplo Spritesheet Momodora')

Geralmente, _engines_ vão oferecer algum recurso que permita que você crie animações e as inicie/pare pelo código, como é o caso do "AnimationPlayer" no Godot. Para _frameworks_, é mais comum que você tenha que ditar os frames da animação e o _timing_ manualmente. De qualquer forma, a animação de personagens vai ser sempre um comando atrelado a alguma ação ou verbo (correr, pular, cair, parar, atacar, etc.). Além destes, existem também as animações _idle_, que são animações executadas enquanto nenhuma ação é tomada.

### Recursos 2D/3D - Efeitos: partículas e shaders
Além de _sprites_, _tiles_ e outros recursos que podem ser criados manualmente, temos opções de diversos efeitos para melhorar o visual dos jogos.

Estes costumam ser criados/calculados em tempo de execução, shaders e partículas. Partículas são pequenas texturas ou objetos geométricos que são emitidos a partir de um ou vários pontos para dar a impressão de algum fenômeno como fumaça, fogo, eletricidade, etc. Shaders funcionam como "filtros" que alteram os pixels disponíveis na tela em tempo real, podendo mudar completamente a impressão de toda a tela, ou de um pedaço dela, criando efeitos visuais diversos. 

![Exemplos Partículas](../Arquivos/Imagens/11_05.jpg 'Exemplos Partículas')

![Exemplos Shaders](../Arquivos/Imagens/11_06.jpg 'Exemplos Shaders')

Enquanto partículas são objetos visuais reais, e shaders são apenas alterações calculadas pela GPU, ambos requerem uma certa capacidade de processamento maior do que meros objetos como sprites em tela.

### Recursos 3D - Modelos e texturas
Quando se tratando de objetos 3D, atrelá-los ao seu jogo é uma ação mais "simples" do que o trabalho com elementos 2D. Primeiramente, a maioria das _engines_ vai permitir que importe seu modelo diretamente com a textura sem dificuldade alguma. Algumas vão exigir um formato específico, mas estes são sempre formatos de fácil exportação a partir de programas de modelagem. Algumas engines vão exigir um trabalho extra da ligar sua textura manualmente ao modelo, mas isso também costuma ser automatizado. 

É preferível já exportar o modelo pronto com as texturas necessárias, pois isso costuma evitar problemas do lado da _engine_ como mapeamento incorreto de texturas. Enquanto isso pode ser consertado na própria engine, é mais fácil fazer uma única importação completa.

### Recursos 3D - Modelos e colisões
Da mesma forma que é necessário criar uma colisão para personagens e objetos em jogos 2D, também costuma ser necessário criar colisões para objetos 3D. Em termos de hitboxes e hurtboxes, as regras que se aplicam para os objetos 2D também se aplicam aqui. Ter uma hitbox menor no seu player, e uma maior nos inimigos costuma ser uma boa solução.

Agora, em termos puramente de colisão de objetos, o costume para personagens e modelos é um pouco mais complexo. Geralmente, as _engines_ vão permitir que você crie um objeto de colisão a partir do modelo. Porém, modelos geralmente têm geometria complexa e de difícil cálculo, e criar uma colisão assim para todos os modelos em seu jogo é um ótimo jeito de deixar a execução dele bem lenta. É claro, isso depende também da quantidade de objetos, se eles são atualizados a cada frame ou não, e o processamento do computador. 

Entretanto, no geral é preferível utilizar primitivas para as colisões de objetos diversos (especialmente os que se movem), a não ser que o formato do objeto seja importante para a execução do jogo de alguma forma. Por exemplo, as montanhas no _Breath of the Wild_ precisam ter suas colisões perfeitamente alinhadas porque o personagem vai escalá-las e interagir com elas diretamente.

Para personagens jogáveis e inimigos, costumamos usar o formato de uma cápsula para suas colisões, pois é o formato que melhor interage com diferenças de altitude, rampas e afins.

### Recursos 3D - Skyboxes, iluminação, efeitos e shaders
A preocupação com fundos e camadas distintas não existe exatamente para jogos 3D. Até porque todos os seus objetos existirão no espaço, como na vida real. Se você quiser que montanhas existam no horizonte, você pode modelá-las (preferivelmente uma versão low poly para objetos distantes). Seu "plano de fundo" será na verdade uma _skybox_, que é basicamente um fundo para ambientes 3D, envolvendo as fronteiras do mapa carregado.

Visualmente, sua cena será montada pelos objetos que incluir nelas. Porém, alguns outros objetos podem ajudar a melhorar o formato do seu ambiente, como luzes criadas na _engine_, criando efeitos de iluminação diversos. Além disso, _shaders_ e partículas também existem em jogos 3D e podem ser usados com resultados melhores que suas versões 2D.

### Recursos Gerais - HUDs e interfaces
A sigla HUD (heads up interface) se refere ao pedaço da interface/tela que fica entre o mundo simulado e o jogador. Geralmente, mostra informações essenciais para os jogadores como barras de vida, contagem de vidas, munição, itens coletados, tempo restante, e quaisquer outros detalhes que o desenvolvedor julga importantes para o jogador.

A implementação de um HUD é simples, basta incluir uma camada visual bidimensional mais externa a todo o resto do jogo. É necessário tomar cuidado para que a informação do HUD não obstrua a visão do jogador. Por esse motivo, HUDs geralmente se limitam ao topo e fundo da tela. De forma a não atrapalharem o jogo, mas ainda exibirem as informações necessárias para o jogador.

Em certos casos, é interessante encontrar outros jeitos de mostrar informação ao jogador, como fiz no meu projeto _Vortex Tautology_, onde a vida do personagem é demonstrada pela cor/presença do escudo. Ou em um jogo como Dead Space, onde informações importantes são demonstradas no próprio personagem jogável e objetos no próprio jogo. Esse tipo de detalhe sempre é apreciado quando feito da maneira correta.

![Display de informações em Dead Space](../Arquivos/Imagens/11_07.png 'Display de informações em Dead Space')

Em termos de interfaces gerais, como menus e inventários, simplesmente montá-los como uma tela interativa com o mouse é o suficiente. Na maioria dos casos, também é interessante adicionar certa redundância a comandos interativos em menus, como setas de teclado para escolher opções, várias teclas para confirmação, usabilidade de controle, etc. Sempre lembrando de ter bom senso, pouco ainda ter opções diversas para um jogo de celular com o qual o jogador vai interagir apenas por toque.

## Recursos Sonoros
Recursos sonoros são mais simples para inclusão do que os visuais, mas requerem alguns cuidados únicos.

### Música de fundo
Em questões de música, a abordagem principal é atrelar uma música a um _local_, uma _fase_, ou um _evento_. Nem todos os jogos seguem essa ideia. Alguns jogos como _The Legend of Zelda: Breath of the Wild_ vão oferecer música somente em _cutscenes_, e outras músicas atmosféricas aleatoriamente durante o decorrer do jogo. Alguns jogos como _Nier: Automata_ vão oferecer variações da mesma música para momentos diferentes em uma área (citaria um exemplo, mas não quero dar nenhum _spoiler_ da história do jogo).

Dessa forma, sua preocupação primária com a música é decidir quando e onde ela tocará. Para um _approach_ de áreas, isso costuma ser bem fácil. Qualquer que seja o _script_ responsável pela manutenção dessa área pode iniciar a música na inicialização desse próprio _script_. Ou ainda outro _approach_ é ter um gerenciador de músicas global que checa ou reage a uma mudança de área e troca a música quando necessário. A primeira opção é geralmente a mais simples, mas cada uma tem suas vantagens.

Esse mesmo conceito pode ser aplicado para _cutscenes_ e outros eventos similares. Para um jogo de mapa aberto, uma área maior que detecta a presença do personagem jogável pode ser responsável por uma troca de músicas.

Caso queira músicas adaptáveis a certas ações (por exemplo, um mesmo tema muda dependendo de onde você está no mapa, ou se você está segurando uma arma ou não), eu costumo criar um arquivo musical com o mesmo tempo e melodia, apenas com as harmonias diferentes, e fazer uma transição de um por outro respeitando o tempo passado, usando as funções da própria _engine_. Talvez outro método seja melhor para o seu caso.

Enfim, para músicas que acontecem "aleatoriamente", isso é algo que você terá que bolar por si. Se ficam atreladas a um _timer_ global, ou se existe um _check_ de RNG a cada tantos minutos, ou se existem _triggers_ que causam que uma música comece.

### Efeitos sonoros
Para efeitos sonoros, a preocupação costuma ser outra. Efeitos sonoros vêm em vários tipos: sons atrelados a ações, sons atrelados a não-ações, sons atrelados ao ambiente, sons reativos do ambiente, entre outros.

No geral, minha abordagem para efeitos sonoros é a de que cada entidade responsável pelos sons faz a chamada à função responsável por tocar este som. Talvez essa chamada seja executada no próprio script dessa entidade, talvez haja um gerenciador de sons global que fica responsável por cuidar disso. Independentemente, a chamada fica por parte da entidade geradora do som.

Por exemplo, cada ação do personagem jogável chama o seu som correspondente (ao tirar a espada da bainha, um som metálico soa, ao iniciar a animação de ataque, o personagem faz o "huh" atrelado ao seu ataque). Alguns sons serão reativos, estes podem ser atrelados ao objeto que recebe a ação ou ao objeto que pratica a ação (ao andar no chão de terra, um som soa, e ao andar num chão de mármore, outro; ou ao atacar uma rocha com uma espada, um som de colisão metálica soa, enquanto ao atacar uma grama, um som de corte soa).

A maneira mais simples de fazer com que os efeitos sonoros façam sentido no contexto de um jogo é atrelá-los diretamente a essas ações e reações. Seja uma colisão, seja um input, seja uma animação de ação ou _idle_, esta execução pode estar responsável por chamar a execução do áudio.

### Canais de áudio
Talvez você tenha um problema com diferentes ações afogando o sem de outras. Algumas _engines_ e ambientes vão te oferecer diferentes canais de áudio que podem acontecer simultaneamente. Separar diferentes tipos de sons para diferentes canais pode te ajudar a gerenciar volumes e quais áudios devem sobrepor os outros.

Por exemplo, a fala de um personagem deve ser mais alta que a música de fundo, para que os jogadores possam ouvi-lo. Da mesma forma, efeitos sonoros no geral devem ser mais altos que a BGM, já que sinalizam algo mais importante.

Outro caso é de ações repetitivas. Por exemplo, se eu posso atirar um laser várias vezes por segundo, é importante tomar cuidado de que o som não seja cortado para tocar novamente, e que este som não toque inúmeras vezes em um segundo, ao ponto que se torne irreconhecível.

Isso dá trabalho, mas também é importante se assegurar de que todos os sons similares estão no mesmo volume geral. Sons de ação similares devem estar na mesma faixa de volume para manter a coesão do mundo de seu jogo. Por exemplo, se o efeito sonoro para pulo é 3 vezes mais alto do que o efeito sonoro para o ataque, isso vai incomodar o seu jogador.

Às vezes, sons vão acontecer simultânameamente, e é importante reconhecer se um vai ser cancelado, ou se um vai se sobrepor ao outro, ou se simplesmente vão acontecer ao mesmo tempo.

Estes são os principais cuidados que você deve tomar com os sons de seu jogo. Esse processo é mais _chato_ do que _complicado_ em si. O bom senso será o seu principal guia para melhorar os sons de seu jogo. Lembre-se sempre de testar o jogo várias vezes para certificar-se de que todos estão funcionando da maneira que deseja.

## Conclusão
Neste capítulo discutimos diversas formas como artefatos audiovisuais podem ser integrados a um jogo, e vários cuidados que devem ser tomados durante esse processo.

No [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo12.md), falarei um pouco sobre _level_ e _world design_.
