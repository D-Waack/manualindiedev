
# Capítulo 10: Música e Efeitos Sonoros
"Nenhum preço tão alto." - Rei Pálido, "_Hollow Knight_" (2017)

![Capítulo 10 capa](../Arquivos/Imagens/capa_09.jpg 'No cost too great.')

## Introdução
Se você já jogou algo sem a música ou os efeitos sonoros, você sabe a diferença enorme que os sons fazem. Esse é outro ponto artístico sobre o qual eu só posso opinar como desenvolvedor. Se houver alguém com experiência musical na sua equipe, o melhor a fazer é seguir o que decidirem, mas deixo aqui alguns recursos que provavelmente podem te ajudar.

Sons em jogos vêm em dois tipos: efeitos sonoros, e músicas de fundo. Vou falar um pouco sobre cada um deles. Os efeitos sonoros estão geralmente atrelados a ações ou acontecimentos, como coletar um item, passos em diferentes áreas do cenário, um pulo, um personagem levando dano, etc. Músicas de fundo são, como o nome implica, músicas que tocam no fundo em cada cena.

## Recursos para Criação de Música
Programas e aplicativos para produção musical costumam ser caros, mas felizmente existem algumas opções grátis.

- Notação:
Programas de notação servem para criar partituras. Enquanto eles são mais úteis para um compositor tentando criar uma partitura para sua nova peça musical, eles também servem como ótimas interfaces para criação organizada de um tema musical para um jogo. Enquanto meus amigos formados em música vão falar de todas as vantagens do _Sibelius_, uma ótima alternativa grátis é o _Musescore_.

Sibelius: pago, complexo, difícil de entender e aprender, mais voltado a profissionais;  
Musescore: grátis, simples, mas com muitas opções, mais fácil de aprender para qualquer público, _soundfont_ livre para uso.

Pessoalmente, eu usava muito o Musescore 3. Hoje existe uma nova versão, Musescore 4, a qual eu ainda não aprendi a usar bem, e parece ainda ter alguns _bugs_. Mas são basicamente o mesmo _software_. A melhor vantagem do Musescore é que você pode exportar suas partituras diretamente como um arquivo musical completamente livre para uso, sem preocupação com direitos autorais.

![Musescore Interface](../Arquivos/Imagens/10_01.png 'Musescore Interface')

- Produção musical:
Existem programas muito mais adequados para produção musical em si. Geralmente, os chamamos de DAWs (Digital Audio Workstations). Estes são muito mais robustos que os programas de notação, oferecendo a possibilidade de ajuste manual de notas, importação de plugins de instrumentos, automatização e controle de ritmos, controle avançado de volumes, aplicação de efeitos diversos, entre várias outras funções. Porém, você provavelmente deve imaginar que isso é uma solução muito mais cara.

O DAW considerado por muitos o melhor da indústria, _FL Studio_, tem sua versão mais simples custando 100 dólares. E a versão mais completa custa um total de 500 dólares. Se você não se interessa em produção de música, esse é um preço muito caro para pagar em um _software_ que só usará de vez em quando. Porém, é um preço bom para a licença vitalícia de um DAW profissional.

![Flstudio Interface](../Arquivos/Imagens/10_02.png 'Flstudio Interface')

É claro, existem alternativas grátis para DAWs também. As que eu conheço melhor são o _LMMS_ e o _Cakewalk_. Enquanto ambos são funcionais, o _cakewalk_ é o mais fácil de usar e completo entre os dois. Entretanto, ele contém mais _bugs_. Recomendaria o _cakewalk_ caso queira uma alternativa grátis ao FL Studio. Inclusive, foi o que eu usei junto ao musescore para os projetos desenvolvidos durante a criação deste manual.

Outra coisa que encarece a utilização de DAWs são os _plugins_. Uma DAW não tem tantos instrumentos por padrão quanto os programas de notação. Enquanto alguns vão oferecer alguns VSTs (plugins de instrumentos) e _samples_ que você pode usar, na maioria dos casos você terá que procurar plugins de instrumentos em outras fontes para utilizar em seu DAW. Alguns desses são grátis, outros são caríssimos.

