
# Capítulo 5: Lidando com Problemas Diversos
"Você se encontrou com um destino terrível, não foi?" - Vendedor de Máscaras Alegre, _The Legend of Zelda - Majora's Mask_ (2000)

![Capítulo 5 capa](../Arquivos/Imagens/capa_05.jpg 'A man chooses, a slave obeys.')

## Introdução

_Esse capítulo é destinado aos responsáveis pela programação no seu projeto._

Se você chegou aqui, assumimos que já começou o desenvolvimento do seu jogo. Porém, não é como se eu houvesse te dado um passo a passo sobre o que fazer para cada problema. Minha intenção é cultivar em você e sua equipe uma independência. E quando dizemos independência no mundo do _software_, queremos dizer a capacidade de encontrar soluções aos diferentes problemas que encontramos, onde quer que seja.

Neste capítulo, eu discuto como abordar os problemas mais comuns encontrados no desenvolvimento (em termos de programação).

## Não sei criar/implementar X

O primeiro passo quando não se sabe fazer alguma coisa é pensar. Pensar é uma habilidade, e como toda habilidade, ela exige experiência e prática. Dessa forma, se você não tem certa quantidade de experiência, pensar _nunca_ será o suficiente. O pensar é complementado pelo conhecimento. Em outras palavras, quanto mais você sabe, mais fácil será resolver o problema meramente por pensar. 

Esse conhecimento toma forma como entendimento de conceitos de programação, estruturas de dados, gerenciamento de diferentes tipos de arquivos, _loops_ de jogo; bem como conhecimento da _engine_ ou _framework_ com o qual você está trabalhando.

Porém, até você adquirir este conhecimento, você precisa buscar outros meios.

O principal meio entre esses será:

### A Pesquisa

Isso pode parecer estranho, mas uma das maiores habilidades que todo programador deve ter é a de utilizar o Google. Na maioria dos casos em que você quer implementar algo, alguém mais experiente que você já o fez. Nem sempre isso vai estar disponível para sua visualização, mas você pode assumir geralmente que se você quis criar algo, outra pessoa já quis também.

Porém, um detalhe importante é que a grande maioria do conteúdo de TI é escrito _em inglês_. Enquanto você pode procurar seu caso em português (e certas vezes você vai encontrar os resultados desejados mais facilmente pela menor quantidade), utilizar o inglês vai se mostrar necessário na maioria dos casos. Se você não tem entendimento ou fluência no inglês, passar sua pesquisa por um tradutor como _DeepL_ ou mesmo o _Google Tradutor_ pode ser o suficiente, mas entenda que você também terá que traduzir as páginas, pois estarão em inglês.

Essa opção surgiu ao público durante a escrita deste manual, mas agora também temos ferramentas de inteligência artificial como o _ChatGPT_ que podem oferecer essas informações de maneira mais fácil (com certa margem de erro).

É importante que você entenda o que quer fazer antes de começar a pesquisa. Isso virá com o tempo e experiência, mas quanto melhor você descrever o que procura, mais fácil fica encontrar o que quer que seja. No início, suas pesquisas serão mais generalizadas, mas quanto mais você entender do assunto, mais sofisticadas elas serão. 

Conseguir _entender_ o que você precisa às vezes é tão importante quanto a implementação de sua ideia.

- Macro vs Micro

O tipo de resposta que você vai encontrar depende do tipo de pesquisa que você vai fazer.

Se você procurar algo como "Como criar um jogo similar a _Fire Emblem_ em Unity", você pode encontrar exatamente o que procura, como também pode não encontrar nada. Entretanto, se você dividir sua pesquisa em pedaços menores, talvez você comece a encontrar resultados mais interessantes. Por exemplo, para um mapa de Fire Emblem, você pesquisaria "como criar um mapa _grid_ em Unity", e então "como criar pathfinding em uma _grid_ em Unity". Esse tipo de informação é muito mais fácil de encontrar.

Eventualmente, suas pesquisas ficarão mais precisas ainda. No exemplo anterior, eu não procuraria por como criar o _pathfinding_, eu simplesmente buscaria um modelo do algoritmo A* para implementá-lo diretamente. Se o exemplo fosse feito em Godot, nem isso eu procuraria, pois já o implementei vezes o suficiente que eu posso lembrá-lo de cabeça ou buscar o código em um dos meus projetos antigos.

O que leva a uma questão interessante:

## O que fazer com os resultados

Você conseguiu achar um resultado para sua pesquisa, mas ele se trata de um monte de texto incompreensível (código) em algum fórum de dúvida, ou _blogpost_, ou _output_ do Chat GPT. 

Você pode simplesmente copiá-lo e colá-lo na sua _engine_, mas você vai notar rapidamente que isso não funciona. Nomes de variáveis, funções, lógica. Nada disso vai bater com o que você tinha anteriormente, e isso é normal. Afinal, foi outra pessoa (ou IA) que escreveu o código.

