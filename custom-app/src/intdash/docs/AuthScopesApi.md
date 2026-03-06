# AuthScopesApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getScope**](#getscope) | **GET** /auth/scopes/{scope_uuid} | Get Scope|
|[**listScopes**](#listscopes) | **GET** /auth/scopes | List Scopes|

# **getScope**
> Scope getScope()

スコープを取得します。

### Example

```typescript
import {
    AuthScopesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthScopesApi(configuration);

let scopeUuid: string; //The Scope UUID. (default to undefined)

const { status, data } = await apiInstance.getScope(
    scopeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **scopeUuid** | [**string**] | The Scope UUID. | defaults to undefined|


### Return type

**Scope**

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

# **listScopes**
> Scopes listScopes()

スコープのリストを取得します。

### Example

```typescript
import {
    AuthScopesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthScopesApi(configuration);

let uuid: Array<string>; //スコープのUUID (optional) (default to undefined)
let name: Array<string>; //スコープの名前による部分一致検索。文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)

const { status, data } = await apiInstance.listScopes(
    uuid,
    name,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uuid** | **Array&lt;string&gt;** | スコープのUUID | (optional) defaults to undefined|
| **name** | **Array&lt;string&gt;** | スコープの名前による部分一致検索。文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 30|


### Return type

**Scopes**

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

