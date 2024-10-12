# PostgreSQL基本操作

## DataBaseの概要
このドキュメントでは、データベースの作成から接続、一覧表示、削除など基本的な操作手順を記す

## セットアップ手順

### 手順1: データベース作成
1. PostgreSQL に接続する
    ```bash
    psql -U Action0358 -d postgres
    ```
2. PostgreSQL のプロンプトで以下の SQL 文を実行して `mydatabase` を作成する
    ```sql
    CREATE DATABASE mydatabase;
    ```
3. データベース一覧を確認して、`mydatabase` が作成されたことを確認する
    ```sql
    \l
    ```

### 手順2: SQL スクリプトの実行
1. データベースが作成された後、シェルに戻り、以下のコマンドで SQL スクリプトを実行する
    ```bash
    psql -U Action0358 -d mydatabase -f /Pg_Practice/DataBase/create_table.sql
    ```

### 手順3: テーブル一覧表示
1. mydatabase に接続する
    ```bash
    psql -U Action0358 -d mydatabase
    ```
2. インタラクティブモードでテーブル一覧を確認する
    ```sql
    sql \dt
    ```

### 補足操作
1. 別のデータベースに接続（今回は postgres に接続とする）
    ```sql
    \c postgres
    ```
2. データベースの削除(今回は mydatabase とする)
    ```sql
    DROP DATABASE mydatabase;
    ```