# UserAPIToken


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | APIトークンのID | [default to undefined]
**name** | **string** | APIトークンの名前 | [default to undefined]
**token** | **string** | APIトークン | [optional] [default to undefined]
**scopes** | [**Array&lt;Scope&gt;**](Scope.md) | スコープ | [default to undefined]
**last_used_at** | **string** | 最後に使用された日時 | [default to undefined]
**expired_at** | **string** | 有効期限 | [default to undefined]
**created_at** | **string** | 作成日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]

## Example

```typescript
import { UserAPIToken } from './api';

const instance: UserAPIToken = {
    id,
    name,
    token,
    scopes,
    last_used_at,
    expired_at,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
