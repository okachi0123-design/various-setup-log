# SQLAlchemy

## SQLAlchemyとは

SQLAlchemyは、PythonからSQLデータベースを操作するためのライブラリ。

主に以下の機能がある。

- SQLAlchemy Core
- SQLAlchemy ORM

- `ORM`はPythonのコードとSQLクエリを繋げて実行してくれるので、SQLクエリの記述を省略できる

## 構築ログ

### 1.仮想環境を有効化する

```bash
source .venv/bin/activate
```
### 2.ライブラリをインストール
`pip install sqlakchemy `
#### なければSQLドライバ、SQL本体もインストール
`pip install psycopg2`
- psycopg2  PostgreSQL用ドライバ
- SQL本体は/SQL以下を参照

### 3.`pip list`などで確認
### 4.from importで接続
from sqlalchemy 
