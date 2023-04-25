
# Capítulo 1: Design
"É perigoso ir sozinho! Leve isto." - Velho em uma caverna, "The Legend of Zelda" (1986)

![Capítulo 1 capa](https://i.imgur.com/GHZYcAZ.jpg "It's dangerous to go alone! Take this.")


A especificação de qualquer *software* é uma das etapas mais importantes no seu desenvolvimento.   
Jogos eletrônicos se encaixam também na categoria de _software_. Mas as mesmas regras se aplicam a eles?  

Mais ou menos. Apesar de serem _software_, existem detalhes sobre o desenvolvimento de jogos que os diferem de outros projetos de _software_. No entanto, a etapa da especificação não deixa de ser de extrema importância para os jogos.

Pode ser sua intenção começar a trabalhar na história, na arte, música ou programação do seu jogo imediatamente. E as chances são altas de que você já tem uma boa ideia do que fazer com pelo menos um desses. Mas enquanto eles são todos aspectos nos quais você e sua equipe vão trabalhar eventualmente, é importante dar forma a estas idealizações. Ou seja, colocar essas ideias "no papel" de alguma forma.

Qual é a importância real disso? Primeiramente, a organização. A diferença entre um projeto organizado que alcança sucesso e um que acaba cancelado muitas vezes está na etapa de formalização das ideias. Isso ocorre por vários motivos:

- Diferenças de visões criativas entre integrantes da equipe;
- Esquecimento de decisões e escolhas feitas anteriormente;
- Aumento constante do escopo do projeto;
- Falta de foco na manutenção do projeto;
- entre outros...

Estes problemas devem ser evitados para que o risco de cancelmaneto seja o menor possível. Por isso, a primeira coisa que fazemos é sempre documentar tudo o que planejamos realizar no projeto, para ter-se uma base sólida para consultar quando necessário. Você não precisa delimitar o seu projeto inteiramente no primeiro momento, e naturalmente acontecerão mudanças no decorrer do desenvolvimento. Mas é importante criar um documento que servirá para ancorar o seu projeto, pelo menos na fase inicial.

Além de ser um ótimo jeito de organizar e documentar suas ideias, manter um documento assim pode ser útil caso entre um novo membro na sua equipe, ou se precisar demonstrar suas ideias para um possível investidor em uma campanha de _crowdfunding_. Dessa forma, o documento deve conter a quantidade de detalhes que será relevante ao leitor. Nesse caso, também é interessante que inclua detalhes sobre o que será necessário na construção do jogo.

Entramos então no mérito do **design**. Você pode pensar no design como um planejamento, uma idealização, ou como uma especificação. Geralmente, no contexto de desenvolvimento de jogos, nós chamamos o documento de design pelo nome criativo "Game Design Document" (Documento de Design de Jogo).

## Game Design Document (GDD)

Não existe um padrão exato para como o GDD deve ser criado. E se você procurar online, você vai encontrar dúzias de padrões e templates diferentes. Na hora de delimitar o formato do seu documento, é importante considerar quem verá o documento e quanto tempo você quer passar detalhando-o. Pessoalmente, eu tento ser curto e objetivo nos meus, tentando passar o máximo de informação no menor espaço possível.

O seu GDD pode estar em qualquer lugar entre um documento simples de 3 ou 4 páginas, até um enorme documento extremamente detalhado como a [_Doom Bible_](https://5years.doomworld.com/doombible/doombible.pdf) (GDD do jogo Doom de 1993). Como o seu projeto acabou de começar, meu conselho é seguir a primeira opção. Porém, durante o desenvolvimento do seu projeto, é esperado que o documento cresça consideravalmente, então sinta-se à vontade para colocar quanto detalhe achar interessante no futuro.

Eu criei um template bem simples que costumo usar para a proposta inicial do jogo, e vou usá-lo aqui para exemplificar um preenchimento inicial. Se desejar usá-lo: 
- [Versão Word](/Arquivos/modelo_GDDv1.2.docx) 
- [Versão LibreOffice](/Arquivos/modelo_GDDv1.2.odt)

Se procura por inspiração, vários exemplos notáveis de GDDs podem ser encontrados no seguinte repositório no Github: [Awesome GDDs](https://github.com/Roobyx/awesome-game-design). Note que a maioria destes vão ser muito maiores e mais complexos do que a especificação do seu projeto. Isso é esperado.

Enquanto eu deixei várias notas no modelo do documento, achei relevante falar brevemente sobre cada campo aqui. Você pode encontrar o GDD inicial para os 2 projetos desenvolvidos em conjunto com o manual nos seguintes links: [Sleepy Runner], [Topdown Space Shooter]

### Conceito
A primeiro seção, "Conceito", tem o objetivo de explicar a ideia por trás do jogo de maneira simples e sucinta.  
O "título provisório" é exatamente o que o nome implica. Talvez te interesse incluir um título de projeto. Não se preocupe muito em decidi-lo, o título final do jogo em si pode ser decidido mais a frente no projeto.  
O "conceito inicial" é uma explicação de qual é a ideia geral para o jogo. Explique a ideia do jogo, e porque ela é interessante.  
"Gêneros" se refere a classificação do jogo: É um shooter como _Call of Duty_? Ou um jogo de plataforma como _Super Mario Odyssey_? Talvez seja um jogo de corrida, ou um _metroidvania_. Qual é o estilo da arte? O estilo da câmera? Pense em outros gêneros também.  
A intenção de "detalhes interessantes" é dar um destaque aos atributos únicos ou de maior interesse no seu jogo. Isso pode ser parte do que descreveu no conceito inicial.  
O "público alvo" é também bem óbvio. Para qual público este jogo é criado? Ou seja, que tipo de jogador você deseja interessar com seu projeto?

### Conceito Exemplificado 1
Título Provisório: Sleepy Runner  
Conceito Inicial: Um jogo sobre um pequeno espírito da névoa correndo através da terra. Sleepy foi forçado a vestir as botas dos pés inquietos, tornando-o incapaz de parar de correr. Este é um jogo onde o personagem corre automaticamente, e o jogador deve tocar na tela e interagir com diversos objetos para livrá-lo de todos os perigos em seu caminho.  
Gêneros: Plataforma, Puzzle, Autorunner, Sidescroller, Pixelart, Mobile  
Detalhes Interessantes: O jogo toma um formato diferente do habitual. Geralmente, jogos do gênero “autorunner” (corredor autmático) contêm mapas infinitos (endless runners), onde o jogador deve reagir a diferentes obstáculos escolhidos pseudo-aleatoriamente que vêm cada vez mais rápido (e.g. Subway Surfer, Temple Run, entre outros). A ideia desse jogo não é essa, nesse sentido, ele é mais parecido com um jogo puzzle, tendo fases curtas onde o jogador deve descobrir a melhor forma de alcançar determinado objetivo, controlando objetos da fase como plataformas e objetos do cenário.  
Público Alvo: O público-alvo são os jogadores de celular casuais. O jogo será simples e fácil de entender, com uma estética agradável.  

### Detalhes Técnicos
A segunda seção, "Detalhes Técnicos" se refere a vários aspectos que serão importantes durante a construção do jogo. Caso não saiba como responder um, não se preocupe, isso ficará melhor definido conforme seu projeto evoluir.  
A "plataforma" é, como o nome sugere, a plataforma onde seu jogo será executado. Podem ser computadores, celulares, navegadores, consoles de jogos, entre outros. E qualquer combinação destes. Lembre-se que fazer uma versão para um ambiente diferente (port) pode não ser um processo tão simples. Certas ferramentas e motores vão facilitar muito esse processo, para outros casos será impossível. O mesmo pode acontecer entre diferentes sistemas operacionais de computador. A plataforma em que deseja que seu jogo rode deve influenciar a escolha do ambiente de desenvolvimento.  
As "tencologias" estão intimamente relacionadas ao tópico anterior. Nós entraremos no mérito de como preencher esse tópico no capítulo seguinte. Porém, basicamente, se referem a o que você vai usar para criar o seu jogo. Por exemplo, motores como Unity, Unreal e Godot, ou _frameworks_ como Spritekit, Phaser e Starling. Talvez algo mais específico como RPG Maker, ou algo mais fácil de usar como o Game Maker. Qual linguagem será usada? Talvez javascript ou C++? Ou quem sabe usará uma ferramenta em que não há necessidade de programar em uma linguagem? Novamente, será mais interessante preencher isto no próximo capítulo, a não ser que já tenha alguma preferência.
A "interação" se refere às interfaces com as quais o seu jogador vai interagir com o jogo em si. Seja através de _touchscreen_, controles, mouses/teclados ou algum outro tipo de dispositivo de _input_. Também vale incluir situações especiais como controle por movimento/giroscópio. No caso de controles de console, é interessante incluir se existe vibração e outras reações do controle também.  
A "monetização" se refere a como você pretende ganhar dinheiro com o jogo. Se pretende vendê-lo como um jogo separado. Ou se será free 2 play com microstransações para diferentes personagens, cosméticos, etc. Quem sabe seu jogo é completamente grátis e não pretende ganhar dinheiro algum com ele? Qualquer que seja sua ideia, aqui é o lugar onde pode incluí-la.
As "ferramentas de desenvolvimento" são uma lista de ferramentas que serão utilizadas para a criação de recursos diversos como música, arte, modelos 3D, mapas, entre vários outros.

### Detalhes Técnicos Exeplificados 1

### Detalhes Conceituais
A terceira seção, "Detalhes Conceituais", começa a lidar com alguns aspectos mais abstratos, relacionados à narrativa. É possível que seu jogo não tenha um enredo, personagens ou um cenário específico. Por exemplo, um jogo _Candy Crush_ ou algo como Xadrez dificilmente vai ter uma história. Neste caso, pode pular os tópicos que achar desnecessários.
O "cenário" se refere ao mundo onde o jogo acontece. Deve ser descrito o tipo de ambiente onde a história aconteceria. Pode ser simplesmente descrito como um mundo _steampunk_ ou _cyberpunk_, ou um mundo fantástico, ou um mundo igual ao mundo real. Ou você pode dar mais detalhes. O importante é que um leitor potencial (e você mesmo) consiga imaginar o mundo onde a história do jogo acontece.  
Os "personagens" são os diversos personagens que aparecerão no seu jogo. Protagonistas, NPCs, inimigos, vilões todos podem ser considerados personagens. Caso tenha algum rascunho da aparência de cada um, seria interessante incluí-los aqui também. Mas isso pode ser feito mais adiante, caso ainda não tenha nenhum.  
O "enredo" se refere a história do jogo em si, a narrativa que será contada durante o decorrer do jogo. Não é necessário entrar em detalhes minuciosos sobre cada acontecimento no primeiro momento, mas, se preferir, pode ser feito. Lembre-se que durante o desenvolvimento você e seu time podem fazer várias decisões de mudança na história, então talvez poupe o seu tempo descrever de maneira bem simples até que o projeto esteja mais avançado. Criar uma _storyboard_ demonstrando a história eventualmente também deve estar nos seus planos, mas isso também pode esperar até que tenha um design definido para os personagens.  
O "contexto" engloba qualquer detalhe do enredo que não encaixe nos tópicos anteriores. Por exemplo, se isso é uma sequência, e o que ocorreu antes. Ou se existem acontecimentos paralelos que afetam a história do jogo, mas não são mostrados durante a narrativa.  
Os "temas" são palavras-chave que definirão o estilo do enredo que tem em mente.
O "formato da narrativa" se refere a como a história será contada. Serão _cutscenes_ cinematográficas, ou algo mais simples como caixas de diálogo, animações simples, etc.?

### Detalhes Conceituais Exemplificados 1

### Detalhes de Gameplay

### Detalhes Audiovisuais

### Objetos e Assets de Jogo

### Wishlist
