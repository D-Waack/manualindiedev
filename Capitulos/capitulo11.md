
# Capítulo 11: Integrando Recursos Audiovisuais
"Mas o futuro se recusou a mudar." - "_Chrono Trigger_" (1995)

![Capítulo 11 capa](../Arquivos/Imagens/capa_11.jpg 'But the future refused to change.')

## Introdução
Pouco adianta criar recursos como _sprites_, modelos e temas musicais se você não souber como incluí-los em seu jogo. Esse capítulo vai discutir um pouco sobre técnicas para incluí-los e o que fazer com cada um deles.

## Recursos Visuais
Recursos visuais são extremamente importantes, mas também vêm em várias formas diferentes. Aqui, é importante fazer uma distinção entre recursos 2D, 3D e outros diversos formatos.

### Recursos 2D - Planos e camadas

### Recursos 2D - Sprites e camada principal

### Recursos 2D - Planos de fundo e camadas secundárias

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
