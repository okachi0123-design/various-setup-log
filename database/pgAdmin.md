## pgAdmin 4のインストール

pgAdminは、PostgreSQLを画面上で操作するための管理ツールである。

PostgreSQL本体はWSLへインストールし、pgAdminはWindowsへインストールする。

### 1. pgAdmin公式ダウンロードページを開く

- URL: https://www.pgadmin.org/download/

### 2. Windows版をダウンロードする

以下のようなWindows 64bit版インストーラを選択する。

```text
pgadmin4-9.16-x64.exe
```

`CURRENT_MAINTAINER`は管理者情報のファイルであり、インストーラではない。

### 3. インストーラを実行する

ダウンロードした`.exe`ファイルを実行する。

個人のPCで使用する場合は、以下を選択する。

```text
Install for me only
```

### 4. 画面の指示に従ってインストールする

インストール先などは、基本的に初期設定のままで進める。

## 構成

```text
Windows
└── pgAdmin 4
    └── PostgreSQLを画面で操作するツール

WSL Ubuntu
└── PostgreSQL
    └── データベース本体
```
