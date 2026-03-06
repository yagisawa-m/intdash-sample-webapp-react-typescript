# HookReceiverTenant

共有グローバルフックに登録されたHookにのみ配信されます。

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delivery_uuid** | **string** |  | [default to undefined]
**hook_uuid** | **string** |  | [default to undefined]
**resource_type** | [**HookResourceType**](HookResourceType.md) |  | [default to undefined]
**action** | [**HookTenantAction**](HookTenantAction.md) |  | [default to undefined]
**is_test** | **boolean** | テスト実行かどうか | [optional] [default to undefined]
**tenant_id** | **number** | 対象となるテナントのID。テナントIDは共有グローバルフックにのみ付与されます。 | [default to undefined]
**occurred_at** | **string** | 発生時刻 | [default to undefined]

## Example

```typescript
import { HookReceiverTenant } from './api';

const instance: HookReceiverTenant = {
    delivery_uuid,
    hook_uuid,
    resource_type,
    action,
    is_test,
    tenant_id,
    occurred_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
