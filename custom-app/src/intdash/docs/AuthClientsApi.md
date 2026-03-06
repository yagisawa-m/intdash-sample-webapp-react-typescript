# AuthClientsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createMyOAuth2Clients**](#createmyoauth2clients) | **POST** /auth/users/me/clients | Create My OAuth2Client|
|[**deleteMyOAuth2Client**](#deletemyoauth2client) | **DELETE** /auth/users/me/clients/{client_id} | Delete My OAuth2Client|
|[**deleteOAuth2Client**](#deleteoauth2client) | **DELETE** /auth/clients/{client_id} | Delete OAuth2Client|
|[**getMyOAuth2Client**](#getmyoauth2client) | **GET** /auth/users/me/clients/{client_id} | Get My OAuth2Client|
|[**getOAuth2Client**](#getoauth2client) | **GET** /auth/clients/{client_id} | Get OAuth2Client|
|[**listMyOAuth2Clients**](#listmyoauth2clients) | **GET** /auth/users/me/clients | List My OAuth2Clients|
|[**listOAuth2Clients**](#listoauth2clients) | **GET** /auth/clients | List OAuth2Clients|
|[**listUsersOAuth2Clients**](#listusersoauth2clients) | **GET** /auth/users/{user_uuid}/clients | List User\&#39;s OAuth2Clients|
|[**updateMyOAuth2Client**](#updatemyoauth2client) | **PATCH** /auth/users/me/clients/{client_id} | Update My OAuth2Client|
|[**updateOAuth2Client**](#updateoauth2client) | **PATCH** /auth/clients/{client_id} | Update OAuth2Client|

# **createMyOAuth2Clients**
> OAuth2ClientWithSecret createMyOAuth2Clients()

自分（ユーザー）のOAuth2クライアントを作成します。

### Example

```typescript
import {
    AuthClientsApi,
    Configuration,
    CreateMyOAuth2ClientRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthClientsApi(configuration);

let createMyOAuth2ClientRequest: CreateMyOAuth2ClientRequest; // (optional)

const { status, data } = await apiInstance.createMyOAuth2Clients(
    createMyOAuth2ClientRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createMyOAuth2ClientRequest** | **CreateMyOAuth2ClientRequest**|  | |


### Return type

**OAuth2ClientWithSecret**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteMyOAuth2Client**
> deleteMyOAuth2Client()

自分（ユーザー）のOAuth2クライアントを削除します。

### Example

```typescript
import {
    AuthClientsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthClientsApi(configuration);

let clientId: string; //OAuth2クライアントID (default to undefined)

const { status, data } = await apiInstance.deleteMyOAuth2Client(
    clientId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **clientId** | [**string**] | OAuth2クライアントID | defaults to undefined|


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

# **deleteOAuth2Client**
> deleteOAuth2Client()

OAuth2クライアントを削除します。

### Example

```typescript
import {
    AuthClientsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthClientsApi(configuration);

let clientId: string; //OAuth2クライアントID (default to undefined)

const { status, data } = await apiInstance.deleteOAuth2Client(
    clientId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **clientId** | [**string**] | OAuth2クライアントID | defaults to undefined|


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

# **getMyOAuth2Client**
> OAuth2Client getMyOAuth2Client()

自分（ユーザー）のOAuth2クライアントを取得します。

### Example

```typescript
import {
    AuthClientsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthClientsApi(configuration);

let clientId: string; //OAuth2クライアントID (default to undefined)

const { status, data } = await apiInstance.getMyOAuth2Client(
    clientId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **clientId** | [**string**] | OAuth2クライアントID | defaults to undefined|


### Return type

**OAuth2Client**

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

# **getOAuth2Client**
> OAuth2Client getOAuth2Client()

OAuth2クライアントを取得します。

### Example

```typescript
import {
    AuthClientsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthClientsApi(configuration);

let clientId: string; //OAuth2クライアントID (default to undefined)

const { status, data } = await apiInstance.getOAuth2Client(
    clientId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **clientId** | [**string**] | OAuth2クライアントID | defaults to undefined|


### Return type

**OAuth2Client**

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

# **listMyOAuth2Clients**
> OAuth2Clients listMyOAuth2Clients()

自分（ユーザー）のOAuth2クライアントのリストを取得します。

### Example

```typescript
import {
    AuthClientsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthClientsApi(configuration);

const { status, data } = await apiInstance.listMyOAuth2Clients();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**OAuth2Clients**

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

# **listOAuth2Clients**
> OAuth2Clients listOAuth2Clients()

OAuth2クライアントのリストを取得します。

### Example

```typescript
import {
    AuthClientsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthClientsApi(configuration);

let id: Array<string>; //OAuth2クライアントID (optional) (default to undefined)
let name: Array<string>; //名前による部分一致検索 (optional) (default to undefined)
let sort: string; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。   - name   - created_at   - updated_at (optional) (default to 'name+')
let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)

const { status, data } = await apiInstance.listOAuth2Clients(
    id,
    name,
    sort,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | **Array&lt;string&gt;** | OAuth2クライアントID | (optional) defaults to undefined|
| **name** | **Array&lt;string&gt;** | 名前による部分一致検索 | (optional) defaults to undefined|
| **sort** | [**string**] | 並べ替えに使用するキー。接尾辞 &#x60;+&#x60; を付けた場合は昇順、 &#x60;-&#x60; を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 &#x60;name-&#x60; を指定すると、nameによる降順で出力されます。   - name   - created_at   - updated_at | (optional) defaults to 'name+'|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 30|


### Return type

**OAuth2Clients**

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

# **listUsersOAuth2Clients**
> OAuth2Clients listUsersOAuth2Clients()

ユーザーのOAuth2クライアントのリストを取得します。

### Example

```typescript
import {
    AuthClientsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthClientsApi(configuration);

let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.listUsersOAuth2Clients(
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|


### Return type

**OAuth2Clients**

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

# **updateMyOAuth2Client**
> OAuth2Client updateMyOAuth2Client()

自分（ユーザー）のOAuth2クライアントを更新します。

### Example

```typescript
import {
    AuthClientsApi,
    Configuration,
    UpdateOAuth2ClientRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthClientsApi(configuration);

let clientId: string; //OAuth2クライアントID (default to undefined)
let updateOAuth2ClientRequest: UpdateOAuth2ClientRequest; // (optional)

const { status, data } = await apiInstance.updateMyOAuth2Client(
    clientId,
    updateOAuth2ClientRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateOAuth2ClientRequest** | **UpdateOAuth2ClientRequest**|  | |
| **clientId** | [**string**] | OAuth2クライアントID | defaults to undefined|


### Return type

**OAuth2Client**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**304** | Not Modified |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateOAuth2Client**
> OAuth2Client updateOAuth2Client()

OAuth2クライアントを更新します。

### Example

```typescript
import {
    AuthClientsApi,
    Configuration,
    UpdateOAuth2ClientRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthClientsApi(configuration);

let clientId: string; //OAuth2クライアントID (default to undefined)
let updateOAuth2ClientRequest: UpdateOAuth2ClientRequest; // (optional)

const { status, data } = await apiInstance.updateOAuth2Client(
    clientId,
    updateOAuth2ClientRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateOAuth2ClientRequest** | **UpdateOAuth2ClientRequest**|  | |
| **clientId** | [**string**] | OAuth2クライアントID | defaults to undefined|


### Return type

**OAuth2Client**

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

