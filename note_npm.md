## NPMって？
- https://www.npmjs.com/
- Node Package Manager
- Node.jsをインストールしたら一緒にインストールされる
- コマンドプロンプトやVisual Studio Codeのターミナルでコマンドを実行する

## 参考
- https://techacademy.jp/magazine/16105
- https://qiita.com/maitake9116/items/7825d90c09f3e2f87dea

## npmのバージョンを表示する
```
npm --version
```

## インストールされているパッケージを表示する
- listは"ls"で略せる
```
npm list
```
- "-g"はglobalの略、どのディレクトリからでも利用できるパッケージ
```
npm list -g
```

## 初期化、package.jsonを作成する
- package.jsonにインストールしたパッケージやスクリプトを書くことができる
- package.jsonを作成するにあたり、いろいろと入力を求められるがEnterキー連打でOK
```
npm init
```
- 作成直後のpackage.jsonは以下のとおり
```json
{
  "name": "notenode",
  "version": "1.0.0",
  "description": "Node.jsの備忘録",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/HayaUp/NoteNode.js.git"
  },
  "author": "",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/HayaUp/NoteNode.js/issues"
  },
  "homepage": "https://github.com/HayaUp/NoteNode.js#readme"
}
```

## パッケージをインストールする
- installは"i"で略せる
- package.jsonに"dependencies"フィールドが追加される

    インストールしたパッケージ名とバージョンが記述される
```
npm install package_name
```
- global install
```
npm install -g package_name
```
- 開発用としてインストールするなら"--save-dev"をつける

    dependenciesではなく"devDependencies"にパッケージ名とバージョンが記述される
```
npm install --save-dev package_name
```

## パッケージをアンインストールする
```
npm uninstall package_name
```
- global uninstall
```
npm uninstall -g package_name
```

## package.jsonのscriptsを実行する
```
npm run script_name
```
- pacakge.jsonのscriptsに記したスクリプトを実行する
```
npm run test
```