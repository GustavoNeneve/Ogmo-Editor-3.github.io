# Personalização de Projeto

Cada jogo tem requisitos e preferências diferentes quanto ao tratamento de dados. Para suportar esses casos de uso únicos, o OGMO Editor oferece a capacidade de substituir comportamentos usando hooks JavaScript. Esses hooks são um recurso avançado e não são necessários para o uso normal, mas são ótimos para quem deseja personalizar a saída do OGMO Editor.

# Configuração

Na visualização de `Project Settings`, defina `External Script Location` como o caminho para um arquivo `.js`, relativo ao local do projeto. O script neste local será executado quando um projeto for carregado ou quando o projeto for salvo.

# Configuração do Script

Quando o script é executado, o valor de retorno da última instrução executada deve ser um objeto com uma função para cada ponto de substituição. Um exemplo de script é fornecido abaixo, que recomendamos usar como ponto de partida.

```js
function hook() {
  const fs = require('fs');

  console.log('Project is loaded!');

  return {
    beforeLoadLevel: (project, data) => {
      for (let layer of data.layers) {
        if (!layer.data) continue;
        layer.data = layer.data.map(tile => tile === 0 ? -1 : tile);
      }

      return data;
    },

    beforeSaveLevel: (project, data) => {
      for (let layer of data.layers) {
        if (!layer.data) continue;
        layer.data = layer.data.map(tile => tile === -1 ? 0 : tile);
      }
      return data;
    },

    beforeSaveProject: (project, data) => {
      data.customProjectProperty = Math.random();
      return data;
    }
  }
}

hook();
```

Neste exemplo, o módulo `fs` do Node.js é carregado, mas não utilizado, apenas para fins de demonstração. Quando um nível é salvo, o script modifica os tilemaps para que os tiles vazios sejam salvos com o valor `0`, e não `-1` como é o padrão. Ao carregar o nível, essa alteração é revertida para que o OGMO Editor ainda trate essas células como vazias. Quando o projeto é salvo, um número aleatório é atribuído a uma propriedade no arquivo do projeto chamada `customProjectProperty`.

# Hooks Disponíveis

  - `BeforeLoadLevel(project, data)` - Modifica o objeto de nível em `data` após o nível ter sido lido do sistema de arquivos e parseado. Esta é a última etapa antes que o nível seja retornado ao editor.

  - `BeforeSaveLevel(project, data)` - Modifica o objeto de nível em `data` antes que o objeto de nível seja serializado e gravado no sistema de arquivos.

  - `BeforeSaveProject(project, data)` - Modifica o objeto de projeto em `data` para alterar o projeto que é salvo no sistema de arquivos.

# Detalhes Técnicos

Os scripts são carregados através do módulo `vm` do Node.js e são executados no mesmo contexto do editor. Isso significa que os scripts têm acesso para carregar módulos Node.js via `require` e todos os outros recursos JavaScript integrados. Como um script pode ser executado múltiplas vezes durante a vida útil do OGMO Editor, variáveis declaradas com `const` não podem ser redeclaradas. Ao envolver todo o script em uma função, você garante que os scripts não poluam desnecessariamente o namespace global, e as variáveis `const` serão adequadamente redeclaradas.

Executar no mesmo contexto do OGMO Editor também significa que há acesso irrestrito ao DOM e aos objetos do OGMO Editor. Tenha cuidado ao modificar os internos do editor, pois não é possível garantir que alterações não tenham efeitos negativos no futuro.
