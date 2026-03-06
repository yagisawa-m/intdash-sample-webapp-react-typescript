# CreateMeasBaseTime


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**basetime** | **string** | 基準時刻（計測が開始された時刻）（RFC3339形式） | [default to undefined]
**priority** | **number** | 基準時刻の優先度 | [default to undefined]
**name** | **string** | 基準時刻の名前 | [default to undefined]
**elapsed_time** | **number** | 基準時刻を受信した基準時刻からの経過時間（ナノ秒）。 | [default to undefined]

## Example

```typescript
import { CreateMeasBaseTime } from './api';

const instance: CreateMeasBaseTime = {
    basetime,
    priority,
    name,
    elapsed_time,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
