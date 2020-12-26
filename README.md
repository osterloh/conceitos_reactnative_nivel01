<h1 align="center"><a href="https://pt-br.reactjs.org/" target="_blank" style="text-decoration: none">
    <img alt="ReactJs" src="./assets/logo.svg" width="50%"/>
    <br>
    Introdução ao ReactJs
</a></h1>

## Descrição

Este projeto foi desenvolvido em <strong>[React Native](https://reactnative.dev/)</strong> para fins de capacitação pessoal

## Como Usar

Para clonar e executar este aplicativo, você precisará [Git](https://git-scm.com), [Node.js v12.20.0](https://nodejs.org/) ou superior + [Yarn 1.22.5](https://yarnpkg.com/) ou superior, [Android Studio](https://developer.android.com/studio) e [Java 8](https://www.oracle.com/br/java/technologies/javase/javase-jdk8-downloads.html) instalado no seu computador.

- Para configurar o Android Studio é possível seguir o tutorial desenvolvido pela equipe da (Rocketseat)[https://rocketseat.com.br/], clicando <strong>[aqui](https://react-native.rocketseat.dev/)</strong>.

- Executar no seu terminal:

```bash
# Para clonar este repositório
$ git clone https://github.com/osterloh/conceitos_reactnative_nivel01.git

# Entrar no repositório
$ cd conceitos_reactnative_nivel01

# Instalar as dependências
$ yarn

#  Executar o sistema
$ react-native run-android
$ yarn start
```

## Etapas do desenvolvimento do projeto

- Antes de iniciar o projeto React Native, é necessário ter o CLI do React Native instalado:

```js
yarn global add react-native-cli
```

- Com o CLI instalado podemos definir em qual diretório o projeto irá ficar armazendo e executar o comando para criar o projeto, neste exemplo utilizei o nome <u>mobile</u> para o projeto:

```js
react-native init mobile
```

- Após criar o projeto podemos entrar no diretório criado:

```js
cd mobile
```

- Para compilar o projeto, executamos o <i>react-native run-android </i> e para abrir o <strong>Metro Bundle</strong>, que responsável por construir o BUNDLE para que o dispositivo consiga interpretar o conteúdo desenvolvido e mostrar em tela:

```js
react-native run-android
yarn start
```

- No React Native não utilizamos elementos HTML, como por exemplo:

```bash
* <div>
* <h1>
* <p>
* ...
```

- No React Native utilizamos elementos que são exportados do pacote do react-native, e os elementos não possuem valor semântico (significado), não possuem estilização própria e todos os componentes possuem por padrão 'display: flex'. Por exemplo:

```bash
* View: div, footer, header, main, aside, section.
* Text: p, span, strong, h1, h2, h3.
```

- Para configurar a estilização das páginas, é necessário importar o StyleSheet do react-native. A estilização é feita diretamente via código Javascript e não em um arquivo <strong>.css</strong>. Os elementos que serão estilizados são declarados no formato CamelCase, caso seja um elemento compost, e não separado por (-) como nos arquivos css:

```js
import React from "react";
import { View, StyleSheet } from "react-native";

export default function App() {
  return <View />;
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: "#7159c1",
  },
});
```

- Para aplicar o estilo configurado, basta chamar o estilo através do style:

```js
export default function App() {
  return <View style={styles.container} />;
}
```

- A estilização deve ser aplicada para cada elemento, pois eles não são herdados de elemento pai para elementos filhos:

```js
import React from "react";
import { View, Text, StyleSheet } from "react-native";

export default function App() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>Hello World!</Text>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: "#7159c1",
    justifyContent: "center",
    alignItems: "center",
  },
  title: {
    color: "#FFF",
    fontSize: 32,
    fontWeight: "bold",
  },
});
```

## Tecnologias

- [React Native](https://reactnative.dev/)
- [yarn](https://yarnpkg.com/)
- [Android Studio](https://developer.android.com/studio)

---

Desenvolvido por [Johnatan Luiz Osterloh](https://www.linkedin.com/in/johnatanosterloh/)
