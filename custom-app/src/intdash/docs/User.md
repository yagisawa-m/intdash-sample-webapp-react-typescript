# User


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | ユーザーのUUID | [default to undefined]
**name** | **string** | ユーザーの名前 | [default to undefined]
**nickname** | **string** | ユーザーの表示名 | [default to undefined]
**disabled** | **boolean** | * &#x60;true&#x60;: このユーザーは無効化されています * &#x60;false&#x60; : このユーザーは有効です。 | [default to undefined]
**description** | **string** | ユーザーの説明 | [default to undefined]
**is_super** | **boolean** | &#x60;true&#x60; の場合、このユーザーはスーパーユーザーです。 | [default to undefined]
**emails** | [**Array&lt;UserEmail&gt;**](UserEmail.md) |  | [default to undefined]
**last_sign_in_at** | **string** | 最後にログインした日時 | [default to undefined]
**roles** | **Array&lt;string&gt;** | 割り当てられたロールのUUID | [default to undefined]
**password** | [**UserPassword**](UserPassword.md) |  | [default to undefined]
**created_at** | **string** | 作成日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]

## Example

```typescript
import { User } from './api';

const instance: User = {
    uuid,
    name,
    nickname,
    disabled,
    description,
    is_super,
    emails,
    last_sign_in_at,
    roles,
    password,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
