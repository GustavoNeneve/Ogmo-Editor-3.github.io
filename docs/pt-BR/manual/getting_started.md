# [Primeiros Passos](#getting-started)

Este Guia de Início Rápido vai ajudá-lo a navegar pelo Ogmo Editor 3 para criar níveis únicos para os seus jogos!

Primeiro, baixe o OGMO Editor 3 [aqui](https://ogmoeditor.itch.io/editor).

## [Iniciando um Novo Projeto](#starting-a-new-project)

O coração de uma sessão do OGMO Editor é um arquivo de Projeto `.ogmo`. Esse arquivo de Projeto contém uma lista de todas as camadas, tilesets e entidades que você pode usar ao criar níveis. Isso significa que todos os níveis compartilharão a mesma estrutura básica.

<p align="center">
  <img  src="https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/manual/ogmo-home.png" alt="OGMO Editor Home">
</p>

Abra o OGMO Editor 3 e clique em `New Project` para começar! Você será solicitado a criar um novo arquivo `.ogmo`. Após selecionar o nome e o local do arquivo, você verá a visualização de `Project Settings`.

## [Configurações do Projeto](#project-settings)

Na visualização de `Project Settings`, você definirá as configurações gerais do projeto, que afetam tanto os seus níveis quanto o comportamento do OGMO Editor durante a criação de níveis.

<p align="center">
  <img  src="https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/manual/ogmo-project.png" alt="OGMO Editor Project Settings">
</p>

Nessa visualização, você pode definir o seguinte:

- **NAME** - O nome do seu Projeto. Ele aparecerá na tela inicial em `Recent Projects`.
- **PROJECT DIRECTORY DEPTH** - Informa ao OGMO Editor a profundidade com que ele deve buscar arquivos ao indexá-los automaticamente.
- **BG COLOR** - A cor de fundo do editor.
- **GRID COLOR** - A cor da sobreposição da grade no editor.
- **ANGLE EXPORT MODE** - Selecione `Radians` ou `Degrees` para que o OGMO Editor exporte os metadados de ângulo no formato de sua preferência.
- **MIN LEVEL SIZE** - Define a largura e altura mínimas dos seus níveis.
- **MAX LEVEL SIZE** - Define a largura e altura máximas dos seus níveis.
- **LEVEL VALUES** - Crie metadados personalizados para os seus níveis. Todos os níveis compartilharão os mesmos parâmetros, mas os valores podem ser definidos individualmente.

Quando terminar de configurar os dados gerais do Projeto, clique na aba `Layers` à esquerda para continuar.

## [Adicionando Camadas](#adding-layers)

<p align="center">
  <img  src="https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/manual/ogmo-layers.png" alt="OGMO Editor Layers">
</p>

Todo Projeto no OGMO Editor precisa de pelo menos uma camada. Uma camada pode conter Tiles, Grid Cells, Decals ou Entities. Para adicionar uma camada, na aba `Layers`, clique no botão `+ New Layer`. Por ora, tente adicionar uma camada do tipo Tile chamada `Tiles` e uma camada de Entity chamada `Entities`.

Após criar essas camadas, você pode reordená-las clicando e arrastando-as na lista abaixo do botão `+ New Layer`. Arraste a camada `Entities` para que ela fique acima da camada `Tiles`.

Você pode aprender mais sobre Tile Layers [aqui]() e Entity Layers [aqui]().

## [Adicionando Entities](#adding-entities)

<p align="center">
  <img  src="https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/manual/ogmo-entities.png" alt="OGMO Editor Entities">
</p>

As Entities oferecem uma maneira de adicionar objetos dinâmicos aos seus níveis. Uma Entity pode representar um inimigo, uma placa de sinalização, uma entrada, o que você puder imaginar! Adicionar entities é simples — basta navegar até a aba `Entities` e clicar no botão `+ New Entity`. Dê o nome que quiser à sua entity. Tente adicionar outra e mude a cor dela para diferenciá-la da primeira. Clique no quadrado vermelho para alterar o `Entity Icon Color`.

Você pode aprender mais sobre Entities [aqui]().

## [Adicionando Tilesets](#adding-tilesets)

<p align="center">
  <img  src="https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/manual/ogmo-tiles.png" alt="OGMO Editor Entities">
</p>

Um tileset é um arquivo de imagem composto por uma coleção de tiles dispostos em uma grade. Você usa Tile Layers para organizar esses tiles em um nível! Para adicionar um tileset ao seu projeto, vá até a aba `Tilesets` e pressione o botão `+ New Tileset`. O OGMO Editor solicitará que você navegue pelo sistema de arquivos para selecionar uma imagem de tileset. Se não tiver uma disponível, sinta-se à vontade para usar [esta](https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/manual/tiles.png)! Defina o nome do tileset e as dimensões dos tiles antes de continuar!

## [Salvando um Projeto](#saving-a-project)

Agora que temos camadas, entities e um tileset para trabalhar, pressione o botão `Save` no canto inferior esquerdo do OGMO Editor. Isso salvará o arquivo do Projeto no caminho definido quando você clicou em `New Project` no início deste guia.

## [Usando o Editor](#using-the-editor)

<p align="center">
  <img  src="https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/manual/ogmo-editor.png" alt="OGMO Editor">
</p>

Após salvar o Projeto, você será levado para a visualização principal do editor. Essa visualização é composta por três colunas:
- A coluna da esquerda contém suas camadas e uma lista de níveis salvos e não salvos.
- A coluna do meio possui o espaço de trabalho principal.
- A coluna da direita abriga as paletas de tiles, grids, decals e entities (dependendo da camada selecionada). Quando uma entity é selecionada, ela também exibe um editor para definir valores personalizados por entity.

Selecione a camada `Tiles`. Na coluna da direita, seu tileset deve ser selecionado automaticamente e populará a Tile Palette. Se você tiver mais de um tileset, poderia alternar entre eles por lá.

Use a `Pencil Tool` e clique em um tile na Tile Palette. Desenhe na grade do espaço de trabalho principal para aplicar esse tile ao seu nível. Experimente também as outras ferramentas!

Você pode aprender mais sobre Tile Layers [aqui]().

Se quiser redimensionar o nível, simplesmente clique e arraste uma das setas logo fora da grade do nível! Para navegar pelo nível, use o scroll do mouse para dar zoom e segure `SPACEBAR`, clique e arraste para percorrer o nível. Para redefinir o zoom e a posição, pressione o botão `Level Center` no canto inferior esquerdo do espaço de trabalho principal.

Agora, selecione a camada `Entities`. Na coluna da direita, você verá as entities que adicionou anteriormente. Clique em uma para selecioná-la e depois clique na grade para posicionar a entity no seu nível.

## [Salvando Níveis](#saving-levels)

Para salvar o nível, simplesmente pressione `Ctrl+S` (`Cmd+S` no MacOS). Você será solicitado a escolher um caminho para salvar o nível. Uma vez salvo, o nível aparecerá na árvore de diretórios na coluna da esquerda. Você pode clicar com o botão direito no nível na árvore de diretórios para realizar diferentes ações.

O nível será salvo como um arquivo JSON legível por humanos e fácil de parsear.

Você pode aprender mais sobre este formato [aqui]().

## [Conclusão](#wrapping-up)

Agora que você entende como usar o OGMO Editor, esperamos que o utilize para criar conteúdo maravilhoso!

Explore o restante do manual para conhecer todas as diferentes funcionalidades que o OGMO Editor tem a oferecer!
