# Group


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | グループのUUID | [default to undefined]
**parent_group_uuid** | **string** | 親グループのUUID。nullの場合、親グループは存在しません。 | [default to undefined]
**name** | **string** | グループの名前 | [default to undefined]
**created_at** | **string** | 作成日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]

## Example

```typescript
import { Group } from './api';

const instance: Group = {
    uuid,
    parent_group_uuid,
    name,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
