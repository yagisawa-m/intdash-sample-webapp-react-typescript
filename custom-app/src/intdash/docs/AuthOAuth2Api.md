# AuthOAuth2Api

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**authOauth2JwksGet**](#authoauth2jwksget) | **GET** /auth/oauth2/jwks | List JSON Web Keys|
|[**issueToken**](#issuetoken) | **POST** /auth/oauth2/token | Token Endpoint|
|[**oauth2Authorization**](#oauth2authorization) | **GET** /auth/oauth2/authorization | Authorization Endpoint|
|[**reovokeToken**](#reovoketoken) | **POST** /auth/oauth2/revocation | Revoke Token|

# **authOauth2JwksGet**
> OAuth2JWKs authOauth2JwksGet()

JSON Web Keysのリストを取得します。 [RFC7517:JSON Web Key](https://tools.ietf.org/html/rfc7517)

### Example

```typescript
import {
    AuthOAuth2Api,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthOAuth2Api(configuration);

const { status, data } = await apiInstance.authOauth2JwksGet();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**OAuth2JWKs**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/jwk-set+json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **issueToken**
> IssueToken200Response issueToken()

OAuth2のアクセストークンを取得します。 [RFC6749:The OAuth 2.0 Authorization Framework](https://tools.ietf.org/html/rfc6749)

### Example

```typescript
import {
    AuthOAuth2Api,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthOAuth2Api(configuration);

let grantType: string; //グラントタイプ (optional) (default to undefined)
let refreshToken: string; //認可時に発行されたリフレッシュトークン。grant_typeが `refresh_token` の場合にだけ指定します。 (optional) (default to undefined)
let tenantUuid: string; //テナントのUUID。grant_typeが `password` の場合にだけ指定します。 grant_typeが `password` で、テナントUUIDを省略した場合は、デフォルトのテナントが使用されます。 (optional) (default to '00000000-0000-0000-0000-000000000000')
let username: string; //ユーザーの名前。grant_typeが `password` の場合にだけ指定します。 (optional) (default to undefined)
let password: string; //パスワード。grant_typeが `password` の場合にだけ指定します。 (optional) (default to undefined)
let clientId: string; //OAuth2クライアントのID (optional) (default to undefined)
let clientSecret: string; //OAuth2のクライアントシークレット。 OAuth2クライアントの `token_endpoint_auth_method` が `client_secret_post` の場合にだけ指定します。 (optional) (default to undefined)
let clientCertification: string; //OAuth2のクライアント証明書。 OAuth2クライアントの `token_endpoint_auth_method` が `tls_client_auth` の場合にだけ指定します。 (optional) (default to undefined)
let redirectUri: string; //認可後のリダイレクト先URI。 grant_typeが `authorization_code` の場合にだけ必要です。 (optional) (default to undefined)
let codeVerifier: string; //PKCE code verifier.  * 使用可能な文字:  `[a-Z] / [0-9] / \\\"-\\\" / \\\".\\\" / \\\"_\\\" / \\\"~\\\"`  * 長さ: 43文字以上、128文字以下 (optional) (default to undefined)
let code: string; //認可コード (optional) (default to undefined)

const { status, data } = await apiInstance.issueToken(
    grantType,
    refreshToken,
    tenantUuid,
    username,
    password,
    clientId,
    clientSecret,
    clientCertification,
    redirectUri,
    codeVerifier,
    code
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **grantType** | [**string**]**Array<&#39;password&#39; &#124; &#39;authorization_code&#39; &#124; &#39;refresh_token&#39; &#124; &#39;client_credentials&#39;>** | グラントタイプ | (optional) defaults to undefined|
| **refreshToken** | [**string**] | 認可時に発行されたリフレッシュトークン。grant_typeが &#x60;refresh_token&#x60; の場合にだけ指定します。 | (optional) defaults to undefined|
| **tenantUuid** | [**string**] | テナントのUUID。grant_typeが &#x60;password&#x60; の場合にだけ指定します。 grant_typeが &#x60;password&#x60; で、テナントUUIDを省略した場合は、デフォルトのテナントが使用されます。 | (optional) defaults to '00000000-0000-0000-0000-000000000000'|
| **username** | [**string**] | ユーザーの名前。grant_typeが &#x60;password&#x60; の場合にだけ指定します。 | (optional) defaults to undefined|
| **password** | [**string**] | パスワード。grant_typeが &#x60;password&#x60; の場合にだけ指定します。 | (optional) defaults to undefined|
| **clientId** | [**string**] | OAuth2クライアントのID | (optional) defaults to undefined|
| **clientSecret** | [**string**] | OAuth2のクライアントシークレット。 OAuth2クライアントの &#x60;token_endpoint_auth_method&#x60; が &#x60;client_secret_post&#x60; の場合にだけ指定します。 | (optional) defaults to undefined|
| **clientCertification** | [**string**] | OAuth2のクライアント証明書。 OAuth2クライアントの &#x60;token_endpoint_auth_method&#x60; が &#x60;tls_client_auth&#x60; の場合にだけ指定します。 | (optional) defaults to undefined|
| **redirectUri** | [**string**] | 認可後のリダイレクト先URI。 grant_typeが &#x60;authorization_code&#x60; の場合にだけ必要です。 | (optional) defaults to undefined|
| **codeVerifier** | [**string**] | PKCE code verifier.  * 使用可能な文字:  &#x60;[a-Z] / [0-9] / \\\&quot;-\\\&quot; / \\\&quot;.\\\&quot; / \\\&quot;_\\\&quot; / \\\&quot;~\\\&quot;&#x60;  * 長さ: 43文字以上、128文字以下 | (optional) defaults to undefined|
| **code** | [**string**] | 認可コード | (optional) defaults to undefined|


### Return type

**IssueToken200Response**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth2Authorization**
> oauth2Authorization()

OAuth2認可エンドポイント。 [RFC6749:The OAuth 2.0 Authorization Framework](https://tools.ietf.org/html/rfc6749)

### Example

```typescript
import {
    AuthOAuth2Api,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthOAuth2Api(configuration);

let clientId: string; //OAuth2クライアントID (default to undefined)
let responseType: 'code'; //OAuth2のresponse_type。 `code` のみサポートされています。 (default to undefined)
let redirectUri: string; //認可後のリダイレクト先URI (default to undefined)
let state: string; //CSRF対策のためのstate (default to undefined)
let codeChallenge: string; //PKCEコードチャレンジ。 `code_verifier` から計算したSHA-256ハッシュを、Base64 URLエンコードしたもの。 (optional) (default to undefined)
let codeChallengeMethod: 'S256'; //PKCEコードチャレンジの方式。 `S256` （SHA-256）のみサポートされます。 (optional) (default to undefined)

const { status, data } = await apiInstance.oauth2Authorization(
    clientId,
    responseType,
    redirectUri,
    state,
    codeChallenge,
    codeChallengeMethod
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **clientId** | [**string**] | OAuth2クライアントID | defaults to undefined|
| **responseType** | [**&#39;code&#39;**]**Array<&#39;code&#39;>** | OAuth2のresponse_type。 &#x60;code&#x60; のみサポートされています。 | defaults to undefined|
| **redirectUri** | [**string**] | 認可後のリダイレクト先URI | defaults to undefined|
| **state** | [**string**] | CSRF対策のためのstate | defaults to undefined|
| **codeChallenge** | [**string**] | PKCEコードチャレンジ。 &#x60;code_verifier&#x60; から計算したSHA-256ハッシュを、Base64 URLエンコードしたもの。 | (optional) defaults to undefined|
| **codeChallengeMethod** | [**&#39;S256&#39;**]**Array<&#39;S256&#39;>** | PKCEコードチャレンジの方式。 &#x60;S256&#x60; （SHA-256）のみサポートされます。 | (optional) defaults to undefined|


### Return type

void (empty response body)

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**302** | APIサーバーで設定されているログインページや同意ページへのリダイレクト |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reovokeToken**
> reovokeToken()

トークンを無効化します。 このエンドポイントをコールしてからトークンが無効化されるまで、通常数秒程度かかります。 [RFC7009:OAuth 2.0 Token Revocation](https://tools.ietf.org/html/rfc7009)

### Example

```typescript
import {
    AuthOAuth2Api,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthOAuth2Api(configuration);

let clientId: string; //OAuth2クライアントID (default to undefined)
let tokenTypeHint: string; //OAuth2トークンタイプについてのヒント (optional) (default to 'refresh_token')
let token: string; //無効化したいリフレッシュトークンまたはアクセストークン。 指定を省略した場合、サーバーは、cookieの `_bearer_token` に指定されたアクセストークン、または、Authorizationヘッダーに指定されたアクセストークン（ `Bearer` トークン）を無効化します。 (optional) (default to undefined)

const { status, data } = await apiInstance.reovokeToken(
    clientId,
    tokenTypeHint,
    token
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **clientId** | [**string**] | OAuth2クライアントID | defaults to undefined|
| **tokenTypeHint** | [**string**]**Array<&#39;access_token&#39; &#124; &#39;refresh_token&#39;>** | OAuth2トークンタイプについてのヒント | (optional) defaults to 'refresh_token'|
| **token** | [**string**] | 無効化したいリフレッシュトークンまたはアクセストークン。 指定を省略した場合、サーバーは、cookieの &#x60;_bearer_token&#x60; に指定されたアクセストークン、または、Authorizationヘッダーに指定されたアクセストークン（ &#x60;Bearer&#x60; トークン）を無効化します。 | (optional) defaults to undefined|


### Return type

void (empty response body)

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

