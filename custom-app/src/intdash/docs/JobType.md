# JobType

- update   - 計測内の動画データのうち、新しくサーバーが受信した部分（HLSにまだ変換されていない部分）を     HLSに変換するジョブ。通常は計測実行中に行います。 - finalize   - 計測全体をサーバーに回収した後に、動画データ全体をHLSに変換するジョブ - delete   - 変換によって作成されたHLSデータを削除するジョブ。     このジョブを実行すると、HLSプレイリスト、セグメントファイル、     データベース内のHLSに関する情報が削除され、この動画のHLSによる再生はできなくなります。

## Enum

* `Update` (value: `'update'`)

* `Finalize` (value: `'finalize'`)

* `Delete` (value: `'delete'`)

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
