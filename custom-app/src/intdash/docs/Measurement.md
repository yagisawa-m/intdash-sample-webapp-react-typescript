# Measurement


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | 計測のUUID | [default to undefined]
**name** | **string** | 計測の名前 | [default to undefined]
**description** | **string** | 計測の説明 | [default to undefined]
**basetime** | **string** | 計測の基準時刻（RFC3339形式） | [default to undefined]
**basetime_type** | [**MeasurementBaseTimeType**](MeasurementBaseTimeType.md) |  | [default to undefined]
**max_priority_basetime_id** | **number** | 現在設定されている基準時刻ID | [optional] [default to undefined]
**edge_uuid** | **string** | エッジのUUID | [default to undefined]
**duration** | **number** | 計測時間（ &#x60;max_elapsed_time&#x60; を使用してください） | [default to undefined]
**max_elapsed_time** | **number** | 計測時間（マイクロ秒） | [optional] [default to undefined]
**completed** | **boolean** | &#x60;true&#x60; の場合、この計測はサーバーへのデータの回収が完了しています。 | [optional] [default to undefined]
**_protected** | **boolean** | &#x60;true&#x60; の場合、計測は保護されています。保護されている計測は削除できません。 保護されている計測を削除したい場合は、まず保護を解除してください。 | [default to undefined]
**sequences** | [**MeasurementSequencesSummary**](MeasurementSequencesSummary.md) |  | [default to undefined]
**markers** | [**Array&lt;MeasurementMarker&gt;**](MeasurementMarker.md) |  | [optional] [default to undefined]
**created_at** | **string** | 計測の作成日時 | [default to undefined]
**updated_at** | **string** | 計測の最終更新日時 | [default to undefined]
**processed_ratio** | **number** | 代わりに &#x60;sequences.received_chunks_ratio&#x60; を使用してください。処理済み率を表します。 | [default to undefined]
**ended** | **boolean** | 代わりに &#x60;sequences.status&#x60; を使用してください。エッジにおいてデータの取得が終了しているかどうかを示します。 | [default to undefined]
**status** | **string** | 代わりに &#x60;sequences.status&#x60; を使用してください。 計測のステータスを表します:   - measuring     - 計測中   - resending     - 再送中。計測（エッジにおけるデータの取得）は終了しましたが、エッジにデータが残っており、サーバーに再送中です。   - finished     - 完了。サーバーへのデータの回収が完了しています。 | [default to undefined]
**received_data_points** | **number** | 代わりに &#x60;sequences.received_data_points&#x60; を使用してください。 サーバーが受信したデータポイントの数。符号無し64bit整数。 | [default to undefined]

## Example

```typescript
import { Measurement } from './api';

const instance: Measurement = {
    uuid,
    name,
    description,
    basetime,
    basetime_type,
    max_priority_basetime_id,
    edge_uuid,
    duration,
    max_elapsed_time,
    completed,
    _protected,
    sequences,
    markers,
    created_at,
    updated_at,
    processed_ratio,
    ended,
    status,
    received_data_points,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
