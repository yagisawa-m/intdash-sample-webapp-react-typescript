# MediaVideosApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**cancelCreatingJpeg**](#cancelcreatingjpeg) | **PUT** /media/videos/{video_uuid}/jpegs/{jpeg_uuid}/cancel_convert | Cancel Creating JPEG|
|[**cancelCreatingMP4**](#cancelcreatingmp4) | **PUT** /media/videos/{video_uuid}/mp4s/{mp4_uuid}/cancel_convert | Cancel Creating MP4|
|[**cancelCreatingProjectJpeg**](#cancelcreatingprojectjpeg) | **PUT** /media/projects/{project_uuid}/videos/{video_uuid}/jpegs/{jpeg_uuid}/cancel_convert | Cancel Creating Project JPEG|
|[**cancelCreatingProjectMP4**](#cancelcreatingprojectmp4) | **PUT** /media/projects/{project_uuid}/videos/{video_uuid}/mp4s/{mp4_uuid}/cancel_convert | Cancel Creating Project MP4|
|[**createJpeg**](#createjpeg) | **POST** /media/videos/{video_uuid}/jpegs | Create JPEG|
|[**createMP4**](#createmp4) | **POST** /media/videos/{video_uuid}/mp4s | Create MP4|
|[**createProjectJpeg**](#createprojectjpeg) | **POST** /media/projects/{project_uuid}/videos/{video_uuid}/jpegs | Create Project JPEG|
|[**createProjectMP4**](#createprojectmp4) | **POST** /media/projects/{project_uuid}/videos/{video_uuid}/mp4s | Create Project MP4|
|[**deleteJpeg**](#deletejpeg) | **DELETE** /media/videos/{video_uuid}/jpegs/{jpeg_uuid} | Delete JPEG|
|[**deleteMP4**](#deletemp4) | **DELETE** /media/videos/{video_uuid}/mp4s/{mp4_uuid} | Delete MP4|
|[**deleteProjectJpeg**](#deleteprojectjpeg) | **DELETE** /media/projects/{project_uuid}/videos/{video_uuid}/jpegs/{jpeg_uuid} | Delete Project JPEG|
|[**deleteProjectMP4**](#deleteprojectmp4) | **DELETE** /media/projects/{project_uuid}/videos/{video_uuid}/mp4s/{mp4_uuid} | Delete Project MP4|
|[**getJpeg**](#getjpeg) | **GET** /media/videos/{video_uuid}/jpegs/{jpeg_uuid} | Get JPEG|
|[**getJpegAsZip**](#getjpegaszip) | **GET** /media/videos/{video_uuid}/jpegs/{jpeg_uuid}/images/selected.zip | Get JPEG as zip|
|[**getJpegs**](#getjpegs) | **GET** /media/videos/{video_uuid}/jpegs | List JPEGs|
|[**getMP4**](#getmp4) | **GET** /media/videos/{video_uuid}/mp4s/{mp4_uuid} | Get MP4|
|[**getMP4s**](#getmp4s) | **GET** /media/videos/{video_uuid}/mp4s | List MP4s|
|[**getProjectJpeg**](#getprojectjpeg) | **GET** /media/projects/{project_uuid}/videos/{video_uuid}/jpegs/{jpeg_uuid} | Get Project JPEG|
|[**getProjectJpegAsZip**](#getprojectjpegaszip) | **GET** /media/projects/{project_uuid}/videos/{video_uuid}/jpegs/{jpeg_uuid}/images/selected.zip | Get Project JPEG as zip|
|[**getProjectJpegs**](#getprojectjpegs) | **GET** /media/projects/{project_uuid}/videos/{video_uuid}/jpegs | List Project JPEGs|
|[**getProjectMP4**](#getprojectmp4) | **GET** /media/projects/{project_uuid}/videos/{video_uuid}/mp4s/{mp4_uuid} | Get Project MP4|
|[**getProjectMP4s**](#getprojectmp4s) | **GET** /media/projects/{project_uuid}/videos/{video_uuid}/mp4s | List Project MP4s|
|[**getProjectVideo**](#getprojectvideo) | **GET** /media/projects/{project_uuid}/videos/{video_uuid} | Get Project Video|
|[**getProjectVideos**](#getprojectvideos) | **GET** /media/projects/{project_uuid}/videos | List Project Videos|
|[**getVideo**](#getvideo) | **GET** /media/videos/{video_uuid} | Get Video|
|[**getVideos**](#getvideos) | **GET** /media/videos | List Videos|

# **cancelCreatingJpeg**
> Jpeg cancelCreatingJpeg()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画（video）からJPEGデータへの変換をキャンセルします。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let jpegUuid: string; //JPEGのUUID (default to undefined)

const { status, data } = await apiInstance.cancelCreatingJpeg(
    videoUuid,
    jpegUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **jpegUuid** | [**string**] | JPEGのUUID | defaults to undefined|


### Return type

**Jpeg**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **cancelCreatingMP4**
> MP4 cancelCreatingMP4()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画（video）からMP4データへの変換をキャンセルします。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let mp4Uuid: string; //MP4のUUID (default to undefined)

const { status, data } = await apiInstance.cancelCreatingMP4(
    videoUuid,
    mp4Uuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **mp4Uuid** | [**string**] | MP4のUUID | defaults to undefined|


### Return type

**MP4**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **cancelCreatingProjectJpeg**
> Jpeg cancelCreatingProjectJpeg()

動画（video）からJPEGデータへの変換をキャンセルします。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let jpegUuid: string; //JPEGのUUID (default to undefined)

const { status, data } = await apiInstance.cancelCreatingProjectJpeg(
    projectUuid,
    videoUuid,
    jpegUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **jpegUuid** | [**string**] | JPEGのUUID | defaults to undefined|


### Return type

**Jpeg**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **cancelCreatingProjectMP4**
> MP4 cancelCreatingProjectMP4()

動画（video）からMP4データへの変換をキャンセルします。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let mp4Uuid: string; //MP4のUUID (default to undefined)

const { status, data } = await apiInstance.cancelCreatingProjectMP4(
    projectUuid,
    videoUuid,
    mp4Uuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **mp4Uuid** | [**string**] | MP4のUUID | defaults to undefined|


### Return type

**MP4**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createJpeg**
> Jpeg createJpeg()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画（video）を変換してJPEGデータを作成します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration,
    CreateJpegRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let createJpegRequest: CreateJpegRequest; // (optional)

const { status, data } = await apiInstance.createJpeg(
    videoUuid,
    createJpegRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createJpegRequest** | **CreateJpegRequest**|  | |
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|


### Return type

**Jpeg**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createMP4**
> MP4 createMP4()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画（video）を変換してMP4データを作成します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration,
    CreateMP4Request
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let createMP4Request: CreateMP4Request; // (optional)

const { status, data } = await apiInstance.createMP4(
    videoUuid,
    createMP4Request
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createMP4Request** | **CreateMP4Request**|  | |
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|


### Return type

**MP4**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createProjectJpeg**
> Jpeg createProjectJpeg()

動画（video）を変換してJPEGデータを作成します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration,
    CreateJpegRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let createJpegRequest: CreateJpegRequest; // (optional)

const { status, data } = await apiInstance.createProjectJpeg(
    projectUuid,
    videoUuid,
    createJpegRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createJpegRequest** | **CreateJpegRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|


### Return type

**Jpeg**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createProjectMP4**
> MP4 createProjectMP4()

動画（video）を変換してMP4データを作成します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration,
    CreateMP4Request
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let createMP4Request: CreateMP4Request; // (optional)

const { status, data } = await apiInstance.createProjectMP4(
    projectUuid,
    videoUuid,
    createMP4Request
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createMP4Request** | **CreateMP4Request**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|


### Return type

**MP4**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteJpeg**
> deleteJpeg()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画（video）から変換されたJPEGデータを削除します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let jpegUuid: string; //JPEGのUUID (default to undefined)

const { status, data } = await apiInstance.deleteJpeg(
    videoUuid,
    jpegUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **jpegUuid** | [**string**] | JPEGのUUID | defaults to undefined|


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

# **deleteMP4**
> deleteMP4()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画（video）から変換されたMP4データを削除します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let mp4Uuid: string; //MP4のUUID (default to undefined)

const { status, data } = await apiInstance.deleteMP4(
    videoUuid,
    mp4Uuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **mp4Uuid** | [**string**] | MP4のUUID | defaults to undefined|


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

# **deleteProjectJpeg**
> deleteProjectJpeg()

動画（video）から変換されたJPEGデータを削除します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let jpegUuid: string; //JPEGのUUID (default to undefined)

const { status, data } = await apiInstance.deleteProjectJpeg(
    projectUuid,
    videoUuid,
    jpegUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **jpegUuid** | [**string**] | JPEGのUUID | defaults to undefined|


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

# **deleteProjectMP4**
> deleteProjectMP4()

動画（video）から変換されたMP4データを削除します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let mp4Uuid: string; //MP4のUUID (default to undefined)

const { status, data } = await apiInstance.deleteProjectMP4(
    projectUuid,
    videoUuid,
    mp4Uuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **mp4Uuid** | [**string**] | MP4のUUID | defaults to undefined|


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

# **getJpeg**
> Jpeg getJpeg()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画（video）から変換されたJPEGデータの情報を取得します。 JPEGファイル自体を取得するには、`GET /media/videos/{video_uuid}/jpegs/{jpeg_uuid}/images/selected.zip` を使用してください。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let jpegUuid: string; //JPEGのUUID (default to undefined)

const { status, data } = await apiInstance.getJpeg(
    videoUuid,
    jpegUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **jpegUuid** | [**string**] | JPEGのUUID | defaults to undefined|


### Return type

**Jpeg**

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

# **getJpegAsZip**
> File getJpegAsZip()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） JPEGデータをZIPファイルにまとめた形で取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let jpegUuid: string; //JPEGのUUID (default to undefined)
let indexes: Array<number>; //取得したいJPEGのインデックス番号（最初の番号は1）。指定がない場合はすべて取得します。 `indexes` パラメーターを複数回指定することで、複数のJPEGファイルを取得することができます。 (optional) (default to undefined)

const { status, data } = await apiInstance.getJpegAsZip(
    videoUuid,
    jpegUuid,
    indexes
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **jpegUuid** | [**string**] | JPEGのUUID | defaults to undefined|
| **indexes** | **Array&lt;number&gt;** | 取得したいJPEGのインデックス番号（最初の番号は1）。指定がない場合はすべて取得します。 &#x60;indexes&#x60; パラメーターを複数回指定することで、複数のJPEGファイルを取得することができます。 | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getJpegs**
> Jpegs getJpegs()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画（video）から変換されたJPEGデータのリストを取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)

const { status, data } = await apiInstance.getJpegs(
    videoUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|


### Return type

**Jpegs**

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

# **getMP4**
> MP4 getMP4()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画（video）から変換されたMP4データの情報を取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let mp4Uuid: string; //MP4のUUID (default to undefined)

const { status, data } = await apiInstance.getMP4(
    videoUuid,
    mp4Uuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **mp4Uuid** | [**string**] | MP4のUUID | defaults to undefined|


### Return type

**MP4**

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

# **getMP4s**
> MP4s getMP4s()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画（video）から変換されたMP4データのリストを取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)

const { status, data } = await apiInstance.getMP4s(
    videoUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|


### Return type

**MP4s**

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

# **getProjectJpeg**
> Jpeg getProjectJpeg()

動画（video）から変換されたJPEGデータの情報を取得します。 JPEGファイル自体を取得するには、`GET /media/projects/{project_uuid}/videos/{video_uuid}/jpegs/{jpeg_uuid}/images/selected.zip` を使用してください。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let jpegUuid: string; //JPEGのUUID (default to undefined)

const { status, data } = await apiInstance.getProjectJpeg(
    projectUuid,
    videoUuid,
    jpegUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **jpegUuid** | [**string**] | JPEGのUUID | defaults to undefined|


### Return type

**Jpeg**

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

# **getProjectJpegAsZip**
> File getProjectJpegAsZip()

JPEGデータをZIPファイルにまとめた形で取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let jpegUuid: string; //JPEGのUUID (default to undefined)
let indexes: Array<number>; //取得したいJPEGのインデックス番号（最初の番号は1）。指定がない場合はすべて取得します。 `indexes` パラメーターを複数回指定することで、複数のJPEGファイルを取得することができます。 (optional) (default to undefined)

const { status, data } = await apiInstance.getProjectJpegAsZip(
    projectUuid,
    videoUuid,
    jpegUuid,
    indexes
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **jpegUuid** | [**string**] | JPEGのUUID | defaults to undefined|
| **indexes** | **Array&lt;number&gt;** | 取得したいJPEGのインデックス番号（最初の番号は1）。指定がない場合はすべて取得します。 &#x60;indexes&#x60; パラメーターを複数回指定することで、複数のJPEGファイルを取得することができます。 | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProjectJpegs**
> Jpegs getProjectJpegs()

動画（video）から変換されたJPEGデータのリストを取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)

const { status, data } = await apiInstance.getProjectJpegs(
    projectUuid,
    videoUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|


### Return type

**Jpegs**

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

# **getProjectMP4**
> MP4 getProjectMP4()

動画（video）から変換されたMP4データの情報を取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)
let mp4Uuid: string; //MP4のUUID (default to undefined)

const { status, data } = await apiInstance.getProjectMP4(
    projectUuid,
    videoUuid,
    mp4Uuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|
| **mp4Uuid** | [**string**] | MP4のUUID | defaults to undefined|


### Return type

**MP4**

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

# **getProjectMP4s**
> MP4s getProjectMP4s()

動画（video）から変換されたMP4データのリストを取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)

const { status, data } = await apiInstance.getProjectMP4s(
    projectUuid,
    videoUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|


### Return type

**MP4s**

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

# **getProjectVideo**
> Video getProjectVideo()

動画を取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)

const { status, data } = await apiInstance.getProjectVideo(
    projectUuid,
    videoUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|


### Return type

**Video**

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

# **getProjectVideos**
> Videos getProjectVideos()

動画（video）のリストを取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let uuid: string; //動画（video）のUUID (optional) (default to undefined)
let measUuid: string; //計測のUUID (optional) (default to undefined)
let channel: number; //チャンネル (optional) (default to undefined)
let sort: string; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。例えば、 `name-` を指定すると、nameによる降順で出力されます。    - `channel`   - `created_at`   - `updated_at` (optional) (default to 'create_at+')
let page: number; //取得するページ番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 100)

const { status, data } = await apiInstance.getProjectVideos(
    projectUuid,
    uuid,
    measUuid,
    channel,
    sort,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **uuid** | [**string**] | 動画（video）のUUID | (optional) defaults to undefined|
| **measUuid** | [**string**] | 計測のUUID | (optional) defaults to undefined|
| **channel** | [**number**] | チャンネル | (optional) defaults to undefined|
| **sort** | [**string**] | 並べ替えに使用するキー。接尾辞 &#x60;+&#x60; を付けた場合は昇順、 &#x60;-&#x60; を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。例えば、 &#x60;name-&#x60; を指定すると、nameによる降順で出力されます。    - &#x60;channel&#x60;   - &#x60;created_at&#x60;   - &#x60;updated_at&#x60; | (optional) defaults to 'create_at+'|
| **page** | [**number**] | 取得するページ番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 100|


### Return type

**Videos**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getVideo**
> Video getVideo()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画を取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let videoUuid: string; //変換元の動画（video）のUUID (default to undefined)

const { status, data } = await apiInstance.getVideo(
    videoUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **videoUuid** | [**string**] | 変換元の動画（video）のUUID | defaults to undefined|


### Return type

**Video**

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

# **getVideos**
> Videos getVideos()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） 動画（video）のリストを取得します。

### Example

```typescript
import {
    MediaVideosApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaVideosApi(configuration);

let uuid: string; //動画（video）のUUID (optional) (default to undefined)
let measUuid: string; //計測のUUID (optional) (default to undefined)
let channel: number; //計測のチャンネル。チャンネルが存在しない計測データ（iscp-v2）の動画のみを取得したい場合は0を指定します。未指定の場合、チャンネルの有無問わず全ての動画を取得します。 (optional) (default to undefined)
let sort: string; //並べ替えに使用するキー。接尾辞 `+` を付けた場合は昇順、 `-` を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。例えば、 `name-` を指定すると、nameによる降順で出力されます。    - `channel`   - `created_at`   - `updated_at` (optional) (default to 'create_at+')
let page: number; //取得するページ番号 (optional) (default to 1)
let perPage: number; //1回のリクエストで取得する件数 (optional) (default to 100)

const { status, data } = await apiInstance.getVideos(
    uuid,
    measUuid,
    channel,
    sort,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uuid** | [**string**] | 動画（video）のUUID | (optional) defaults to undefined|
| **measUuid** | [**string**] | 計測のUUID | (optional) defaults to undefined|
| **channel** | [**number**] | 計測のチャンネル。チャンネルが存在しない計測データ（iscp-v2）の動画のみを取得したい場合は0を指定します。未指定の場合、チャンネルの有無問わず全ての動画を取得します。 | (optional) defaults to undefined|
| **sort** | [**string**] | 並べ替えに使用するキー。接尾辞 &#x60;+&#x60; を付けた場合は昇順、 &#x60;-&#x60; を付けた場合は降順で出力されます。 接尾辞を省略した場合は昇順となります。例えば、 &#x60;name-&#x60; を指定すると、nameによる降順で出力されます。    - &#x60;channel&#x60;   - &#x60;created_at&#x60;   - &#x60;updated_at&#x60; | (optional) defaults to 'create_at+'|
| **page** | [**number**] | 取得するページ番号 | (optional) defaults to 1|
| **perPage** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to 100|


### Return type

**Videos**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

