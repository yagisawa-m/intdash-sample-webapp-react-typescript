# MeasurementSequencesSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**received_chunks_ratio** | **number** | シーケンスチャンク回収率。計測内に含まれるシーケンスチャンクのうち、 サーバーへの保存が完了したシーケンスチャンクの割合です。 | [optional] [default to undefined]
**received_data_points** | **number** | サーバーが受信したデータポイントの数。符号無し64bit整数。 | [optional] [default to undefined]
**expected_data_points** | **number** | サーバーが受信することが想定されるデータポイントの総数（既に受信済みのデータポイントを含む）。符号無し64bit整数。 | [optional] [default to undefined]
**status** | **string** | 計測のステータス:   - ready     - 計測準備中   - measuring     - 計測中   - resending     - 再送中。計測（エッジにおけるデータの取得）は終了しましたが、エッジにデータが残っており、サーバーに再送中です。   - finished（非推奨。段階的にcompletedへ移行）     - 完了。サーバーへのデータの回収が完了しています。   - completed     - 完了。サーバーへのデータの回収が完了しています。 | [optional] [default to undefined]

## Example

```typescript
import { MeasurementSequencesSummary } from './api';

const instance: MeasurementSequencesSummary = {
    received_chunks_ratio,
    received_data_points,
    expected_data_points,
    status,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
