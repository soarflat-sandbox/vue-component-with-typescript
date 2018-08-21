# vue-component-with-typescript

## TypeScript で Vue.js（Vue コンポーネント）を書くために必要なもの（webpack でのビルド前提）

- [ts-loader](https://github.com/TypeStrong/ts-loader)
- [vue-class-component](https://github.com/vuejs/vue-class-component)
- [vue-property-decorator](https://github.com/kaorun343/vue-property-decorator)
- `vue-shims.d.ts`

### vue-class-component

TypeScript のクラス構文で Vue コンポーネントを定義できる。

本来のオブジェクト構文より、クラス構文の方が見通しがよくなる。

### vue-property-decorator

Vue コンポーネントに関連する様々なデコレータ（`@Watch`や`@Prop`など）を利用できる（vue-class-component に依存している）。

vue-class-component を利用するだけよりも、より見通しの良いクラス構文を書ける。

### `vue-shims.d.ts`

SFC（拡張子が`.vue`のファイル）を TypeScript ファイルとして認識させるために必要。

本リポジトリのように開発ディレクトリ（今回は`src`）に配置するだけで良い。
