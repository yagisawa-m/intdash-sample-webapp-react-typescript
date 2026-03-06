# MeasSignalsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createProjectSignal**](#createprojectsignal) | **POST** /v1/projects/{project_uuid}/signals | Create Project Signal|
|[**createSignal**](#createsignal) | **POST** /v1/signals | Create Signal|
|[**deleteProjectSignal**](#deleteprojectsignal) | **DELETE** /v1/projects/{project_uuid}/signals/{signal_uuid} | Delete Project Signal|
|[**deleteSignal**](#deletesignal) | **DELETE** /v1/signals/{signal_uuid} | Delete Signal|
|[**getProjectSignal**](#getprojectsignal) | **GET** /v1/projects/{project_uuid}/signals/{signal_uuid} | Get Project Signal|
|[**getSignal**](#getsignal) | **GET** /v1/signals/{signal_uuid} | Get Signal|
|[**listProjectSignals**](#listprojectsignals) | **GET** /v1/projects/{project_uuid}/signals | List Project Signals|
|[**listSignals**](#listsignals) | **GET** /v1/signals | List Signals|
|[**updateProjectSignal**](#updateprojectsignal) | **PUT** /v1/projects/{project_uuid}/signals/{signal_uuid} | Update Project Signal|
|[**updateSignal**](#updatesignal) | **PUT** /v1/signals/{signal_uuid} | Update Signal|

# **createProjectSignal**
> Signal createProjectSignal()

信号定義を作成します。  * **Note**     - 既存の信号定義と `label` が重複する場合、または `uuid` が重複する場合は、       ステータスコード `409 Conflict` が返却されます。

### Example

```typescript
import {
    MeasSignalsApi,
    Configuration,
    CreateSignalRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasSignalsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let createSignalRequest: CreateSignalRequest; // (optional)

const { status, data } = await apiInstance.createProjectSignal(
    projectUuid,
    createSignalRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createSignalRequest** | **CreateSignalRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


### Return type

**Signal**

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

# **createSignal**
> Signal createSignal()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/signals` を使用してください）  信号定義を作成します。   * **Note**      - 既存の信号定義と `label` が重複する場合、または `uuid` が重複する場合は、        ステータスコード `409 Conflict` が返却されます。

### Example

```typescript
import {
    MeasSignalsApi,
    Configuration,
    CreateSignalRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasSignalsApi(configuration);

let createSignalRequest: CreateSignalRequest; // (optional)

const { status, data } = await apiInstance.createSignal(
    createSignalRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createSignalRequest** | **CreateSignalRequest**|  | |


### Return type

**Signal**

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

# **deleteProjectSignal**
> deleteProjectSignal()

信号定義を削除します。

### Example

```typescript
import {
    MeasSignalsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasSignalsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let signalUuid: string; //信号定義のUUID (default to undefined)

const { status, data } = await apiInstance.deleteProjectSignal(
    projectUuid,
    signalUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **signalUuid** | [**string**] | 信号定義のUUID | defaults to undefined|


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

# **deleteSignal**
> deleteSignal()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/signals/{signal_uuid}` を使用してください） 信号定義を削除します。

### Example

```typescript
import {
    MeasSignalsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasSignalsApi(configuration);

let signalUuid: string; //信号定義のUUID (default to undefined)

const { status, data } = await apiInstance.deleteSignal(
    signalUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **signalUuid** | [**string**] | 信号定義のUUID | defaults to undefined|


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

# **getProjectSignal**
> Signal getProjectSignal()

信号定義を取得します。

### Example

```typescript
import {
    MeasSignalsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasSignalsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let signalUuid: string; //信号定義のUUID (default to undefined)

const { status, data } = await apiInstance.getProjectSignal(
    projectUuid,
    signalUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **signalUuid** | [**string**] | 信号定義のUUID | defaults to undefined|


### Return type

**Signal**

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

# **getSignal**
> Signal getSignal()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/signals/{signal_uuid}` を使用してください） 信号定義を取得します。

### Example

```typescript
import {
    MeasSignalsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasSignalsApi(configuration);

let signalUuid: string; //信号定義のUUID (default to undefined)

const { status, data } = await apiInstance.getSignal(
    signalUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **signalUuid** | [**string**] | 信号定義のUUID | defaults to undefined|


### Return type

**Signal**

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

# **listProjectSignals**
> Signals listProjectSignals()

信号定義のリストを取得します。

### Example

```typescript
import {
    MeasSignalsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasSignalsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let label: Array<string>; //ラベルが指定した文字列から始まる信号定義を取得します。 文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 (optional) (default to undefined)
let sort: 'label' | 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to undefined)

const { status, data } = await apiInstance.listProjectSignals(
    projectUuid,
    label,
    sort,
    order,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **label** | **Array&lt;string&gt;** | ラベルが指定した文字列から始まる信号定義を取得します。 文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 | (optional) defaults to undefined|
| **sort** | [**&#39;label&#39; | &#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;label&#39; &#124; &#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|


### Return type

**Signals**

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

# **listSignals**
> Signals listSignals()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/signals` を使用してください） 信号定義のリストを取得します。

### Example

```typescript
import {
    MeasSignalsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasSignalsApi(configuration);

let label: Array<string>; //ラベルが指定した文字列から始まる信号定義を取得します。 文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 (optional) (default to undefined)
let sort: 'label' | 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to undefined)

const { status, data } = await apiInstance.listSignals(
    label,
    sort,
    order,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **label** | **Array&lt;string&gt;** | ラベルが指定した文字列から始まる信号定義を取得します。 文字列をダブルクォーテーションで囲むと、完全一致のものだけを取得します。 | (optional) defaults to undefined|
| **sort** | [**&#39;label&#39; | &#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;label&#39; &#124; &#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|


### Return type

**Signals**

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

# **updateProjectSignal**
> Signal updateProjectSignal()

信号定義を更新します。

### Example

```typescript
import {
    MeasSignalsApi,
    Configuration,
    UpdateSignalRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasSignalsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let signalUuid: string; //信号定義のUUID (default to undefined)
let updateSignalRequest: UpdateSignalRequest; // (optional)

const { status, data } = await apiInstance.updateProjectSignal(
    projectUuid,
    signalUuid,
    updateSignalRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateSignalRequest** | **UpdateSignalRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **signalUuid** | [**string**] | 信号定義のUUID | defaults to undefined|


### Return type

**Signal**

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

# **updateSignal**
> Signal updateSignal()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/signals/{signal_uuid}` を使用してください） 信号定義を更新します。

### Example

```typescript
import {
    MeasSignalsApi,
    Configuration,
    UpdateSignalRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasSignalsApi(configuration);

let signalUuid: string; //信号定義のUUID (default to undefined)
let updateSignalRequest: UpdateSignalRequest; // (optional)

const { status, data } = await apiInstance.updateSignal(
    signalUuid,
    updateSignalRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateSignalRequest** | **UpdateSignalRequest**|  | |
| **signalUuid** | [**string**] | 信号定義のUUID | defaults to undefined|


### Return type

**Signal**

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

