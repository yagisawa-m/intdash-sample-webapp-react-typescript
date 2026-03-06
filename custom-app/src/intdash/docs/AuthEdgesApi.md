# AuthEdgesApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**assignOwner**](#assignowner) | **POST** /auth/edges/{edge_uuid}/owner | Assign Owner|
|[**createEdge**](#createedge) | **POST** /auth/edges | Create Edge|
|[**createMyEdge**](#createmyedge) | **POST** /auth/users/me/edges | Create My Edge|
|[**createMyEdgeWithUUID**](#createmyedgewithuuid) | **PUT** /auth/users/me/edges/{edge_uuid} | Create My Edge With UUID|
|[**createUsersEdge**](#createusersedge) | **POST** /auth/users/{user_uuid}/edges | Create User\&#39;s Edge|
|[**deleteEdge**](#deleteedge) | **DELETE** /auth/edges/{edge_uuid} | Delete Edge|
|[**deleteMyEdge**](#deletemyedge) | **DELETE** /auth/users/me/edges/{edge_uuid} | Delete My Edge|
|[**deleteUsersEdge**](#deleteusersedge) | **DELETE** /auth/users/{user_uuid}/edges/{edge_uuid} | Delete User\&#39;s Edge|
|[**getEdge**](#getedge) | **GET** /auth/edges/{edge_uuid} | Get Edge|
|[**getMeAsEdge**](#getmeasedge) | **GET** /auth/edges/me | Get Edge having the same UUID as Me|
|[**getMyEdge**](#getmyedge) | **GET** /auth/users/me/edges/{edge_uuid} | Get My Edge|
|[**getUsersEdge**](#getusersedge) | **GET** /auth/users/{user_uuid}/edges/{edge_uuid} | Get User\&#39;s Edge|
|[**listEdges**](#listedges) | **GET** /auth/edges | List Edges|
|[**listMyEdges**](#listmyedges) | **GET** /auth/users/me/edges | List My Edges|
|[**listUsersEdges**](#listusersedges) | **GET** /auth/users/{user_uuid}/edges | List User\&#39;s Edges|
|[**removeOwner**](#removeowner) | **DELETE** /auth/edges/{edge_uuid}/owner | Unassign Owner|
|[**updateEdge**](#updateedge) | **PATCH** /auth/edges/{edge_uuid} | Update Edge|
|[**updateMyEdge**](#updatemyedge) | **PATCH** /auth/users/me/edges/{edge_uuid} | Update My Edge|
|[**updateUsersEdge**](#updateusersedge) | **PATCH** /auth/users/{user_uuid}/edges/{edge_uuid} | Update User\&#39;s Edge|

# **assignOwner**
> EdgeOwner assignOwner()

エッジに所有者を割り当てます。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration,
    AssignOwnerRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let edgeUuid: string; //エッジのUUID (default to undefined)
let assignOwnerRequest: AssignOwnerRequest; // (optional)

const { status, data } = await apiInstance.assignOwner(
    edgeUuid,
    assignOwnerRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **assignOwnerRequest** | **AssignOwnerRequest**|  | |
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|


### Return type

**EdgeOwner**

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

# **createEdge**
> Edge createEdge()

所有者がない状態でエッジを作成します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration,
    CreateEdgeRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let createEdgeRequest: CreateEdgeRequest; // (optional)

const { status, data } = await apiInstance.createEdge(
    createEdgeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createEdgeRequest** | **CreateEdgeRequest**|  | |


### Return type

**Edge**

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

# **createMyEdge**
> Edge createMyEdge()

新しいエッジを作成し、自分（ユーザー）を所有者に設定します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration,
    CreateEdgeRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let createEdgeRequest: CreateEdgeRequest; // (optional)

const { status, data } = await apiInstance.createMyEdge(
    createEdgeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createEdgeRequest** | **CreateEdgeRequest**|  | |


### Return type

**Edge**

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

# **createMyEdgeWithUUID**
> Edge createMyEdgeWithUUID()

指定したUUIDを持つ新しいエッジを作成し、自分を所有者に設定します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration,
    CreateEdgeRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let edgeUuid: string; //エッジのUUID (default to undefined)
let createEdgeRequest: CreateEdgeRequest; // (optional)

const { status, data } = await apiInstance.createMyEdgeWithUUID(
    edgeUuid,
    createEdgeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createEdgeRequest** | **CreateEdgeRequest**|  | |
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|


### Return type

**Edge**

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

# **createUsersEdge**
> Edge createUsersEdge()

指定されたユーザーを所有者とするエッジを作成します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration,
    CreateEdgeRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let userUuid: string; // (default to undefined)
let createEdgeRequest: CreateEdgeRequest; // (optional)

const { status, data } = await apiInstance.createUsersEdge(
    userUuid,
    createEdgeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createEdgeRequest** | **CreateEdgeRequest**|  | |
| **userUuid** | [**string**] |  | defaults to undefined|


### Return type

**Edge**

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

# **deleteEdge**
> deleteEdge()

エッジを削除します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let edgeUuid: string; //エッジのUUID (default to undefined)

const { status, data } = await apiInstance.deleteEdge(
    edgeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

# **deleteMyEdge**
> deleteMyEdge()

自分（ユーザー）が所有するエッジを削除します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let edgeUuid: string; //エッジのUUID (default to undefined)

const { status, data } = await apiInstance.deleteMyEdge(
    edgeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

# **deleteUsersEdge**
> deleteUsersEdge()

ユーザーが所有するエッジを削除します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let userUuid: string; // (default to undefined)
let edgeUuid: string; //エッジのUUID (default to undefined)

const { status, data } = await apiInstance.deleteUsersEdge(
    userUuid,
    edgeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|
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

# **getEdge**
> Edge getEdge()

エッジを取得します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let edgeUuid: string; //エッジのUUID (default to undefined)

const { status, data } = await apiInstance.getEdge(
    edgeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|


### Return type

**Edge**

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

# **getMeAsEdge**
> Edge getMeAsEdge()

自分のUUIDと同じエッジUUIDを持つエッジを取得します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

const { status, data } = await apiInstance.getMeAsEdge();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Edge**

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

# **getMyEdge**
> Edge getMyEdge()

自分（ユーザー）が所有するエッジを取得します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let edgeUuid: string; //エッジのUUID (default to undefined)

const { status, data } = await apiInstance.getMyEdge(
    edgeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|


### Return type

**Edge**

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

# **getUsersEdge**
> Edge getUsersEdge()

ユーザーが所有するエッジを取得します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let userUuid: string; // (default to undefined)
let edgeUuid: string; //エッジのUUID (default to undefined)

const { status, data } = await apiInstance.getUsersEdge(
    userUuid,
    edgeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|


### Return type

**Edge**

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

# **listEdges**
> Edges listEdges()

エッジのリストを取得します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let uuid: Array<string>; //エッジのUUID (optional) (default to undefined)
let name: Array<string>; //名前による部分一致検索 (optional) (default to undefined)
let nickname: Array<string>; //表示名による部分一致検索 (optional) (default to undefined)
let ownerUuid: Array<string>; //所有者ユーザーのUUID (optional) (default to undefined)
let hasOwner: 'true' | 'false'; //所有者の有無。  * `true` : 所有者が設定されているエッジを取得します。 * `false` : 所有者が設定されていないエッジを取得します。 (optional) (default to undefined)
let sort: string; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。   - name   - created_at   - updated_at (optional) (default to 'name+')
let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)

const { status, data } = await apiInstance.listEdges(
    uuid,
    name,
    nickname,
    ownerUuid,
    hasOwner,
    sort,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uuid** | **Array&lt;string&gt;** | エッジのUUID | (optional) defaults to undefined|
| **name** | **Array&lt;string&gt;** | 名前による部分一致検索 | (optional) defaults to undefined|
| **nickname** | **Array&lt;string&gt;** | 表示名による部分一致検索 | (optional) defaults to undefined|
| **ownerUuid** | **Array&lt;string&gt;** | 所有者ユーザーのUUID | (optional) defaults to undefined|
| **hasOwner** | [**&#39;true&#39; | &#39;false&#39;**]**Array<&#39;true&#39; &#124; &#39;false&#39;>** | 所有者の有無。  * &#x60;true&#x60; : 所有者が設定されているエッジを取得します。 * &#x60;false&#x60; : 所有者が設定されていないエッジを取得します。 | (optional) defaults to undefined|
| **sort** | [**string**] | 並べ替えに使用するキー。接尾辞 &#x60;+&#x60; を付けた場合は昇順、 &#x60;-&#x60; を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 &#x60;name-&#x60; を指定すると、nameによる降順で出力されます。   - name   - created_at   - updated_at | (optional) defaults to 'name+'|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 30|


### Return type

**Edges**

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

# **listMyEdges**
> Edges listMyEdges()

自分（ユーザー）が所有するエッジのリストを取得します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

const { status, data } = await apiInstance.listMyEdges();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Edges**

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

# **listUsersEdges**
> Edges listUsersEdges()

指定されたユーザーが所有するエッジのリストを取得します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.listUsersEdges(
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUuid** | [**string**] |  | defaults to undefined|


### Return type

**Edges**

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

# **removeOwner**
> removeOwner()

エッジに所有者がない状態にします。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let edgeUuid: string; //エッジのUUID (default to undefined)

const { status, data } = await apiInstance.removeOwner(
    edgeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

# **updateEdge**
> Edge updateEdge()

エッジを更新します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration,
    PatchEdgeRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let edgeUuid: string; //エッジのUUID (default to undefined)
let patchEdgeRequest: PatchEdgeRequest; // (optional)

const { status, data } = await apiInstance.updateEdge(
    edgeUuid,
    patchEdgeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **patchEdgeRequest** | **PatchEdgeRequest**|  | |
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|


### Return type

**Edge**

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

# **updateMyEdge**
> Edge updateMyEdge()

自分（ユーザー）が所有するエッジを更新します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration,
    PatchEdgeRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let edgeUuid: string; //エッジのUUID (default to undefined)
let patchEdgeRequest: PatchEdgeRequest; // (optional)

const { status, data } = await apiInstance.updateMyEdge(
    edgeUuid,
    patchEdgeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **patchEdgeRequest** | **PatchEdgeRequest**|  | |
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|


### Return type

**Edge**

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

# **updateUsersEdge**
> Edge updateUsersEdge()

ユーザーが所有するエッジを更新します。

### Example

```typescript
import {
    AuthEdgesApi,
    Configuration,
    PatchEdgeRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthEdgesApi(configuration);

let userUuid: string; // (default to undefined)
let edgeUuid: string; //エッジのUUID (default to undefined)
let patchEdgeRequest: PatchEdgeRequest; // (optional)

const { status, data } = await apiInstance.updateUsersEdge(
    userUuid,
    edgeUuid,
    patchEdgeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **patchEdgeRequest** | **PatchEdgeRequest**|  | |
| **userUuid** | [**string**] |  | defaults to undefined|
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|


### Return type

**Edge**

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

