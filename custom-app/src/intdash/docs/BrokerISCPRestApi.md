# BrokerISCPRestApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**closeUpstream**](#closeupstream) | **PUT** /iscp/projects/{project_uuid}/upstreams/{stream_id}/close | Close Upstream|
|[**createUpstream**](#createupstream) | **POST** /iscp/projects/{project_uuid}/upstreams | Create Upstream|
|[**sendUpstreamChunks**](#sendupstreamchunks) | **POST** /iscp/projects/{project_uuid}/upstreams/{stream_id}/chunks | Send Upstream Chunks|
|[**sendUpstreamMetadata**](#sendupstreammetadata) | **POST** /iscp/projects/{project_uuid}/upstream_metadatas | Send Upstream Metadata|

# **closeUpstream**
> Upstream closeUpstream()

アップストリームをクローズします。

### Example

```typescript
import {
    BrokerISCPRestApi,
    Configuration,
    CloseUpstreamRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPRestApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let streamId: string; //ストリームのID (default to undefined)
let closeUpstreamRequest: CloseUpstreamRequest; // (optional)

const { status, data } = await apiInstance.closeUpstream(
    projectUuid,
    streamId,
    closeUpstreamRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **closeUpstreamRequest** | **CloseUpstreamRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **streamId** | [**string**] | ストリームのID | defaults to undefined|


### Return type

**Upstream**

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

# **createUpstream**
> Upstream createUpstream()

アップストリームを作成します。

### Example

```typescript
import {
    BrokerISCPRestApi,
    Configuration,
    CreateUpstreamRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPRestApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let createUpstreamRequest: CreateUpstreamRequest; // (optional)

const { status, data } = await apiInstance.createUpstream(
    projectUuid,
    createUpstreamRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createUpstreamRequest** | **CreateUpstreamRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


### Return type

**Upstream**

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

# **sendUpstreamChunks**
> Upstream sendUpstreamChunks()

アップストリームチャンクを送信します。

### Example

```typescript
import {
    BrokerISCPRestApi,
    Configuration,
    SendUpstreamChunksRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPRestApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let streamId: string; //ストリームのID (default to undefined)
let sendUpstreamChunksRequest: SendUpstreamChunksRequest; // (optional)

const { status, data } = await apiInstance.sendUpstreamChunks(
    projectUuid,
    streamId,
    sendUpstreamChunksRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **sendUpstreamChunksRequest** | **SendUpstreamChunksRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **streamId** | [**string**] | ストリームのID | defaults to undefined|


### Return type

**Upstream**

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

# **sendUpstreamMetadata**
> sendUpstreamMetadata()

メタデータを送信します。

### Example

```typescript
import {
    BrokerISCPRestApi,
    Configuration,
    SendUpstreamMetadataRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPRestApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let sendUpstreamMetadataRequest: SendUpstreamMetadataRequest; // (optional)

const { status, data } = await apiInstance.sendUpstreamMetadata(
    projectUuid,
    sendUpstreamMetadataRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **sendUpstreamMetadataRequest** | **SendUpstreamMetadataRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | No Content |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

