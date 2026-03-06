# MeasurementSequenceGroup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | 計測シーケンスのUUID | [default to undefined]
**expected_data_points** | **number** | この計測シーケンスでサーバーが受信することが想定されるデータポイントの総数 （既に受信済みのデータポイントを含む） 符号なし64bit整数。 | [optional] [default to undefined]
**received_data_points** | **number** | この計測シーケンスでサーバーが受信したデータポイントの総数 符号なし64bit整数。 | [optional] [default to undefined]
**received_chunks_count** | **number** | サーバーが受信したシーケンスチャンクの総数。 | [optional] [default to undefined]
**final_sequence_number** | **number** | 最後の計測シーケンスの番号。 | [optional] [default to undefined]
**created_at** | **string** | 作成日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]

## Example

```typescript
import { MeasurementSequenceGroup } from './api';

const instance: MeasurementSequenceGroup = {
    uuid,
    expected_data_points,
    received_data_points,
    received_chunks_count,
    final_sequence_number,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