O que você tem que fazer com o resultado encontrado é entendê-lo e adaptá-lo para o seu projeto. Na prática, você só precisaria adaptá-lo, mas isso pode ser tão simples quanto mudar o nome de uma variável, ou pode ser um trabalho extremamente complexo, e é por isso que entender o código é tão importante. Além disso, entender o código também agrega ao seu aprendizado.

### Entendendo o código

Se você é um iniciante na linguagem, entender o código não vai ser tão simples. Conhecer o formato da linguagem é muito importante. Mas isso pode ser aprendido diretamente na prática.

O passo a passo que eu sigo para entender qualquer código costuma ser:
- Ler o código, linha por linha (se eu já entendo do assunto, torna-se apenas uma questão de ler e lembrar/reconhecer o que cada linha faz) 
- Testar o código, linha por linha (escrever o código por pedaços e testar o que ele faz na prática gera entendimento imediato do funcionamento de cada linha)
- Procurar funções desconhecidas na documentação (geralmente, a documentação da _engine_ vai explicar exatamente o que cada função faz)

São passos simples, mas não pense que esse processo é sempre fácil. Você sempre vai se encontrar quebrando a cabeça tentando entender certa lógica e ligando os pontos aos poucos. Não se preocupe, isso é parte do aprendizado. Em certos casos, eu procuro a documentação antes de testar. Em outros, eu simplesmente testo sem procurar a documentação. Isso não é um processo rígido.

Às vezes, você pode ter que pesquisar separadamente o que certa linha ou função faz. Isso acontece se tiver uma documentação deficiente, ou complexa demais. Outras vezes, você terá que procurar outro resultado porque o que encontrou não é o que esperava. Nesse caso, não se desespere. Continue procurando. Existe uma solução para quase todos os problemas. (E para os outros existem "gambiarras".)

Lembre-se sempre: na maioria dos casos, copiar e colar código sem entendê-lo é uma prática ruim e vai atrapalhar o seu projeto.

Existem casos em que isso não será um problema, por exemplo, se você instalar um módulo ou _plugin_ ao seu projeto, e este funciona de maneira separada ao código para o seu jogo. Por exemplo, um módulo Ruby no seu projeto de RPG Maker VX Ace. Nesses casos, você já chega com um "bloco" pronto para uso, e só será necessário entender seu código se quiser mudar como esse módulo funciona.

De qualquer forma, entendendo o código e incorporando-o ao seu projeto, você resolverá o problema pelo qual pesquisou. Mas nem sempre as coisas vão ser tão fáceis.

## Não encontrei como implementar X

Se a sua pesquisa não gerar frutos, ou se a IA gera um resultado sem sentido, existe a possibilidade de que você está pesquisando mal, e existe a possibilidade de que o conteúdo que você procura simplesmente não existe publicamente.

Nestes casos, você tem algumas opções:
- Revisar a pesquisa;
- Ler a documentação;
- Procurar uma comunidade de desenvolvedores;
- Criar um post de dúvida.

Revisar a pesquisa sempre é preferível. Talvez mudar alguma palavra chave te ajude a encontrar exatamente a solução ao seu problema. Isso ocorreu comigo inúmeras vezes. Mas já encontrei casos onde eu não conseguia encontrar uma referência de forma alguma.

A próxima opção é ler a documentação. Toda _engine_ vai ter uma documentação, mas nem todas vão ter a mesma qualidade. Engines como Unreal, Unity e Godot têm ótimas documentações, e isso ajuda muito no desenvolvimento. Fazer uma pesquisa na documentação pode ser a solução para sua dúvida, mas lembre-se que a linguagem utilizada nesses materiais costuma ser bem técnica.

Quando nenhum desses funciona, sua próxima opção deve ser perguntar a alguém. Existem muitas comunidades de desenvolvedores em plataformas como o _Discord_, onde pessoas podem discutir ideias e tirar dúvidas. Procure uma ligada a sua _engine_, quem sabe você até encontre alguém disposto a ajudar no seu projeto.

Caso nenhuma dessas sugestões te dê resultados, uma boa opção será a do fórum de dúvidas.

### Postando em um fórum de dúvidas

Se você já teve que procurar por alguma dúvida de desenvolvimento, você provavelmente já se deparou com um fórum de dúvidas de programação. Neles, usuários fazem perguntas sobre como implementar determinada função de código, ou sobre boas práticas e dúvidas de utilização gerais. Nesses fóruns, usuários mais experientes respondem estas perguntas para ajudar os usuários com dúvidas.

Esse tipo de fórum é onde você deve ir quando não consegue achar uma solução para o seu problema.

Geralmente, o fórum vai ter uma seção em algum lugar te oferecendo sugestões e regras para como criar seus posts e como incluir _tags_ neles, ou em qual subfórum ele deve ficar. É importante ler essas regras de post antes de fazer qualquer pergunta, mas aqui eu deixo algumas orientações sobre seus posts:

