# MediaLiveApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**connectLive**](#connectlive) | **GET** /media/ws/edges/{edge_uuid}/fmp4s/{channel} | Get realtime video stream|
|[**connectProjectLive**](#connectprojectlive) | **GET** /media/projects/{project_uuid}/ws/edges/{edge_uuid}/fmp4s/{channel} | Get Project realtime video stream|

# **connectLive**
> connectLive()

**Deprecated** このエンドポイントの代わりに [`GET /v1/stream`](#operation/Stream) でデータを取得し、WebCodecsを使用して取得したデータをデコードしてください。

### Example

```typescript
import {
    MediaLiveApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaLiveApi(configuration);

let edgeUuid: string; //エッジのUUID (default to undefined)
let channel: number; //チャンネル (default to undefined)

const { status, data } = await apiInstance.connectLive(
    edgeUuid,
    channel
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|
| **channel** | [**number**] | チャンネル | defaults to undefined|


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
|**101** | Switching Protocols |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **connectProjectLive**
> connectProjectLive()

**Deprecated** このエンドポイントの代わりに [`GET /v1/stream`](#operation/Stream) でデータを取得し、WebCodecsを使用して取得したデータをデコードしてください。

### Example

```typescript
import {
    MediaLiveApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaLiveApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let edgeUuid: string; //エッジのUUID (default to undefined)
let channel: number; //チャンネル (default to undefined)

const { status, data } = await apiInstance.connectProjectLive(
    projectUuid,
    edgeUuid,
    channel
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|
| **channel** | [**number**] | チャンネル | defaults to undefined|


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
|**101** | Switching Protocols |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

