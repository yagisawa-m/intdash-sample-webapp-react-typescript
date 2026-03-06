# CreateOAuth2ClientClientCredentialsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | 名前 | [default to undefined]
**grant_type** | **string** | グラントタイプ | [default to undefined]
**token_endpoint_auth_method** | **string** | トークンエンドポイントの認証方式 | [default to TokenEndpointAuthMethodEnum_ClientSecretPost]
**tls_client_auth_subject_dn** | **string** | TLSクライアント認証のサブジェクトDN | [optional] [default to undefined]

## Example

```typescript
import { CreateOAuth2ClientClientCredentialsRequest } from './api';

const instance: CreateOAuth2ClientClientCredentialsRequest = {
    name,
    grant_type,
    token_endpoint_auth_method,
    tls_client_auth_subject_dn,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
