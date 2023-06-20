
# Capítulo 12: Level/World Design & Balancing
"Eu costumava ser um aventureiro como você. Aí eu levei uma flechada no joelho..." - Guarda da cidade, _Skyrim_ (2011)

![Capítulo 12 capa](../Arquivos/Imagens/capa_13.jpg 'I used to be an adventurer like you. Then I took an arrow in the knee...')

## Introdução
A maioria dos jogos tenta simular uma espécie de mundo ou ambiente onde as coisas acontecem. Esse mundo não precisa ser realista ou ter um formato específico, mas designers costumam usar algumas técnicas para manter seus mapas e mundos coerentes e divertidos. _Level desgin_ não é o meu forte, mas observando os jogos podemos tirar algumas conclusões.

## Formatos de Levels
O formato de seus mapas sempre será ditado pelo gênero/estilo do seu jogo. Mapas 3D costumam oferecer ambientes mais realistas, no sentido de que podem construir realmente o ambiente que querem representar. Enquanto mapas 2D oferecem uma representação ou aproximação desse ambiente. Eu posso modelar um quarto para um jogo 3D, enquanto em um jogo 2D eu teria que sacrificar uma dessas dimensões, seja o eixo de profundidade (mapas sidescroller) ou altura (mapas topdown). 

![3D Real, Spyro the Dragon - Reiginited Trilogy](../Arquivos/Imagens/12_01.png '3D Real, Spyro the Dragon - Reiginited Trilogy')

![2D Sidescroller Quarto](../Arquivos/Imagens/12_02.png '2D Sidescroller Quarto')

![2D Topdown Hotline Miami](../Arquivos/Imagens/12_03.png '2D Sidescroller Quarto')

Em certos casos, jogos 2D podem passar a ideia de um mundo tridimensional usando certos efeitos e ilusões, como é o caso com _Super Mario Kart_, muitos jogos do estilo topdown oblíquo como _Chrono Trigger_, e jogos isométricos como _Hades_ conseguem passar a ideia de um mundo 3D mesmo entre 2 dimensões. Alguns jogos ainda misturam os dois, como _Final Fantasy: Tactics_ com um mapa 3D e _sprites_ 2D.

![3D Fake, Super Mario Kart](../Arquivos/Imagens/12_05.jpg '3D Fake, Super Mario Kart')

![Topdown Oblíquo, Chrono Trigger](../Arquivos/Imagens/12_04.png '3D Fake, Super Mario Kart')

![3D Fake, Hades](../Arquivos/Imagens/12_06.jpg '3D Fake, Hades')

Deve ter ficado evidente que o estilo visual e o estilo de mapa estão intimamente ligados ao estilo do jogo em si. E por isso, você provavelmente já tem uma boa ideia de como irá montar seus mapas. Afinal, é muito difícil criar um jogo sem visualizar como seus mapas vão ser. Mas caso esteja na dúvida, procure jogos similares ao seu, tente entender os pros e cons de cada estilo de mapa, e como melhor encaixam para as mecânicas que deseja criar.

### Tipos de Level Design
O design para o seu mapa vai depender completamente do tipo de jogo que você está construindo. Se o seu jogo é baseado em fases sequenciais como _Super Mario_, seu _design_ será um. E se ele é um _metroidvania_ como _Symphony of the Night_ ou _Super Metroid_, seu _design_ terá de ser completamente diferente. Os tipos de _level design_ são inúmeros. Seja qual for o gênero principal do seu jogo, desde puzzles, plataformas, shooters, etc., o _design_ para seus mapas será influenciado por ele.

Por causa disso, o melhor jeito de entender o tipo de _level design_ que você procura é procurar diferentes jogos do mesmo gênero. Mesmo dentro de um gênero, é comum encontrar certa variedade, e você não precisa se prender às convenções de um gênero para criar seus mapas. Mas tente sempre entender o que funciona, e por que esses _designs_ funcionam, antes de começar a tentar subverter os estilos de mapas.

## Processo de _Level design_
Eu a aponto na introdução deste manual, mas existe uma ótima palestra no canal do GDC sobre [_level design_](https://www.youtube.com/watch?v=4RlpMhBKNr0). Enquanto isso se aplica mais a jogos 2D de plataforma, a filosofia do desenvolvedor de Celeste é um ótimo começo caso você não entenda muito sobre o assunto.

O meu processo no geral envolve:
- Pensar em um conceito ou ideia por trás da fase;
- Prototipar e testar a fase;
- Ajustar até que fique divertida e desafiadora o suficiente.

Novamente, esse é um processo simples para jogos 2D. Em jogos 3D, você terá que pensar espacialmente para projetar o mapa, e tentar criar ambientes que façam mais sentido do que os nos contextos 2D. Essa preocupação com manter a coerência com o mundo real é algo que depende também do estilo do seu jogo. 

Enquanto jogos como os da série _Hitman_, por exemplo, se beneficiam principalmente em projetar mapas baseados ambientes reais como hotéis, teatros, aeroportos, etc. Grande parte dos jogos 3D tentam manter um equilíbrio entre criar um mapa que representa o mundo real corretamente, e criar um mapa que complemente as mecânicas do jogo. 

Certos jogos sequer dão ênfase a isso, priorizando o _gameplay_ primeiro. E na maioria dos casos, o jogador **não** espera um nível tão grande de fidelidade ao mundo real de um jogo, a não ser que isso seja um ponto focal do _marketing_ do jogo. Por isso, o formato para os mapas fica a critério do desenvolvedor. O mais importante é que o mapa faça sentido dentro do contexto do mundo do jogo, respeitando as regras do _worldbuilding_ e sempre priorizando a lógica interna.

## Ferramentas
Para começar com o _level design_, o bom e velho **papel e caneta** já vai servir de muito. Existem ferramentas mais sofisticadas, mas o importante é desenhar os seus mapas de alguma forma, com plataformas e/ou pontos de referência, e quaisquer anotações que julgar necessárias.

Pessoalmente, gosto muito de usar a ferramenta [draw.io](https://www.drawio.com/) para montar o _design_ inicial dos meus mapas. Apesar de ser bem básica, ela é perfeita para montar diagramas diversos.

Caso já tenha uma ideia geral de como será seu mapa, ferramentas como o [Tiled](https://www.mapeditor.org/) e o [LDtk](https://ldtk.io/) são ótimos para prototipar diferentes versões do mapa e importá-las direto na sua _engine_. Algumas _engines_ vão oferecer seus próprios editores de mapas também, mas não se deve contar com isso para qualquer _engine_.

Prototipar mapas 3D é um processo um pouco mais complexo, não é possível montar um mapa simples com _tiles_. Para estes casos, trabalhar com primitivas e objetos 3D simples (sem texturas) no [Blender](https://www.blender.org/) é uma boa opção. Novamente, algumas _engines_ vão permitir que você crie objetos 3Ds simples e faça todo o processo de prototipação nela mesma, antes de montar os modelos para o mapa real.

## Conclusão
Durante esse capítulo, discuto brevemente o mérito do _level design_ e algumas ferramentas que podem ser úteis para um desenvolvedor tentando projetar fases.

No [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo13.md), discutiremos sobre as versões _beta_, a reta final para o seu projeto.
