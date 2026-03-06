# OAuth2ClientWithSecret


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_id** | **string** | OAuth2クライアントID | [default to undefined]
**name** | **string** | 名前 | [default to undefined]
**grant_types** | **Array&lt;string&gt;** | グラントタイプ | [default to undefined]
**token_endpoint_auth_method** | **string** | トークンエンドポイントの認証方式 | [default to undefined]
**redirect_uris** | **Array&lt;string&gt;** | 認可後のリダイレクト先URI | [default to undefined]
**response_types** | **Array&lt;string&gt;** | レスポンスタイプ | [default to undefined]
**scopes** | **Array&lt;string&gt;** | スコープ | [default to undefined]
**audiences** | **Array&lt;string&gt;** | オーディエンス | [default to undefined]
**tls_client_auth_subject_dn** | **string** | TLSクライアント認証のサブジェクトDN | [default to undefined]
**user_uuid** | **string** | 所有しているユーザーのUUID | [optional] [default to undefined]
**created_at** | **string** | 作成日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]
**client_secret** | **string** | token_endpoint_auth_methodが &#x60;none&#x60; 以外だったら required | [optional] [default to undefined]

## Example

```typescript
import { OAuth2ClientWithSecret } from './api';

const instance: OAuth2ClientWithSecret = {
    client_id,
    name,
    grant_types,
    token_endpoint_auth_method,
    redirect_uris,
    response_types,
    scopes,
    audiences,
    tls_client_auth_subject_dn,
    user_uuid,
    created_at,
    updated_at,
    client_secret,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
