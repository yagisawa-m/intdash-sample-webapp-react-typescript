# APITokenIntrospectionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**active** | **boolean** | &#x60;true&#x60; の場合、このAPIトークンは有効です。 | [default to undefined]
**tenant_id** | **number** | テナントID。デフォルトテナント以外を対象とする場合にのみ返されます。 | [optional] [default to undefined]
**user_uuid** | **string** | ユーザーのUUID | [optional] [default to undefined]
**scopes** | [**Array&lt;Scope&gt;**](Scope.md) | APIトークンが認可されているスコープ | [optional] [default to undefined]
**expired_at** | **string** | APIトークンの有効期限 | [optional] [default to undefined]
**created_at** | **string** | APIトークンの作成日時 | [optional] [default to undefined]

## Example

```typescript
import { APITokenIntrospectionResponse } from './api';

const instance: APITokenIntrospectionResponse = {
    active,
    tenant_id,
    user_uuid,
    scopes,
    expired_at,
    created_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
