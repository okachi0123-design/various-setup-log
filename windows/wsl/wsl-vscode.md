# WSLとVScodeを活用した開発環境の設定ログ

## 工程
### 1.WSLを起動(ここではubuntu)　なければ用意`../wsl.md`
### 2.なければVScodeを用意　various-setup-log/vscode/vscode.md
### 3.VSCodeを開いてWSL拡張機能をインストール　
- 左側の拡張機能を選択→WSLと検索→インストール
- ＊名前（WSL  Microsoft  microsoft.com）
### 4.WSL内に作業用ディレクトリを用意、作業ディレクトリに移動　
- `mkdir -p ~/dirname`
- `cd ~/dirname`
### 5.WSLからVSCodeを開く　 
- `code .`
- VSCodeを開いて、（DIRNAME [WSL:UBUNTU]）の項目が出れば成功
### 6.諸設定を済ませる
- 最初に制限モードになる場合があるので、上の青いバーの管理から「このフォルダーを信頼する」を選択して、機能を有効化
### 7.VSCode内でWSLターミナルを起動
- （Ctrl + `）or メニューから（ターミナル → 新しいターミナル）→ 登録した作業用ディレクトリが`pwd`の状態でターミナルが開かれる
### 8.そのターミナルで開発用ファイルを作る
- ターミナルで`touch filename.（pyなど）`を打ってファイルを作成
- そのファイルの項目ができるので、そこにコードを打ち込めば開発できる
