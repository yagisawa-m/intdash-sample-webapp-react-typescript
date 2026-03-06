# AuthGroupsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createGroup**](#creategroup) | **POST** /auth/groups | Create Group|
|[**createSubGroup**](#createsubgroup) | **POST** /auth/groups/{group_uuid}/groups | Create Sub Group|
|[**deleteGroup**](#deletegroup) | **DELETE** /auth/groups/{group_uuid} | Delete Group|
|[**getGroup**](#getgroup) | **GET** /auth/groups/{group_uuid} | Get Group|
|[**listGroups**](#listgroups) | **GET** /auth/groups | List Groups|
|[**listMyGroups**](#listmygroups) | **GET** /auth/users/me/groups | List My Groups|
|[**listSubGroup**](#listsubgroup) | **GET** /auth/groups/{group_uuid}/groups | List Sub Groups|
|[**updateGroup**](#updategroup) | **PATCH** /auth/groups/{group_uuid} | Update Group|

# **createGroup**
> Group createGroup()

グループを作成します。

### Example

```typescript
import {
    AuthGroupsApi,
    Configuration,
    CreateGroupRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupsApi(configuration);

let createGroupRequest: CreateGroupRequest; // (optional)

const { status, data } = await apiInstance.createGroup(
    createGroupRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createGroupRequest** | **CreateGroupRequest**|  | |


### Return type

**Group**

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

# **createSubGroup**
> Group createSubGroup()

サブグループを作成します。

### Example

```typescript
import {
    AuthGroupsApi,
    Configuration,
    CreateGroupRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupsApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let createGroupRequest: CreateGroupRequest; // (optional)

const { status, data } = await apiInstance.createSubGroup(
    groupUuid,
    createGroupRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createGroupRequest** | **CreateGroupRequest**|  | |
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|


### Return type

**Group**

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

# **deleteGroup**
> deleteGroup()

グループを削除します。

### Example

```typescript
import {
    AuthGroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupsApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)

const { status, data } = await apiInstance.deleteGroup(
    groupUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|


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

# **getGroup**
> Group getGroup()

グループを取得します。

### Example

```typescript
import {
    AuthGroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupsApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)

const { status, data } = await apiInstance.getGroup(
    groupUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|


### Return type

**Group**

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

# **listGroups**
> Groups listGroups()

グループのリストを取得します。

### Example

```typescript
import {
    AuthGroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupsApi(configuration);

let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)
let sort: 'created_at' | 'created_at+' | 'created_at-' | 'updated_at' | 'updated_at+' | 'updated_at-' | 'name' | 'name+' | 'name-'; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。 (optional) (default to undefined)

const { status, data } = await apiInstance.listGroups(
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

**Groups**

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

# **listMyGroups**
> Groups listMyGroups()

自分（ユーザー）が所属するグループのリストを取得します。

### Example

```typescript
import {
    AuthGroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupsApi(configuration);

let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)
let sort: 'created_at' | 'created_at+' | 'created_at-' | 'updated_at' | 'updated_at+' | 'updated_at-' | 'name' | 'name+' | 'name-'; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。 (optional) (default to undefined)

const { status, data } = await apiInstance.listMyGroups(
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

**Groups**

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

# **listSubGroup**
> Groups listSubGroup()

サブグループを取得します。

### Example

```typescript
import {
    AuthGroupsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupsApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)
let sort: 'created_at' | 'created_at+' | 'created_at-' | 'updated_at' | 'updated_at+' | 'updated_at-' | 'name' | 'name+' | 'name-'; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。 (optional) (default to undefined)

const { status, data } = await apiInstance.listSubGroup(
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

**Groups**

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

# **updateGroup**
> Group updateGroup()

グループを更新します。

### Example

```typescript
import {
    AuthGroupsApi,
    Configuration,
    UpdateGroupRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupsApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let updateGroupRequest: UpdateGroupRequest; // (optional)

const { status, data } = await apiInstance.updateGroup(
    groupUuid,
    updateGroupRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateGroupRequest** | **UpdateGroupRequest**|  | |
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|


### Return type

**Group**

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

