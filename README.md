# JavaScript_test1

ローカルのvscodeにjs実行環境を構築したメモ  

js実行環境のインストールはprogateの記事を参考にした  
https://prog-8.com/docs/es6-env-win

vscodeの実行ログが文字化けしたので、以下の記事を参考にした  
https://confrage.jp/visual-studio-codeのターミナルの文字化けの回避方法/  

ファイル → 基本設定 → 設定  
検索窓に「terminal.integrated.shellArgs.windows」と入力し  
「setting.jsonで編集」を押下。  
以下のように編集した。  

```json
↓ もともと書いてあった  
{
    "git.autofetch": true,  
    "diffEditor.ignoreTrimWhitespace": false  
}  
↑ もともと書いてあった
↓ 追記
{
    "terminal.integrated.shellArgs.windows": [
      "/k",
      "chcp",
      "65001"
    ]
}
```
vscodeの拡張機能"runner"で実行できた。