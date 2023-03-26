<div width="100%">
  <img src="https://user-images.githubusercontent.com/76600539/227807021-b1312dae-d393-4146-b5b5-0d8439c28847.png" alt="Testing library logo" width="45%" height="300px">
  <img src="https://user-images.githubusercontent.com/76600539/227807062-e41adb47-8829-4f3d-ab2e-ab9c3c5a6514.png" alt="jest logo" width="45%" height="300px">
</div>


# Configuração para testes

*config para Vite + React.js + Typescript*
### Instalação de Dependencias

**gerando um arquivo de configuração básico**
```

npx jest --init

```

**alterando a propriedade `transform` em `jest.config.js`**
*[link stackoverflow](https://stackoverflow.com/questions/56547215/react-testing-library-why-is-tobeinthedocument-not-a-function)*
```js
module.exports = {
  transform: {
     '^.+\\.(ts|tsx)?$': 'ts-jest',
    "^.+\\.(js|jsx)$": "babel-jest",
  },
};

```


**instalando o [babel](https://jestjs.io/docs/getting-started#using-babel)**
```

npm install --save-dev babel-jest @babel/core @babel/preset-env

```

**instalar o `@babel/preset-typescript`**
```

npm install --save-dev @babel/preset-typescript

```

** configurando o `babel.config.js`**
```javascript
\\ babel.config.js

module.exports = {
  presets: [
    ['@babel/preset-env', {targets: {node: 'current'}}],
    '@babel/preset-typescript',
  ],
};
```

**configurando o [ts-jest](https://github.com/kulshekhar/ts-jest)**

_não precisa exucutar o `npx ts-jest config:init`_

|                     | using npm                      | using yarn                           |
| ------------------: | ------------------------------ | ------------------------------------ |
|  **Prerequisites** | `npm i -D jest typescript`     | `yarn add --dev jest typescript`     |
|     **Installing** | `npm i -D ts-jest @types/jest` | `yarn add --dev ts-jest @types/jest` |
|**Creating config** | `npx ts-jest config:init`      | `yarn ts-jest config:init`           |
|  **Running tests** | `npm test` or `npx jest`       | `yarn test` or `yarn jest`           |
****


**importando `@jest/globals`**

```
npm install --save-dev @jest/globals

```

**instalando o ts-node**

```
npm install --save-dev ts-node

```

**instalando o jest-environment-jsdom**

```
npm install --save-dev jest-environment-jsdom

```

**instalando todas dependencia de uma só vez**
```
npm i  @babel/core @babel/preset-env @babel/preset-typescript @jest/globals @types/jest babel-jest jest jest-environment-jsdom ts-jest ts-node typescript -D

```

### Testing Library
**instalando @testing-library/jest-domcomponents**
```
npm install --save-dev @testing-library/jest-dom

```


**instalando a Dom Testing library (teste para Web UI)**
```
npm install --save-dev @testing-library/dom

```


**instalando a React Testing Library (*DOM Testing Library by adding APIs for working with React components*)**
```
npm install --save-dev @testing-library/react

```
**Doc**
- [Jest](https://jestjs.io/docs/configuration)
- [Testing Library](https://testing-library.com/)
- [Babel](https://babeljs.io/docs/)
