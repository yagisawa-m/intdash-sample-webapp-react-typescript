# Signal


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | 信号定義のUUID | [default to undefined]
**label** | **string** | 信号定義のラベル | [default to undefined]
**description** | **string** | 信号定義の説明 | [default to undefined]
**data_type** | **number** | データタイプ | [default to undefined]
**data_id** | **string** | データID | [default to undefined]
**channel** | **number** | チャンネル | [default to undefined]
**conversion** | [**SignalConversion**](SignalConversion.md) |  | [default to undefined]
**display** | [**SignalDisplay**](SignalDisplay.md) |  | [default to undefined]
**hash** | **string** | 信号定義のハッシュ値 | [default to undefined]
**created_at** | **string** | 信号定義の作成日時 | [default to undefined]
**updated_at** | **string** | 信号定義の最終更新日時 | [default to undefined]

## Example

```typescript
import { Signal } from './api';

const instance: Signal = {
    uuid,
    label,
    description,
    data_type,
    data_id,
    channel,
    conversion,
    display,
    hash,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
