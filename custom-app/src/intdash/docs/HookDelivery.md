# HookDelivery


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [default to undefined]
**hook_uuid** | **string** |  | [default to undefined]
**redelivered_by** | **string** | 再配信元の配信UUID | [optional] [default to undefined]
**status** | [**HookDeliveryStatus**](HookDeliveryStatus.md) |  | [default to undefined]
**reason** | **string** | 失敗したときの理由 | [default to undefined]
**is_test** | **boolean** | テスト実行かどうか | [default to undefined]
**request** | [**HookHTTPRequest**](HookHTTPRequest.md) |  | [optional] [default to undefined]
**response** | [**HookHTTPResponse**](HookHTTPResponse.md) |  | [optional] [default to undefined]
**finished_at** | **string** | 配信実行が完了した時刻 | [optional] [default to undefined]
**created_at** | **string** | 作成時刻 | [default to undefined]

## Example

```typescript
import { HookDelivery } from './api';

const instance: HookDelivery = {
    uuid,
    hook_uuid,
    redelivered_by,
    status,
    reason,
    is_test,
    request,
    response,
    finished_at,
    created_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
