# AuthProjectMembersApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addProjectMember**](#addprojectmember) | **POST** /auth/projects/{project_uuid}/members | Add Project Member|
|[**addProjectOwnerAttribute**](#addprojectownerattribute) | **PUT** /auth/projects/{project_uuid}/members/{user_uuid}/owner | Add Project Owner Attribute|
|[**getProjectMember**](#getprojectmember) | **GET** /auth/projects/{project_uuid}/members/{user_uuid} | Get Project Member|
|[**listProjectMembers**](#listprojectmembers) | **GET** /auth/projects/{project_uuid}/members | List Project Members|
|[**removeProjectMember**](#removeprojectmember) | **DELETE** /auth/projects/{project_uuid}/members/{user_uuid} | Remove Project Member|
|[**removeProjectOwnerAttribute**](#removeprojectownerattribute) | **DELETE** /auth/projects/{project_uuid}/members/{user_uuid}/owner | Remove Project Owner Attribute|
|[**updateProjectMember**](#updateprojectmember) | **PATCH** /auth/projects/{project_uuid}/members/{user_uuid} | Update Project Member|

# **addProjectMember**
> Member addProjectMember()

プロジェクトメンバーを追加します。

### Example

```typescript
import {
    AuthProjectMembersApi,
    Configuration,
    AddProjectMemberRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectMembersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let addProjectMemberRequest: AddProjectMemberRequest; // (optional)

const { status, data } = await apiInstance.addProjectMember(
    projectUuid,
    addProjectMemberRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **addProjectMemberRequest** | **AddProjectMemberRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


### Return type

**Member**

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

# **addProjectOwnerAttribute**
> Member addProjectOwnerAttribute()

オーナー属性を追加します。オーナー属性を追加したメンバーは自動的にそのプロジェクトにおける全ての権限が付与されます。

### Example

```typescript
import {
    AuthProjectMembersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectMembersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.addProjectOwnerAttribute(
    projectUuid,
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **userUuid** | [**string**] |  | defaults to undefined|


### Return type

**Member**

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

# **getProjectMember**
> Member getProjectMember()

プロジェクトメンバーを取得します。

### Example

```typescript
import {
    AuthProjectMembersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectMembersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.getProjectMember(
    projectUuid,
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **userUuid** | [**string**] |  | defaults to undefined|


### Return type

**Member**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listProjectMembers**
> Members listProjectMembers()

プロジェクトメンバーリストを取得します。

### Example

```typescript
import {
    AuthProjectMembersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectMembersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let userUuid: Array<string>; //ユーザーのUUID (optional) (default to undefined)
let isOwner: boolean; //* `true` を指定した場合、オーナーのみを取得します。 * `false` を指定した場合、オーナー以外を取得します。 * 指定を省略した場合、オーナーであるかにかかわらずメンバーを取得します。 (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)
let sort: 'created_at' | 'created_at+' | 'created_at-' | 'updated_at' | 'updated_at+' | 'updated_at-' | 'name' | 'name+' | 'name-'; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。 (optional) (default to undefined)

const { status, data } = await apiInstance.listProjectMembers(
    projectUuid,
    userUuid,
    isOwner,
    page,
    perPage,
    sort
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **userUuid** | **Array&lt;string&gt;** | ユーザーのUUID | (optional) defaults to undefined|
| **isOwner** | [**boolean**] | * &#x60;true&#x60; を指定した場合、オーナーのみを取得します。 * &#x60;false&#x60; を指定した場合、オーナー以外を取得します。 * 指定を省略した場合、オーナーであるかにかかわらずメンバーを取得します。 | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 30|
| **sort** | [**&#39;created_at&#39; | &#39;created_at+&#39; | &#39;created_at-&#39; | &#39;updated_at&#39; | &#39;updated_at+&#39; | &#39;updated_at-&#39; | &#39;name&#39; | &#39;name+&#39; | &#39;name-&#39;**]**Array<&#39;created_at&#39; &#124; &#39;created_at+&#39; &#124; &#39;created_at-&#39; &#124; &#39;updated_at&#39; &#124; &#39;updated_at+&#39; &#124; &#39;updated_at-&#39; &#124; &#39;name&#39; &#124; &#39;name+&#39; &#124; &#39;name-&#39;>** | 並べ替えに使用するキー。接尾辞 &#x60;+&#x60; を付けた場合は昇順、 &#x60;-&#x60; を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 &#x60;name-&#x60; を指定すると、nameによる降順で出力されます。 | (optional) defaults to undefined|


### Return type

**Members**

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

# **removeProjectMember**
> removeProjectMember()

プロジェクトからメンバーを外します。

### Example

```typescript
import {
    AuthProjectMembersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectMembersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.removeProjectMember(
    projectUuid,
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
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

# **removeProjectOwnerAttribute**
> removeProjectOwnerAttribute()

オーナー属性を取り除きます。

### Example

```typescript
import {
    AuthProjectMembersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectMembersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.removeProjectOwnerAttribute(
    projectUuid,
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
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
|**304** | Not Modified |  -  |
|**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProjectMember**
> Member updateProjectMember()

プロジェクトメンバーを更新します。

### Example

```typescript
import {
    AuthProjectMembersApi,
    Configuration,
    UpdateProjectMemberRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthProjectMembersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let userUuid: string; // (default to undefined)
let updateProjectMemberRequest: UpdateProjectMemberRequest; // (optional)

const { status, data } = await apiInstance.updateProjectMember(
    projectUuid,
    userUuid,
    updateProjectMemberRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateProjectMemberRequest** | **UpdateProjectMemberRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **userUuid** | [**string**] |  | defaults to undefined|


### Return type

**Member**

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

