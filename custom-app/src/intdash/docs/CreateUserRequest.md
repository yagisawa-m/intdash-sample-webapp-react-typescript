# CreateUserRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | ユーザーの名前 | [default to undefined]
**nickname** | **string** | ユーザーの表示名 | [optional] [default to undefined]
**description** | **string** | ユーザーの説明 | [optional] [default to undefined]
**role_uuids** | **Array&lt;string&gt;** | ロールのUUID。指定したロールがユーザーに割り当てられます。 | [default to undefined]
**email** | **string** | ユーザーのメールアドレス | [optional] [default to undefined]

## Example

```typescript
import { CreateUserRequest } from './api';

const instance: CreateUserRequest = {
    name,
    nickname,
    description,
    role_uuids,
    email,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
