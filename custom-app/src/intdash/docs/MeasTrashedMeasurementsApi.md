# MeasTrashedMeasurementsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteProjectTrashedMeasurement**](#deleteprojecttrashedmeasurement) | **DELETE** /v1/projects/{project_uuid}/trashed_measurements/{measurement_uuid} | Delete Project Trashed Measurement and Delete Data Points Immediately|
|[**deleteTrashedMeasurement**](#deletetrashedmeasurement) | **DELETE** /v1/trashed_measurements/{measurement_uuid} | Delete Trashed Measurement and Delete Data Points Immediately|
|[**listProjectTrashedMeasurements**](#listprojecttrashedmeasurements) | **GET** /v1/projects/{project_uuid}/trashed_measurements | List Project Trashed Measurements|
|[**listTrashedMeasurements**](#listtrashedmeasurements) | **GET** /v1/trashed_measurements | List Trashed Measurements|
|[**restoreProjectTrashedMeasurement**](#restoreprojecttrashedmeasurement) | **DELETE** /v1/projects/{project_uuid}/trashed_measurements/{measurement_uuid}/restore | Restore Project Measurement|
|[**restoreTrashedMeasurement**](#restoretrashedmeasurement) | **DELETE** /v1/trashed_measurements/{measurement_uuid}/restore | Restore Measurement|

# **deleteProjectTrashedMeasurement**
> deleteProjectTrashedMeasurement()

ゴミ箱に入っている計測と、その計測に関連付けられているデータポイントを直ちに削除します。

### Example

```typescript
import {
    MeasTrashedMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasTrashedMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.deleteProjectTrashedMeasurement(
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

# **deleteTrashedMeasurement**
> deleteTrashedMeasurement()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/trashed_measurements/{measurement_uuid}` を使用してください） ゴミ箱に入っている計測と、その計測に関連付けられているデータポイントを直ちに削除します。

### Example

```typescript
import {
    MeasTrashedMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasTrashedMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.deleteTrashedMeasurement(
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

# **listProjectTrashedMeasurements**
> TrashedMeasurements listProjectTrashedMeasurements()

ゴミ箱に入っている計測のリストを取得します。

### Example

```typescript
import {
    MeasTrashedMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasTrashedMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let limit: number; //1回のリクエストで取得する件数。`0` を指定した場合は、デフォルト値の50件となります。 (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to undefined)

const { status, data } = await apiInstance.listProjectTrashedMeasurements(
    projectUuid,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数。&#x60;0&#x60; を指定した場合は、デフォルト値の50件となります。 | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|


### Return type

**TrashedMeasurements**

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

# **listTrashedMeasurements**
> TrashedMeasurements listTrashedMeasurements()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/trashed_measurements` を使用してください） ゴミ箱に入っている計測のリストを取得します。

### Example

```typescript
import {
    MeasTrashedMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasTrashedMeasurementsApi(configuration);

let limit: number; //1回のリクエストで取得する件数。`0` を指定した場合は、デフォルト値の50件となります。 (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to undefined)

const { status, data } = await apiInstance.listTrashedMeasurements(
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **limit** | [**number**] | 1回のリクエストで取得する件数。&#x60;0&#x60; を指定した場合は、デフォルト値の50件となります。 | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|


### Return type

**TrashedMeasurements**

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

# **restoreProjectTrashedMeasurement**
> restoreProjectTrashedMeasurement()

ゴミ箱に入っている計測を復元します。

### Example

```typescript
import {
    MeasTrashedMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasTrashedMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.restoreProjectTrashedMeasurement(
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

# **restoreTrashedMeasurement**
> restoreTrashedMeasurement()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/trashed_measurements/{measurement_uuid}/restore` を使用してください） ゴミ箱に入っている計測を復元します。

### Example

```typescript
import {
    MeasTrashedMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasTrashedMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.restoreTrashedMeasurement(
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

