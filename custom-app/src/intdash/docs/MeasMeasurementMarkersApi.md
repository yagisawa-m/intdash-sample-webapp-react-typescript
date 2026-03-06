# MeasMeasurementMarkersApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createMeasurementMarker**](#createmeasurementmarker) | **POST** /v1/measurements/{measurement_uuid}/markers | Create Measurement Marker by Measurement UUID|
|[**createProjectMeasurementMarker**](#createprojectmeasurementmarker) | **POST** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/markers | Create Project Measurement Marker by Measurement UUID|
|[**deleteMeasurementMarker**](#deletemeasurementmarker) | **DELETE** /v1/measurements/markers/{measurement_marker_uuid} | Delete Measurement Marker|
|[**deleteMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**](#deletemeasurementmarkerwithmeasurementuuidandmarkeruuid) | **DELETE** /v1/measurements/{measurement_uuid}/markers/{measurement_marker_uuid} | Delete Measurement Marker using Measurement UUID|
|[**deleteMeasurementMarkers**](#deletemeasurementmarkers) | **DELETE** /v1/measurements/{measurement_uuid}/markers | Delete Measurement Markers by Measurement UUID|
|[**deleteProjectMeasurementMarker**](#deleteprojectmeasurementmarker) | **DELETE** /v1/projects/{project_uuid}/measurements/markers/{measurement_marker_uuid} | Delete Project Measurement Marker|
|[**deleteProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**](#deleteprojectmeasurementmarkerwithmeasurementuuidandmarkeruuid) | **DELETE** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/markers/{measurement_marker_uuid} | Delete Project Measurement Marker using Measurement UUID|
|[**deleteProjectMeasurementMarkers**](#deleteprojectmeasurementmarkers) | **DELETE** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/markers | Delete Project Measurement Markers by Measurement UUID|
|[**getMeasurementMarker**](#getmeasurementmarker) | **GET** /v1/measurements/markers/{measurement_marker_uuid} | Get Measurement Marker|
|[**getMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**](#getmeasurementmarkerwithmeasurementuuidandmarkeruuid) | **GET** /v1/measurements/{measurement_uuid}/markers/{measurement_marker_uuid} | Get Measurement Marker using Measurement UUID|
|[**getMeasurementMarkersWithMeasurementUUID**](#getmeasurementmarkerswithmeasurementuuid) | **GET** /v1/measurements/{measurement_uuid}/markers | List Measurement Markers by Measurement UUID|
|[**getProjectMeasurementMarker**](#getprojectmeasurementmarker) | **GET** /v1/projects/{project_uuid}/measurements/markers/{measurement_marker_uuid} | Get Project Measurement Marker|
|[**getProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**](#getprojectmeasurementmarkerwithmeasurementuuidandmarkeruuid) | **GET** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/markers/{measurement_marker_uuid} | Get Project Measurement Marker using Measurement UUID|
|[**getProjectMeasurementMarkersWithMeasurementUUID**](#getprojectmeasurementmarkerswithmeasurementuuid) | **GET** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/markers | List Project Measurement Markers by Measurement UUID|
|[**listMeasurementMarkers**](#listmeasurementmarkers) | **GET** /v1/measurements/markers | List Measurement Markers|
|[**listProjectMeasurementMarkers**](#listprojectmeasurementmarkers) | **GET** /v1/projects/{project_uuid}/measurements/markers | List Project Measurement Markers|
|[**updateMeasurementMarker**](#updatemeasurementmarker) | **PUT** /v1/measurements/markers/{measurement_marker_uuid} | Update Measurement Marker|
|[**updateMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**](#updatemeasurementmarkerwithmeasurementuuidandmarkeruuid) | **PUT** /v1/measurements/{measurement_uuid}/markers/{measurement_marker_uuid} | Replace Measurement Marker using Measurement UUID|
|[**updateProjectMeasurementMarker**](#updateprojectmeasurementmarker) | **PUT** /v1/projects/{project_uuid}/measurements/markers/{measurement_marker_uuid} | Update Project Measurement Marker|
|[**updateProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**](#updateprojectmeasurementmarkerwithmeasurementuuidandmarkeruuid) | **PUT** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/markers/{measurement_marker_uuid} | Replace Project Measurement Marker using Measurement UUID|

# **createMeasurementMarker**
> MeasurementMarker createMeasurementMarker()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/markers` を使用してください） 計測マーカーを作成します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration,
    MeasurementMarkerPostRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let measurementMarkerPostRequest: MeasurementMarkerPostRequest; // (optional)

const { status, data } = await apiInstance.createMeasurementMarker(
    measurementUuid,
    measurementMarkerPostRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementMarkerPostRequest** | **MeasurementMarkerPostRequest**|  | |
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**MeasurementMarker**

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

# **createProjectMeasurementMarker**
> MeasurementMarker createProjectMeasurementMarker()

計測マーカーを作成します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration,
    MeasurementMarkerPostRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let measurementMarkerPostRequest: MeasurementMarkerPostRequest; // (optional)

const { status, data } = await apiInstance.createProjectMeasurementMarker(
    projectUuid,
    measurementUuid,
    measurementMarkerPostRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementMarkerPostRequest** | **MeasurementMarkerPostRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**MeasurementMarker**

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

# **deleteMeasurementMarker**
> deleteMeasurementMarker()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/markers/{measurement_marker_uuid}` を使用してください） 計測マーカーを削除します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)

const { status, data } = await apiInstance.deleteMeasurementMarker(
    measurementMarkerUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


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

# **deleteMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**
> deleteMeasurementMarkerWithMeasurementUUIDAndMarkerUUID()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/markers/{Measurement_marker_uuid}` を使用してください） 計測マーカーを削除します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)

const { status, data } = await apiInstance.deleteMeasurementMarkerWithMeasurementUUIDAndMarkerUUID(
    measurementUuid,
    measurementMarkerUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


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

# **deleteMeasurementMarkers**
> deleteMeasurementMarkers()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/markers` を使用してください） 計測マーカーを削除します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.deleteMeasurementMarkers(
    measurementUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


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

# **deleteProjectMeasurementMarker**
> deleteProjectMeasurementMarker()

計測マーカーを削除します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)

const { status, data } = await apiInstance.deleteProjectMeasurementMarker(
    projectUuid,
    measurementMarkerUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


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

# **deleteProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**
> deleteProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID()

計測マーカーを削除します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)

const { status, data } = await apiInstance.deleteProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID(
    projectUuid,
    measurementUuid,
    measurementMarkerUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


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

# **deleteProjectMeasurementMarkers**
> deleteProjectMeasurementMarkers()

計測マーカーを削除します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.deleteProjectMeasurementMarkers(
    projectUuid,
    measurementUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


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

# **getMeasurementMarker**
> MeasurementMarker getMeasurementMarker()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/markers/{measurement_marker_uuid}` を使用してください） 計測マーカーを取得します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)

const { status, data } = await apiInstance.getMeasurementMarker(
    measurementMarkerUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


### Return type

**MeasurementMarker**

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

# **getMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**
> MeasurementMarker getMeasurementMarkerWithMeasurementUUIDAndMarkerUUID()

**Deprecated** このエンドポイントではなく、 `GET /measurements/{measurement_uuid}` を使用してください。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)

const { status, data } = await apiInstance.getMeasurementMarkerWithMeasurementUUIDAndMarkerUUID(
    measurementUuid,
    measurementMarkerUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


### Return type

**MeasurementMarker**

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

# **getMeasurementMarkersWithMeasurementUUID**
> MeasurementMarkersWithoutPage getMeasurementMarkersWithMeasurementUUID()

(**Deprecated** このエンドポイントではなく、 `GET /measurements/{measurement_uuid}` を使用してください。) 計測UUIDを指定して、その計測に付与されたマーカーの一覧を取得します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.getMeasurementMarkersWithMeasurementUUID(
    measurementUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**MeasurementMarkersWithoutPage**

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

# **getProjectMeasurementMarker**
> MeasurementMarker getProjectMeasurementMarker()

計測マーカーを取得します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)

const { status, data } = await apiInstance.getProjectMeasurementMarker(
    projectUuid,
    measurementMarkerUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


### Return type

**MeasurementMarker**

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

# **getProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**
> MeasurementMarker getProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID()

**Deprecated** このエンドポイントではなく、 `GET /measurements/{measurement_uuid}` を使用してください。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)

const { status, data } = await apiInstance.getProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID(
    projectUuid,
    measurementUuid,
    measurementMarkerUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


### Return type

**MeasurementMarker**

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

# **getProjectMeasurementMarkersWithMeasurementUUID**
> MeasurementMarkersWithoutPage getProjectMeasurementMarkersWithMeasurementUUID()

(**Deprecated** このエンドポイントではなく、 `GET /measurements/{measurement_uuid}` を使用してください。) 計測UUIDを指定して、その計測に付与されたマーカーの一覧を取得します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.getProjectMeasurementMarkersWithMeasurementUUID(
    projectUuid,
    measurementUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**MeasurementMarkersWithoutPage**

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

# **listMeasurementMarkers**
> MeasurementMarkers listMeasurementMarkers()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/markers` を使用してください） 計測マーカーのリストを取得します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let uuid: Array<string>; //計測マーカーのUUID (optional) (default to undefined)
let name: Array<string>; //計測マーカーの名前 (optional) (default to undefined)
let startUnixMicro: number; //取得対象区間の始点（マイクロ秒単位のUNIX時刻）（始点は対象区間に含まれます）。 範囲マーカーについては、マーカーの始点が取得対象区間に入っている場合に取得されます。 (optional) (default to undefined)
let endUnixMicro: number; //取得対象区間の終点（マイクロ秒単位のUNIX時刻）（終点は対象区間に含まれません）。 範囲マーカーについては、マーカーの始点が取得対象区間に入っている場合に取得されます。 (optional) (default to undefined)
let tagKey: Array<string>; //タグのキーと値を使って条件を指定し、条件に一致する計測マーカーを取得します。 キーのみを指定した場合は、指定されたキーを持つ計測マーカーを取得します。 キーと値を指定した場合は、指定されたキーを持ち、その値として指定された値を含む計測マーカーを取得します。 `tag.<key>=<value>` 条件は複数個指定することができ、OR条件で使用されます。 ただし `!tag.<key>` と組み合わせた場合、  `!tag.<key>` が優先されます。  例:      | measurement marker | tag (key: value) |     | ------------------ | ---------------- |     | 1                  | a: value1        |     |                    | c: value2        |     |                    | e: 1             |      | 2                  | a: b             |     |                    | c: d             |      | 3                  | a: b             |    -  `?tag.e=` の場合、計測マーカー1番が取得されます。   -  `?!tag.c=` の場合、計測マーカー3番が取得されます。   -  `?tag.a=&!tag.e=` の場合、計測マーカー2、3番が取得されます。   -  `?tag.a=val&tag.c=d` の場合、計測マーカー1、2番が取得されます。 (optional) (default to undefined)
let tagKey2: Array<string>; //タグのキーを使って条件を指定し、条件に一致する計測キャプチャを除外します。 タグの値は無視されます。 `!tag.<key>` を複数個指定した場合、AND条件となります。 また、 `tag.<key>=<value>` と組み合わせて使用した場合、 `tag.<key>=<value>`  よりも `!tag.<key>` が優先されます。 例: 上の `tag.<key>` の説明を参照してください。 (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)
let sort: 'name' | 'base_time' | 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'base_time')
let page: number; //取得するページの番号 (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)

const { status, data } = await apiInstance.listMeasurementMarkers(
    uuid,
    name,
    startUnixMicro,
    endUnixMicro,
    tagKey,
    tagKey2,
    limit,
    sort,
    page,
    order
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uuid** | **Array&lt;string&gt;** | 計測マーカーのUUID | (optional) defaults to undefined|
| **name** | **Array&lt;string&gt;** | 計測マーカーの名前 | (optional) defaults to undefined|
| **startUnixMicro** | [**number**] | 取得対象区間の始点（マイクロ秒単位のUNIX時刻）（始点は対象区間に含まれます）。 範囲マーカーについては、マーカーの始点が取得対象区間に入っている場合に取得されます。 | (optional) defaults to undefined|
| **endUnixMicro** | [**number**] | 取得対象区間の終点（マイクロ秒単位のUNIX時刻）（終点は対象区間に含まれません）。 範囲マーカーについては、マーカーの始点が取得対象区間に入っている場合に取得されます。 | (optional) defaults to undefined|
| **tagKey** | **Array&lt;string&gt;** | タグのキーと値を使って条件を指定し、条件に一致する計測マーカーを取得します。 キーのみを指定した場合は、指定されたキーを持つ計測マーカーを取得します。 キーと値を指定した場合は、指定されたキーを持ち、その値として指定された値を含む計測マーカーを取得します。 &#x60;tag.&lt;key&gt;&#x3D;&lt;value&gt;&#x60; 条件は複数個指定することができ、OR条件で使用されます。 ただし &#x60;!tag.&lt;key&gt;&#x60; と組み合わせた場合、  &#x60;!tag.&lt;key&gt;&#x60; が優先されます。  例:      | measurement marker | tag (key: value) |     | ------------------ | ---------------- |     | 1                  | a: value1        |     |                    | c: value2        |     |                    | e: 1             |      | 2                  | a: b             |     |                    | c: d             |      | 3                  | a: b             |    -  &#x60;?tag.e&#x3D;&#x60; の場合、計測マーカー1番が取得されます。   -  &#x60;?!tag.c&#x3D;&#x60; の場合、計測マーカー3番が取得されます。   -  &#x60;?tag.a&#x3D;&amp;!tag.e&#x3D;&#x60; の場合、計測マーカー2、3番が取得されます。   -  &#x60;?tag.a&#x3D;val&amp;tag.c&#x3D;d&#x60; の場合、計測マーカー1、2番が取得されます。 | (optional) defaults to undefined|
| **tagKey2** | **Array&lt;string&gt;** | タグのキーを使って条件を指定し、条件に一致する計測キャプチャを除外します。 タグの値は無視されます。 &#x60;!tag.&lt;key&gt;&#x60; を複数個指定した場合、AND条件となります。 また、 &#x60;tag.&lt;key&gt;&#x3D;&lt;value&gt;&#x60; と組み合わせて使用した場合、 &#x60;tag.&lt;key&gt;&#x3D;&lt;value&gt;&#x60;  よりも &#x60;!tag.&lt;key&gt;&#x60; が優先されます。 例: 上の &#x60;tag.&lt;key&gt;&#x60; の説明を参照してください。 | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|
| **sort** | [**&#39;name&#39; | &#39;base_time&#39; | &#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;name&#39; &#124; &#39;base_time&#39; &#124; &#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'base_time'|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|


### Return type

**MeasurementMarkers**

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

# **listProjectMeasurementMarkers**
> MeasurementMarkers listProjectMeasurementMarkers()

計測マーカーのリストを取得します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let uuid: Array<string>; //計測マーカーのUUID (optional) (default to undefined)
let name: Array<string>; //計測マーカーの名前 (optional) (default to undefined)
let startUnixMicro: number; //取得対象区間の始点（マイクロ秒単位のUNIX時刻）（始点は対象区間に含まれます）。 範囲マーカーについては、マーカーの始点が取得対象区間に入っている場合に取得されます。 (optional) (default to undefined)
let endUnixMicro: number; //取得対象区間の終点（マイクロ秒単位のUNIX時刻）（終点は対象区間に含まれません）。 範囲マーカーについては、マーカーの始点が取得対象区間に入っている場合に取得されます。 (optional) (default to undefined)
let tagKey: Array<string>; //タグのキーと値を使って条件を指定し、条件に一致する計測マーカーを取得します。 キーのみを指定した場合は、指定されたキーを持つ計測マーカーを取得します。 キーと値を指定した場合は、指定されたキーを持ち、その値として指定された値を含む計測マーカーを取得します。 `tag.<key>=<value>` 条件は複数個指定することができ、OR条件で使用されます。 ただし `!tag.<key>` と組み合わせた場合、  `!tag.<key>` が優先されます。  例:      | measurement marker | tag (key: value) |     | ------------------ | ---------------- |     | 1                  | a: value1        |     |                    | c: value2        |     |                    | e: 1             |      | 2                  | a: b             |     |                    | c: d             |      | 3                  | a: b             |    -  `?tag.e=` の場合、計測マーカー1番が取得されます。   -  `?!tag.c=` の場合、計測マーカー3番が取得されます。   -  `?tag.a=&!tag.e=` の場合、計測マーカー2、3番が取得されます。   -  `?tag.a=val&tag.c=d` の場合、計測マーカー1、2番が取得されます。 (optional) (default to undefined)
let tagKey2: Array<string>; //タグのキーを使って条件を指定し、条件に一致する計測キャプチャを除外します。 タグの値は無視されます。 `!tag.<key>` を複数個指定した場合、AND条件となります。 また、 `tag.<key>=<value>` と組み合わせて使用した場合、 `tag.<key>=<value>`  よりも `!tag.<key>` が優先されます。 例: 上の `tag.<key>` の説明を参照してください。 (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)
let sort: 'name' | 'base_time' | 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'base_time')
let page: number; //取得するページの番号 (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)

const { status, data } = await apiInstance.listProjectMeasurementMarkers(
    projectUuid,
    uuid,
    name,
    startUnixMicro,
    endUnixMicro,
    tagKey,
    tagKey2,
    limit,
    sort,
    page,
    order
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **uuid** | **Array&lt;string&gt;** | 計測マーカーのUUID | (optional) defaults to undefined|
| **name** | **Array&lt;string&gt;** | 計測マーカーの名前 | (optional) defaults to undefined|
| **startUnixMicro** | [**number**] | 取得対象区間の始点（マイクロ秒単位のUNIX時刻）（始点は対象区間に含まれます）。 範囲マーカーについては、マーカーの始点が取得対象区間に入っている場合に取得されます。 | (optional) defaults to undefined|
| **endUnixMicro** | [**number**] | 取得対象区間の終点（マイクロ秒単位のUNIX時刻）（終点は対象区間に含まれません）。 範囲マーカーについては、マーカーの始点が取得対象区間に入っている場合に取得されます。 | (optional) defaults to undefined|
| **tagKey** | **Array&lt;string&gt;** | タグのキーと値を使って条件を指定し、条件に一致する計測マーカーを取得します。 キーのみを指定した場合は、指定されたキーを持つ計測マーカーを取得します。 キーと値を指定した場合は、指定されたキーを持ち、その値として指定された値を含む計測マーカーを取得します。 &#x60;tag.&lt;key&gt;&#x3D;&lt;value&gt;&#x60; 条件は複数個指定することができ、OR条件で使用されます。 ただし &#x60;!tag.&lt;key&gt;&#x60; と組み合わせた場合、  &#x60;!tag.&lt;key&gt;&#x60; が優先されます。  例:      | measurement marker | tag (key: value) |     | ------------------ | ---------------- |     | 1                  | a: value1        |     |                    | c: value2        |     |                    | e: 1             |      | 2                  | a: b             |     |                    | c: d             |      | 3                  | a: b             |    -  &#x60;?tag.e&#x3D;&#x60; の場合、計測マーカー1番が取得されます。   -  &#x60;?!tag.c&#x3D;&#x60; の場合、計測マーカー3番が取得されます。   -  &#x60;?tag.a&#x3D;&amp;!tag.e&#x3D;&#x60; の場合、計測マーカー2、3番が取得されます。   -  &#x60;?tag.a&#x3D;val&amp;tag.c&#x3D;d&#x60; の場合、計測マーカー1、2番が取得されます。 | (optional) defaults to undefined|
| **tagKey2** | **Array&lt;string&gt;** | タグのキーを使って条件を指定し、条件に一致する計測キャプチャを除外します。 タグの値は無視されます。 &#x60;!tag.&lt;key&gt;&#x60; を複数個指定した場合、AND条件となります。 また、 &#x60;tag.&lt;key&gt;&#x3D;&lt;value&gt;&#x60; と組み合わせて使用した場合、 &#x60;tag.&lt;key&gt;&#x3D;&lt;value&gt;&#x60;  よりも &#x60;!tag.&lt;key&gt;&#x60; が優先されます。 例: 上の &#x60;tag.&lt;key&gt;&#x60; の説明を参照してください。 | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|
| **sort** | [**&#39;name&#39; | &#39;base_time&#39; | &#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;name&#39; &#124; &#39;base_time&#39; &#124; &#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'base_time'|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|


### Return type

**MeasurementMarkers**

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

# **updateMeasurementMarker**
> MeasurementMarker updateMeasurementMarker()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/markers/{measurement_marker_uuid}` を使用してください） 計測マーカーを更新します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration,
    MeasurementMarkerPutRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)
let measurementMarkerPutRequest: MeasurementMarkerPutRequest; // (optional)

const { status, data } = await apiInstance.updateMeasurementMarker(
    measurementMarkerUuid,
    measurementMarkerPutRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementMarkerPutRequest** | **MeasurementMarkerPutRequest**|  | |
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


### Return type

**MeasurementMarker**

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

# **updateMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**
> MeasurementMarker updateMeasurementMarkerWithMeasurementUUIDAndMarkerUUID()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/markers/{Measurement_marker_uuid}` を使用してください） 計測マーカーの情報を更新します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration,
    MeasurementMarkerPutRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)
let measurementMarkerPutRequest: MeasurementMarkerPutRequest; // (optional)

const { status, data } = await apiInstance.updateMeasurementMarkerWithMeasurementUUIDAndMarkerUUID(
    measurementUuid,
    measurementMarkerUuid,
    measurementMarkerPutRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementMarkerPutRequest** | **MeasurementMarkerPutRequest**|  | |
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


### Return type

**MeasurementMarker**

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

# **updateProjectMeasurementMarker**
> MeasurementMarker updateProjectMeasurementMarker()

計測マーカーを更新します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration,
    MeasurementMarkerPutRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)
let measurementMarkerPutRequest: MeasurementMarkerPutRequest; // (optional)

const { status, data } = await apiInstance.updateProjectMeasurementMarker(
    projectUuid,
    measurementMarkerUuid,
    measurementMarkerPutRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementMarkerPutRequest** | **MeasurementMarkerPutRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


### Return type

**MeasurementMarker**

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

# **updateProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID**
> MeasurementMarker updateProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID()

計測マーカーの情報を更新します。

### Example

```typescript
import {
    MeasMeasurementMarkersApi,
    Configuration,
    MeasurementMarkerPutRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementMarkersApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)
let measurementMarkerPutRequest: MeasurementMarkerPutRequest; // (optional)

const { status, data } = await apiInstance.updateProjectMeasurementMarkerWithMeasurementUUIDAndMarkerUUID(
    projectUuid,
    measurementUuid,
    measurementMarkerUuid,
    measurementMarkerPutRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementMarkerPutRequest** | **MeasurementMarkerPutRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


### Return type

**MeasurementMarker**

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

