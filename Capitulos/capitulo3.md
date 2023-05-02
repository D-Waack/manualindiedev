
# Capítulo 3: O Ciclo de Desenvolvimento
"Eu já te contei a definição de insanidade?" - Vaas Montenegro, "Far Cry 3" (2012)

![Capítulo 3 capa](../Arquivos/Imagens/capa_03.png 'Have I ever told you the definition of insanity?')

## Introdução

Se tudo deu certo, você já escolheu qual será sua _engine_ e já tem certa noção de como organizará seus arquivos. Nesse caso, você já está pronto para começar o desenvolvimento de seu jogo.

Geralmente, definimos o ciclo de vida para o desenvolvimento de um jogo da seguinte forma: **Pré-Produção** -> **Produção** -> **Alfa** -> **Beta** -> **Produto Final**

Seguindo esta classificação, você teria passado pela etapa de pré-produção. A pré-produção na indústria como um todo geralmente é um processo mais formal. Isso não é um problema. Em muitos casos, um pequeno protótipo é projetado também durante a pré-produção. Decidim incluir isto na etapa de produção, por vários motivos.

A partir de agora, você e sua equipe entrarão no que eu chamo de ciclos de desenvolvimento. Outros vão chamá-los de _sprints_. O nome pouco importa. Esse nomenclatura é emprestada do Scrum, um _framework_ para a criação de projetos de _software_. O que interessa para o nosso caso é o ciclo de trabalho, e como isso será avaliado. A princípio, o que você vai definir é simples:

- A divisão das tarefas;
- O ritmo de trabalho.

### Divisão de tarefas 

Se seu projeto é solo, decidir isso vai ser bem fácil. Torna-se apenas uma questão de prioridades. E, para essse caso, existe um caminho ideal que vou discutiro mais a frente. Porém, se você trabalha em um grupo, as coisas ficam um pouco mais complexas.

Uma ótima coisa quando trabalhando em grupo é que várias pessoas podem trabalhar ao mesmo tempo. Porém, isso vai gerar maior trabalho organizacional, porque nem todas as competências devem ser desenvolvidas no mesmo ritmo.

Por exemplo, se sua equipe tem 2 programadores, ambos podem facilmenete trabalhar em diferentes aspectos de seu jogo. Digamos, um trabalha no movimento do personagem e o outro trabalha no funcionamento dos menus principais. Da mesma forma, se a equipe tem 2 artistas, um pode trabalhar no _design_ de um personagem, enquanto o outro trabalha em fundos, ou em outro personagem. O mesmo se aplica a músicos, _level designers_, e a lista segue.

No entanto, o trabalho do programador e do artista não seguem o mesmo ritmo. E, em certos casos, um depende de um resultado do outro. Por exemplo, implementar uma certa ação como puxar uma alvanca no jogo _Tomb Raider_ precisaria que os animadores tivessem completado a animação de puxar a alavanca. Esses animadores precisaram esperar que os modeladores tivessem completado o modelo de Lara Croft. E esses modeladores precisaram usar a _concept art_ do time de arte para criar o modelo e suas texturas.

O seu trabalho como gerente do time é certificar-se de que um membro não vai atrasar o outro, e tentar evitar retrabalhos ao máximo possível. Quanto menor o seu time, mais fácil é organizar isso, mas isso também quer dizer um ritmo de trabalho menor.

### Ritmo de trabalho

Os ciclos de desenvolvimento estarão atrelados a um **período de tempo** específico.

A ideia por trás do Scrum é de dividir o seu projeto em partes menores, cada uma sendo implementada em um período delimitado pela equipe (geralmente de 2-4 semanas). Dessa forma, o processo de produção fica mais simples e organizado. Eu não "trabalho no jogo", eu "termino o sistema de dano e _knockback_". 

Isso implica em algumas coisas para você e para sua equipe: Vocês terão metas a cumprir (onde podem ter sucesso ou não); vocês terão metas a decidir; vocês devem refletir sobre o resultado encontrado ao final de cada ciclo.

Existe flexibilidade no tamanho destes ciclos, e quanto é feito em cada um. E isso é importante que decidam. Pessoalmente, para projetos pequenos eu costumo trabalhar com ciclos de 1 semana. Talvez para você seja melhor 2 semanas. Para o contexto _indie_, eu não recomendo nada maior que isso a não ser que sua equipe não tenha tempo algum para trabalhar no projeto. No geral, é melhor termos ciclos com tempos menores, mesmo que as metas para estes ciclos sejam mais simples.

