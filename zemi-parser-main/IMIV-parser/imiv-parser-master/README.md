# imiv-parser

IMI Vocabulary Notation parser for JavaScript

このライブラリは [IMI共通語彙基盤ライブラリ　バージョン1.0.0 (2018年9月7日 公開, MIT ライセンス)](https://imi.go.jp/goi/library/ver100) からのフォークであり、IMI語彙記法のパーサ機能を単体で利用できるようにしたものです。

最新のIMI語彙記法の文法に対応して更新していく予定です。

# License

imiv-parser is released under the MIT License.

# Installation

## npm

```shell
$ npm install imiv-parser
```

### browser

```html
<script src="https://unpkg.com/imiv-parser/imiv-parser.js"></script>
```

# Usage

## Node

```js
const IMIVParser = require("imiv-parser");
const result = IMIVParser.parse(`...`);
console.log(JSON.stringify(result,null,2));
```

## browser

```js
//  API will be available in the IMIVParser global object.
const result = IMIVParser.parse(`...`);
console.log(JSON.stringify(result,null,2));
```

# Compatibility

imiv-parser is generated by [PEG.js 0.10.0](https://pegjs.org/), and  generated parsers should run well in the following environments :

-   Node.js 0.10.0+
-   Internet Explorer 8+
-   Edge
-   Firefox
-   Chrome
-   Safari
-   Opera

(Above list is copied from <https://pegjs.org/documentation#compatibility> )

# Planning

- ~~準拠するスペックを [IMI語彙記法 ワーキングドラフト](https://imi.go.jp/goi/vocabularynotation-spec_wd) から [IMI語彙記法 バージョン1.0](https://imi.go.jp/goi/vocabularynotation-spec)  にアップデート~~
- ~~NPM に登録する~~

# Changelog

## 0.1.0 (2018-11-02)

[IMI語彙記法 ワーキングドラフト](https://imi.go.jp/goi/vocabularynotation-spec_wd) に対応した初版

## 1.0.0 (2018-11-05)

[IMI語彙記法 バージョン1.0](https://imi.go.jp/goi/vocabularynotation-spec) に対応。

- `datamodel` に対する制約指定が文法から除外されたことを反映した
- `class` に対する制約指定文法が **ゼロまたは任意の制約** であったものが **ゼロまたはひとつの型制約** に変更されたことを反映した

## 1.0.1 (2018-12-10)

- NPM に登録
- README を NPM 対応に修正