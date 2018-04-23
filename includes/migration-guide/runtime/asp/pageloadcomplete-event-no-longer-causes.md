### <a name="pageloadcomplete-event-no-longer-causes-systemwebuiwebcontrolsentitydatasource-control-to-invoke-data-binding"></a>Page.LoadComplete イベントによって、System.Web.UI.WebControls.EntityDataSource コントロールがデータ バインディングを呼び出さなくなりました

|   |   |
|---|---|
|説明|<xref:System.Web.UI.Page.LoadComplete> イベントが原因で、<xref:System.Web.UI.WebControls.EntityDataSource?displayProperty=name> のコントロールがパラメーターの作成/更新/削除に変更を加えるためにデータ バインディングを呼び出すことがなくなりました。 この変更により、データベースへの不要なアクセスが排除され、コントロールの値がリセットされるのを防ぐことができるほか、<xref:System.Web.UI.WebControls.SqlDataSource?displayProperty=name> や <xref:System.Web.UI.WebControls.ObjectDataSource?displayProperty=name>などのように他のデータ コントロールと一貫性の取れた動作が生成されます。 この変更により、アプリケーションが <xref:System.Web.UI.Page.LoadComplete> イベントのデータ バインディングの呼び出しに依存するような珍しい状況において、異なる動作が生成されるようになりました。|
|提案される解決策|データバインドの必要がある場合は、ポストバックの前半であるイベントでデータバインドを手動で呼び出します。|
|スコープ|エッジ|
|Version|4.5|
|型|ランタイム|

