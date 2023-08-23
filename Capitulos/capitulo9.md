
# Capítulo 9: Arte, Modelos, Visual
"Pesaroso seja o coração, Penitente cheio de clemência" - Tirso, "_Blasphemous_" (2019)

![Capítulo 9 capa](../Arquivos/Imagens/capa_10.jpg 'Sorrowful be the heart, Penitent One full of clemency.')

## Introdução
Recursos visuais vêm em vários formatos diferentes. _Sprites_, modelos 3D, texturas, etc. 

A parte visual de qualquer jogo é extremamente importante. E enquanto é possível fazer um jogo somente com recursos grátis encontrados _online_, geralmente é preferível que sejam criados seus próprios recursos, ou pelo menos adaptados para que melhor se encaixem para o seu jogo.

Geralmente, o _estilo visual_ é mais importante do que fidelidade gráfica ou realismo. Mas isso depende completamente do tipo de jogo que você deseja criar, e o tipo de audiência que deseja alcançar.

## Recursos 2D
### Estilos
Jogos 2D costumam vir com seu próprio jargão para os diferentes itens gráficos. Entre os diversos estilos que você pode encontrar deles, alguns formatos de destacam:

- _Pixel art_ (arte retrô, similar a de jogos dos anos 80 e 90, quando a resolução de _display_ em telas era limitada, e a arte refletia isso com gráficos pixelizados);
- _Vector art_ (arte criada usando vetores em vez de píxeis, permite mudança de resolução sem perda de detalhes, mas difícil criar arte detalhada usando as primitivas gráficas);
- _Raster art_ (ou arte normal, geralmente no formato de arte digital, formato de píxeis, mas sem a resolução baixa característica de _pixel art_).

Para cada formato, os estilos também podem variar consideravelmente. Isso depende do artista. Geralmente, jogos _indie_ costumam seguir com o caminho da _pixel art_. Entretanto, existem vários jogos _indie_ que são criados para resoluções maiores. Arte de vetor é mais incomum, mas você pode encontrá-la em certos jogos do _Newgrounds_, por exemplo.

O estilo de arte para seu jogo deve seguir a preferência do time. _Pixel art_ e arte digital são 2 habilidades diferentes (apesar de que saber uma contribui para enteder a outra). _Pixel art_ costuma ser mais simples, porque você tem um limite de píxeis com os quais trabalhar, tornando mais "fácil" o trabalho do artista. Entretanto, de certa forma é mais difícil, porque você tem que passar todo o detalhe que deseja em uma quantidade bem limitada de píxeis.

Se você não tem experiência com arte, eu sugiro seguir com _pixel art_. Mas, novamente, siga com o estilo que melhor preferir.

### Objetos
No contexto 2D, nós temos alguns termos que vão aparecer em muitos jogos. 
- _Sprites_

_Sprites_ são pequenas imagens que se sobrepõem a uma cena visual. Geralmente, _sprites_ vão ser personagens ou objetos com os quais se pode interagir. O _sprite_ não faz parte do cenário, e muitas vezes é animado.

- _Tiles_

O termo _tile_ se refere a pequenos quadrantes gráficos que aparecem em jogos antigos. Eles também são muito usados no contexto de jogos 2D. O termo refere a qualquer quadrante de um mapa quadriculado.

- Plano de Fundo

O fundo da tela, atrás do cenário. Este pode ser estático, ter um _scrolling_ (arrastamento) simples ou pode ter _scrolling parallax_, um formato onde o plano de fundo tem diferentes camadas que se movem em velocidades diferentes para criar a ilusão de um horizonte mais realista (muito utilizado em jogos da era 16-bit).

### Ferramentas e links
Para a criação de imagens e arte 2D, existem diversas ferramentas. Enquanto você podia usar algo como o _Photoshop_ para criar qualquer tipo de gráfico, vamos listar algumas opções mais acessíveis.