- Seja claro, focado e objetivo: Você não precisa explicar seu jogo inteiro no seu post. Alguns detalhes podem ser sempre relevantes como se o seu projeto é 3D ou 2D, e qual versão da _engine_ você está usando, mas, na maioria dos casos, você só deve incluir detalhes que se aplicam diretamente ao problema em questão. Se o meu problema é na aceleração do meu personagem, pouco importa como o meu mapa é gerado.
- Simples é melhor: Uma explicação _muito_ elaborada sobre o seu caso pode fazer com que pessoas o ignorem, infelizmente. Tente ser simples, incluindo apenas detalhes importantes. Caso alguém fique na dúvida, eles vão pedir para que elabore sobre o problema, mostre código ou mande uma versão do seu projeto para que eles possam olhá-la (**muito cuidado** com isso, tente evitar disponibilizar seu projeto completo caso não queira que ele seja roubado. A maioria das pessoas nesses fóruns são de boa índole, mas apenas um usuário mal intencionado pode causar grande estrago).
- Mostre evidências: nesse contexto, uma imagem não equivale a mil palavras, mas ajuda bastante a entender seu problema.
- Engaje: Ajude-os a ajudá-lo. Responda as perguntas que fizerem, tente contribuir.

O maior problema com questões em fóruns é que nada garante que sua pergunta será respondida em um tempo curto, e em certos casos elas simplesmente não são respondidas. Por isso, costumo deixar esse tipo de post para último caso.

## Erros no código
Outro caso que você inevitavelmente vai encontrar são erros no seu código. 

Erros podem ser coisas simples, como uma vírgula faltando, ou algo muito mais complexo que destrói todo o seu sistema de iluminação e que você descobre por acidente um mês depois (nem me pergunte). Por esse motivo, é sempre bom testar o seu código com frequência e diagnosticar os erros antes que eles fiquem complicados demais para análise.

No geral, quando um erro de execução é encontrado, o próprio console da _engine_ vai te oferecer uma mensagem sobre ele. Eles podem ser erros de sintaxe, erros de variáveis, de parâmetros, de lógica, entre outros. E, geralmente, serão resolvidos com mudanças no seu código. A mensagem de erro vai ser o seu melhor amigo nestes casos, pois ela vai apontar em qual script, e qual linha o erro ocorreu, e porque ele ocorreu.

Certas vezes, o erro vai ser algo óbvio e basta consertar o código na linha especificada. Outras vezes, você não vai entender o motivo do erro. Nesses casos, seguir o mesmo processo de pesquisa explicado anteriomente vai servir.

## Execução Inesperada
Às vezes, você vai implementar algo e o console não vai apontar um "erro" explícito, mas o jogo não funcionará do jeito que você esperava.

Esse tipo de erro é muito comum. E o motivo geralmente é que existe algum erro na sua lógica. Muitas vezes por algo que você deixou passar, uma variável que você confundiu e atribuiu o valor errado. Por exemplo, você percebe que seu personagem jogável está se movendo lento demais, e eventualmente descobre que estava atribuindo ao personagem _Direção + Velocidade_ em vez de _Direção * Velocidade_. Isso não vai causar nenhum erro no console, e a execução vai seguir normalmente, mas o jogo ainda não está funcionando da maneira esperada.

Às vezes, o erro vai estar em um lugar óbvio. Outras vezes, nem tanto. Nesses casos, o método mais eficiente costuma seguir todo o caminho lógico de trás para frente até encontrar algum tipo de valor inconsistente. Isso não é tão simples de explicar, mas basicamente, tente imprimir no console todos os valores que podem influenciar a execução inesperada, ou crie "checkpoints" na execução. A lógica é que se "até aqui os valores estão conforme esperado", então você sabe que o erro veio num momento mais adiante da execução.

Esses erros costumam ser bem simples, mas também estressantes. Mantenha a calma, continue procurando, e teste com frequência. Quanto mais cedo você encontrar estes erros, mais fácil será resolvê-los.

## Erros recorrentes

Algumas vezes você encontrará certos problemas padrão. Por exemplo, se o seu jogo está lento, geralmente isso indica que você está fazendo muitas operações ao mesmo tempo, ou que falhou em parar alguma execução. Para estes casos, tente fazer condições abrangentes, por exemplo usar "> 2" em vez de "= 3" para certo índice, mesmo sabendo que o valor máximo sempre será 3. Tente também evitar criar ou deletar muitos objetos ao mesmo tempo (considere usar _object pooling_). Além disso, evite utilizar funções recursivas, a não ser que tenha certeza que elas sempre se limitarão a poucas recursões. Mais sobre essas práticas em capítulos posteriores.

Certas vezes você notará que o jogo não reage ao seu input. Nesse caso, certifique-se de que está configurando o _input_ para as opções corretamente dentro da engine ou framework.

Cito estes por serem problemas que enocntrava com frequência quando iniciante. Sempre certifique-se de que a sintaxe que escreveu está correta, e de que está usando as variáveis certas, e você vai evitar mais algumas centenas de erros similares.

## Conclusão
Neste capítulo descrevemos um _workflow_ para lidar com situações adversas durante um ciclo de desenvolvimento. É importante que todo desenvolvedor tenha um plano concreto para lidar com estas situações, pois não vão ser poucas às vezes em que se depararão com elas.

No [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo6.md), vamos falar sobre o passo seguinte ao protótipo 0, o início do desenvolvimento das versões _alfa_.
