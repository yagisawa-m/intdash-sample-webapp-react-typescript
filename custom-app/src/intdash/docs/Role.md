# Role


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | ロールのUUID | [default to undefined]
**name** | **string** | ロールの名前 | [default to undefined]
**scopes** | [**Array&lt;Scope&gt;**](Scope.md) | ロールのスコープ | [default to undefined]
**created_at** | **string** | 作成日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]

## Example

```typescript
import { Role } from './api';

const instance: Role = {
    uuid,
    name,
    scopes,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
