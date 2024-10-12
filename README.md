# PostgreSQL基本操作

## DataBaseの概要
DataBaseの作成から接続、一覧表示、削除など基本的な操作手順を記す

## セットアップ手順

手順1. **データベース作成**:
    まず、postgres データベースに接続し、データベースを作成する
    ```bash
    psql -U Action0358 -d postgres
    ```
    そして、PostgreSQL のプロンプトで以下の SQL 文を実行して mydatabase を作成する
    ```sql
    CREATE DATABASE mydatabase;
    ```
    データベース一覧を確認して、mydatabase が作成されたことを確認できる
    ```sql
    \l
    ```

手順2. **SQL スクリプトの実行**:
    シェルに戻り、データベースが作成された後に SQL スクリプトを実行する
    ```bash
    psql -U Action0358 -d mydatabase -f /Pg_Practice/DataBase/create_table.sql
    ```
    これで、mydatabase にテーブルが作成される

手順3. **テーブル一覧表示**:
    mydatabase に接続する
    ```bash
    psql -U Action0358 -d mydatabase
    ```
    インタラクティブモードでテーブル一覧を確認
    ```sql
    \dt
    ```

## 補足

1. **別のデータベースに接続（今回は postgres に接続とする）**
    ```sql
    \c postgres
     ```

2. **データベースの削除(今回は mydatabase とする)**
    ```sql
    DROP DATABASE mypostgres;
     ```


## SQL操作
QLスクリプトをファイルごとに分けて保存して実行する

**データ挿入**
    ```bash
    psql -U Action0358 -d mydatabase -f /Pg_Practice/DataBase/insert_data.sql
    ```

**データ取得**
    ```bash
    psql -U Action0358 -d mydatabase -f /Pg_Practice/DataBase/select_data.sql
    ```
    データを確認するために、データを取得するクエリを実行する

**データ更新**
    ```bash
    psql -U Action0358 -d mydatabase -f /Pg_Practice/DataBase/update_data.sql
    ```


**データ削除**
    ```bash
    psql -U Action0358 -d mydatabase -f /Pg_Practice/DataBase/delete_data.sql
    ```