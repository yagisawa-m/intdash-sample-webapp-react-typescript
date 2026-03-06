# UpdateSignalRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | **number** | チャンネル | [optional] [default to undefined]
**conversion** | [**SignalConversion**](SignalConversion.md) |  | [optional] [default to undefined]
**data_id** | **string** | データID | [optional] [default to undefined]
**data_type** | **number** | データタイプ | [optional] [default to undefined]
**description** | **string** | 信号定義の説明 | [optional] [default to undefined]
**display** | [**SignalDisplay**](SignalDisplay.md) |  | [optional] [default to undefined]
**label** | **string** | 信号定義のラベル | [optional] [default to undefined]

## Example

```typescript
import { UpdateSignalRequest } from './api';

const instance: UpdateSignalRequest = {
    channel,
    conversion,
    data_id,
    data_type,
    description,
    display,
    label,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
