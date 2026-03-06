# BrokerEdgeConnectionsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getEdgeConnection**](#getedgeconnection) | **GET** /v1/edge_connections/{edge_connection_uuid} | Get Edge Connection|
|[**getProjectEdgeConnection**](#getprojectedgeconnection) | **GET** /v1/projects/{project_uuid}/edge_connections/{edge_connection_uuid} | Get Project Edge Connection|
|[**listEdgeConnections**](#listedgeconnections) | **GET** /v1/edge_connections | List Edge Connections|
|[**listProjectEdgeConnections**](#listprojectedgeconnections) | **GET** /v1/projects/{project_uuid}/edge_connections | List Project Edge Connections|

# **getEdgeConnection**
> EdgeConnection getEdgeConnection()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/edge_connection/{edge_connection_uuid}` を使用してください） エッジ接続（ `/v1/ws/measurements` に接続されたエッジの接続情報）を取得します。

### Example

```typescript
import {
    BrokerEdgeConnectionsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerEdgeConnectionsApi(configuration);

let edgeConnectionUuid: string; //エッジ接続のUUID (default to undefined)

const { status, data } = await apiInstance.getEdgeConnection(
    edgeConnectionUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edgeConnectionUuid** | [**string**] | エッジ接続のUUID | defaults to undefined|


### Return type

**EdgeConnection**

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

# **getProjectEdgeConnection**
> EdgeConnection getProjectEdgeConnection()

エッジ接続（ `/v1/ws/measurements` に接続されたエッジの接続情報）を取得します。

### Example

```typescript
import {
    BrokerEdgeConnectionsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerEdgeConnectionsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let edgeConnectionUuid: string; //エッジ接続のUUID (default to undefined)

const { status, data } = await apiInstance.getProjectEdgeConnection(
    projectUuid,
    edgeConnectionUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **edgeConnectionUuid** | [**string**] | エッジ接続のUUID | defaults to undefined|


### Return type

**EdgeConnection**

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

# **listEdgeConnections**
> EdgeConnectionList listEdgeConnections()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/edge_connection` を使用してください）  エッジ接続のリストを取得します。  エッジ接続は、エッジが `/v1/ws/measurements` エンドポイントに接続したときに新規作成され、  3日間更新がないと削除されます。

### Example

```typescript
import {
    BrokerEdgeConnectionsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerEdgeConnectionsApi(configuration);

let edge: Array<string>; //エッジのUUID (optional) (default to undefined)
let groupByEdge: boolean; //最新接続日時でエッジごとにグルーピングするかどうか (optional) (default to false)
let sort: 'last_lived_at' | 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'last_lived_at')
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to 'desc')
let limit: number; //1回のリクエストで取得する件数 (optional) (default to 100)
let page: number; //取得するページの番号 (optional) (default to 1)

const { status, data } = await apiInstance.listEdgeConnections(
    edge,
    groupByEdge,
    sort,
    order,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edge** | **Array&lt;string&gt;** | エッジのUUID | (optional) defaults to undefined|
| **groupByEdge** | [**boolean**] | 最新接続日時でエッジごとにグルーピングするかどうか | (optional) defaults to false|
| **sort** | [**&#39;last_lived_at&#39; | &#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;last_lived_at&#39; &#124; &#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'last_lived_at'|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to 'desc'|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 100|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|


### Return type

**EdgeConnectionList**

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

# **listProjectEdgeConnections**
> EdgeConnectionList listProjectEdgeConnections()

エッジ接続のリストを取得します。 エッジ接続は、エッジが `/v1/ws/measurements` エンドポイントに接続したときに新規作成され、 3日間更新がないと削除されます。

### Example

```typescript
import {
    BrokerEdgeConnectionsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerEdgeConnectionsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let edge: Array<string>; //エッジのUUID (optional) (default to undefined)
let groupByEdge: boolean; //最新接続日時でエッジごとにグルーピングするかどうか (optional) (default to false)
let sort: 'last_lived_at' | 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'last_lived_at')
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to 'desc')
let limit: number; //1回のリクエストで取得する件数 (optional) (default to 100)
let page: number; //取得するページの番号 (optional) (default to 1)

const { status, data } = await apiInstance.listProjectEdgeConnections(
    projectUuid,
    edge,
    groupByEdge,
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
| **edge** | **Array&lt;string&gt;** | エッジのUUID | (optional) defaults to undefined|
| **groupByEdge** | [**boolean**] | 最新接続日時でエッジごとにグルーピングするかどうか | (optional) defaults to false|
| **sort** | [**&#39;last_lived_at&#39; | &#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;last_lived_at&#39; &#124; &#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'last_lived_at'|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to 'desc'|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 100|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to 1|


### Return type

**EdgeConnectionList**

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

