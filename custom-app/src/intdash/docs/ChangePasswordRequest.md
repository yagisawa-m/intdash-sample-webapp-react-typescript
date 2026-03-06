# ChangePasswordRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**password** | **string** | 新しいパスワード | [default to undefined]
**old_password** | **string** | 現在のパスワード | [optional] [default to undefined]
**recovery_token** | **string** | リカバリートークン。パスワード再設定用の確認メールに含まれています。 | [optional] [default to undefined]

## Example

```typescript
import { ChangePasswordRequest } from './api';

const instance: ChangePasswordRequest = {
    password,
    old_password,
    recovery_token,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
