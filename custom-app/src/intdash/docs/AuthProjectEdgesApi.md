# AuthProjectEdgesApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addProjectEdges**](#addprojectedges) | **POST** /auth/projects/{project_uuid}/edges | Add Project Edge|
|[**getProjectEdge**](#getprojectedge) | **GET** /auth/projects/{project_uuid}/edges/{edge_uuid} | Get Project Edge|
|[**listProjectEdges**](#listprojectedges) | **GET** /auth/projects/{project_uuid}/edges | List Project Edges|
|[**removeProjectEdge**](#removeprojectedge) | **DELETE** /auth/projects/{project_uuid}/edges/{edge_uuid} | Remove Project Edge|
|[**updateProjectEdge**](#updateprojectedge) | **PATCH** /auth/projects/{project_uuid}/edges/{edge_uuid} | Update Project Edge|

# **addProjectEdges**
> ProjectEdge addProjectEdges()

エッジをプロジェクトに追加します。

### Example

```typescript
import {
    AuthProjectEdgesApi,
    Configuration,
    AddProjectEdgeRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectEdgesApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let addProjectEdgeRequest: AddProjectEdgeRequest; // (optional)

const { status, data } = await apiInstance.addProjectEdges(
    projectUuid,
    addProjectEdgeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **addProjectEdgeRequest** | **AddProjectEdgeRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


### Return type

**ProjectEdge**

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
|**409** | Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProjectEdge**
> ProjectEdge getProjectEdge()

プロジェクトに所属するエッジを取得します。

### Example

```typescript
import {
    AuthProjectEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectEdgesApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let edgeUuid: string; //エッジのUUID (default to undefined)

const { status, data } = await apiInstance.getProjectEdge(
    projectUuid,
    edgeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|


### Return type

**ProjectEdge**

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

# **listProjectEdges**
> ProjectEdges listProjectEdges()

プロジェクトに所属するエッジのリストを取得します。

### Example

```typescript
import {
    AuthProjectEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectEdgesApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let edgeUuid: Array<string>; //エッジのUUID (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)
let sort: 'created_at' | 'created_at+' | 'created_at-' | 'updated_at' | 'updated_at+' | 'updated_at-' | 'nickname' | 'nickname+' | 'nickname-'; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。 (optional) (default to undefined)

const { status, data } = await apiInstance.listProjectEdges(
    projectUuid,
    edgeUuid,
    page,
    perPage,
    sort
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **edgeUuid** | **Array&lt;string&gt;** | エッジのUUID | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 30|
| **sort** | [**&#39;created_at&#39; | &#39;created_at+&#39; | &#39;created_at-&#39; | &#39;updated_at&#39; | &#39;updated_at+&#39; | &#39;updated_at-&#39; | &#39;nickname&#39; | &#39;nickname+&#39; | &#39;nickname-&#39;**]**Array<&#39;created_at&#39; &#124; &#39;created_at+&#39; &#124; &#39;created_at-&#39; &#124; &#39;updated_at&#39; &#124; &#39;updated_at+&#39; &#124; &#39;updated_at-&#39; &#124; &#39;nickname&#39; &#124; &#39;nickname+&#39; &#124; &#39;nickname-&#39;>** | 並べ替えに使用するキー。接尾辞 &#x60;+&#x60; を付けた場合は昇順、 &#x60;-&#x60; を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 &#x60;name-&#x60; を指定すると、nameによる降順で出力されます。 | (optional) defaults to undefined|


### Return type

**ProjectEdges**

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

# **removeProjectEdge**
> removeProjectEdge()

プロジェクトからエッジを外します。

### Example

```typescript
import {
    AuthProjectEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectEdgesApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let edgeUuid: string; //エッジのUUID (default to undefined)

const { status, data } = await apiInstance.removeProjectEdge(
    projectUuid,
    edgeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|


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

# **updateProjectEdge**
> ProjectEdge updateProjectEdge()

プロジェクトエッジを更新します。

### Example

```typescript
import {
    AuthProjectEdgesApi,
    Configuration,
    UpdateProjectEdgeRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectEdgesApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let edgeUuid: string; //エッジのUUID (default to undefined)
let updateProjectEdgeRequest: UpdateProjectEdgeRequest; // (optional)

const { status, data } = await apiInstance.updateProjectEdge(
    projectUuid,
    edgeUuid,
    updateProjectEdgeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateProjectEdgeRequest** | **UpdateProjectEdgeRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|


### Return type

**ProjectEdge**

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

