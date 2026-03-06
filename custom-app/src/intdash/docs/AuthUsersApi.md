# AuthUsersApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**assignRole**](#assignrole) | **PUT** /auth/users/{user_uuid}/roles/{role_uuid} | Assign Role|
|[**createAPIToken**](#createapitoken) | **POST** /auth/users/{user_uuid}/tokens | Create API Token|
|[**createEmail**](#createemail) | **POST** /auth/users/{user_uuid}/emails | Create Email|
|[**createTemporaryPassword**](#createtemporarypassword) | **PUT** /auth/users/{user_uuid}/password | Create Temporary Password|
|[**createUser**](#createuser) | **POST** /auth/users | Create User|
|[**deleteAPIToken**](#deleteapitoken) | **DELETE** /auth/users/{user_uuid}/tokens/{user_api_token_id} | Delete API Token|
|[**deleteEmail**](#deleteemail) | **DELETE** /auth/users/{user_uuid}/emails/{user_email_id} | Delete Email|
|[**deleteUser**](#deleteuser) | **DELETE** /auth/users/{user_uuid} | Delete User|
|[**disableUser**](#disableuser) | **PUT** /auth/users/{user_uuid}/disable | Disable User|
|[**enableUser**](#enableuser) | **PUT** /auth/users/{user_uuid}/enable | Enable User|
|[**getUser**](#getuser) | **GET** /auth/users/{user_uuid} | Get User|
|[**introspectAPIToken**](#introspectapitoken) | **POST** /auth/users/tokens/introspection | Introspect API Token|
|[**listAPITokens**](#listapitokens) | **GET** /auth/users/{user_uuid}/tokens | List API Tokens|
|[**listUsers**](#listusers) | **GET** /auth/users | List Users|
|[**listUsersRoles**](#listusersroles) | **GET** /auth/users/{user_uuid}/roles | List User\&#39;s Roles|
|[**sendVerificationEmail**](#sendverificationemail) | **PUT** /auth/users/{user_uuid}/emails/{user_email_id}/verification | Send Verification Email|
|[**unassignRole**](#unassignrole) | **DELETE** /auth/users/{user_uuid}/roles/{role_uuid} | Unassign Role|
|[**unlockPassword**](#unlockpassword) | **PUT** /auth/users/{user_uuid}/password/unlock | Unlock Password|
|[**updateAPIToken**](#updateapitoken) | **PATCH** /auth/users/{user_uuid}/tokens/{user_api_token_id} | Update API Token|
|[**updateEmail**](#updateemail) | **PATCH** /auth/users/{user_uuid}/emails/{user_email_id} | Update Email|
|[**updateToVerified**](#updatetoverified) | **PUT** /auth/users/{user_uuid}/emails/{user_email_id}/verified | Set Email as Verified|
|[**updateUser**](#updateuser) | **PATCH** /auth/users/{user_uuid} | Update User|

# **assignRole**
> Role assignRole()

ユーザーにロールを割り当てます。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)
let roleUuid: string; //ロールのUUID (default to undefined)

const { status, data } = await apiInstance.assignRole(
    userUuid,
    roleUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|
| **roleUuid** | [**string**] | ロールのUUID | defaults to undefined|


### Return type

**Role**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**304** | Not Modified |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createAPIToken**
> UserAPIToken createAPIToken()

ユーザーのAPIトークンを作成します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration,
    CreateUserAPITokenRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)
let createUserAPITokenRequest: CreateUserAPITokenRequest; // (optional)

const { status, data } = await apiInstance.createAPIToken(
    userUuid,
    createUserAPITokenRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createUserAPITokenRequest** | **CreateUserAPITokenRequest**|  | |
| **userUuid** | [**string**] |  | defaults to undefined|


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

# **createEmail**
> UserEmail createEmail()

ユーザーのメールアドレスを設定します。 メールアドレスの設定が成功すると、確認用URLを含むメールがそのアドレスに送信されます。 確認用URLには、メールアドレス確認用トークンとメールアドレスのIDが含まれます。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration,
    CreateEmailRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)
let createEmailRequest: CreateEmailRequest; // (optional)

const { status, data } = await apiInstance.createEmail(
    userUuid,
    createEmailRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createEmailRequest** | **CreateEmailRequest**|  | |
| **userUuid** | [**string**] |  | defaults to undefined|


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

# **createTemporaryPassword**
> UserPassword createTemporaryPassword()

ユーザーのパスワードを、ランダムな一時パスワードに変更します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.createTemporaryPassword(
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|


### Return type

**UserPassword**

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

# **createUser**
> User createUser()

ユーザーを作成します。新しいユーザーには自動生成された一時パスワードが設定されます。 ユーザー作成のリクエストにメールアドレス（ `email` ）が含まれていた場合は、 そのメールアドレスに確認メールが送信されます。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration,
    CreateUserRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let createUserRequest: CreateUserRequest; // (optional)

const { status, data } = await apiInstance.createUser(
    createUserRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createUserRequest** | **CreateUserRequest**|  | |


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
|**201** | Created |  -  |
|**409** | Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteAPIToken**
> deleteAPIToken()

ユーザーのAPIトークンを削除します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)
let userApiTokenId: number; //APIトークンのID (default to undefined)

const { status, data } = await apiInstance.deleteAPIToken(
    userUuid,
    userApiTokenId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|
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

# **deleteEmail**
> deleteEmail()

ユーザーのメールアドレスを削除します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)
let userEmailId: number; //ユーザーのメールアドレスのID (default to undefined)

const { status, data } = await apiInstance.deleteEmail(
    userUuid,
    userEmailId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|
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

# **deleteUser**
> deleteUser()

ユーザーを削除します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.deleteUser(
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | No Content |  -  |
|**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disableUser**
> User disableUser()

ユーザーを無効化します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.disableUser(
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|


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
|**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enableUser**
> User enableUser()

ユーザーを有効化します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.enableUser(
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|


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
|**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getUser**
> User getUser()

ユーザーを取得します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.getUser(
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|


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

# **introspectAPIToken**
> APITokenIntrospectionResponse introspectAPIToken()

APIトークンの検証を行います。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration,
    APITokenIntrospectionRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let aPITokenIntrospectionRequest: APITokenIntrospectionRequest; // (optional)

const { status, data } = await apiInstance.introspectAPIToken(
    aPITokenIntrospectionRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **aPITokenIntrospectionRequest** | **APITokenIntrospectionRequest**|  | |


### Return type

**APITokenIntrospectionResponse**

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

# **listAPITokens**
> UserAPITokens listAPITokens()

ユーザーのAPIトークンのリストを取得します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.listAPITokens(
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|


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

# **listUsers**
> Users listUsers()

ユーザーのリストを取得します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let uuid: Array<string>; //ユーザーのUUID (optional) (default to undefined)
let roleUuid: Array<string>; //ロールのUUID (optional) (default to undefined)
let name: Array<string>; //ユーザーの名前による部分一致検索。文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 (optional) (default to undefined)
let nickname: Array<string>; //ユーザーの表示名による部分一致検索。文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 (optional) (default to undefined)
let email: Array<string>; //メールアドレスによる部分一致検索。文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 (optional) (default to undefined)
let disabled: boolean; //* `true` を指定した場合、無効化されているユーザーのみを取得します。 * `false` を指定した場合、有効なユーザーのみを取得します。 * 指定を省略した場合、有効／無効にかかわらずユーザーを取得します。 (optional) (default to undefined)
let isSuper: boolean; //* `true` を指定した場合、スーパーユーザーのみを取得します。 * `false` を指定した場合、スーパーユーザー以外を取得します。 * 指定を省略した場合、スーパーユーザーであるかにかかわらずユーザーを取得します。 (optional) (default to undefined)
let isTemporary: boolean; //* `true` を指定した場合、一時パスワードを使用しているユーザーのみを取得します。 * `false` を指定した場合、パスワードを設定済みのユーザーのみを取得します。 * 指定を省略した場合、一時パスワードを使用しているかにかかわらずユーザーを取得します。 (optional) (default to undefined)
let minSignInAttemptCount: number; //ログイン失敗回数の最小値。ログイン失敗回数がこの数値以上のユーザーを取得します。 (optional) (default to undefined)
let maxSignInAttemptCount: number; //ログイン失敗回数の最大値。ログイン失敗回数がこの数値以下のユーザーを取得します。 (optional) (default to undefined)
let sort: string; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。   - name   - created_at   - updated_at   - last_sign_in_at (optional) (default to 'name+')
let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)

const { status, data } = await apiInstance.listUsers(
    uuid,
    roleUuid,
    name,
    nickname,
    email,
    disabled,
    isSuper,
    isTemporary,
    minSignInAttemptCount,
    maxSignInAttemptCount,
    sort,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uuid** | **Array&lt;string&gt;** | ユーザーのUUID | (optional) defaults to undefined|
| **roleUuid** | **Array&lt;string&gt;** | ロールのUUID | (optional) defaults to undefined|
| **name** | **Array&lt;string&gt;** | ユーザーの名前による部分一致検索。文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 | (optional) defaults to undefined|
| **nickname** | **Array&lt;string&gt;** | ユーザーの表示名による部分一致検索。文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 | (optional) defaults to undefined|
| **email** | **Array&lt;string&gt;** | メールアドレスによる部分一致検索。文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 | (optional) defaults to undefined|
| **disabled** | [**boolean**] | * &#x60;true&#x60; を指定した場合、無効化されているユーザーのみを取得します。 * &#x60;false&#x60; を指定した場合、有効なユーザーのみを取得します。 * 指定を省略した場合、有効／無効にかかわらずユーザーを取得します。 | (optional) defaults to undefined|
| **isSuper** | [**boolean**] | * &#x60;true&#x60; を指定した場合、スーパーユーザーのみを取得します。 * &#x60;false&#x60; を指定した場合、スーパーユーザー以外を取得します。 * 指定を省略した場合、スーパーユーザーであるかにかかわらずユーザーを取得します。 | (optional) defaults to undefined|
| **isTemporary** | [**boolean**] | * &#x60;true&#x60; を指定した場合、一時パスワードを使用しているユーザーのみを取得します。 * &#x60;false&#x60; を指定した場合、パスワードを設定済みのユーザーのみを取得します。 * 指定を省略した場合、一時パスワードを使用しているかにかかわらずユーザーを取得します。 | (optional) defaults to undefined|
| **minSignInAttemptCount** | [**number**] | ログイン失敗回数の最小値。ログイン失敗回数がこの数値以上のユーザーを取得します。 | (optional) defaults to undefined|
| **maxSignInAttemptCount** | [**number**] | ログイン失敗回数の最大値。ログイン失敗回数がこの数値以下のユーザーを取得します。 | (optional) defaults to undefined|
| **sort** | [**string**] | 並べ替えに使用するキー。接尾辞 &#x60;+&#x60; を付けた場合は昇順、 &#x60;-&#x60; を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 &#x60;name-&#x60; を指定すると、nameによる降順で出力されます。   - name   - created_at   - updated_at   - last_sign_in_at | (optional) defaults to 'name+'|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 30|


### Return type

**Users**

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

# **listUsersRoles**
> Roles listUsersRoles()

ユーザーのロールのリストを取得します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.listUsersRoles(
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|


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

# **sendVerificationEmail**
> UserEmailVerification sendVerificationEmail()

メールアドレスを確認するため確認メールを送信します。メールアドレス確認用トークンを使用します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)
let userEmailId: number; //ユーザーのメールアドレスのID (default to undefined)

const { status, data } = await apiInstance.sendVerificationEmail(
    userUuid,
    userEmailId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|
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

# **unassignRole**
> unassignRole()

ユーザーへのロールの割り当てを解除します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)
let roleUuid: string; //ロールのUUID (default to undefined)

const { status, data } = await apiInstance.unassignRole(
    userUuid,
    roleUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|
| **roleUuid** | [**string**] | ロールのUUID | defaults to undefined|


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

# **unlockPassword**
> UserPassword unlockPassword()

ユーザーのパスワードのロックを解除します。このユーザーのログイン失敗回数は0にリセットされます。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.unlockPassword(
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|


### Return type

**UserPassword**

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

# **updateAPIToken**
> UserAPIToken updateAPIToken()

ユーザーのAPIトークンを更新します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration,
    UpdateUserAPITokenRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)
let userApiTokenId: number; //APIトークンのID (default to undefined)
let updateUserAPITokenRequest: UpdateUserAPITokenRequest; // (optional)

const { status, data } = await apiInstance.updateAPIToken(
    userUuid,
    userApiTokenId,
    updateUserAPITokenRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateUserAPITokenRequest** | **UpdateUserAPITokenRequest**|  | |
| **userUuid** | [**string**] |  | defaults to undefined|
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

# **updateEmail**
> UserEmail updateEmail()

ユーザーのメールアドレスを更新します。 メールアドレスの設定が成功すると、確認用URLを含むメールがそのアドレスに送信されます。 確認用URLには、メールアドレス確認用トークンとメールアドレスのIDが含まれます。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration,
    PatchEmailRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)
let userEmailId: number; //ユーザーのメールアドレスのID (default to undefined)
let patchEmailRequest: PatchEmailRequest; // (optional)

const { status, data } = await apiInstance.updateEmail(
    userUuid,
    userEmailId,
    patchEmailRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **patchEmailRequest** | **PatchEmailRequest**|  | |
| **userUuid** | [**string**] |  | defaults to undefined|
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

# **updateToVerified**
> UserEmail updateToVerified()

ユーザーのメールアドレスを確認済みにします。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration,
    UpdateEmailVerifiedRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)
let userEmailId: number; //ユーザーのメールアドレスのID (default to undefined)
let updateEmailVerifiedRequest: UpdateEmailVerifiedRequest; // (optional)

const { status, data } = await apiInstance.updateToVerified(
    userUuid,
    userEmailId,
    updateEmailVerifiedRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateEmailVerifiedRequest** | **UpdateEmailVerifiedRequest**|  | |
| **userUuid** | [**string**] |  | defaults to undefined|
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

# **updateUser**
> User updateUser()

ユーザーを更新します。

### Example

```typescript
import {
    AuthUsersApi,
    Configuration,
    PatchUserRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthUsersApi(configuration);

let userUuid: string; // (default to undefined)
let patchUserRequest: PatchUserRequest; // (optional)

const { status, data } = await apiInstance.updateUser(
    userUuid,
    patchUserRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **patchUserRequest** | **PatchUserRequest**|  | |
| **userUuid** | [**string**] |  | defaults to undefined|


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

