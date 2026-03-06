# UpdateMeasBaseTime


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**basetime** | **string** | 基準時刻（計測が開始された時刻）（RFC3339形式） | [optional] [default to undefined]
**priority** | **number** | 基準時刻の優先度 | [optional] [default to undefined]
**name** | **string** | 基準時刻の名前 | [optional] [default to undefined]
**elapsed_time** | **number** | 基準時刻を受信した基準時刻からの経過時間（ナノ秒）。 | [optional] [default to undefined]

## Example

```typescript
import { UpdateMeasBaseTime } from './api';

const instance: UpdateMeasBaseTime = {
    basetime,
    priority,
    name,
    elapsed_time,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
