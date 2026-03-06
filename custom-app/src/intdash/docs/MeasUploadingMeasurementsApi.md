# MeasUploadingMeasurementsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listMeasurementStatuses**](#listmeasurementstatuses) | **GET** /v1/measurements/upload | List Uploading Statuses of Measurements|
|[**listProjectMeasurementStatuses**](#listprojectmeasurementstatuses) | **GET** /v1/projects/{project_uuid}/measurements/upload | List Project Uploading Statuses of Measurements|
|[**uploadMeasurement**](#uploadmeasurement) | **POST** /v1/measurements/upload | Create Measurement from CSV File|
|[**uploadMeasurementIntoMeasurement**](#uploadmeasurementintomeasurement) | **POST** /v1/measurements/{measurement_uuid}/upload | Store Data Points by CSV File|
|[**uploadProjectMeasurement**](#uploadprojectmeasurement) | **POST** /v1/projects/{project_uuid}/measurements/upload | Create Project Measurement from CSV File|
|[**uploadProjectMeasurementIntoMeasurement**](#uploadprojectmeasurementintomeasurement) | **POST** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/upload | Store Project Data Points by CSV File|

# **listMeasurementStatuses**
> MeasurementUploadStatusesGetResponse listMeasurementStatuses()

（ **Deprecated** このエンドポイントではなく、`GET /measurements/jobs` を使用してください。） 計測のアップロードのリストを取得します。

### Example

```typescript
import {
    MeasUploadingMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasUploadingMeasurementsApi(configuration);

let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)
let sort: 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'created_at')
let page: number; //取得するページの番号 (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)

const { status, data } = await apiInstance.listMeasurementStatuses(
    limit,
    sort,
    page,
    order
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|
| **sort** | [**&#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'created_at'|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|


### Return type

**MeasurementUploadStatusesGetResponse**

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

# **listProjectMeasurementStatuses**
> MeasurementUploadStatusesGetResponse listProjectMeasurementStatuses()

（ **Deprecated** このエンドポイントではなく、`GET /measurements/jobs` を使用してください。） 計測のアップロードのリストを取得します。

### Example

```typescript
import {
    MeasUploadingMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasUploadingMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)
let sort: 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'created_at')
let page: number; //取得するページの番号 (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)

const { status, data } = await apiInstance.listProjectMeasurementStatuses(
    projectUuid,
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
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|
| **sort** | [**&#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'created_at'|
| **page** | [**number**] | 取得するページの番号 | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|


### Return type

**MeasurementUploadStatusesGetResponse**

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

# **uploadMeasurement**
> MeasurementUploadPostResponse uploadMeasurement()

CSVまたはMP4（**MP4はexperimental**）ファイルをアップロードし、計測を作成します。 計測には、指定されたエッジUUIDが関連付けられます。  `base_time` （基準時刻）は、RFC3339による表現か、UNIX時刻（マイクロ秒）を指定してください。 基準時刻が指定されていない場合は、CSVファイルのデータ行の1行目の時刻が基準時刻として使用されます。 CSVファイルのデータは、時刻順にソートされている必要があります。 `meas_end` パラメーターの設定は任意です。指定しない場合、 `true` となります。  CSVファイルの例: ``` time,       col1,   col2, col3,      col4,   col5, col6,      col7,   col8, col9,      col10 1539263579, val11,  12,   13.12345,  val14,  15,   16.12345,  val17,  18, 19.12345,  val110 1539263580, val21,  22,   23.12345,  val24,  25,   26.12345,  val27,  28, 29.12345,  val210 1539263581, val31,  32,   33.12345,  val34,  35,   36.12345,  val37,  38, 39.12345,  val310 1539263582, val41,  42,   43.12345,  val44,  45,   46.12345,  val47,  48, 49.12345,  val410 ``` 空白行がある場合、行番号のカウントは加算されますが、その行は処理されません。 例えば、以下のような場合の空白行は無視されます。 ``` time,       col1,   col2, col3,      col4,   col5, col6,      col7,   col8, col9,      col10 1539263579, val11,  12,   13.12345,  val14,  15,   16.12345,  val17,  18, 19.12345,  val110  1539263581, val31,  32,   33.12345,  val34,  35,   36.12345,  val37,  38, 39.12345,  val310 1539263582, val41,  42,   43.12345,  val44,  45,   46.12345,  val47,  48, 49.12345,  val410 ```  [Go parser library](https://golang.org/pkg/encoding/csv/) も参照してください。  時刻の列には、RFC3339による表現か、UNIX時刻（秒）を使用することができます。 ## エスケープ 値の内部で `,` を使用したい場合は、その値全体を `\"` で囲んでください。 また、値の内部で `\"` を使用したい場合は、値全体を `\"` で囲み、さらに、 `\"` を `\"\"` のように表記してください。 値を `\"` で囲まないと、CSVファイルのパースの際にエラーが発生します。  エスケープの例: ``` time,col1 1539263579,\"ab,cde\"                  .....OK (parsed as \'ab,cde\') 1539263579,\"ab\"\"cde\"                 .....OK (parsed as \'ab\"cde\') 1539263579,     abcde                .....OK (parsed as \'     abcde\') 1539263579,\"     abcde\"              .....OK (parsed as \'     abcde\') 1539263579,ab\"cde                    .....NG 1539263579, \"abcde\"                  .....NG 1539263579,ab,cde                    .....NG(wrong number of fields) ```

### Example

```typescript
import {
    MeasUploadingMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasUploadingMeasurementsApi(configuration);

let edgeUuid: string; //エッジのUUID (default to undefined)
let dataFile: File; //アップロードするファイル (default to undefined)
let baseTime: string; //計測の基準時刻。MP4ファイルをアップロードする場合は必須です。 (optional) (default to undefined)
let baseTimeType: string; //基準時刻のタイプ (optional) (default to 'edge_rtc')
let channel: number; //計測のチャンネル（十進表記の文字列） (optional) (default to undefined)
let measEnd: boolean; //`true` にすると、計測は終了したものとして扱われます。 (optional) (default to undefined)
let labelDataType: string; //列名とデータタイプの対応。 データタイプは、 `int` 、` string` 、 `float` のいずれかを指定してください。 例: ``` {   \\\"column_1\\\": \\\"float\\\",   \\\"column_2\\\": \\\"string\\\",   \\\"column_3\\\": \\\"int\\\" } ``` (optional) (default to undefined)

const { status, data } = await apiInstance.uploadMeasurement(
    edgeUuid,
    dataFile,
    baseTime,
    baseTimeType,
    channel,
    measEnd,
    labelDataType
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|
| **dataFile** | [**File**] | アップロードするファイル | defaults to undefined|
| **baseTime** | [**string**] | 計測の基準時刻。MP4ファイルをアップロードする場合は必須です。 | (optional) defaults to undefined|
| **baseTimeType** | [**string**]**Array<&#39;edge_rtc&#39; &#124; &#39;ntp&#39; &#124; &#39;gps&#39; &#124; &#39;api_first_received&#39; &#124; &#39;volatile&#39; &#124; &#39;manual&#39; &#124; &#39;undefined&#39;>** | 基準時刻のタイプ | (optional) defaults to 'edge_rtc'|
| **channel** | [**number**] | 計測のチャンネル（十進表記の文字列） | (optional) defaults to undefined|
| **measEnd** | [**boolean**] | &#x60;true&#x60; にすると、計測は終了したものとして扱われます。 | (optional) defaults to undefined|
| **labelDataType** | [**string**] | 列名とデータタイプの対応。 データタイプは、 &#x60;int&#x60; 、&#x60; string&#x60; 、 &#x60;float&#x60; のいずれかを指定してください。 例: &#x60;&#x60;&#x60; {   \\\&quot;column_1\\\&quot;: \\\&quot;float\\\&quot;,   \\\&quot;column_2\\\&quot;: \\\&quot;string\\\&quot;,   \\\&quot;column_3\\\&quot;: \\\&quot;int\\\&quot; } &#x60;&#x60;&#x60; | (optional) defaults to undefined|


### Return type

**MeasurementUploadPostResponse**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**202** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uploadMeasurementIntoMeasurement**
> MeasurementUploadPostResponse uploadMeasurementIntoMeasurement()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/upload` を使用してください）  CSVファイルをアップロードし、計測にデータを追加します。

### Example

```typescript
import {
    MeasUploadingMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasUploadingMeasurementsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)
let dataFile: File; //アップロードするファイル (default to undefined)
let channel: number; //作成された計測のチャンネル (optional) (default to undefined)
let measEnd: boolean; //* `true` : 終了した計測 * `false` : 終了していない計測 (optional) (default to undefined)
let labelDataType: string; //列名とデータタイプの対応。 データタイプは、 `int` 、` string` 、 `float` のいずれかを指定してください。 例: ``` {   \\\"column_1\\\": \\\"float\\\",   \\\"column_2\\\": \\\"string\\\",   \\\"column_3\\\": \\\"int\\\" } ``` (optional) (default to undefined)

const { status, data } = await apiInstance.uploadMeasurementIntoMeasurement(
    measurementUuid,
    dataFile,
    channel,
    measEnd,
    labelDataType
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **dataFile** | [**File**] | アップロードするファイル | defaults to undefined|
| **channel** | [**number**] | 作成された計測のチャンネル | (optional) defaults to undefined|
| **measEnd** | [**boolean**] | * &#x60;true&#x60; : 終了した計測 * &#x60;false&#x60; : 終了していない計測 | (optional) defaults to undefined|
| **labelDataType** | [**string**] | 列名とデータタイプの対応。 データタイプは、 &#x60;int&#x60; 、&#x60; string&#x60; 、 &#x60;float&#x60; のいずれかを指定してください。 例: &#x60;&#x60;&#x60; {   \\\&quot;column_1\\\&quot;: \\\&quot;float\\\&quot;,   \\\&quot;column_2\\\&quot;: \\\&quot;string\\\&quot;,   \\\&quot;column_3\\\&quot;: \\\&quot;int\\\&quot; } &#x60;&#x60;&#x60; | (optional) defaults to undefined|


### Return type

**MeasurementUploadPostResponse**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**202** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uploadProjectMeasurement**
> MeasurementUploadPostResponse uploadProjectMeasurement()

CSVまたはMP4（**MP4はexperimental**）ファイルをアップロードし、計測を作成します。 計測には、指定されたエッジUUIDが関連付けられます。  `base_time` （基準時刻）は、RFC3339による表現か、UNIX時刻（マイクロ秒）を指定してください。 基準時刻が指定されていない場合は、CSVファイルのデータ行の1行目の時刻が基準時刻として使用されます。 CSVファイルのデータは、時刻順にソートされている必要があります。 `meas_end` パラメーターの設定は任意です。指定しない場合、 `true` となります。  CSVファイルの例: ``` time,       col1,   col2, col3,      col4,   col5, col6,      col7,   col8, col9,      col10 1539263579, val11,  12,   13.12345,  val14,  15,   16.12345,  val17,  18, 19.12345,  val110 1539263580, val21,  22,   23.12345,  val24,  25,   26.12345,  val27,  28, 29.12345,  val210 1539263581, val31,  32,   33.12345,  val34,  35,   36.12345,  val37,  38, 39.12345,  val310 1539263582, val41,  42,   43.12345,  val44,  45,   46.12345,  val47,  48, 49.12345,  val410 ``` 空白行がある場合、行番号のカウントは加算されますが、その行は処理されません。 例えば、以下のような場合の空白行は無視されます。 ``` time,       col1,   col2, col3,      col4,   col5, col6,      col7,   col8, col9,      col10 1539263579, val11,  12,   13.12345,  val14,  15,   16.12345,  val17,  18, 19.12345,  val110  1539263581, val31,  32,   33.12345,  val34,  35,   36.12345,  val37,  38, 39.12345,  val310 1539263582, val41,  42,   43.12345,  val44,  45,   46.12345,  val47,  48, 49.12345,  val410 ```  [Go parser library](https://golang.org/pkg/encoding/csv/) も参照してください。  時刻の列には、RFC3339による表現か、UNIX時刻（秒）を使用することができます。 ## エスケープ 値の内部で `,` を使用したい場合は、その値全体を `\"` で囲んでください。 また、値の内部で `\"` を使用したい場合は、値全体を `\"` で囲み、さらに、 `\"` を `\"\"` のように表記してください。 値を `\"` で囲まないと、CSVファイルのパースの際にエラーが発生します。  エスケープの例: ``` time,col1 1539263579,\"ab,cde\"                  .....OK (parsed as \'ab,cde\') 1539263579,\"ab\"\"cde\"                 .....OK (parsed as \'ab\"cde\') 1539263579,     abcde                .....OK (parsed as \'     abcde\') 1539263579,\"     abcde\"              .....OK (parsed as \'     abcde\') 1539263579,ab\"cde                    .....NG 1539263579, \"abcde\"                  .....NG 1539263579,ab,cde                    .....NG(wrong number of fields) ```

### Example

```typescript
import {
    MeasUploadingMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasUploadingMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let edgeUuid: string; //エッジのUUID (default to undefined)
let dataFile: File; //アップロードするファイル (default to undefined)
let baseTime: string; //計測の基準時刻。MP4ファイルをアップロードする場合は必須です。 (optional) (default to undefined)
let baseTimeType: string; //基準時刻のタイプ (optional) (default to 'edge_rtc')
let channel: number; //計測のチャンネル（十進表記の文字列） (optional) (default to undefined)
let measEnd: boolean; //`true` にすると、計測は終了したものとして扱われます。 (optional) (default to undefined)
let labelDataType: string; //列名とデータタイプの対応。 データタイプは、 `int` 、` string` 、 `float` のいずれかを指定してください。 例: ``` {   \\\"column_1\\\": \\\"float\\\",   \\\"column_2\\\": \\\"string\\\",   \\\"column_3\\\": \\\"int\\\" } ``` (optional) (default to undefined)

const { status, data } = await apiInstance.uploadProjectMeasurement(
    projectUuid,
    edgeUuid,
    dataFile,
    baseTime,
    baseTimeType,
    channel,
    measEnd,
    labelDataType
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **edgeUuid** | [**string**] | エッジのUUID | defaults to undefined|
| **dataFile** | [**File**] | アップロードするファイル | defaults to undefined|
| **baseTime** | [**string**] | 計測の基準時刻。MP4ファイルをアップロードする場合は必須です。 | (optional) defaults to undefined|
| **baseTimeType** | [**string**]**Array<&#39;edge_rtc&#39; &#124; &#39;ntp&#39; &#124; &#39;gps&#39; &#124; &#39;api_first_received&#39; &#124; &#39;volatile&#39; &#124; &#39;manual&#39; &#124; &#39;undefined&#39;>** | 基準時刻のタイプ | (optional) defaults to 'edge_rtc'|
| **channel** | [**number**] | 計測のチャンネル（十進表記の文字列） | (optional) defaults to undefined|
| **measEnd** | [**boolean**] | &#x60;true&#x60; にすると、計測は終了したものとして扱われます。 | (optional) defaults to undefined|
| **labelDataType** | [**string**] | 列名とデータタイプの対応。 データタイプは、 &#x60;int&#x60; 、&#x60; string&#x60; 、 &#x60;float&#x60; のいずれかを指定してください。 例: &#x60;&#x60;&#x60; {   \\\&quot;column_1\\\&quot;: \\\&quot;float\\\&quot;,   \\\&quot;column_2\\\&quot;: \\\&quot;string\\\&quot;,   \\\&quot;column_3\\\&quot;: \\\&quot;int\\\&quot; } &#x60;&#x60;&#x60; | (optional) defaults to undefined|


### Return type

**MeasurementUploadPostResponse**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**202** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uploadProjectMeasurementIntoMeasurement**
> MeasurementUploadPostResponse uploadProjectMeasurementIntoMeasurement()

CSVファイルをアップロードし、計測にデータを追加します。

### Example

```typescript
import {
    MeasUploadingMeasurementsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasUploadingMeasurementsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)
let dataFile: File; //アップロードするファイル (default to undefined)
let channel: number; //作成された計測のチャンネル (optional) (default to undefined)
let measEnd: boolean; //* `true` : 終了した計測 * `false` : 終了していない計測 (optional) (default to undefined)
let labelDataType: string; //列名とデータタイプの対応。 データタイプは、 `int` 、` string` 、 `float` のいずれかを指定してください。 例: ``` {   \\\"column_1\\\": \\\"float\\\",   \\\"column_2\\\": \\\"string\\\",   \\\"column_3\\\": \\\"int\\\" } ``` (optional) (default to undefined)

const { status, data } = await apiInstance.uploadProjectMeasurementIntoMeasurement(
    projectUuid,
    measurementUuid,
    dataFile,
    channel,
    measEnd,
    labelDataType
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|
| **dataFile** | [**File**] | アップロードするファイル | defaults to undefined|
| **channel** | [**number**] | 作成された計測のチャンネル | (optional) defaults to undefined|
| **measEnd** | [**boolean**] | * &#x60;true&#x60; : 終了した計測 * &#x60;false&#x60; : 終了していない計測 | (optional) defaults to undefined|
| **labelDataType** | [**string**] | 列名とデータタイプの対応。 データタイプは、 &#x60;int&#x60; 、&#x60; string&#x60; 、 &#x60;float&#x60; のいずれかを指定してください。 例: &#x60;&#x60;&#x60; {   \\\&quot;column_1\\\&quot;: \\\&quot;float\\\&quot;,   \\\&quot;column_2\\\&quot;: \\\&quot;string\\\&quot;,   \\\&quot;column_3\\\&quot;: \\\&quot;int\\\&quot; } &#x60;&#x60;&#x60; | (optional) defaults to undefined|


### Return type

**MeasurementUploadPostResponse**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**202** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

