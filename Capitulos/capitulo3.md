
# Capítulo 3: O Ciclo de Desenvolvimento
"Eu já te contei a definição de insanidade?" - Vaas Montenegro, _Far Cry 3_ (2012)

![Capítulo 3 capa](../Arquivos/Imagens/capa_03.jpg 'Have I ever told you the definition of insanity?')

## Introdução

Se tudo deu certo durante o [capítulo interior](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo2.md), você escolheu qual será sua _engine_ e já tem certa noção de como organizará seus arquivos. Nesse caso, você já está pronto para começar o desenvolvimento de seu jogo.

Geralmente, definimos o ciclo de vida para o desenvolvimento de um jogo da seguinte forma: **Pré-Produção** -> **Produção (Alfa)** -> **Produção (Beta)** -> **Produto Final**

Seguindo esta classificação, você teria passado pela etapa de pré-produção. A pré-produção na indústria como um todo geralmente é um processo mais formal do que o que descrevi aqui. Isso não será um problema. Em muitos casos, um pequeno protótipo é projetado também durante a pré-produção. Decidi incluir isto na etapa de produção, por questões de simplicidade.

A partir de agora, você e sua equipe entrarão no que eu chamo de ciclos de desenvolvimento. Outros vão chamá-los de _sprints_. Você pode usar um nome diferente também se preferir. O que importa é o conceito e execução. Essa nomenclatura é emprestada do Scrum, um _framework_ para a criação de projetos de _software_. 

Não vamos nos apegar muito à estrutura do Scrum em si. E a maioria das fontes sugere que o padrão na indústria é utilizar uma espécie de Scrum adaptado ao contexto de jogos. O que interessa para o nosso caso é a organização, reflexão, o próprio ciclo de trabalho, e como ele será avaliado. A princípio, o que você vai definir é simples:

- A divisão das tarefas;
- O ritmo de trabalho.

Vamos falar um pouco melhor destes em seguida.

### Divisão de tarefas 

Se seu projeto é solo, decidir isso vai ser bem fácil. Torna-se apenas uma questão de prioridades. E, para essse caso, existe um caminho ideal que vou discutir mais a frente. Porém, se você trabalha em um grupo, as coisas ficam um pouco mais complexas.

Uma ótima coisa quando trabalhando em grupo é que várias pessoas podem trabalhar em diferentes frentes ao mesmo tempo. Porém, isso vai gerar maior trabalho organizacional, porque nem todas as competências devem ser desenvolvidas no mesmo ritmo.

Por exemplo, se sua equipe tem 2 programadores, ambos podem facilmente trabalhar em diferentes aspectos de seu jogo. Digamos, um trabalha no movimento do personagem e o outro trabalha no funcionamento dos menus principais. Da mesma forma, se a equipe tem 2 artistas, um pode trabalhar no _design_ de um personagem, enquanto o outro trabalha em fundos, ou em outro personagem. O mesmo se aplica a músicos, _level designers_, e a lista segue.

No entanto, os trabalhos do programador e do artista não seguem o mesmo ritmo. E, em certos casos, um depende de um resultado do outro. Por exemplo, implementar uma certa ação como puxar uma alvanca no jogo _Tomb Raider_ precisaria que os animadores tivessem completado a animação de puxar a alavanca. Esses animadores precisaram esperar que os modeladores tivessem completado o modelo de Lara Croft. E esses modeladores precisaram usar a _concept art_ do time de arte para criar o modelo e suas texturas.

![Lara Croft Alavanca](../Arquivos/Imagens/03_01.jpg 'Lara Croft e a alavanca')

(Isso é apenas um exemplo ilustrativo. Na prática, é possível que os desenvolvedores implementem todas as funções relacionadas à alavanca antes que as animações sejam criadas, e voltem para incluí-las mais à frente no desenvolvimento.)

O trabalho do gerente do time é certificar-se de que um membro não vai atrasar o outro, e tentar evitar retrabalhos ao máximo possível. Quanto menor o seu time, mais fácil é organizar isso, mas isso também quer dizer um ritmo de trabalho menor.

### Ritmo de trabalho

Os ciclos de desenvolvimento estarão atrelados a um **período de tempo** específico.

A ideia por trás do Scrum é de dividir o seu projeto em partes menores, cada uma sendo implementada em um período delimitado pela equipe (geralmente de 2-4 semanas). Dessa forma, o processo de produção fica mais simples e organizado. Por exemplo, eu não "trabalho no jogo", mas sim "termino o sistema de dano e _knockback_". 

Isso implica em algumas coisas para você e sua equipe: Vocês terão metas a cumprir (onde podem ter sucesso ou não); terão metas a decidir; e devem refletir sobre o resultado encontrado ao final de cada ciclo.

