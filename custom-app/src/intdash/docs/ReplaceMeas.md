# ReplaceMeas


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | 計測の名前 | [optional] [default to undefined]
**description** | **string** | 計測の説明 | [optional] [default to undefined]
**basetime_type** | [**MeasurementBaseTimeType**](MeasurementBaseTimeType.md) | 計測の基準時刻タイプ **非推奨** 代わりに基準時刻APIを使用して、当該基準時刻の優先度を明示的に設定してください。この値をセットすると、基準時刻タイプの優先度を強制的に一番高いものに変更します。 | [optional] [default to undefined]

## Example

```typescript
import { ReplaceMeas } from './api';

const instance: ReplaceMeas = {
    name,
    description,
    basetime_type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
