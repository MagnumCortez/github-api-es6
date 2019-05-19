### Instalando Babel

```sh
yarn add @babel/cli -D

yarn add @babel/preset-env - D

yarn add @babel/core -D
```

Criando e Configurando Babel - .babelrc
```js
{
	"presets": ["@babel/preset-env"],
}
```

Adicionado script - package.json
```js
"scripts": {
	"dev": "babel ./src/main.js -o ./src/bundle.js"
}
```

### Intalando Webpack

```sh
yarn add webpack webpack-cli -D

yarn add babel-loader -D
```

Configurando Webpack - webpack.config.js
```js
module.exports = {
	entry: './src/main.js',
	output: {
		path: __dirname + '/public',
		filename: 'bundle.js',
	},
	devServer: {
		contentBase:  __dirname + '/public'
	},
	module: {
		rules: [
			{
				test: /\.js$/,
				exclude: /node_module/,
				use: {
					loader: 'babel-loader',
				}
			}
		],
	}
}
```

Alterando configuração para webpack - package.json
```js
"scripts": {
	"dev": "webpack --mode=development -w"
}
```

### Intalando Webpack Dev Server

```sh
yarn add webpack-dev-server -D
```

Alterando configuração para webpack-dev-server - package.json
```js
"scripts": {
	"dev": "webpack-dev-server --mode=development"
}
```

### Intalando Axios

```sh
yarn add axios
```

### Intalando Async do ES8 e Polyfill

```sh
yarn add @babel/plugin-transform-async-to-generator -D

yarn add @babel/polyfill -D
```

Configurando o plugin async - .babelrc
```js
{
	"presets": ["@babel/preset-env"],
	"plugins": [
		"@babel/plugin-transform-async-to-generator"
	]
}
```

Configurando o plugin polyfill - webpack.config.js
```js
entry: ['@babel/polyfill', './src/main.js'],
```