Existe flexibilidade no tamanho destes ciclos, e quanto é feito em cada um. Isso é importante que decidam. Pessoalmente, para projetos pequenos eu costumo trabalhar com ciclos de 1 semana. Talvez para você seja melhor 2 semanas. Para o contexto _indie_, eu não recomendo nada muito maior que isso a não ser que sua equipe não tenha muito tempo para trabalhar no projeto. 

## O Ciclo

Entendendo o conceito de ciclo, resta executá-los. Os passos são simples: Planejar o ciclo, executá-lo, concluí-lo, testar os resultados.

### 1. Planejar o ciclo

Você e sua equipe (ou apenas você) discutirão quais aspectos do jogo serão mais importantes/interessantes criar por ora. Membros diferentes podem trabalhar em frentes diferentes ao mesmo tempo. 

Na teoria, um líder competente seria capaz de dirigir o jogo sozinho, sem que as diferentes competências dialogassem entre si. Por exemplo, o time de modelagem e CG não precisa saber o que o time de implementação anda fazendo. Entretanto, para projetos _indie_ isso se mostra não só difícil, mas uma opção ruim.

Quanto mais diálogo houver entre os integrantes, mais eles podem contribuir uns com os outros, e apoiarem-se entre si. O líder deve estimular diálogo entre os membros de forma que todos saibam o progresso entre eles, e não haja surpresas mais a frente.

A delimitação do ciclo pode ser feita através de uma reunião pessoal, uma chamada de vídeo, ou mensagens de texto. É preferível que possam se comunicar por voz, pois isso ajuda a fluir a discussão. Isso deve ser decidido logo no início do ciclo, ou no final do anterior.

Lembrando sempre que a opinião que deve pesar mais para cada aspecto é a dos especialistas para esse aspecto, mas que as opiniões do resto da equipe são de importância também. Enquanto, por exemplo, o programador pode não saber tanto de arte, seu _input_ sobre o processo pode ser muito útil para o artista. Isso também é importante porque mais a frente no projeto você terá de unir todos estes aspectos diferentes.

Outra coisa importante é manter em mente o ritmo de trabalho de cada pessoa. Alguns membros vão ter mais tempo e terminar seu trabalho antes de outros, outros vão ter imprevistos e gerar atrasos. Como você vai lidar com estes aspectos fica ao critério seu e de sua equipe. Se vai dar mais trabalho para um para agilizar o processo, ou se vai pedir que um membro complemente onde outro faltar. Não existe uma resposta certa, isso apenas deve ser considerado durante o desenvolvimento.

Caso você trabalhe sozinho, discutir consigo mesmo é uma opção, mas debater essas ideias com amigos que também se interessam por jogos é uma ótima opção. Talvez não para discutir minúcias do desenvolvimento, mas trocar ideias com outras pessoas sempre é proveitoso para organização de suas ideias.

Durante a discussão sobre as tarefas, podem surgir ideias que não serão executadas durante este ciclo, ou sugestões que ainda não precisam ser consideradas. **Anote-as** na _wishlist_ do seu GDD.

Além disso, você vai decidir o que será feito durante o ciclo em si. **Anote isso também**, em um documento separado do GDD. Uma simples lista deve servir. Para essa lista, vamos usar outro termo emprestado, o _backlog_.

### 1.1 Sobre as Metas

Se você delimitar um trabalho muito complexo para um tempo muito curto, o mesmo provavelmente não será terminado. Isso é normal e esperado, mas pode gerar certo estresse para a sua equipe. Dessa forma, ficam algumas dicas para delimitar os seus ciclos:

- Objetivos específicos

 Quanto menos ambiguidade no que foi planejado, mais fácil é entender e executar cada tarefa.
 
- Objetivos simples

 Você não precisa descrever o ciclo inteiro em uma única palavra. Pode dividi-lo em pedaços menores. Por exemplo, "sistema de física" pode ser dividido em "movimento e colisão", e movimento pode ser dividido em "input, velocidade, gravidade". Velocidade ainda pode ser dividido em "aceleração e fricção". Onde vocês vão parar de dividir fica a preferência de cada um, e muitas vezes a melhor opção depende do caso, mas dividir o trabalho em pedaços menores costuma ser mais fácil. Além disso, caso não consigam desenvolver todos os detalhes durante o ciclo, o trabalho que já foi feito e o que falta fica mais claro.
 
- Quando na dúvida, objetivos gerais, mas não vagos

 Em certos casos, as opções acima não serão possíveis, pois você e sua equipe não entendem o escopo da próxima tarefa. Por exemplo, na primeira vez que você criar um sistema de física, você não vai saber como dividi-lo em aspectos mais simples. Nesse caso, delimitar estes diferentes aspectos pode ser parte do objetivo. Se a sua equipe é inexperiente, "pesquisar sobre sistemas de física e começar a implementá-lo para o personagem jogável" é melhor do que "sistema de física".

