# Git
Gitを使う上での学びを記す。

## コミットに署名する
GitHubでのコミッターはメールアドレスベースの判定を行っているので割と簡単に偽装できる。
コミットに署名をすると間違いなく自分のコミットであることを証明できる。

### GPGの鍵生成
```
gpg --full-generate-key
```

鍵の種類は「RSA と RSA (デフォルト)」を選択。その他は聞かれた通りに回答。

### 署名に用いる鍵の特定
```
gpg --list-secret-keys --keyid-format LONG
```

上記のコマンドを実行すると、登録されている鍵の一覧が確認できる。鍵の用途が `SC` となっている鍵があるはずなので、それを出力する。

```
sec   rsa4096/1234567890ABCDEF 2025-12-25 [SC] [expires: 2029-12-25]
```

上記でいう `1234567890ABCDEF` が鍵名に当たる。(「鍵名」という表現が正しいのかはわからない。)

```
gpg --armor --export [鍵名]
```

公開鍵が出力される。これをGitHubに登録する。

### 基本的な手順
https://docs.github.com/ja/authentication/managing-commit-signature-verification/signing-commits