## O Ciclo

Entendendo o conceito de ciclo, resta executá-los. Os passos são simples:

### 1. Planejar o ciclo

Você e sua equipe (ou apenas você) discutirão quais aspectos do jogo serão mais importantes/interessantes criar por ora. Membros diferentes podem trabalhar em frentes diferentes ao mesmo tempo. 

Na teoria, um líder competente seria capaz de dirigir o jogo sozinho, sem que as diferentes competências dialoguem entre si. Por exemplo, o time de modelagem e CG não precisa saber o que o time de implementação anda fazendo. Entretanto, para projetos _indie_ isso se mostra não só difícil, mas uma opção ruim.

Quanto mais diálogo houver entre as diferentes competências, mais elas podem contribuir uma com a outra, e apoiarem-se entre si. O líder deve estimular diálogo entre os membros de forma que todos saibam o progresso entre eles, e não haja surpresas mais a frente.

A delimitação do ciclo pode ser feita através de uma reunião pessoal, uma chamada de vídeo, ou mensagens de texto. É preferível que possam se comunicar por voz, pois isso ajuda a fluir a discussão. Isso deve ser decidido logo no início do ciclo, ou no final do anterior.

Lembrando sempre que a opinião que deve pesar mais para cada aspecto é a dos especialistas para esse aspecto, mas que as opiniões do resto da equipe são de importância também. Enquanto o programador pode não saber tanto de arte, seu _input_ sobre o processo pode ser muito útil para o artista. Isso é importante porque mais a frente no projeto você terá de unir todos estes aspectos diferentes.

Outra coisa importante é manter em mente o ritmo de trabalho de cada pessoa. Alguns membros vão ter mais tempo e terminar seu trabalho antes de outros, outros vão ter imprevistos e gerar atrasos. Como você vai lidar com estes aspectos fica ao critério seu e de sua equipe. Se vai dar mais trabalho para um para agilizar o processo, ou se vai pedir que um membro complemente onde outro faltar. Não existe uma resposta certa, isso apenas deve ser considerado para evitar atrasos.

Durante essa discussão, podem surgir ideias que não serão executadas durante este ciclo, ou sugestões que ainda não precisam ser consideradas. **Anote-as** na _wishlist_ do seu GDD.

Se você delimitar um trabalho muito complexo para um tempo muito curto, o mesmo provavelmente não será terminado. Isso é normal e esperado, mas gera certo estresse para a sua equipe. Dessa forma, ficam algumas dicas para delimitar os seus ciclos:

- Objetivos específicos

 Quanto menos ambiguidade no que foi planejado, mais fácil é entender e executar cada tarefa.
 
- Objetivos simples

 Você não precisa descrever o ciclo inteiro em uma única palavra. Pode dividi-lo em pedaços menores. Por exemplo, "sistema de física" pode ser dividido em "movimento e colisão", e movimento pode ser dividido em "input, velocidade, gravidade". Isso fica a preferência de cada um, e muitas vezes a melhor opção depende do caso, mas dividir o trabalho em pedaços menores costuma ser mais fácil. Além disso, caso não consiga compreender todos os detalhes, o trabalho que já foi feito fica bem claro.
 
- Quando na dúvida, objetivos gerais, mas não vagos

 Em certos casos, as opções acima não serão possíveis, pois você e sua equipe não entendem o escopo da próxima tarefa. Por exemplo, na primeira vez que você criar um sistema de física, você não vai saber como dividi-lo em pedaços. Nesse caso, delimitar estes diferentes aspectos pode ser parte do objetivo. Se a sua equipe é inexperiente, "pesquisar sobre sistemas de física e começar a implementá-lo para o personagem jogável" é melhor do que "sistema de física".

Aqui eu foquei especificamente para o pessoal da programação, mas o mesmo se aplica aos outros membros de cada equipe. Seja sempre específico e focado com seus objetivos.

### Executar o Ciclo

Durante o tempo delimitado para seu ciclo, você ou o time fará o que foi decidido. O programador vai criar um sistema, o artista vai trabalhar em algum _design_, o músico vai criar um tema. Ao líder fica o papel de ver se todo mundo está trabalhando conforme foi decidido. Lembrando sempre de respeitar o tempo e privacidade de sua equipe.

## Conclusão
