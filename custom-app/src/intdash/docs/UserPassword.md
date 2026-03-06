# UserPassword


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempt_count** | **number** | ログイン失敗回数。ログインに成功すると0にリセットされます。 | [default to undefined]
**is_temporary** | **boolean** | &#x60;true&#x60; の場合、このユーザーのパスワードは一時パスワードです。 | [default to undefined]
**temporary_password** | **string** | 一時パスワード | [optional] [default to undefined]
**last_attempt_at** | **string** | 最終ログイン試行日時 | [default to undefined]
**expired_at** | **string** | パスワードの有効期限 | [optional] [default to undefined]
**created_at** | **string** | 作成日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]

## Example

```typescript
import { UserPassword } from './api';

const instance: UserPassword = {
    attempt_count,
    is_temporary,
    temporary_password,
    last_attempt_at,
    expired_at,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
