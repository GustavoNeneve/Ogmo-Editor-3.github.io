# Entity Layers

## Ferramentas

### Entity Select Tool - <img src="https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/icons/selection.png" class="down-eight" width="32"/>

**Botão Esquerdo do Mouse Pressionado**

- Se o cursor estiver sobre uma entity, deseleciona as entities selecionadas e seleciona a entity.
  + Shift: Adiciona a entity às entities selecionadas.

**Botão Esquerdo do Mouse Pressionado + Arrastar**

- Se o cursor não estiver sobre uma entity, cria um retângulo de seleção.
  + Soltar Botão Esquerdo: Seleciona as entities dentro do retângulo de seleção.
  + Shift + Soltar Botão Esquerdo: Alterna o estado de seleção das entities dentro do retângulo de seleção.

- Se o cursor estiver sobre uma entity, move as entities selecionadas, alinhadas à grade.
  + Ctrl: move as entities selecionadas sem alinhar à grade.

**Botão Direito do Mouse Pressionado + Arrastar**

- Cria um retângulo de seleção para exclusão.
  + Soltar Botão Direito: Exclui as entities dentro do retângulo de seleção.

**Atalhos**

- Alt: Muda para a Entity Resize Tool.

### Entity Create Tool - <img src="https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/icons/entity-create.png" class="down-eight" width="32"/>

**Botão Esquerdo do Mouse Pressionado**

- Cria uma entity a partir do modelo do pincel, alinhada à grade. Seleciona a entity automaticamente.
  + Ctrl: Cria a entity sem alinhar à grade.
  + Shift: Adiciona a entity à seleção existente.
  + Arrastar: Move a entity criada.

**Soltar Botão Esquerdo**

- Se uma entity foi criada, a ferramenta é automaticamente alterada para a Entity Select Tool.

**Botão Direito do Mouse Pressionado**

- Exclui a entity na posição do cursor.
  + Arrastar: Exclui entities.

**Arrastar**

- Pré-visualiza a entity na posição do cursor.

### Entity Resize Tool - <img src="https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/icons/entity-scale.png" class="down-eight" width="32"/>

**Botão Esquerdo do Mouse Pressionado + Arrastar**

- Redimensiona as entities selecionadas (se as entities forem redimensionáveis).

### Entity Rotation Tool - <img src="https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/icons/entity-rotate.png" class="down-eight" width="32"/>

**Botão Esquerdo do Mouse Pressionado + Arrastar**

- Rotaciona as entities selecionadas (se as entities forem rotacionáveis).

### Entity Node Tool - <img src="https://raw.githubusercontent.com/Ogmo-Editor-3/ogmo-editor-3.github.io/gh-pages/img/icons/entity-nodes.png" class="down-eight" width="32"/>

**Botão Esquerdo do Mouse Pressionado**

- Cria e seleciona um nó para cada entity selecionada, alinhado à grade.
  + Ctrl: Cria nó(s) sem alinhar à grade.
  + Arrastar: Move o(s) nó(s) selecionado(s).
  - Sobre nó(s) existente(s): Seleciona o(s) nó(s).

**Botão Direito do Mouse Pressionado**

- Exclui o(s) nó(s) sob o cursor.
