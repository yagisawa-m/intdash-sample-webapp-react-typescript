# HookReceiver


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delivery_uuid** | **string** |  | [default to undefined]
**hook_uuid** | **string** |  | [default to undefined]
**resource_type** | [**HookResourceType**](HookResourceType.md) |  | [default to undefined]
**action** | [**HookTenantAction**](HookTenantAction.md) |  | [default to undefined]
**edge_uuid** | **string** | 対象となるエッジUUID。テスト実行時はランダム値となります。 | [default to undefined]
**is_test** | **boolean** | テスト実行かどうか | [default to undefined]
**tenant_id** | **number** | 対象となるテナントのID。テナントIDは共有グローバルフックにのみ付与されます。 | [default to undefined]
**occurred_at** | **string** | 発生時刻 | [default to undefined]
**project_uuid** | **string** | 対象となるプロジェクトのUUID。 | [default to undefined]
**measurement_uuid** | **string** | 対象となる計測UUID。テスト実行時はランダム値となります。 | [default to undefined]
**user_uuid** | **string** | 対象となるユーザーUUID。テスト実行時はランダム値となります。 | [default to undefined]
**member_uuid** | **string** | 対象となるエッジUUID。テスト実行時はランダム値となります。 | [default to undefined]

## Example

```typescript
import { HookReceiver } from './api';

const instance: HookReceiver = {
    delivery_uuid,
    hook_uuid,
    resource_type,
    action,
    edge_uuid,
    is_test,
    tenant_id,
    occurred_at,
    project_uuid,
    measurement_uuid,
    user_uuid,
    member_uuid,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
