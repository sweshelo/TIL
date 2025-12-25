# フックの話

## Linter 

JSのLintに長らく ESLint + Prettier を使って、これらを Lint-staged と husky で動かすということをやっていたが、coderabbitai が Biome を使っているのを見て、一部のリポジトリで移行してみた。

BiomeがESLintとPrettierの両方を代替できる。

## Hooks

ついでにHooksについても [lefthook](https://github.com/evilmartians/lefthook) というものがあり、こちらも Linter-staged と husky を代替出来そうだった。YAMLでGitコマンド実行時のフックを定義する。

## Oxc
…という代替をやったところ、[Oxc Project](https://github.com/oxc-project)が開発している [Oxlint](https://github.com/oxc-project/oxc)というのがもっと爆速らしいという情報を得た。

OxlintはBiomeと違い、ESLintの代替を目指しているらしい。