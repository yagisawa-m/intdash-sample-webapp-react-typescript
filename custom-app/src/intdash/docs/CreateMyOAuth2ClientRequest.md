# CreateMyOAuth2ClientRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | 名前 | [default to undefined]
**grant_type** | **string** | グラントタイプ | [default to undefined]
**redirect_uris** | **Array&lt;string&gt;** |  | [default to undefined]
**token_endpoint_auth_method** | **string** | トークンエンドポイントの認証方式 | [default to TokenEndpointAuthMethodEnum_ClientSecretPost]
**tls_client_auth_subject_dn** | **string** | TLSクライアント認証のサブジェクトDN | [optional] [default to undefined]

## Example

```typescript
import { CreateMyOAuth2ClientRequest } from './api';

const instance: CreateMyOAuth2ClientRequest = {
    name,
    grant_type,
    redirect_uris,
    token_endpoint_auth_method,
    tls_client_auth_subject_dn,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
