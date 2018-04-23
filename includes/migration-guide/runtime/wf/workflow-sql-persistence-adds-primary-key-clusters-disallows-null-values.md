### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>Workflow SQL の永続化で主キー クラスターが追加され、一部の列の null 値が許可されない

|   |   |
|---|---|
|説明|.NET Framework 4.7 以降では、SqlWorkflowInstanceStoreSchema.sql スクリプトで SQL Workflow Instance Store (SWIS) に作成されたテーブルにはクラスター化された主キーが使用されます。 そのため、ID では <code>null</code> 値はサポートされません。 SWIS の操作には、この変更による影響はありません。 SQL Server トランザクション レプリケーションをサポートするように更新されました。|
|提案される解決策|この変更では、SQL ファイルの SqlWorkflowInstanceStoreSchemaUpgrade.sql を既存のインストールに適用する必要があります。 新しいデータベースのインストールは自動的に変更されます。|
|スコープ|エッジ|
|Version|4.7|
|型|ランタイム|

