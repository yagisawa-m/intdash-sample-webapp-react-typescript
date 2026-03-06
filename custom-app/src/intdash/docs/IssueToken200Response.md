# IssueToken200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access_token** | **string** | アクセストークン | [optional] [default to undefined]
**expires_in** | **number** | アクセストークンの有効期限（期限切れまでの秒数） | [optional] [default to undefined]
**refresh_token** | **string** | リフレッシュトークン | [optional] [default to undefined]
**refresh_token_expires_in** | **number** | リフレッシュトークンの有効期限（期限切れまでの秒数） | [optional] [default to undefined]
**scope** | **string** | スコープのリスト（スペース区切り）。 - temporary     - 一時的なユーザーを表します。 | [optional] [default to undefined]
**token_type** | **string** | トークンタイプ。 &#x60;Bearer&#x60; に固定。 | [optional] [default to undefined]

## Example

```typescript
import { IssueToken200Response } from './api';

const instance: IssueToken200Response = {
    access_token,
    expires_in,
    refresh_token,
    refresh_token_expires_in,
    scope,
    token_type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
