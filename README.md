
#Dependências

### Intalando Babel

yarn add @babel/cli -D

yarn add @babel/preset-env - D

yarn add @babel/core -D

// Executar babel - package.json
"scripts": {
	"dev": "babel ./src/main.js -o ./src/bundle.js"
}


### Intalando Webpack

yarn add webpack webpack-cli -D

yarn add babel-loader -D

// Executar webpack - package.json
"scripts": {
	"dev": "webpack --mode=development -w"
}


### Intalando Webpack Dev Server

yarn add webpack-dev-server -D

// Executar webpack-dev-server - package.json
"scripts": {
	"dev": "webpack-dev-server --mode=development"
}

### Intalando Axios

yarn add axios


### Intalando async e Await do ES8

yarn add @babel/plugin-transform-async-to-generator -D

// configurando o plugin - .babelrc
"plugins": [
	"@babel/plugin-transform-async-to-generator"
]

yarn add @babel/polyfill -D

// configurando o plugin - webpack.config.js
entry: ['@babel/polyfill', './src/main.js'],