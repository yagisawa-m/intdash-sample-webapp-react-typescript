# HookReceiverEdge


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delivery_uuid** | **string** |  | [default to undefined]
**hook_uuid** | **string** |  | [default to undefined]
**resource_type** | [**HookResourceType**](HookResourceType.md) |  | [default to undefined]
**action** | [**HookEdgeAction**](HookEdgeAction.md) |  | [default to undefined]
**edge_uuid** | **string** | 対象となるエッジUUID。テスト実行時はランダム値となります。 | [default to undefined]
**is_test** | **boolean** | テスト実行かどうか | [default to undefined]
**tenant_id** | **number** | 対象となるテナントのID。テナントIDは共有グローバルフックにのみ付与されます。 | [optional] [default to undefined]
**occurred_at** | **string** | 発生時刻 | [default to undefined]

## Example

```typescript
import { HookReceiverEdge } from './api';

const instance: HookReceiverEdge = {
    delivery_uuid,
    hook_uuid,
    resource_type,
    action,
    edge_uuid,
    is_test,
    tenant_id,
    occurred_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
