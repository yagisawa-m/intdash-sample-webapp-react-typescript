# AuthProjectsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createProject**](#createproject) | **POST** /auth/groups/{group_uuid}/projects | Create Project|
|[**deleteProject**](#deleteproject) | **DELETE** /auth/projects/{project_uuid} | Delete Project|
|[**getProject**](#getproject) | **GET** /auth/projects/{project_uuid} | Get Project|
|[**listGroupProjects**](#listgroupprojects) | **GET** /auth/groups/{group_uuid}/projects | List Group Projects|
|[**listMyProjects**](#listmyprojects) | **GET** /auth/users/me/projects | List My Projects|
|[**listProjects**](#listprojects) | **GET** /auth/projects | List Projects|
|[**updateProject**](#updateproject) | **PATCH** /auth/projects/{project_uuid} | Update Project|

# **createProject**
> Project createProject()

プロジェクトを作成します。

### Example

```typescript
import {
    AuthProjectsApi,
    Configuration,
    CreateProjectRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectsApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let createProjectRequest: CreateProjectRequest; // (optional)

const { status, data } = await apiInstance.createProject(
    groupUuid,
    createProjectRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createProjectRequest** | **CreateProjectRequest**|  | |
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|


### Return type

**Project**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created |  -  |
|**403** | Forbidden |  -  |
|**409** | Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteProject**
> deleteProject()

プロジェクトを削除します。プロジェクトを削除できるのはプロジェクトのオーナーのみです。

### Example

```typescript
import {
    AuthProjectsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)

const { status, data } = await apiInstance.deleteProject(
    projectUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


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

# **getProject**
> Project getProject()

プロジェクトを取得します。

### Example

```typescript
import {
    AuthProjectsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)

const { status, data } = await apiInstance.getProject(
    projectUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


### Return type

**Project**

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

# **listGroupProjects**
> Projects listGroupProjects()

プロジェクトのリストを取得します。

### Example

```typescript
import {
    AuthProjectsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectsApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)
let sort: 'created_at' | 'created_at+' | 'created_at-' | 'updated_at' | 'updated_at+' | 'updated_at-' | 'name' | 'name+' | 'name-'; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。 (optional) (default to undefined)

const { status, data } = await apiInstance.listGroupProjects(
    groupUuid,
    page,
    perPage,
    sort
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 30|
| **sort** | [**&#39;created_at&#39; | &#39;created_at+&#39; | &#39;created_at-&#39; | &#39;updated_at&#39; | &#39;updated_at+&#39; | &#39;updated_at-&#39; | &#39;name&#39; | &#39;name+&#39; | &#39;name-&#39;**]**Array<&#39;created_at&#39; &#124; &#39;created_at+&#39; &#124; &#39;created_at-&#39; &#124; &#39;updated_at&#39; &#124; &#39;updated_at+&#39; &#124; &#39;updated_at-&#39; &#124; &#39;name&#39; &#124; &#39;name+&#39; &#124; &#39;name-&#39;>** | 並べ替えに使用するキー。接尾辞 &#x60;+&#x60; を付けた場合は昇順、 &#x60;-&#x60; を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 &#x60;name-&#x60; を指定すると、nameによる降順で出力されます。 | (optional) defaults to undefined|


### Return type

**Projects**

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

# **listMyProjects**
> Projects listMyProjects()

自分（ユーザー）が所属するプロジェクトのリストを取得します。

### Example

```typescript
import {
    AuthProjectsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectsApi(configuration);

let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)
let sort: 'created_at' | 'created_at+' | 'created_at-' | 'updated_at' | 'updated_at+' | 'updated_at-' | 'name' | 'name+' | 'name-'; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。 (optional) (default to undefined)

const { status, data } = await apiInstance.listMyProjects(
    page,
    perPage,
    sort
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 30|
| **sort** | [**&#39;created_at&#39; | &#39;created_at+&#39; | &#39;created_at-&#39; | &#39;updated_at&#39; | &#39;updated_at+&#39; | &#39;updated_at-&#39; | &#39;name&#39; | &#39;name+&#39; | &#39;name-&#39;**]**Array<&#39;created_at&#39; &#124; &#39;created_at+&#39; &#124; &#39;created_at-&#39; &#124; &#39;updated_at&#39; &#124; &#39;updated_at+&#39; &#124; &#39;updated_at-&#39; &#124; &#39;name&#39; &#124; &#39;name+&#39; &#124; &#39;name-&#39;>** | 並べ替えに使用するキー。接尾辞 &#x60;+&#x60; を付けた場合は昇順、 &#x60;-&#x60; を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 &#x60;name-&#x60; を指定すると、nameによる降順で出力されます。 | (optional) defaults to undefined|


### Return type

**Projects**

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

# **listProjects**
> Projects listProjects()

プロジェクトのリストを取得します。

### Example

```typescript
import {
    AuthProjectsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectsApi(configuration);

let sinceCreatedAt: string; //指定した時刻より後に作成されたリソースを取得します。 (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)
let sort: 'created_at' | 'created_at+' | 'created_at-' | 'updated_at' | 'updated_at+' | 'updated_at-' | 'name' | 'name+' | 'name-'; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。 (optional) (default to undefined)

const { status, data } = await apiInstance.listProjects(
    sinceCreatedAt,
    page,
    perPage,
    sort
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **sinceCreatedAt** | [**string**] | 指定した時刻より後に作成されたリソースを取得します。 | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 30|
| **sort** | [**&#39;created_at&#39; | &#39;created_at+&#39; | &#39;created_at-&#39; | &#39;updated_at&#39; | &#39;updated_at+&#39; | &#39;updated_at-&#39; | &#39;name&#39; | &#39;name+&#39; | &#39;name-&#39;**]**Array<&#39;created_at&#39; &#124; &#39;created_at+&#39; &#124; &#39;created_at-&#39; &#124; &#39;updated_at&#39; &#124; &#39;updated_at+&#39; &#124; &#39;updated_at-&#39; &#124; &#39;name&#39; &#124; &#39;name+&#39; &#124; &#39;name-&#39;>** | 並べ替えに使用するキー。接尾辞 &#x60;+&#x60; を付けた場合は昇順、 &#x60;-&#x60; を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 &#x60;name-&#x60; を指定すると、nameによる降順で出力されます。 | (optional) defaults to undefined|


### Return type

**Projects**

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

# **updateProject**
> Project updateProject()

プロジェクトを更新します。

### Example

```typescript
import {
    AuthProjectsApi,
    Configuration,
    UpdateProjectRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let updateProjectRequest: UpdateProjectRequest; // (optional)

const { status, data } = await apiInstance.updateProject(
    projectUuid,
    updateProjectRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateProjectRequest** | **UpdateProjectRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


### Return type

**Project**

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

