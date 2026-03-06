# DataPointError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**time** | [**DataPointTime**](DataPointTime.md) |  | [default to undefined]
**measurement_uuid** | **string** | このデータポイントが含まれる計測のUUID | [default to undefined]
**created_at** | **string** | このデータポイントが作成された日時 | [default to undefined]
**data_type** | **string** | データタイプ | [default to undefined]
**data_id** | **string** | エラーが発生した場合、 &#x60;&lt;channel&gt;/intdash/measurement/get/data/error&#x60; | [default to undefined]
**data** | [**DataPointDataError**](DataPointDataError.md) |  | [default to undefined]

## Example

```typescript
import { DataPointError } from './api';

const instance: DataPointError = {
    time,
    measurement_uuid,
    created_at,
    data_type,
    data_id,
    data,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
