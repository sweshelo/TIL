# Package Manager
パッケージマネージャを使う上での学びを記す。(なお私はBunを使っている。)

## Lifecycle Scripts
`bun install` などを実行した際に自動で動作するスクリプトを `package.json` の `scripts` 節に `preinstall` のような名前で定義しておくことができる。
しかしこれが開発用のパッケージを前提としていたりして、Dockerのイメージビルド時に足枷になる場合がある。そういった場合は `--ignore-scripts` という引数を与えて NPMスクリプトを実行すれば良い。
