# Generative AI
生成AIに関する情報を記す。

## TOON
Token Oriented Object Notiation の略。生成AIに渡されるテキストデータにおいて、JSONにおけるデータ構造を示す `{` などもトークンとして消費されることから、不要なトークンを排除することを念頭においたデータ構造らしい。

CSVを彷彿とさせるヘッダには、データの件数が先に提示されている。

```toon
user[1]{name,birth,country}:
sweshelo, 09-07, Japan
```

ライブラリもある。
https://github.com/toon-format/toon
