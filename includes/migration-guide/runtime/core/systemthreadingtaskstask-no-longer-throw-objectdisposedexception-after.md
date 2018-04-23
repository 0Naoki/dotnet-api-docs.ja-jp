### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a>System.Threading.Tasks.Task は、オブジェクトが破棄された後、ObjectDisposedException をスローしなくなりました

|   |   |
|---|---|
|説明|<xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>を除き、<xref:System.Threading.Tasks.Task?displayProperty=name> メソッドでオブジェクトが破棄された後も <xref:System.ObjectDisposedException?displayProperty=name> の例外がスローされることがなくなりました。この変更により、キャッシュされたタスクを使用できるようになりました。 たとえば、メソッドで新しいタスクを割り当てる代わりに、既に完了した操作を表す、キャッシュされたタスクを返すことができます。 これは、タスクの任意のコンシューマーによって破棄されてしまうと、使用不可能になってしまう以前の .NET Framework のバージョンでは不可能でした。|
|提案される解決策|オブジェクトが破棄されたとき、Task メソッドが <xref:System.ObjectDisposedException?displayProperty=name> をスローしなくなったことに注意してください。 アプリが、タスクが破棄されたことを確認するために、この例外に依存していた場合は、<xref:System.Threading.Tasks.Task.Status> を使用してタスクのステータスを明示的に確認するように、アプリを更新する必要があります。|
|スコープ|マイナー|
|Version|4.5|
|型|ランタイム|

