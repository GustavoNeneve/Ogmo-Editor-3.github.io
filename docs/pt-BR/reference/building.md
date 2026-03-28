# Compilando a partir do Código-Fonte

Este projeto requer Haxe, Node v10+ e diversas dependências para cada um deles.

## [Preparando o Node](#preparing-node)
* Instale o [Node](https://nodejs.org/)

## [Preparando o Haxe](#preparing-haxe)
* Instale o [Haxe](https://haxe.org/download/)
* Instale as seguintes Haxelibs:
```
haxelib install electron 4.1.4
haxelib install jQueryExtern
haxelib install haxe-loader
```

## [Compilando](#building)
```
npm i
npm run build
```
Isso compila o aplicativo e o coloca no diretório `bin`. Você pode então iniciá-lo executando `npm start`, ou iniciando o electron no diretório.

## [Desenvolvimento](#development)
Acelere o desenvolvimento usando o servidor de desenvolvimento do Webpack! Executar `npm run dev` compila o aplicativo, inicia um servidor que monitorará alterações no projeto e, em seguida, inicia o electron. Se alterações forem encontradas, o Webpack recompilará o código-fonte e atualizará o aplicativo. Se houver erros, eles aparecerão nas DevTools do aplicativo.

Enquanto o servidor de desenvolvimento estiver em execução, todo o código dentro dos condicionais `#if debug` será incluído.

NOTAS:
  * Alterações em `App.hx` não são monitoradas, e o aplicativo precisará ser recompilado manualmente se alterações forem feitas ali.
  * O aplicativo precisará ser recompilado normalmente (`npm run build`) para ser executado novamente após o uso do servidor de desenvolvimento.

## [Empacotando](#packaging)
```
npm i
npm run build
npm run dist
```
Isso compila e, em seguida, empacota o aplicativo em um executável.
