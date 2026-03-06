# Job


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | ジョブのUUID | [default to undefined]
**meas_uuid** | **string** | 計測のUUID | [default to undefined]
**type** | [**JobType**](JobType.md) |  | [default to undefined]
**status** | [**JobStatus**](JobStatus.md) |  | [default to undefined]
**message** | **string** | ステータスの説明 | [default to undefined]
**created_at** | **string** | ジョブが作成された日時 | [default to undefined]
**updated_at** | **string** | ジョブの最終更新日時 | [default to undefined]

## Example

```typescript
import { Job } from './api';

const instance: Job = {
    uuid,
    meas_uuid,
    type,
    status,
    message,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
