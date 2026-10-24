```
git config --get credential.helper
```
これで、現在のMacに保存されている認証情報を更新すべきか、別の認証方法を設定すべきか判断できる

#### 結果
```
osxkeychain
```
osxkeychainなら、macOSのキーチェーンに保存されたGitHubの認証情報が古くなっている可能性が高い

### 古いGitHub認証情報を削除
```
printf "protocol=https\nhost=github.com\nusername=Takahiro-Kunii\n\n" | git credential-osxkeychain erase
```
指定したGitHubユーザーの保存済み認証情報を削除

git fetchを実行
```
git fetch origin
```
認証情報を聞かれたら、Usernameとgithubで用意したトークンを入力
