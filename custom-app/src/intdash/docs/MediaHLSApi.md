# MediaHLSApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getFMP4**](#getfmp4) | **GET** /media/measurements/{meas_uuid}/channels/{channel}/mp4s/measurement.mp4 | Get HLS as FMP4|
|[**getHLSes**](#gethlses) | **GET** /media/hlses | List HLSes|
|[**getPlaylist**](#getplaylist) | **GET** /media/measurements/{meas_uuid}/channels/{channel}/hlses/playlist.m3u8 | Get HLS Playlist|
|[**getProjectFMP4**](#getprojectfmp4) | **GET** /media/projects/{project_uuid}/measurements/{meas_uuid}/channels/{channel}/mp4s/measurement.mp4 | Get Project HLS as FMP4|
|[**getProjectHLSes**](#getprojecthlses) | **GET** /media/projects/{project_uuid}/hlses | List Project HLSes|
|[**getProjectPlaylist**](#getprojectplaylist) | **GET** /media/projects/{project_uuid}/measurements/{meas_uuid}/channels/{channel}/hlses/playlist.m3u8 | Get Project HLS Playlist|

# **getFMP4**
> File getFMP4()

**Deprecated** このエンドポイントの代わりに [`POST /media/videos/{video_uuid}/mp4s`](#operation/createMP4) を使用してください。 mp4リソース作成後、 `MP4`オブジェクトの `file_path`にあるPATHに従って動画を取得してください

### Example

```typescript
import {
    MediaHLSApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaHLSApi(configuration);

let measUuid: string; //計測のUUID (default to undefined)
let channel: number; //チャンネル (default to undefined)

const { status, data } = await apiInstance.getFMP4(
    measUuid,
    channel
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **channel** | [**number**] | チャンネル | defaults to undefined|


### Return type

**File**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: video/mp4


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getHLSes**
> HLSList getHLSes()

**Deprecated** このエンドポイントではなく [`GET /media/videos`](#operation/getVideos) を使用してください

### Example

```typescript
import {
    MediaHLSApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaHLSApi(configuration);

let start: number; //取得対象範囲の始点（マイクロ秒単位のUNIX時刻） (optional) (default to undefined)
let end: number; //取得対象範囲の終点（マイクロ秒単位のUNIX時刻） (optional) (default to undefined)
let edgeUuid: string; //エッジのUUID (optional) (default to undefined)
let channel: number; //チャンネル (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)

const { status, data } = await apiInstance.getHLSes(
    start,
    end,
    edgeUuid,
    channel,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**number**] | 取得対象範囲の始点（マイクロ秒単位のUNIX時刻） | (optional) defaults to undefined|
| **end** | [**number**] | 取得対象範囲の終点（マイクロ秒単位のUNIX時刻） | (optional) defaults to undefined|
| **edgeUuid** | [**string**] | エッジのUUID | (optional) defaults to undefined|
| **channel** | [**number**] | チャンネル | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|


### Return type

**HLSList**

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

# **getPlaylist**
> string getPlaylist()

**Depricated** このエンドポイントの代わりに、Videoオブジェクトの `hls`にあるPATHにしたがってPlaylistを取得してください。

### Example

```typescript
import {
    MediaHLSApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaHLSApi(configuration);

let measUuid: string; //計測のUUID (default to undefined)
let channel: number; //チャンネル (default to undefined)
let forceEnd: boolean; //`true` にすると、取得するm3u8形式のプレイリストに強制的にEXT-X-ENDLISTを追加します。 (optional) (default to undefined)

const { status, data } = await apiInstance.getPlaylist(
    measUuid,
    channel,
    forceEnd
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **channel** | [**number**] | チャンネル | defaults to undefined|
| **forceEnd** | [**boolean**] | &#x60;true&#x60; にすると、取得するm3u8形式のプレイリストに強制的にEXT-X-ENDLISTを追加します。 | (optional) defaults to undefined|


### Return type

**string**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.apple.mpegurl


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProjectFMP4**
> File getProjectFMP4()

**Deprecated** このエンドポイントの代わりに [`POST /media/videos/{video_uuid}/mp4s`](#operation/createMP4) を使用してください。 mp4リソース作成後、 `MP4`オブジェクトの `file_path`にあるPATHに従って動画を取得してください

### Example

```typescript
import {
    MediaHLSApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaHLSApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measUuid: string; //計測のUUID (default to undefined)
let channel: number; //チャンネル (default to undefined)

const { status, data } = await apiInstance.getProjectFMP4(
    projectUuid,
    measUuid,
    channel
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **channel** | [**number**] | チャンネル | defaults to undefined|


### Return type

**File**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: video/mp4


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProjectHLSes**
> HLSList getProjectHLSes()

**Deprecated** このエンドポイントではなく [`GET /media/videos`](#operation/getVideos) を使用してください

### Example

```typescript
import {
    MediaHLSApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaHLSApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let start: number; //取得対象範囲の始点（マイクロ秒単位のUNIX時刻） (optional) (default to undefined)
let end: number; //取得対象範囲の終点（マイクロ秒単位のUNIX時刻） (optional) (default to undefined)
let edgeUuid: string; //エッジのUUID (optional) (default to undefined)
let channel: number; //チャンネル (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)

const { status, data } = await apiInstance.getProjectHLSes(
    projectUuid,
    start,
    end,
    edgeUuid,
    channel,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **start** | [**number**] | 取得対象範囲の始点（マイクロ秒単位のUNIX時刻） | (optional) defaults to undefined|
| **end** | [**number**] | 取得対象範囲の終点（マイクロ秒単位のUNIX時刻） | (optional) defaults to undefined|
| **edgeUuid** | [**string**] | エッジのUUID | (optional) defaults to undefined|
| **channel** | [**number**] | チャンネル | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|


### Return type

**HLSList**

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

# **getProjectPlaylist**
> string getProjectPlaylist()

**Depricated** このエンドポイントの代わりに、Videoオブジェクトの `hls`にあるPATHにしたがってPlaylistを取得してください。

### Example

```typescript
import {
    MediaHLSApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaHLSApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measUuid: string; //計測のUUID (default to undefined)
let channel: number; //チャンネル (default to undefined)
let forceEnd: boolean; //`true` にすると、取得するm3u8形式のプレイリストに強制的にEXT-X-ENDLISTを追加します。 (optional) (default to undefined)

const { status, data } = await apiInstance.getProjectPlaylist(
    projectUuid,
    measUuid,
    channel,
    forceEnd
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **channel** | [**number**] | チャンネル | defaults to undefined|
| **forceEnd** | [**boolean**] | &#x60;true&#x60; にすると、取得するm3u8形式のプレイリストに強制的にEXT-X-ENDLISTを追加します。 | (optional) defaults to undefined|


### Return type

**string**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.apple.mpegurl


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

