### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>.NET で証明書を処理できないときに、X509Certificate2.ToString(bool) がスローしなくなった

|   |   |
|---|---|
|説明|以前は、このメソッドは、verbose パラメーターとして <code>true</code> が渡され、.NET Framework ではサポートされない証明書がインストールされていた場合、スローしました。 現在は、メソッドは成功し、証明書のアクセス不能部分を省いた有効な文字列を返します。|
|提案される解決策|<xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)> に依存しているコードは、以前は API がスローしていたような場合には、返される文字列から一部の証明書データ (公開鍵、秘密鍵、拡張子など) が除外されることを予期するように更新する必要があります。|
|スコープ|エッジ|
|Version|4.6|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

