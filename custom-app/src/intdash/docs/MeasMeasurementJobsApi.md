# MeasMeasurementJobsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**cancelMeasurementJob**](#cancelmeasurementjob) | **PUT** /v1/measurements/jobs/{job_uuid}/cancel | Cancel Measurement Job|
|[**cancelProjectMeasurementJob**](#cancelprojectmeasurementjob) | **PUT** /v1/projects/{project_uuid}/measurements/jobs/{job_uuid}/cancel | Cancel Project Measurement Job|
|[**deleteMeasurementJob**](#deletemeasurementjob) | **DELETE** /v1/measurements/jobs/{job_uuid} | Delete Measurement Job|
|[**deleteProjectMeasurementJob**](#deleteprojectmeasurementjob) | **DELETE** /v1/projects/{project_uuid}/measurements/jobs/{job_uuid} | Delete Project Measurement Job|
|[**getMeasurementJob**](#getmeasurementjob) | **GET** /v1/measurements/jobs/{job_uuid} | Get Measurement Job|
|[**getProjectMeasurementJob**](#getprojectmeasurementjob) | **GET** /v1/projects/{project_uuid}/measurements/jobs/{job_uuid} | Get Project Measurement Job|
|[**listMeasurementJobs**](#listmeasurementjobs) | **GET** /v1/measurements/jobs | List Measurement Jobs|
|[**listProjectMeasurementJobs**](#listprojectmeasurementjobs) | **GET** /v1/projects/{project_uuid}/measurements/jobs | List Project Measurement Jobs|

# **cancelMeasurementJob**
> cancelMeasurementJob()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/jobs/{job_uuid}/cancel` を使用してください） ジョブをキャンセルします。

### Example

```typescript
import {
    MeasMeasurementJobsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementJobsApi(configuration);

let jobUuid: string; //ジョブのUUID (default to undefined)

const { status, data } = await apiInstance.cancelMeasurementJob(
    jobUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **jobUuid** | [**string**] | ジョブのUUID | defaults to undefined|


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

# **cancelProjectMeasurementJob**
> cancelProjectMeasurementJob()

ジョブをキャンセルします。

### Example

```typescript
import {
    MeasMeasurementJobsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementJobsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let jobUuid: string; //ジョブのUUID (default to undefined)

const { status, data } = await apiInstance.cancelProjectMeasurementJob(
    projectUuid,
    jobUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **jobUuid** | [**string**] | ジョブのUUID | defaults to undefined|


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

# **deleteMeasurementJob**
> deleteMeasurementJob()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/jobs/{job_uuid}` を使用してください） ジョブを削除します。

### Example

```typescript
import {
    MeasMeasurementJobsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementJobsApi(configuration);

let jobUuid: string; //ジョブのUUID (default to undefined)

const { status, data } = await apiInstance.deleteMeasurementJob(
    jobUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **jobUuid** | [**string**] | ジョブのUUID | defaults to undefined|


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

# **deleteProjectMeasurementJob**
> deleteProjectMeasurementJob()

ジョブを削除します。

### Example

```typescript
import {
    MeasMeasurementJobsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementJobsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let jobUuid: string; //ジョブのUUID (default to undefined)

const { status, data } = await apiInstance.deleteProjectMeasurementJob(
    projectUuid,
    jobUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **jobUuid** | [**string**] | ジョブのUUID | defaults to undefined|


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

# **getMeasurementJob**
> MeasurementJob getMeasurementJob()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/jobs/{job_uuid}` を使用してください） ジョブを取得します。

### Example

```typescript
import {
    MeasMeasurementJobsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementJobsApi(configuration);

let jobUuid: string; //ジョブのUUID (default to undefined)

const { status, data } = await apiInstance.getMeasurementJob(
    jobUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **jobUuid** | [**string**] | ジョブのUUID | defaults to undefined|


### Return type

**MeasurementJob**

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

# **getProjectMeasurementJob**
> MeasurementJob getProjectMeasurementJob()

ジョブを取得します。

### Example

```typescript
import {
    MeasMeasurementJobsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementJobsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let jobUuid: string; //ジョブのUUID (default to undefined)

const { status, data } = await apiInstance.getProjectMeasurementJob(
    projectUuid,
    jobUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **jobUuid** | [**string**] | ジョブのUUID | defaults to undefined|


### Return type

**MeasurementJob**

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

# **listMeasurementJobs**
> MeasurementJobs listMeasurementJobs()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/jobs` を使用してください）  ジョブ（CSVファイルを計測に変換するジョブなど）のリストを取得します。

### Example

```typescript
import {
    MeasMeasurementJobsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementJobsApi(configuration);

let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)
let sort: 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'created_at')
let status: Array<'ready' | 'processing' | 'succeeded' | 'failed' | 'cancelled'>; //ジョブのステータス (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)

const { status, data } = await apiInstance.listMeasurementJobs(
    limit,
    sort,
    status,
    page,
    order
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|
| **sort** | [**&#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'created_at'|
| **status** | **Array<&#39;ready&#39; &#124; &#39;processing&#39; &#124; &#39;succeeded&#39; &#124; &#39;failed&#39; &#124; &#39;cancelled&#39;>** | ジョブのステータス | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|


### Return type

**MeasurementJobs**

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

# **listProjectMeasurementJobs**
> MeasurementJobs listProjectMeasurementJobs()

ジョブ（CSVファイルを計測に変換するジョブなど）のリストを取得します。

### Example

```typescript
import {
    MeasMeasurementJobsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementJobsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)
let sort: 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'created_at')
let status: Array<'ready' | 'processing' | 'succeeded' | 'failed' | 'cancelled'>; //ジョブのステータス (optional) (default to undefined)
let page: number; //取得するページの番号 (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)

const { status, data } = await apiInstance.listProjectMeasurementJobs(
    projectUuid,
    limit,
    sort,
    status,
    page,
    order
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|
| **sort** | [**&#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'created_at'|
| **status** | **Array<&#39;ready&#39; &#124; &#39;processing&#39; &#124; &#39;succeeded&#39; &#124; &#39;failed&#39; &#124; &#39;cancelled&#39;>** | ジョブのステータス | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|


### Return type

**MeasurementJobs**

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

