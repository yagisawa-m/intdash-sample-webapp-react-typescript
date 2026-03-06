# MeasurementSequenceGroupReplace


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**expected_data_points** | **number** | この計測シーケンスでサーバーが受信することが想定されるデータポイントの総数 （既に受信済みのデータポイントを含む） 符号なし64bit整数。 | [optional] [default to undefined]
**final_sequence_number** | **number** | 最後の計測シーケンスの番号 | [optional] [default to undefined]

## Example

```typescript
import { MeasurementSequenceGroupReplace } from './api';

const instance: MeasurementSequenceGroupReplace = {
    expected_data_points,
    final_sequence_number,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
