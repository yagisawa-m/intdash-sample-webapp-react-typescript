# MeasMeasurementsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**completeMeasurement**](#completemeasurement) | **PUT** /v1/measurements/{measurement_uuid}/complete | Complete Measurement|
|[**completeProjectMeasurement**](#completeprojectmeasurement) | **PUT** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/complete | Complete Project Measurement|
|[**createMeasurement**](#createmeasurement) | **POST** /v1/measurements | Create Measurement|
|[**createMeasurementSequenceChunks**](#createmeasurementsequencechunks) | **POST** /v1/measurements/sequences/chunks | Create Measurement Sequence Chunk|
|[**createMeasurementWithUUID**](#createmeasurementwithuuid) | **POST** /v1/measurements/{measurement_uuid} | Create Measurement with UUID|
|[**createProjectMeasurement**](#createprojectmeasurement) | **POST** /v1/projects/{project_uuid}/measurements | Create Project Measurement|
|[**createProjectMeasurementBaseTime**](#createprojectmeasurementbasetime) | **POST** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/basetimes | Create Project Measurement Base Time|
|[**createProjectMeasurementSequenceChunks**](#createprojectmeasurementsequencechunks) | **POST** /v1/projects/{project_uuid}/measurements/sequences/chunks | Create Project Measurement Sequence Chunk|
|[**createProjectMeasurementWithUUID**](#createprojectmeasurementwithuuid) | **POST** /v1/projects/{project_uuid}/measurements/{measurement_uuid} | Create Project Measurement with UUID|
|[**deleteMeasurement**](#deletemeasurement) | **DELETE** /v1/measurements/{measurement_uuid} | Trash Measurement|
|[**deleteMeasurementBaseTime**](#deletemeasurementbasetime) | **DELETE** /v1/measurements/{measurement_uuid}/basetimes/{type} | Delete Measurement Base Time|
|[**deleteProjectMeasurement**](#deleteprojectmeasurement) | **DELETE** /v1/projects/{project_uuid}/measurements/{measurement_uuid} | Trash Project Measurement|
|[**deleteProjectMeasurementBaseTime**](#deleteprojectmeasurementbasetime) | **DELETE** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/basetimes/{type} | Delete Project Measurement Base Time|
|[**deleteProjectMeasurementBaseTimeByID**](#deleteprojectmeasurementbasetimebyid) | **DELETE** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/basetimes/{id} | Delete Project Measurement Base Time By ID|
|[**endMeasurement**](#endmeasurement) | **PUT** /v1/measurements/{measurement_uuid}/end | End Measurement|
|[**endProjectMeasurement**](#endprojectmeasurement) | **PUT** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/end | End Project Measurement|
|[**getMeasurement**](#getmeasurement) | **GET** /v1/measurements/{measurement_uuid} | Get Measurement|
|[**getMeasurementBaseTime**](#getmeasurementbasetime) | **GET** /v1/measurements/{measurement_uuid}/basetimes/{type} | Get Measurement Base Time|
|[**getMeasurementFromMeasurementMarker**](#getmeasurementfrommeasurementmarker) | **GET** /v1/measurements/markers/{measurement_marker_uuid}/measurement | Get Measurement from Marker|
|[**getMeasurementSections**](#getmeasurementsections) | **GET** /v1/measurements/{measurement_uuid}/sections | List Measurement Sections|
|[**getMeasurementSequence**](#getmeasurementsequence) | **GET** /v1/measurements/{measurement_uuid}/sequences/{sequences_uuid} | Get Measurement Sequence|
|[**getProjectMeasurement**](#getprojectmeasurement) | **GET** /v1/projects/{project_uuid}/measurements/{measurement_uuid} | Get Project Measurement|
|[**getProjectMeasurementBaseTime**](#getprojectmeasurementbasetime) | **GET** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/basetimes/{type} | Get Project Measurement Base Time|
|[**getProjectMeasurementBaseTimeByID**](#getprojectmeasurementbasetimebyid) | **GET** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/basetimes/{id} | Get Project Measurement Base Time By ID|
|[**getProjectMeasurementFromMeasurementMarker**](#getprojectmeasurementfrommeasurementmarker) | **GET** /v1/projects/{project_uuid}/measurements/markers/{measurement_marker_uuid}/measurement | Get Project Measurement from Marker|
|[**getProjectMeasurementSections**](#getprojectmeasurementsections) | **GET** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/sections | List Project Measurement Sections|
|[**getProjectMeasurementSequence**](#getprojectmeasurementsequence) | **GET** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/sequences/{sequences_uuid} | Get Project Measurement Sequence|
|[**listMeasurementBaseTimes**](#listmeasurementbasetimes) | **GET** /v1/measurements/{measurement_uuid}/basetimes | List Measurement Base Times|
|[**listMeasurementSequences**](#listmeasurementsequences) | **GET** /v1/measurements/{measurement_uuid}/sequences | List Measurement Sequences|
|[**listMeasurements**](#listmeasurements) | **GET** /v1/measurements | List Measurements|
|[**listProjectMeasurementBaseTimes**](#listprojectmeasurementbasetimes) | **GET** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/basetimes | List Project Measurement Base Times|
|[**listProjectMeasurementSequences**](#listprojectmeasurementsequences) | **GET** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/sequences | List Project Measurement Sequences|
|[**listProjectMeasurements**](#listprojectmeasurements) | **GET** /v1/projects/{project_uuid}/measurements | List Project Measurements|
|[**protectMeasurement**](#protectmeasurement) | **PUT** /v1/measurements/{measurement_uuid}/protected | Protect Measurement|
|[**protectProjectMeasurement**](#protectprojectmeasurement) | **PUT** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/protected | Protect Project Measurement|
|[**replaceMeasurementSequence**](#replacemeasurementsequence) | **PUT** /v1/measurements/{measurement_uuid}/sequences/{sequences_uuid} | Replace Measurement Sequence|
|[**replaceProjectMeasurementSequence**](#replaceprojectmeasurementsequence) | **PUT** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/sequences/{sequences_uuid} | Replace Project Measurement Sequence|
|[**unprotectMeasurement**](#unprotectmeasurement) | **DELETE** /v1/measurements/{measurement_uuid}/protected | Unprotect Measurement|
|[**unprotectProjectMeasurement**](#unprotectprojectmeasurement) | **DELETE** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/protected | Unprotect Project Measurement|
|[**updateMeasurement**](#updatemeasurement) | **PUT** /v1/measurements/{measurement_uuid} | Update Measurement|
|[**updateMeasurementBaseTime**](#updatemeasurementbasetime) | **PUT** /v1/measurements/{measurement_uuid}/basetimes/{type} | Replace Measurement Base Time|
|[**updateMeasurementSequence**](#updatemeasurementsequence) | **PATCH** /v1/measurements/{measurement_uuid}/sequences/{sequences_uuid} | Update Measurement Sequence|
|[**updateProjectMeasurement**](#updateprojectmeasurement) | **PUT** /v1/projects/{project_uuid}/measurements/{measurement_uuid} | Update Project Measurement|
|[**updateProjectMeasurementBaseTime**](#updateprojectmeasurementbasetime) | **PUT** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/basetimes/{type} | Replace Project Measurement Base Time|
|[**updateProjectMeasurementBaseTimeByID**](#updateprojectmeasurementbasetimebyid) | **PATCH** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/basetimes/{id} | Update Project Measurement Base Time By ID|
|[**updateProjectMeasurementSequence**](#updateprojectmeasurementsequence) | **PATCH** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/sequences/{sequences_uuid} | Update Project Measurement Sequence|

# **completeMeasurement**
> Measurement completeMeasurement()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/complete` を使用してください）  計測を回収完了（completed）にします。  completedは、エッジでのデータ取得が終了し（ended）、  かつ、すべてのデータがサーバーに送信されたことを意味します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.completeMeasurement(
    measurementUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**Measurement**

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

# **completeProjectMeasurement**
> Measurement completeProjectMeasurement()

計測を回収完了（completed）にします。 completedは、エッジでのデータ取得が終了し（ended）、 かつ、すべてのデータがサーバーに送信されたことを意味します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.completeProjectMeasurement(
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

**Measurement**

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

# **createMeasurement**
> Measurement createMeasurement()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements` を使用してください）  計測を作成します。   - **Note**    - 計測の保護／非保護を切り替える権限を持たないエッジも、      計測作成時は保護された計測を作成することが可能です。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    MeasCreate
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measCreate: MeasCreate; // (optional)

const { status, data } = await apiInstance.createMeasurement(
    measCreate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measCreate** | **MeasCreate**|  | |


### Return type

**Measurement**

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

# **createMeasurementSequenceChunks**
> CreateMeasurementChunksResult createMeasurementSequenceChunks()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/sequence/chunks` を使用してください） 計測シーケンスにチャンクを作成します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let body: File; // (optional)

const { status, data } = await apiInstance.createMeasurementSequenceChunks(
    body
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **body** | **File**|  | |


### Return type

**CreateMeasurementChunksResult**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/vnd.iscp.v2.protobuf, application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createMeasurementWithUUID**
> Measurement createMeasurementWithUUID()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}` を使用してください） 指定したUUIDの計測を作成します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    MeasCreate
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let measCreate: MeasCreate; // (optional)

const { status, data } = await apiInstance.createMeasurementWithUUID(
    measurementUuid,
    measCreate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measCreate** | **MeasCreate**|  | |
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**Measurement**

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

# **createProjectMeasurement**
> Measurement createProjectMeasurement()

計測を作成します。  - **Note**   - 計測の保護／非保護を切り替える権限を持たないエッジも、     計測作成時は保護された計測を作成することが可能です。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    MeasCreate
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measCreate: MeasCreate; // (optional)

const { status, data } = await apiInstance.createProjectMeasurement(
    projectUuid,
    measCreate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measCreate** | **MeasCreate**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


### Return type

**Measurement**

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

# **createProjectMeasurementBaseTime**
> MeasBaseTime createProjectMeasurementBaseTime()

計測の基準時刻を作成します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    CreateMeasBaseTime
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let createMeasBaseTime: CreateMeasBaseTime; // (optional)

const { status, data } = await apiInstance.createProjectMeasurementBaseTime(
    projectUuid,
    measurementUuid,
    createMeasBaseTime
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createMeasBaseTime** | **CreateMeasBaseTime**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**MeasBaseTime**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createProjectMeasurementSequenceChunks**
> CreateMeasurementChunksResult createProjectMeasurementSequenceChunks()

計測シーケンスにチャンクを作成します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let body: File; // (optional)

const { status, data } = await apiInstance.createProjectMeasurementSequenceChunks(
    projectUuid,
    body
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **body** | **File**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


### Return type

**CreateMeasurementChunksResult**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/vnd.iscp.v2.protobuf, application/json
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createProjectMeasurementWithUUID**
> Measurement createProjectMeasurementWithUUID()

指定したUUIDの計測を作成します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    MeasCreate
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let measCreate: MeasCreate; // (optional)

const { status, data } = await apiInstance.createProjectMeasurementWithUUID(
    projectUuid,
    measurementUuid,
    measCreate
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measCreate** | **MeasCreate**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**Measurement**

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

# **deleteMeasurement**
> deleteMeasurement()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}` を使用してください）  計測を削除します。  - **Note**    - 保護された計測は削除できません。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.deleteMeasurement(
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

# **deleteMeasurementBaseTime**
> deleteMeasurementBaseTime()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/basetimes/{type}` を使用してください）  基準時刻を削除します。   指定された基準時刻が使用中の場合（その計測の `basetime_type` として設定されている場合）は、  その基準時刻は削除できません（ステータスコード `409` が返却されます）。   このような場合は、他の基準時刻をその計測の `basetime_type` にしてから、削除したい基準時刻を削除してください。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let type: 'edge_rtc' | 'ntp' | 'gps' | 'api_first_received' | 'volatile' | 'manual'; //基準時刻のタイプ (default to undefined)

const { status, data } = await apiInstance.deleteMeasurementBaseTime(
    measurementUuid,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **type** | [**&#39;edge_rtc&#39; | &#39;ntp&#39; | &#39;gps&#39; | &#39;api_first_received&#39; | &#39;volatile&#39; | &#39;manual&#39;**]**Array<&#39;edge_rtc&#39; &#124; &#39;ntp&#39; &#124; &#39;gps&#39; &#124; &#39;api_first_received&#39; &#124; &#39;volatile&#39; &#124; &#39;manual&#39;>** | 基準時刻のタイプ | defaults to undefined|


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

# **deleteProjectMeasurement**
> deleteProjectMeasurement()

計測を削除します。 - **Note**   - 保護された計測は削除できません。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.deleteProjectMeasurement(
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

# **deleteProjectMeasurementBaseTime**
> deleteProjectMeasurementBaseTime()

**非推奨** 代わりに「Delete Project Measurement Base Time By ID」を使用してください。 基準時刻を削除します。 指定された基準時刻が使用中の場合（その計測の `basetime_type` として設定されている場合）は、 その基準時刻は削除できません（ステータスコード `409` が返却されます）。 このような場合は、他の基準時刻をその計測の `basetime_type` にしてから、削除したい基準時刻を削除してください。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let type: 'edge_rtc' | 'ntp' | 'gps' | 'api_first_received' | 'volatile' | 'manual'; //基準時刻のタイプ (default to undefined)

const { status, data } = await apiInstance.deleteProjectMeasurementBaseTime(
    projectUuid,
    measurementUuid,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **type** | [**&#39;edge_rtc&#39; | &#39;ntp&#39; | &#39;gps&#39; | &#39;api_first_received&#39; | &#39;volatile&#39; | &#39;manual&#39;**]**Array<&#39;edge_rtc&#39; &#124; &#39;ntp&#39; &#124; &#39;gps&#39; &#124; &#39;api_first_received&#39; &#124; &#39;volatile&#39; &#124; &#39;manual&#39;>** | 基準時刻のタイプ | defaults to undefined|


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

# **deleteProjectMeasurementBaseTimeByID**
> deleteProjectMeasurementBaseTimeByID()

基準時刻を削除します。 指定された基準時刻が使用中の場合（その計測の `basetime_type` として設定されている場合）は、 その基準時刻は削除できません（ステータスコード `409` が返却されます）。 このような場合は、他の基準時刻をその計測の `basetime_type` にしてから、削除したい基準時刻を削除してください。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let id: number; //基準時刻のID (default to undefined)

const { status, data } = await apiInstance.deleteProjectMeasurementBaseTimeByID(
    projectUuid,
    measurementUuid,
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **id** | [**number**] | 基準時刻のID | defaults to undefined|


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

# **endMeasurement**
> SequenceSummary endMeasurement()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/end` を使用してください）  計測終了（ended）とします。endedは、エッジにおけるデータの取得が終了していることを表します。  （サーバーに回収されていないデータがまだエッジに残っている可能性はあります。サーバーへのデータの回収が完了した状態は、completedと呼びます。）

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.endMeasurement(
    measurementUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**SequenceSummary**

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

# **endProjectMeasurement**
> SequenceSummary endProjectMeasurement()

計測終了（ended）とします。endedは、エッジにおけるデータの取得が終了していることを表します。 （サーバーに回収されていないデータがまだエッジに残っている可能性はあります。サーバーへのデータの回収が完了した状態は、completedと呼びます。）

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.endProjectMeasurement(
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

**SequenceSummary**

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

# **getMeasurement**
> Measurement getMeasurement()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}` を使用してください） 計測を取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.getMeasurement(
    measurementUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**Measurement**

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

# **getMeasurementBaseTime**
> MeasBaseTime getMeasurementBaseTime()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/basetimes/{type}` を使用してください） 基準時刻タイプを指定して計測の基準時刻を取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let type: 'edge_rtc' | 'ntp' | 'gps' | 'api_first_received' | 'volatile' | 'manual'; //基準時刻のタイプ (default to undefined)

const { status, data } = await apiInstance.getMeasurementBaseTime(
    measurementUuid,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **type** | [**&#39;edge_rtc&#39; | &#39;ntp&#39; | &#39;gps&#39; | &#39;api_first_received&#39; | &#39;volatile&#39; | &#39;manual&#39;**]**Array<&#39;edge_rtc&#39; &#124; &#39;ntp&#39; &#124; &#39;gps&#39; &#124; &#39;api_first_received&#39; &#124; &#39;volatile&#39; &#124; &#39;manual&#39;>** | 基準時刻のタイプ | defaults to undefined|


### Return type

**MeasBaseTime**

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

# **getMeasurementFromMeasurementMarker**
> Measurement getMeasurementFromMeasurementMarker()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/markers/{measurement_marker_uuid}/measurement` を使用してください）

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)

const { status, data } = await apiInstance.getMeasurementFromMeasurementMarker(
    measurementMarkerUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementMarkerUuid** | [**string**] | 計測マーカーのUUID | defaults to undefined|


### Return type

**Measurement**

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

# **getMeasurementSections**
> MeasurementSectionsGetResponse getMeasurementSections()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/sections` を使用してください）  計測に含まれるセクションのリストを取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let filter: 'processed' | 'unprocessed' | 'both'; //計測セクションの処理ステータス。 `processed` （処理済みの計測セクションを取得）、 `unprocessed` （未処理の計測セクションを取得）、 `both` （両方を取得）のいずれかを選択します。 (optional) (default to 'both')
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)

const { status, data } = await apiInstance.getMeasurementSections(
    measurementUuid,
    filter,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **filter** | [**&#39;processed&#39; | &#39;unprocessed&#39; | &#39;both&#39;**]**Array<&#39;processed&#39; &#124; &#39;unprocessed&#39; &#124; &#39;both&#39;>** | 計測セクションの処理ステータス。 &#x60;processed&#x60; （処理済みの計測セクションを取得）、 &#x60;unprocessed&#x60; （未処理の計測セクションを取得）、 &#x60;both&#x60; （両方を取得）のいずれかを選択します。 | (optional) defaults to 'both'|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|


### Return type

**MeasurementSectionsGetResponse**

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

# **getMeasurementSequence**
> MeasurementSequenceGroup getMeasurementSequence()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/sequences/{sequence_uuid}` を使用してください） 計測シーケンスを取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let sequencesUuid: string; //計測シーケンスのUUID (default to undefined)

const { status, data } = await apiInstance.getMeasurementSequence(
    measurementUuid,
    sequencesUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **sequencesUuid** | [**string**] | 計測シーケンスのUUID | defaults to undefined|


### Return type

**MeasurementSequenceGroup**

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

# **getProjectMeasurement**
> Measurement getProjectMeasurement()

計測を取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.getProjectMeasurement(
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

**Measurement**

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

# **getProjectMeasurementBaseTime**
> MeasBaseTime getProjectMeasurementBaseTime()

**非推奨** 代わりに「Get Project Measurement Base Time By ID」を使用してください。 基準時刻タイプを指定して計測の基準時刻を取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let type: 'edge_rtc' | 'ntp' | 'gps' | 'api_first_received' | 'volatile' | 'manual'; //基準時刻のタイプ (default to undefined)

const { status, data } = await apiInstance.getProjectMeasurementBaseTime(
    projectUuid,
    measurementUuid,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **type** | [**&#39;edge_rtc&#39; | &#39;ntp&#39; | &#39;gps&#39; | &#39;api_first_received&#39; | &#39;volatile&#39; | &#39;manual&#39;**]**Array<&#39;edge_rtc&#39; &#124; &#39;ntp&#39; &#124; &#39;gps&#39; &#124; &#39;api_first_received&#39; &#124; &#39;volatile&#39; &#124; &#39;manual&#39;>** | 基準時刻のタイプ | defaults to undefined|


### Return type

**MeasBaseTime**

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

# **getProjectMeasurementBaseTimeByID**
> MeasBaseTime getProjectMeasurementBaseTimeByID()

基準時刻IDを指定して計測の基準時刻を取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let id: number; //基準時刻のID (default to undefined)

const { status, data } = await apiInstance.getProjectMeasurementBaseTimeByID(
    projectUuid,
    measurementUuid,
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **id** | [**number**] | 基準時刻のID | defaults to undefined|


### Return type

**MeasBaseTime**

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

# **getProjectMeasurementFromMeasurementMarker**
> Measurement getProjectMeasurementFromMeasurementMarker()


### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementMarkerUuid: string; //計測マーカーのUUID (default to undefined)

const { status, data } = await apiInstance.getProjectMeasurementFromMeasurementMarker(
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

**Measurement**

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

# **getProjectMeasurementSections**
> MeasurementSectionsGetResponse getProjectMeasurementSections()

計測に含まれるセクションのリストを取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let filter: 'processed' | 'unprocessed' | 'both'; //計測セクションの処理ステータス。 `processed` （処理済みの計測セクションを取得）、 `unprocessed` （未処理の計測セクションを取得）、 `both` （両方を取得）のいずれかを選択します。 (optional) (default to 'both')
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)

const { status, data } = await apiInstance.getProjectMeasurementSections(
    projectUuid,
    measurementUuid,
    filter,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **filter** | [**&#39;processed&#39; | &#39;unprocessed&#39; | &#39;both&#39;**]**Array<&#39;processed&#39; &#124; &#39;unprocessed&#39; &#124; &#39;both&#39;>** | 計測セクションの処理ステータス。 &#x60;processed&#x60; （処理済みの計測セクションを取得）、 &#x60;unprocessed&#x60; （未処理の計測セクションを取得）、 &#x60;both&#x60; （両方を取得）のいずれかを選択します。 | (optional) defaults to 'both'|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|


### Return type

**MeasurementSectionsGetResponse**

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

# **getProjectMeasurementSequence**
> MeasurementSequenceGroup getProjectMeasurementSequence()

計測シーケンスを取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let sequencesUuid: string; //計測シーケンスのUUID (default to undefined)

const { status, data } = await apiInstance.getProjectMeasurementSequence(
    projectUuid,
    measurementUuid,
    sequencesUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **sequencesUuid** | [**string**] | 計測シーケンスのUUID | defaults to undefined|


### Return type

**MeasurementSequenceGroup**

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

# **listMeasurementBaseTimes**
> MeasBaseTimes listMeasurementBaseTimes()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/basetimes` を使用してください）  計測の基準時刻のリストを取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.listMeasurementBaseTimes(
    measurementUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**MeasBaseTimes**

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

# **listMeasurementSequences**
> MeasurementSequenceGroups listMeasurementSequences()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/sequences` を使用してください） 計測シーケンスのリストを取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.listMeasurementSequences(
    measurementUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**MeasurementSequenceGroups**

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

# **listMeasurements**
> Measurements listMeasurements()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements` を使用してください）  計測のリストを取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let uuid: Array<string>; //計測のUUID (optional) (default to undefined)
let name: string; //名前が指定した文字列から始まる計測を取得します。 文字列をダブルクォーテーションで囲むと、完全一致のものだけが取得されます。 (optional) (default to undefined)
let edgeUuid: string; //計測に関連付けられたエッジのUUID (optional) (default to undefined)
let start: string; //計測を取得するための対象区間の始点（始点は対象区間に含まれます）。 計測の基準時刻が、ここで指定した時刻と同じかそれより後の場合、その計測は取得対象になります。 ただし、 `partial_match` を `true` にした場合については `partial_match` の説明を参照してください。  以下のいずれかの形式で指定します。   - RFC3339(例 `2019-10-29T03:04:05.341268Z` )   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let end: string; //計測を取得するための対象区間の終点（終点は対象区間に含まれません）。 計測の基準時刻が、ここで指定した時刻よりも前の場合、その計測は取得対象になります。 ただし、 `partial_match` を `true` にした場合については `partial_match` の説明を参照してください。  以下のいずれかの形式で指定します。   - RFC3339(例 `2019-10-29T03:04:05.341268Z` )   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let partialMatch: boolean; //`false` の場合、 `start` と `end` によって指定された取得対象区間に 基準時刻(`basetime`)が入っていると、その計測は取得対象になります。  `true` の場合、取得対象区間に計測の一部でも入っていると、その計測は取得対象となります。 計測の始点は基準時刻(`basetime`)、終点は基準時刻に長さを加えたもの(`basetime`+`max_elapsed_time`)です。  以下の図の例では、 `partial_match=false` のように指定すると、 `measurement2` と `measurement3` が取得されます。  `partial_match=true` のように指定すると、 `measurement1` 、 `measurement2` 、 `measurement3` が取得されます。  ```                    :                            :                    :                            :            | measurement1 |                     :            +--------------+                     :                    :           | measurement2 | :                    :           +--------------+ :                    :                       | measurement3 |                    :                       +--------------+     | measurement4 |                            :     +--------------+                            :                    :                            | measurement5 |                    :                            +--------------+                    :                            :                    :                            :            time -------------------+----------------------------+--------------->                    |                            |                   start                        end ```  `partial_match=true` の場合の計測の端点の扱いは以下のようになります。  - 「計測の終点(=`basetime`+`max_elapsed_time`) == 取得対象区間の`start`」の場合、   その計測は取得されません（上図の`measurement4`）。  - 「計測の始点(=`basetime`) == 取得対象区間の `end` 」の場合も、   その計測は取得されません（上図の`measurement5`）。 (optional) (default to false)
let basetimeType: 'edge_rtc' | 'ntp' | 'gps' | 'api_first_received' | 'volatile' | 'manual'; //計測の基準時刻のタイプ (optional) (default to undefined)
let ended: boolean; //計測が終了している（ended）かどうかを指定して計測を取得します。  エッジにおいてデータの取得が終了している場合、その計測は「終了(ended)」となります。 計測は終了(ended)していても、まだサーバーに送信されていないデータがエッジに残っている可能性があります。 * `true`: 終了した計測だけを取得します。 * `false`: 終了していない計測だけを取得します。 (optional) (default to undefined)
let since: string; //指定した時刻以降に更新された計測のみを取得します。  以下のいずれかの形式で指定します。    - RFC3339(例 `2019-10-29T03:04:05.341268Z` )   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let durationStart: number; //計測時間の最小値（マイクロ秒）。これより短い計測は取得しません。 (optional) (default to undefined)
let durationEnd: number; //計測時間の最大値（マイクロ秒）。これより長い計測は取得しません。 (optional) (default to undefined)
let status: Array<'measuring' | 'resending' | 'finished'>; //計測のステータス (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数。ただし、0を指定するとデフォルトの値が使用されます。 (optional) (default to 1000)
let sort: 'name' | 'description' | 'ended' | 'duration' | 'base_time' | 'processed_ratio' | 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'base_time')
let page: number; //取得するページの番号 (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)

const { status, data } = await apiInstance.listMeasurements(
    uuid,
    name,
    edgeUuid,
    start,
    end,
    partialMatch,
    basetimeType,
    ended,
    since,
    durationStart,
    durationEnd,
    status,
    limit,
    sort,
    page,
    order
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uuid** | **Array&lt;string&gt;** | 計測のUUID | (optional) defaults to undefined|
| **name** | [**string**] | 名前が指定した文字列から始まる計測を取得します。 文字列をダブルクォーテーションで囲むと、完全一致のものだけが取得されます。 | (optional) defaults to undefined|
| **edgeUuid** | [**string**] | 計測に関連付けられたエッジのUUID | (optional) defaults to undefined|
| **start** | [**string**] | 計測を取得するための対象区間の始点（始点は対象区間に含まれます）。 計測の基準時刻が、ここで指定した時刻と同じかそれより後の場合、その計測は取得対象になります。 ただし、 &#x60;partial_match&#x60; を &#x60;true&#x60; にした場合については &#x60;partial_match&#x60; の説明を参照してください。  以下のいずれかの形式で指定します。   - RFC3339(例 &#x60;2019-10-29T03:04:05.341268Z&#x60; )   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **end** | [**string**] | 計測を取得するための対象区間の終点（終点は対象区間に含まれません）。 計測の基準時刻が、ここで指定した時刻よりも前の場合、その計測は取得対象になります。 ただし、 &#x60;partial_match&#x60; を &#x60;true&#x60; にした場合については &#x60;partial_match&#x60; の説明を参照してください。  以下のいずれかの形式で指定します。   - RFC3339(例 &#x60;2019-10-29T03:04:05.341268Z&#x60; )   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **partialMatch** | [**boolean**] | &#x60;false&#x60; の場合、 &#x60;start&#x60; と &#x60;end&#x60; によって指定された取得対象区間に 基準時刻(&#x60;basetime&#x60;)が入っていると、その計測は取得対象になります。  &#x60;true&#x60; の場合、取得対象区間に計測の一部でも入っていると、その計測は取得対象となります。 計測の始点は基準時刻(&#x60;basetime&#x60;)、終点は基準時刻に長さを加えたもの(&#x60;basetime&#x60;+&#x60;max_elapsed_time&#x60;)です。  以下の図の例では、 &#x60;partial_match&#x3D;false&#x60; のように指定すると、 &#x60;measurement2&#x60; と &#x60;measurement3&#x60; が取得されます。  &#x60;partial_match&#x3D;true&#x60; のように指定すると、 &#x60;measurement1&#x60; 、 &#x60;measurement2&#x60; 、 &#x60;measurement3&#x60; が取得されます。  &#x60;&#x60;&#x60;                    :                            :                    :                            :            | measurement1 |                     :            +--------------+                     :                    :           | measurement2 | :                    :           +--------------+ :                    :                       | measurement3 |                    :                       +--------------+     | measurement4 |                            :     +--------------+                            :                    :                            | measurement5 |                    :                            +--------------+                    :                            :                    :                            :            time -------------------+----------------------------+---------------&gt;                    |                            |                   start                        end &#x60;&#x60;&#x60;  &#x60;partial_match&#x3D;true&#x60; の場合の計測の端点の扱いは以下のようになります。  - 「計測の終点(&#x3D;&#x60;basetime&#x60;+&#x60;max_elapsed_time&#x60;) &#x3D;&#x3D; 取得対象区間の&#x60;start&#x60;」の場合、   その計測は取得されません（上図の&#x60;measurement4&#x60;）。  - 「計測の始点(&#x3D;&#x60;basetime&#x60;) &#x3D;&#x3D; 取得対象区間の &#x60;end&#x60; 」の場合も、   その計測は取得されません（上図の&#x60;measurement5&#x60;）。 | (optional) defaults to false|
| **basetimeType** | [**&#39;edge_rtc&#39; | &#39;ntp&#39; | &#39;gps&#39; | &#39;api_first_received&#39; | &#39;volatile&#39; | &#39;manual&#39;**]**Array<&#39;edge_rtc&#39; &#124; &#39;ntp&#39; &#124; &#39;gps&#39; &#124; &#39;api_first_received&#39; &#124; &#39;volatile&#39; &#124; &#39;manual&#39;>** | 計測の基準時刻のタイプ | (optional) defaults to undefined|
| **ended** | [**boolean**] | 計測が終了している（ended）かどうかを指定して計測を取得します。  エッジにおいてデータの取得が終了している場合、その計測は「終了(ended)」となります。 計測は終了(ended)していても、まだサーバーに送信されていないデータがエッジに残っている可能性があります。 * &#x60;true&#x60;: 終了した計測だけを取得します。 * &#x60;false&#x60;: 終了していない計測だけを取得します。 | (optional) defaults to undefined|
| **since** | [**string**] | 指定した時刻以降に更新された計測のみを取得します。  以下のいずれかの形式で指定します。    - RFC3339(例 &#x60;2019-10-29T03:04:05.341268Z&#x60; )   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **durationStart** | [**number**] | 計測時間の最小値（マイクロ秒）。これより短い計測は取得しません。 | (optional) defaults to undefined|
| **durationEnd** | [**number**] | 計測時間の最大値（マイクロ秒）。これより長い計測は取得しません。 | (optional) defaults to undefined|
| **status** | **Array<&#39;measuring&#39; &#124; &#39;resending&#39; &#124; &#39;finished&#39;>** | 計測のステータス | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数。ただし、0を指定するとデフォルトの値が使用されます。 | (optional) defaults to 1000|
| **sort** | [**&#39;name&#39; | &#39;description&#39; | &#39;ended&#39; | &#39;duration&#39; | &#39;base_time&#39; | &#39;processed_ratio&#39; | &#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;name&#39; &#124; &#39;description&#39; &#124; &#39;ended&#39; &#124; &#39;duration&#39; &#124; &#39;base_time&#39; &#124; &#39;processed_ratio&#39; &#124; &#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'base_time'|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|


### Return type

**Measurements**

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

# **listProjectMeasurementBaseTimes**
> MeasBaseTimes listProjectMeasurementBaseTimes()

計測の基準時刻のリストを取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.listProjectMeasurementBaseTimes(
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

**MeasBaseTimes**

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

# **listProjectMeasurementSequences**
> MeasurementSequenceGroups listProjectMeasurementSequences()

計測シーケンスのリストを取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.listProjectMeasurementSequences(
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

**MeasurementSequenceGroups**

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

# **listProjectMeasurements**
> Measurements listProjectMeasurements()

計測のリストを取得します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let uuid: Array<string>; //計測のUUID (optional) (default to undefined)
let name: string; //名前が指定した文字列から始まる計測を取得します。 文字列をダブルクォーテーションで囲むと、完全一致のものだけが取得されます。 (optional) (default to undefined)
let edgeUuid: string; //計測に関連付けられたエッジのUUID (optional) (default to undefined)
let start: string; //計測を取得するための対象区間の始点（始点は対象区間に含まれます）。 計測の基準時刻が、ここで指定した時刻と同じかそれより後の場合、その計測は取得対象になります。 ただし、 `partial_match` を `true` にした場合については `partial_match` の説明を参照してください。  以下のいずれかの形式で指定します。   - RFC3339(例 `2019-10-29T03:04:05.341268Z` )   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let end: string; //計測を取得するための対象区間の終点（終点は対象区間に含まれません）。 計測の基準時刻が、ここで指定した時刻よりも前の場合、その計測は取得対象になります。 ただし、 `partial_match` を `true` にした場合については `partial_match` の説明を参照してください。  以下のいずれかの形式で指定します。   - RFC3339(例 `2019-10-29T03:04:05.341268Z` )   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let partialMatch: boolean; //`false` の場合、 `start` と `end` によって指定された取得対象区間に 基準時刻(`basetime`)が入っていると、その計測は取得対象になります。  `true` の場合、取得対象区間に計測の一部でも入っていると、その計測は取得対象となります。 計測の始点は基準時刻(`basetime`)、終点は基準時刻に長さを加えたもの(`basetime`+`max_elapsed_time`)です。  以下の図の例では、 `partial_match=false` のように指定すると、 `measurement2` と `measurement3` が取得されます。  `partial_match=true` のように指定すると、 `measurement1` 、 `measurement2` 、 `measurement3` が取得されます。  ```                    :                            :                    :                            :            | measurement1 |                     :            +--------------+                     :                    :           | measurement2 | :                    :           +--------------+ :                    :                       | measurement3 |                    :                       +--------------+     | measurement4 |                            :     +--------------+                            :                    :                            | measurement5 |                    :                            +--------------+                    :                            :                    :                            :            time -------------------+----------------------------+--------------->                    |                            |                   start                        end ```  `partial_match=true` の場合の計測の端点の扱いは以下のようになります。  - 「計測の終点(=`basetime`+`max_elapsed_time`) == 取得対象区間の`start`」の場合、   その計測は取得されません（上図の`measurement4`）。  - 「計測の始点(=`basetime`) == 取得対象区間の `end` 」の場合も、   その計測は取得されません（上図の`measurement5`）。 (optional) (default to false)
let basetimeType: 'edge_rtc' | 'ntp' | 'gps' | 'api_first_received' | 'volatile' | 'manual'; //計測の基準時刻のタイプ (optional) (default to undefined)
let ended: boolean; //計測が終了している（ended）かどうかを指定して計測を取得します。  エッジにおいてデータの取得が終了している場合、その計測は「終了(ended)」となります。 計測は終了(ended)していても、まだサーバーに送信されていないデータがエッジに残っている可能性があります。 * `true`: 終了した計測だけを取得します。 * `false`: 終了していない計測だけを取得します。 (optional) (default to undefined)
let since: string; //指定した時刻以降に更新された計測のみを取得します。  以下のいずれかの形式で指定します。    - RFC3339(例 `2019-10-29T03:04:05.341268Z` )   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let durationStart: number; //計測時間の最小値（マイクロ秒）。これより短い計測は取得しません。 (optional) (default to undefined)
let durationEnd: number; //計測時間の最大値（マイクロ秒）。これより長い計測は取得しません。 (optional) (default to undefined)
let status: Array<'measuring' | 'resending' | 'finished'>; //計測のステータス (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数。ただし、0を指定するとデフォルトの値が使用されます。 (optional) (default to 1000)
let sort: 'name' | 'description' | 'ended' | 'duration' | 'base_time' | 'processed_ratio' | 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'base_time')
let page: number; //取得するページの番号 (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)

const { status, data } = await apiInstance.listProjectMeasurements(
    projectUuid,
    uuid,
    name,
    edgeUuid,
    start,
    end,
    partialMatch,
    basetimeType,
    ended,
    since,
    durationStart,
    durationEnd,
    status,
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
| **uuid** | **Array&lt;string&gt;** | 計測のUUID | (optional) defaults to undefined|
| **name** | [**string**] | 名前が指定した文字列から始まる計測を取得します。 文字列をダブルクォーテーションで囲むと、完全一致のものだけが取得されます。 | (optional) defaults to undefined|
| **edgeUuid** | [**string**] | 計測に関連付けられたエッジのUUID | (optional) defaults to undefined|
| **start** | [**string**] | 計測を取得するための対象区間の始点（始点は対象区間に含まれます）。 計測の基準時刻が、ここで指定した時刻と同じかそれより後の場合、その計測は取得対象になります。 ただし、 &#x60;partial_match&#x60; を &#x60;true&#x60; にした場合については &#x60;partial_match&#x60; の説明を参照してください。  以下のいずれかの形式で指定します。   - RFC3339(例 &#x60;2019-10-29T03:04:05.341268Z&#x60; )   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **end** | [**string**] | 計測を取得するための対象区間の終点（終点は対象区間に含まれません）。 計測の基準時刻が、ここで指定した時刻よりも前の場合、その計測は取得対象になります。 ただし、 &#x60;partial_match&#x60; を &#x60;true&#x60; にした場合については &#x60;partial_match&#x60; の説明を参照してください。  以下のいずれかの形式で指定します。   - RFC3339(例 &#x60;2019-10-29T03:04:05.341268Z&#x60; )   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **partialMatch** | [**boolean**] | &#x60;false&#x60; の場合、 &#x60;start&#x60; と &#x60;end&#x60; によって指定された取得対象区間に 基準時刻(&#x60;basetime&#x60;)が入っていると、その計測は取得対象になります。  &#x60;true&#x60; の場合、取得対象区間に計測の一部でも入っていると、その計測は取得対象となります。 計測の始点は基準時刻(&#x60;basetime&#x60;)、終点は基準時刻に長さを加えたもの(&#x60;basetime&#x60;+&#x60;max_elapsed_time&#x60;)です。  以下の図の例では、 &#x60;partial_match&#x3D;false&#x60; のように指定すると、 &#x60;measurement2&#x60; と &#x60;measurement3&#x60; が取得されます。  &#x60;partial_match&#x3D;true&#x60; のように指定すると、 &#x60;measurement1&#x60; 、 &#x60;measurement2&#x60; 、 &#x60;measurement3&#x60; が取得されます。  &#x60;&#x60;&#x60;                    :                            :                    :                            :            | measurement1 |                     :            +--------------+                     :                    :           | measurement2 | :                    :           +--------------+ :                    :                       | measurement3 |                    :                       +--------------+     | measurement4 |                            :     +--------------+                            :                    :                            | measurement5 |                    :                            +--------------+                    :                            :                    :                            :            time -------------------+----------------------------+---------------&gt;                    |                            |                   start                        end &#x60;&#x60;&#x60;  &#x60;partial_match&#x3D;true&#x60; の場合の計測の端点の扱いは以下のようになります。  - 「計測の終点(&#x3D;&#x60;basetime&#x60;+&#x60;max_elapsed_time&#x60;) &#x3D;&#x3D; 取得対象区間の&#x60;start&#x60;」の場合、   その計測は取得されません（上図の&#x60;measurement4&#x60;）。  - 「計測の始点(&#x3D;&#x60;basetime&#x60;) &#x3D;&#x3D; 取得対象区間の &#x60;end&#x60; 」の場合も、   その計測は取得されません（上図の&#x60;measurement5&#x60;）。 | (optional) defaults to false|
| **basetimeType** | [**&#39;edge_rtc&#39; | &#39;ntp&#39; | &#39;gps&#39; | &#39;api_first_received&#39; | &#39;volatile&#39; | &#39;manual&#39;**]**Array<&#39;edge_rtc&#39; &#124; &#39;ntp&#39; &#124; &#39;gps&#39; &#124; &#39;api_first_received&#39; &#124; &#39;volatile&#39; &#124; &#39;manual&#39;>** | 計測の基準時刻のタイプ | (optional) defaults to undefined|
| **ended** | [**boolean**] | 計測が終了している（ended）かどうかを指定して計測を取得します。  エッジにおいてデータの取得が終了している場合、その計測は「終了(ended)」となります。 計測は終了(ended)していても、まだサーバーに送信されていないデータがエッジに残っている可能性があります。 * &#x60;true&#x60;: 終了した計測だけを取得します。 * &#x60;false&#x60;: 終了していない計測だけを取得します。 | (optional) defaults to undefined|
| **since** | [**string**] | 指定した時刻以降に更新された計測のみを取得します。  以下のいずれかの形式で指定します。    - RFC3339(例 &#x60;2019-10-29T03:04:05.341268Z&#x60; )   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **durationStart** | [**number**] | 計測時間の最小値（マイクロ秒）。これより短い計測は取得しません。 | (optional) defaults to undefined|
| **durationEnd** | [**number**] | 計測時間の最大値（マイクロ秒）。これより長い計測は取得しません。 | (optional) defaults to undefined|
| **status** | **Array<&#39;measuring&#39; &#124; &#39;resending&#39; &#124; &#39;finished&#39;>** | 計測のステータス | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数。ただし、0を指定するとデフォルトの値が使用されます。 | (optional) defaults to 1000|
| **sort** | [**&#39;name&#39; | &#39;description&#39; | &#39;ended&#39; | &#39;duration&#39; | &#39;base_time&#39; | &#39;processed_ratio&#39; | &#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;name&#39; &#124; &#39;description&#39; &#124; &#39;ended&#39; &#124; &#39;duration&#39; &#124; &#39;base_time&#39; &#124; &#39;processed_ratio&#39; &#124; &#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'base_time'|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|


### Return type

**Measurements**

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

# **protectMeasurement**
> protectMeasurement()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/protected` を使用してください） 計測を保護します。保護された計測は削除できません。 [See](#section/Protected-resources) も参照してください。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.protectMeasurement(
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

# **protectProjectMeasurement**
> protectProjectMeasurement()

計測を保護します。保護された計測は削除できません。 [See](#section/Protected-resources) も参照してください。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.protectProjectMeasurement(
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

# **replaceMeasurementSequence**
> MeasurementSequenceGroup replaceMeasurementSequence()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/sequences/{sequence_uuid}` を使用してください） 計測シーケンスを置換します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    MeasurementSequenceGroupReplace
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let sequencesUuid: string; //計測シーケンスのUUID (default to undefined)
let measurementSequenceGroupReplace: MeasurementSequenceGroupReplace; // (optional)

const { status, data } = await apiInstance.replaceMeasurementSequence(
    measurementUuid,
    sequencesUuid,
    measurementSequenceGroupReplace
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementSequenceGroupReplace** | **MeasurementSequenceGroupReplace**|  | |
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **sequencesUuid** | [**string**] | 計測シーケンスのUUID | defaults to undefined|


### Return type

**MeasurementSequenceGroup**

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

# **replaceProjectMeasurementSequence**
> MeasurementSequenceGroup replaceProjectMeasurementSequence()

計測シーケンスを置換します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    MeasurementSequenceGroupReplace
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let sequencesUuid: string; //計測シーケンスのUUID (default to undefined)
let measurementSequenceGroupReplace: MeasurementSequenceGroupReplace; // (optional)

const { status, data } = await apiInstance.replaceProjectMeasurementSequence(
    projectUuid,
    measurementUuid,
    sequencesUuid,
    measurementSequenceGroupReplace
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementSequenceGroupReplace** | **MeasurementSequenceGroupReplace**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **sequencesUuid** | [**string**] | 計測シーケンスのUUID | defaults to undefined|


### Return type

**MeasurementSequenceGroup**

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

# **unprotectMeasurement**
> unprotectMeasurement()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/protected` を使用してください） 計測の保護を解除します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.unprotectMeasurement(
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

# **unprotectProjectMeasurement**
> unprotectProjectMeasurement()

計測の保護を解除します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.unprotectProjectMeasurement(
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

# **updateMeasurement**
> updateMeasurement()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}` を使用してください） 計測に関する情報を更新します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    ReplaceMeas
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let replaceMeas: ReplaceMeas; // (optional)

const { status, data } = await apiInstance.updateMeasurement(
    measurementUuid,
    replaceMeas
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **replaceMeas** | **ReplaceMeas**|  | |
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


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

# **updateMeasurementBaseTime**
> MeasBaseTime updateMeasurementBaseTime()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/basetimes/{type}` を使用してください）  基準時刻を更新します。  この計測において、使用する基準時刻が設定されていない（ `basetime_type` が `undefined` ）の場合は、  新しい基準時刻を `basetime_type` に設定します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    UpdateMeasBaseTime
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let type: 'edge_rtc' | 'ntp' | 'gps' | 'api_first_received' | 'volatile' | 'manual'; //基準時刻のタイプ (default to undefined)
let updateMeasBaseTime: UpdateMeasBaseTime; // (optional)

const { status, data } = await apiInstance.updateMeasurementBaseTime(
    measurementUuid,
    type,
    updateMeasBaseTime
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateMeasBaseTime** | **UpdateMeasBaseTime**|  | |
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **type** | [**&#39;edge_rtc&#39; | &#39;ntp&#39; | &#39;gps&#39; | &#39;api_first_received&#39; | &#39;volatile&#39; | &#39;manual&#39;**]**Array<&#39;edge_rtc&#39; &#124; &#39;ntp&#39; &#124; &#39;gps&#39; &#124; &#39;api_first_received&#39; &#124; &#39;volatile&#39; &#124; &#39;manual&#39;>** | 基準時刻のタイプ | defaults to undefined|


### Return type

**MeasBaseTime**

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

# **updateMeasurementSequence**
> MeasurementSequenceGroup updateMeasurementSequence()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/sequences/{sequence_uuid}` を使用してください） 計測シーケンスを更新します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    MeasurementSequenceGroupReplace
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let sequencesUuid: string; //計測シーケンスのUUID (default to undefined)
let measurementSequenceGroupReplace: MeasurementSequenceGroupReplace; // (optional)

const { status, data } = await apiInstance.updateMeasurementSequence(
    measurementUuid,
    sequencesUuid,
    measurementSequenceGroupReplace
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementSequenceGroupReplace** | **MeasurementSequenceGroupReplace**|  | |
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **sequencesUuid** | [**string**] | 計測シーケンスのUUID | defaults to undefined|


### Return type

**MeasurementSequenceGroup**

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

# **updateProjectMeasurement**
> updateProjectMeasurement()

計測に関する情報を更新します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    ReplaceMeas
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let replaceMeas: ReplaceMeas; // (optional)

const { status, data } = await apiInstance.updateProjectMeasurement(
    projectUuid,
    measurementUuid,
    replaceMeas
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **replaceMeas** | **ReplaceMeas**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


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

# **updateProjectMeasurementBaseTime**
> MeasBaseTime updateProjectMeasurementBaseTime()

**非推奨** 代わりに「Update Project Measurement Base Time By ID」または「Create Project Measurement Base Time」を使用してください。 基準時刻を更新します。 この計測において、使用する基準時刻が設定されていない（ `basetime_type` が `undefined` ）の場合は、 新しい基準時刻を `basetime_type` に設定します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    UpdateMeasBaseTime
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let type: 'edge_rtc' | 'ntp' | 'gps' | 'api_first_received' | 'volatile' | 'manual'; //基準時刻のタイプ (default to undefined)
let updateMeasBaseTime: UpdateMeasBaseTime; // (optional)

const { status, data } = await apiInstance.updateProjectMeasurementBaseTime(
    projectUuid,
    measurementUuid,
    type,
    updateMeasBaseTime
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateMeasBaseTime** | **UpdateMeasBaseTime**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **type** | [**&#39;edge_rtc&#39; | &#39;ntp&#39; | &#39;gps&#39; | &#39;api_first_received&#39; | &#39;volatile&#39; | &#39;manual&#39;**]**Array<&#39;edge_rtc&#39; &#124; &#39;ntp&#39; &#124; &#39;gps&#39; &#124; &#39;api_first_received&#39; &#124; &#39;volatile&#39; &#124; &#39;manual&#39;>** | 基準時刻のタイプ | defaults to undefined|


### Return type

**MeasBaseTime**

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

# **updateProjectMeasurementBaseTimeByID**
> MeasBaseTime updateProjectMeasurementBaseTimeByID()

基準時刻を更新します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    UpdateMeasBaseTimeByID
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let id: number; //基準時刻のID (default to undefined)
let updateMeasBaseTimeByID: UpdateMeasBaseTimeByID; // (optional)

const { status, data } = await apiInstance.updateProjectMeasurementBaseTimeByID(
    projectUuid,
    measurementUuid,
    id,
    updateMeasBaseTimeByID
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateMeasBaseTimeByID** | **UpdateMeasBaseTimeByID**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **id** | [**number**] | 基準時刻のID | defaults to undefined|


### Return type

**MeasBaseTime**

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

# **updateProjectMeasurementSequence**
> MeasurementSequenceGroup updateProjectMeasurementSequence()

計測シーケンスを更新します。

### Example

```typescript
import {
    MeasMeasurementsApi,
    Configuration,
    MeasurementSequenceGroupReplace
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let sequencesUuid: string; //計測シーケンスのUUID (default to undefined)
let measurementSequenceGroupReplace: MeasurementSequenceGroupReplace; // (optional)

const { status, data } = await apiInstance.updateProjectMeasurementSequence(
    projectUuid,
    measurementUuid,
    sequencesUuid,
    measurementSequenceGroupReplace
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementSequenceGroupReplace** | **MeasurementSequenceGroupReplace**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **sequencesUuid** | [**string**] | 計測シーケンスのUUID | defaults to undefined|


### Return type

**MeasurementSequenceGroup**

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

