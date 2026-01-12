# SSH Agent
SSH Agentのデーモンを立ち上げたのに鍵のパスフレーズ入力を毎度毎度求められる。
gitのSSHクライアントが正しくないのが原因だった。

```bash
git config --global core.sshCommand "C:/Windows/System32/OpenSSH/ssh.exe"
```
