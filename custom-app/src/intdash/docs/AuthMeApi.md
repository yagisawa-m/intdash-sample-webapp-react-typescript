# AuthMeApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**changePassword**](#changepassword) | **PUT** /auth/users/me/password | Change Password|
|[**checkPassword**](#checkpassword) | **POST** /auth/users/me/password/check | Check Password|
|[**createMyAPIToken**](#createmyapitoken) | **POST** /auth/users/me/tokens | Create My API Token|
|[**createMyEmail**](#createmyemail) | **POST** /auth/users/me/emails | Create My Email|
|[**deleteMyAPIToken**](#deletemyapitoken) | **DELETE** /auth/users/me/tokens/{user_api_token_id} | Delete My API Token|
|[**deleteMyEmail**](#deletemyemail) | **DELETE** /auth/users/me/emails/{user_email_id} | Delete My Email|
|[**getMe**](#getme) | **GET** /auth/users/me | Get Me|
|[**listMyAPITokens**](#listmyapitokens) | **GET** /auth/users/me/tokens | List My API Tokens|
|[**listMyRoles**](#listmyroles) | **GET** /auth/users/me/roles | List My Roles|
|[**sendVerificationEmailToMyAddress**](#sendverificationemailtomyaddress) | **PUT** /auth/users/me/emails/{user_email_id}/verification | Send Verification Email to Me|
|[**updateMe**](#updateme) | **PATCH** /auth/users/me | Update Me|
|[**updateMyAPIToken**](#updatemyapitoken) | **PATCH** /auth/users/me/tokens/{user_api_token_id} | Update My API Token|
|[**updateMyAddressToVerified**](#updatemyaddresstoverified) | **PUT** /auth/users/me/emails/{user_email_id}/verified | Set My Email as Verified|
|[**updateMyEmail**](#updatemyemail) | **PATCH** /auth/users/me/emails/{user_email_id} | Update My Email|

# **changePassword**
> UserPassword changePassword()

パスワードを変更します。 現在のパスワード `old_password` または `recovery_token` が必要です。

### Example

```typescript
import {
    AuthMeApi,
    Configuration,
    ChangePasswordRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

let changePasswordRequest: ChangePasswordRequest; // (optional)

const { status, data } = await apiInstance.changePassword(
    changePasswordRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **changePasswordRequest** | **ChangePasswordRequest**|  | |


### Return type

**UserPassword**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **checkPassword**
> CheckPasswordResult checkPassword()

パスワードがポリシーに適合しているかをチェックします。

### Example

```typescript
import {
    AuthMeApi,
    Configuration,
    CheckPasswordRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

let checkPasswordRequest: CheckPasswordRequest; // (optional)

const { status, data } = await apiInstance.checkPassword(
    checkPasswordRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **checkPasswordRequest** | **CheckPasswordRequest**|  | |


### Return type

**CheckPasswordResult**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createMyAPIToken**
> UserAPIToken createMyAPIToken()

自分（ユーザー）のAPIトークンを作成します。

### Example

```typescript
import {
    AuthMeApi,
    Configuration,
    CreateUserAPITokenRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

let createUserAPITokenRequest: CreateUserAPITokenRequest; // (optional)

const { status, data } = await apiInstance.createMyAPIToken(
    createUserAPITokenRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createUserAPITokenRequest** | **CreateUserAPITokenRequest**|  | |


### Return type

**UserAPIToken**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created |  -  |
|**409** | Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createMyEmail**
> UserEmail createMyEmail()

自分（ユーザー）のメールアドレスを設定します。 メールアドレスの設定が成功すると、確認用URLを含むメールがそのアドレスに送信されます。 確認用URLには、メールアドレス確認用トークンとメールアドレスのIDが含まれます。

### Example

```typescript
import {
    AuthMeApi,
    Configuration,
    CreateEmailRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

let createEmailRequest: CreateEmailRequest; // (optional)

const { status, data } = await apiInstance.createMyEmail(
    createEmailRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createEmailRequest** | **CreateEmailRequest**|  | |


### Return type

**UserEmail**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created |  -  |
|**409** | Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteMyAPIToken**
> deleteMyAPIToken()

自分（ユーザー）のAPIトークンを削除します。

### Example

```typescript
import {
    AuthMeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

let userApiTokenId: number; //APIトークンのID (default to undefined)

const { status, data } = await apiInstance.deleteMyAPIToken(
    userApiTokenId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userApiTokenId** | [**number**] | APIトークンのID | defaults to undefined|


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
|**204** | No Content |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteMyEmail**
> deleteMyEmail()

自分（ユーザー）のメールアドレスを削除します。

### Example

```typescript
import {
    AuthMeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

let userEmailId: number; //ユーザーのメールアドレスのID (default to undefined)

const { status, data } = await apiInstance.deleteMyEmail(
    userEmailId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userEmailId** | [**number**] | ユーザーのメールアドレスのID | defaults to undefined|


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
|**204** | No Content |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getMe**
> User getMe()

自分（ユーザー）を取得します。

### Example

```typescript
import {
    AuthMeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

const { status, data } = await apiInstance.getMe();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**User**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listMyAPITokens**
> UserAPITokens listMyAPITokens()

自分（ユーザー）のAPIトークンのリストを取得します。

### Example

```typescript
import {
    AuthMeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

const { status, data } = await apiInstance.listMyAPITokens();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**UserAPITokens**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listMyRoles**
> Roles listMyRoles()

自分（ユーザー）に割り当てられたロールのリストを取得します。

### Example

```typescript
import {
    AuthMeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

const { status, data } = await apiInstance.listMyRoles();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Roles**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sendVerificationEmailToMyAddress**
> UserEmailVerification sendVerificationEmailToMyAddress()

メールアドレスを確認するための確認メールを送信します。

### Example

```typescript
import {
    AuthMeApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

let userEmailId: number; //ユーザーのメールアドレスのID (default to undefined)

const { status, data } = await apiInstance.sendVerificationEmailToMyAddress(
    userEmailId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userEmailId** | [**number**] | ユーザーのメールアドレスのID | defaults to undefined|


### Return type

**UserEmailVerification**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateMe**
> User updateMe()

自分（ユーザー）を更新します。

### Example

```typescript
import {
    AuthMeApi,
    Configuration,
    PatchUserRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

let patchUserRequest: PatchUserRequest; // (optional)

const { status, data } = await apiInstance.updateMe(
    patchUserRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **patchUserRequest** | **PatchUserRequest**|  | |


### Return type

**User**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**403** | Forbidden |  -  |
|**409** | Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateMyAPIToken**
> UserAPIToken updateMyAPIToken()

自分（ユーザー）のAPIトークンを作成します。

### Example

```typescript
import {
    AuthMeApi,
    Configuration,
    UpdateUserAPITokenRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

let userApiTokenId: number; //APIトークンのID (default to undefined)
let updateUserAPITokenRequest: UpdateUserAPITokenRequest; // (optional)

const { status, data } = await apiInstance.updateMyAPIToken(
    userApiTokenId,
    updateUserAPITokenRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateUserAPITokenRequest** | **UpdateUserAPITokenRequest**|  | |
| **userApiTokenId** | [**number**] | APIトークンのID | defaults to undefined|


### Return type

**UserAPIToken**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateMyAddressToVerified**
> UserEmail updateMyAddressToVerified()

自分（ユーザー）のメールアドレスを確認済みにします。

### Example

```typescript
import {
    AuthMeApi,
    Configuration,
    UpdateEmailVerifiedRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

let userEmailId: number; //ユーザーのメールアドレスのID (default to undefined)
let updateEmailVerifiedRequest: UpdateEmailVerifiedRequest; // (optional)

const { status, data } = await apiInstance.updateMyAddressToVerified(
    userEmailId,
    updateEmailVerifiedRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateEmailVerifiedRequest** | **UpdateEmailVerifiedRequest**|  | |
| **userEmailId** | [**number**] | ユーザーのメールアドレスのID | defaults to undefined|


### Return type

**UserEmail**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateMyEmail**
> UserEmail updateMyEmail()

自分（ユーザー）のメールアドレスを更新します。 メールアドレスの設定が成功すると、確認用URLを含むメールがそのアドレスに送信されます。 確認用URLには、メールアドレス確認用トークンとメールアドレスのIDが含まれます。

### Example

```typescript
import {
    AuthMeApi,
    Configuration,
    PatchEmailRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthMeApi(configuration);

let userEmailId: number; //ユーザーのメールアドレスのID (default to undefined)
let patchEmailRequest: PatchEmailRequest; // (optional)

const { status, data } = await apiInstance.updateMyEmail(
    userEmailId,
    patchEmailRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **patchEmailRequest** | **PatchEmailRequest**|  | |
| **userEmailId** | [**number**] | ユーザーのメールアドレスのID | defaults to undefined|


### Return type

**UserEmail**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**409** | Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

