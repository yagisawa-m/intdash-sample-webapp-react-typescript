# HookReceiverProjectMember


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delivery_uuid** | **string** |  | [default to undefined]
**hook_uuid** | **string** |  | [default to undefined]
**resource_type** | [**HookResourceType**](HookResourceType.md) |  | [default to undefined]
**action** | [**HookProjectMemberAction**](HookProjectMemberAction.md) |  | [default to undefined]
**member_uuid** | **string** | 対象となるエッジUUID。テスト実行時はランダム値となります。 | [default to undefined]
**project_uuid** | **string** | 対象となるプロジェクトのUUID。 | [default to undefined]
**is_test** | **boolean** | テスト実行かどうか | [default to undefined]
**tenant_id** | **number** | 対象となるテナントのID。テナントIDは共有グローバルフックにのみ付与されます。 | [optional] [default to undefined]
**occurred_at** | **string** | 発生時刻 | [default to undefined]

## Example

```typescript
import { HookReceiverProjectMember } from './api';

const instance: HookReceiverProjectMember = {
    delivery_uuid,
    hook_uuid,
    resource_type,
    action,
    member_uuid,
    project_uuid,
    is_test,
    tenant_id,
    occurred_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
