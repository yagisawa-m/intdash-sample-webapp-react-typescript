# AuthGroupMembersApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addGroupMember**](#addgroupmember) | **POST** /auth/groups/{group_uuid}/members | Add Group Member|
|[**addGroupOwnerAttribute**](#addgroupownerattribute) | **PUT** /auth/groups/{group_uuid}/members/{user_uuid}/owner | Add Group Owner Attribute|
|[**getGroupMember**](#getgroupmember) | **GET** /auth/groups/{group_uuid}/members/{user_uuid} | Get Group Member|
|[**listGroupMembers**](#listgroupmembers) | **GET** /auth/groups/{group_uuid}/members | List Group Members|
|[**removeGroupMember**](#removegroupmember) | **DELETE** /auth/groups/{group_uuid}/members/{user_uuid} | Remove Group Member|
|[**removeGroupOwnerAttribute**](#removegroupownerattribute) | **DELETE** /auth/groups/{group_uuid}/members/{user_uuid}/owner | Remove Group Owner Attribute|
|[**updateGroupMember**](#updategroupmember) | **PATCH** /auth/groups/{group_uuid}/members/{user_uuid} | Update Group Member|

# **addGroupMember**
> Member addGroupMember()

グループメンバーを追加します。

### Example

```typescript
import {
    AuthGroupMembersApi,
    Configuration,
    AddGroupMemberRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupMembersApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let addGroupMemberRequest: AddGroupMemberRequest; // (optional)

const { status, data } = await apiInstance.addGroupMember(
    groupUuid,
    addGroupMemberRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **addGroupMemberRequest** | **AddGroupMemberRequest**|  | |
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|


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

# **addGroupOwnerAttribute**
> Member addGroupOwnerAttribute()

オーナー属性を追加します。オーナー属性を追加したメンバーは自動的にそのグループにおける全ての権限が付与されます。

### Example

```typescript
import {
    AuthGroupMembersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupMembersApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.addGroupOwnerAttribute(
    groupUuid,
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|
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

# **getGroupMember**
> Member getGroupMember()

グループメンバーを取得します。

### Example

```typescript
import {
    AuthGroupMembersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupMembersApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.getGroupMember(
    groupUuid,
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|
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

# **listGroupMembers**
> Members listGroupMembers()

グループメンバーリストを取得します。

### Example

```typescript
import {
    AuthGroupMembersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupMembersApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let isOwner: boolean; //* `true` を指定した場合、オーナーのみを取得します。 * `false` を指定した場合、オーナー以外を取得します。 * 指定を省略した場合、オーナーであるかにかかわらずメンバーを取得します。 (optional) (default to undefined)
let userUuid: Array<string>; //ユーザーのUUID (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 30)
let sort: 'created_at' | 'created_at+' | 'created_at-' | 'updated_at' | 'updated_at+' | 'updated_at-' | 'name' | 'name+' | 'name-'; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。 例えば、 `name-` を指定すると、nameによる降順で出力されます。 (optional) (default to undefined)

const { status, data } = await apiInstance.listGroupMembers(
    groupUuid,
    isOwner,
    userUuid,
    page,
    perPage,
    sort
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|
| **isOwner** | [**boolean**] | * &#x60;true&#x60; を指定した場合、オーナーのみを取得します。 * &#x60;false&#x60; を指定した場合、オーナー以外を取得します。 * 指定を省略した場合、オーナーであるかにかかわらずメンバーを取得します。 | (optional) defaults to undefined|
| **userUuid** | **Array&lt;string&gt;** | ユーザーのUUID | (optional) defaults to undefined|
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

# **removeGroupMember**
> removeGroupMember()

グループメンバーを除名します。

### Example

```typescript
import {
    AuthGroupMembersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupMembersApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.removeGroupMember(
    groupUuid,
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|
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

# **removeGroupOwnerAttribute**
> removeGroupOwnerAttribute()

オーナー属性を取り除きます。

### Example

```typescript
import {
    AuthGroupMembersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupMembersApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let userUuid: string; // (default to undefined)

const { status, data } = await apiInstance.removeGroupOwnerAttribute(
    groupUuid,
    userUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|
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

# **updateGroupMember**
> Member updateGroupMember()

グループメンバーを更新します。

### Example

```typescript
import {
    AuthGroupMembersApi,
    Configuration,
    UpdateGroupMemberRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthGroupMembersApi(configuration);

let groupUuid: string; //グループのUUID (default to undefined)
let userUuid: string; // (default to undefined)
let updateGroupMemberRequest: UpdateGroupMemberRequest; // (optional)

const { status, data } = await apiInstance.updateGroupMember(
    groupUuid,
    userUuid,
    updateGroupMemberRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateGroupMemberRequest** | **UpdateGroupMemberRequest**|  | |
| **groupUuid** | [**string**] | グループのUUID | defaults to undefined|
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

