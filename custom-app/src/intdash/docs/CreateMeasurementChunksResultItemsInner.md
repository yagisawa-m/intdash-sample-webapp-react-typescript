# CreateMeasurementChunksResultItemsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sequence_number** | **number** | シーケンスナンバー。符号無し32bit整数。 | [default to undefined]
**result** | **string** | 登録結果を表します:   - ok     - 登録成功。   - skipped     - スキップ。既に登録されています。 | [default to undefined]

## Example

```typescript
import { CreateMeasurementChunksResultItemsInner } from './api';

const instance: CreateMeasurementChunksResultItemsInner = {
    sequence_number,
    result,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