- Aseprite (_pixel art_, pago, mas uma das melhores e mais completas ferramentas para criação de _pixel art_)
- Paint.net (_pixel art_ e arte normal)
- Gimp (_pixel art_ e arte normal)
- Ferramentas online diversas (por exemplo: [Pixilart](https://www.pixilart.com/draw))
- [OpenGameArt](https://opengameart.org/) (site com inúmeras opções de recursos gráficos grátis para utilização em jogos)

### Processo
O processo para criação de arte 2D variam de artista para artista. O processo de criação de _pixel art_ pode ser facilmente feito apenas utilizando um mouse, enquanto arte digital mais complexa geralmente irá exigir que você tenha algum tablet ou mesa de digitalização. Estes são custosos, mas facilitam bastante o processo.

Enquanto eu ainda não sou um bom artista, vou deixar algumas dicas para aqueles que também estão neste caminho:
- Use referência: desenhar da imaginação pode parecer uma ótima ideia, mas é um ótimo caminho para te fazer sentir como uma criança de 5 anos. Procure imagens do que você quer representar, tente entender como esses objetos podem ser representados no mundo de seu jogo;
- Se atente a perspectiva: se parte da sua arte é feita de uma perspectiva, e outra parte em outra, isso vai causar confusão para o seu jogador. Procure diferentes estilos como 3/4, oblíquo, _top down_, _sidescroller_, entre vários outros e verifique qual é o melhor estilo visual para o seu jogo. Não fuja desse estilo, a não ser que isso faça sentido, ou seja necessário;
- Utilize as ferramentas disponíveis: enquanto eu não tirei muito proveito disso ainda, já observei muitos desenvolvedores em fóruns criando arte incrível com o auxílio de ferramentas de inteligência artificial como o _stable diffusion_. É claro, o uso desse tipo de ferramenta vem com algumas preocupações éticas, mas creio que utilizar o output de um destes como referência para sua própria arte é um ótimo jeito para tornar esse processo mais fácil;
- Veja estilos de jogos similares: procure entender o que funciona para diferentes jogos com estilos similares ao que você tem em mente. Procure ter inspiração sem copiar ideias de outros.

## Recursos 3D
### Estilos
Em termos de estilos, 3D apresenta uma enorme variedade. Estilos realistas, estilos de desenho animado, estilos retrô. O que vai delimitar o seu estilo visual em um jogo 3D são algumas coisas: os modelos e a quantidade de triângulos deles, as texturas, os _shaders_ e iluminação. Em termos simples, os modelos são os diversos objetos 3D que compõem seus personagens, mapas, objetos, etc. E as texturas são as imagens que "pintam" estes modelos. _Shaders_ e iluminação são calculados durante a execução do seu jogo.

O design visual de jogos 3D é muito mais complexo do que jogos 2D. Em termos de diferenças de estilos, quanto maior a quantidade de _quads_/triângulos em seus modelos, mais realistas e complexos eles podem ser. Entretanto, isso também aumenta a necessidade de processamento da máquina executando o jogo. Mais do que o tamanho dos modelos, a resolução e estilo das texturas é o fator mais importante para questões de estilo visual. 

### Ferramentas e links
Para criação de recursos visuais 3D, você precisará de um programa de modelagem, um programa para criar as texturas e, às vezes, um programa para misturar estes dois.

- Blender (Programa de modelagem, animação 3D, criação de texturas, entre outros, completamente grátis, melhor opção para um desenvolvedor _indie_)
- Gimp (aplicativo gráfico grátis que pode ser utilizado na criação de texturas)
- Maya (Programa profissional de modelagem, pago)
- [Ambient CG](https://opengameart.org/) (Opções de texturas para download e uso)
- [Textures.com](https://www.textures.com/free) (Opções de texturas para download e uso)

A melhor opção para um desenvolvedor _indie_ sempre será o Blender. A não ser que ele já tenha uma assinatura em algum dos outros aplicativos de modelagem mais robustos. Blender têm uma curva de aprendizado bem alta, mas assim que dominado, é uma ferramenta incrível para a criação de modelos e até texturas, além de animações, _UV unwrapping_, _sculpting_, entre diversas outras opções.

O Gimp eu sugiro como uma alternativa gráfica grátis para a criação/edição de texturas, _skyboxes_, etc. 

### Processo
Da mesma forma, o processo para criação de objetos 3D varia de artista para artista, mas as mesmas dicas que citei para recursos 2D se aplicam para 3D, mesmo que em uma forma mais complexa. 

## Conclusão
Neste capítulo, minha intenção foi listar diversas opções que desenvolvedores _indie_ podem usar para a criação dos diversos recursos visuais que serão necessários em seus jogos. 

No [próximo capítulo](https://github.com/D-Waack/manualindiedev/blob/main/Capitulos/capitulo10.md), falamos sobre música e efeitos sonoros.
