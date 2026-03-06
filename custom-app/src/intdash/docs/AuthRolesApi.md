# AuthRolesApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getRole**](#getrole) | **GET** /auth/roles/{role_uuid} | Get Role|
|[**listRoles**](#listroles) | **GET** /auth/roles | List Roles|

# **getRole**
> Role getRole()

ロールを取得します。

### Example

```typescript
import {
    AuthRolesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthRolesApi(configuration);

let roleUuid: string; //ロールのUUID (default to undefined)

const { status, data } = await apiInstance.getRole(
    roleUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listRoles**
> Roles listRoles()

ロールのリストを取得します。

### Example

```typescript
import {
    AuthRolesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthRolesApi(configuration);

let uuid: Array<string>; //ロールのUUID (optional) (default to undefined)
let name: Array<string>; //ロールの名前による部分一致検索。文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)

const { status, data } = await apiInstance.listRoles(
    uuid,
    name,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uuid** | **Array&lt;string&gt;** | ロールのUUID | (optional) defaults to undefined|
| **name** | **Array&lt;string&gt;** | ロールの名前による部分一致検索。文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 30|


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
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

