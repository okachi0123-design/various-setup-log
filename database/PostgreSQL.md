# PostgreSQL インストール方法

## 注意

- PostgreSQLの`5432`番ポートをインターネットへ公開しない。
- Windows版とWSL版のPostgreSQLを同時にインストールすると、接続先が分かりにくくなるため、今回はWSL版を使用する。
- `sudo`で入力するパスワードは、PostgreSQLのパスワードではなくWSLユーザーのパスワードである。

## 工程

### 1. WSLのUbuntuを起動する

Windows TerminalまたはVS Codeから、WSLのUbuntuを開く。

### 2. パッケージ情報を更新する

```bash
sudo apt update
```

### 3. PostgreSQLをインストールする

```bash
sudo apt install postgresql
```

途中で確認された場合は、`Y`を入力してEnterを押す。

### 4. PostgreSQLのインストールを確認する

```bash
psql --version
```

PostgreSQLのバージョンが表示されれば、インストールできている。

### 5. PostgreSQLを起動する

```bash
sudo service postgresql start
```

### 6. PostgreSQLの状態を確認する

```bash
sudo service postgresql status
```

以下のように表示される場合がある。

```text
Active: active (exited)
```

これはPostgreSQL全体を管理する親サービスの状態であり、異常ではない。

実際のPostgreSQLクラスタの状態は、以下のコマンドで確認する。

```bash
pg_lsclusters
```

`Status`が`online`になっていれば、PostgreSQLは起動している。

```text
Ver Cluster Port Status Owner
16  main    5432 online postgres
```

### 7. PostgreSQLへ接続する

```bash
sudo -u postgres psql
```

以下の表示になれば、PostgreSQLへの接続に成功している。

```text
postgres=#
```

### 8. PostgreSQLのユーザーを確認する

PostgreSQLへ接続した状態で、以下を実行する。

```sql
\du
```

インストール時に、管理者ユーザーとして`postgres`が自動作成される。

### 9. データベース一覧を確認する

```sql
\l
```

### 10. PostgreSQLを終了する

```sql
\q
```