Para plugins de instrumentos grátis, recomendo a orquestra [VSCO 2](https://www.audiopluginsforfree.com/versilian-studios-chamber-orchestra-2-community-edition-vsco-2-ce/). E você pode encontrar vários outros neste mesmo site, [Audio Plugins For Free](https://www.audiopluginsforfree.com/). Eu gosto de usar o plugin de um sintetizador _Roland JV 1080_ que comprei de alguém na internet. Porém, existem opções grátis para muitos instrumentos.

- Recursos gratuitos:
Também é possível utilizar músicas grátis, disponíveis pela internet. O site [freesound.org](https://freesound.org) é um ótimo lugar para encontrar arquivos de música liberados para uso. Caso vá seguir por esse caminho, tome cuidado com as permissões. Algumas músicas são permitidas apenas para uso em projetos não lucrativos, outras são liberadas apenas se você der credito ao criador original. (Procure por CC0 caso não queria se preocupar com isso.)

### Processo de Criação Musical
Esse processo será muito mais fácil se você tiver um músico em sua equipe. Eu só costumo sentar ao meu piano e improvisar até encontrar algo que encaixe no **contexto** ou passe o **sentimento** que eu quero passar. Provavelmente, o processo mais adequado para você será diferente. Caso você não tenha ninguém com experiência para criar uma música na sua equipe, contratar um compositor para compor alguns temas pode ser o caminho mais fácil.

Porém, caso ainda deseje criar as músicas para seu próprio jogo, deixo aqui algumas dicas:

- Atente-se ao tom

Se a música que você criar não se encaixa no seu jogo, você provavelmente vai ter que criar outra. Eu tenho certa dificuldade com isso, porque não sou muito bom em criar músicas alegres. Porém, é sempre bom olhar algumas referências, como músicas em jogos similares ao que você está criando. Não roube motivos ou melodias na íntegra, mas sinta-se livre para tirar "inspiração" de temas similares ao que você tem em mente.

- Pense em acordes

Caso bolar uma melodia não seja fácil, pense em uma progressão de acordes no mesmo tom que você quer passar. Copiar uma progressão de acordes é muito mais aceitável do que roubar uma melodia, e você pode partir de uma progressão para criar uma nova melodia que passa o mesmo sentimento da música da qual você pegou "emprestado".

- Improvise

Algumas das melhores melodias que eu criei foram só tentando coisas aleatórias. Talvez isso exija sorte ou algum conhecimento musical que eu não reconheço, mas improvisar sempre me ajudou em composições.

## Processo e Recursos para Efeitos Sonoros
O meu processo para efeitos sonoros costuma ser bem diferente do que uso para criação de temas para música de fundo. Para estes, eu costumo partir de efeitos já criados, utilizando principalmente o site que mencionei antes, [FreeSound](https://freesound.org/). Geralmente, só procuro algumas palavras chaves relacionadas ao som que eu desejo encontrar (em inglês), e clico no filtro de "Creative Commons 0" para poder utilizá-lo em qualquer trabalho, comercial ou não lucrativo.

Baixando estes sons, na maior parte dos casos eu os edito no aplicativo _Audacity_. Nele, posso cortar o áudio para apenas o trecho que desejo utilizar no jogo, e posso adicionar alguns efeitos para melhorá-los também. Como mudar o tom do áudio, ou deixá-lo mais acelerado, invertê-lo, entre outros.

![Audacity Interface](../Arquivos/Imagens/10_03.png 'Audacity Interface')

Alguns programas como o _Chiptone_ vão permitir a criação de efeitos sonoros. Em outros casos, você pode gravar seus próprios efeitos, como é feito por produtores musicais, mas isso é algo com o qual eu tenho pouca experiência para opinar. 

![Chiptone Interface](../Arquivos/Imagens/10_04.png 'Chiptone Interface')

De qualquer forma, uma vez criados os efeitos, é sempre bom testá-los no contexto do jogo, e iterar até encontrar um som ideal para a ação que está tentando criar.

## Conclusão
Ao final desse capítulo, espero que tenha uma certa ideia de como prosseguir para a criação de músicas e efeitos sonoros para o seu jogo. A melhor opção ainda seria contratar ou recrutar um compositor competente para o seu jogo, mas as outras opções que listei serão úteis para uma equipe que não contém nenhum músico, o que não é algo tão incomum.

No [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo11.md), falarei mais sobre o processo de integração destes recursos áudiovisuais ao seu jogo.