Aqui eu foquei especificamente para o pessoal da programação, mas o mesmo se aplica aos outros membros de cada equipe. Seja sempre que possível específico e focado ao delimitar as metas.

### 2. Executar o ciclo

Durante o tempo delimitado para seu ciclo, você e o time farão o que foi decidido. O programador vai criar um sistema, o artista vai trabalhar em algum _design_, o músico vai criar um tema musical. Ao líder fica o papel de ver se todo mundo está trabalhando conforme foi decidido. Lembrando sempre de respeitar o tempo e privacidade de sua equipe.

Durante a execução do ciclo, os membros _vão_ encontrar dificuldades ou dúvidas. O diálogo deve ser sempre presente para que membros possam se apoiar e opinar sobre cada situação.

Caso o trabalho de um ciclo tenha sido terminado por um membro, pode ser interessante a ele começar a trabalhar em outra coisa, ou apoiar outros membros em suas tarefas.

Instruções específicas de como melhor executar cada ciclo virão em seus respectivos capítulos mais a frente.

### 3. Concluir o ciclo

Ao final do tempo delimitado, você deve juntar sua equipe novamente (ou falar com cada um a parte) para discutir o que foi feito durante o mesmo. Aqui poderíamos considerar um binário: o trabalho delimitado foi feito ou não. Mas é mais proveitoso entender o que aconteceu para que o trabalho fosse feito ou não do que focar somente no resultado em si. 

Para o futuro do seu projeto, a avaliação desse trabalho importa tanto quanto a execução dele. Se o trabalho não foi feito, vale analisar algumas questões:

- Houve algum imprevisto que impediu a realização da meta?
- O tempo alocado foi muito curto para essa tarefa?
- Houve alguma dificuldade para a realização do trabalho? (Bem comum)

Entender as respostas a perguntas como essas é fundamental para adaptar e melhorar o ritmo de trabalho. Às vezes, realmente houve um problema. Em outros casos, os membros de sua equipe simplesmente não quiseram trabalhar. E isso é algo com o qual você terá que lidar às vezes.

Caso o trabalho tenha sido feito todo com sucesso, algumas outras perguntas podem ser relevantes:

- O trabalho delimitado foi pouco?
- O que contribuiu para que o trabalho fluísse tão bem?
- O que pode ser feito para melhorar o fluxo?

Novamente, essas perguntas e outras podem ajudar a aprimorar o processo para o próximo ciclo.

De qualquer forma, é esperado que pelo menos alguma coisa tenha sido feita com sucesso. É importante documentar certos aspectos do ciclo:

- O que foi feito com sucesso?
- O que faltou fazer?

Esses detalhes devem ser documentados e mantidos em mente na hora do planejamento do próximo ciclo. O que ficar para trás, e ideias que foram tidas durante o ciclo são documentadas no _backlog_.

Após uma reflexão sobre o resultado do ciclo anterior, geralmente se inicia o próximo, mas existe uma outra etapa muito importante.

### 4. Testando resultados

Após o fechamento de um ciclo, você pode ou não ter um produto executável. Geralmente, esse tipo de protótipo leva um pouco de tempo para sair do chão na etapa de produção, mas depois é facilmente construído por cima do que já existe (_builds_) a cada ciclo (versões _alfa_ e _beta_).

Para o desenvolvimento de jogos, testar estes protótipos é extremamente importante para encontrar _bugs_, problemas e verificar se o jogo está funcionando da maneira desejada. A isso chamamos de _playtesting_. Certas equipes podem ter um membro específico apenas para fazer isso. Em outras, os próprios membros da equipe testam o que foi feito. Outras ainda buscam terceiros para testar cada _build_.

Quando estes testes serão feitos vai depender da sua organização. Em certos casos, pode ser interessante testar um módulo criado ao final do ciclo, durante a avaliação. Assim, aprimorá-lo já entra como parte do próximo ciclo. Em outros casos, pode-se iniciar o trabalho em outro módulo, e testes do anterior podem ser feitos durante o próximo ciclo. 

Eu falo mais sobre _playtesting_ no [capítulo 7](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo7.md).

## Conclusão

Ao final desse capítulo, esperamos que tenha uma boa ideia de como planejará e executará o ciclo de desenvolvimento para o seu jogo. Isso pode parecer bem simplista e vago, mas você perceberá eventualmente que o estabelecimento de metas e reflexão sobre o que foi realizado serão de extrema importância para a organização do seu projeto.

Definido o ciclo, no [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo4.md) falaremos do primeiro ciclo, e como delimitar os próximos até a criação do primeiro protótipo.
