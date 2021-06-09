# use webpack

yarn build で出力される結果を比較する。

## require/module.export

```
// index.js

const message = require('./message');
console.log(message);
```

```
// message.js

module.exports = 'Hi there!';
```

## import/export

```
// index.js

import message from './message';
console.log(message);
```

```
// message.js

export default 'Hi there!';
```

## 結果

上記２つの結果であっても、bundle できることがわかるが、出力される結果は異なる。
出力先は dist ディレクトリにある。
というか、babel などの設定がなくても webpack 使えるのね。

## NPM install / https://webpack.js.org/plugins/npm-install-webpack-plugin/
