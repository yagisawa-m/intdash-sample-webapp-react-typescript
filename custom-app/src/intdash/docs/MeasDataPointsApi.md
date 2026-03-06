# MeasDataPointsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createDataPoints**](#createdatapoints) | **POST** /v1/measurements/data | Store Data Points|
|[**createProjectDataPoints**](#createprojectdatapoints) | **POST** /v1/projects/{project_uuid}/measurements/data | Store Project Data Points|
|[**listDataIDs**](#listdataids) | **GET** /v1/getids | List Edge\&#39;s Data IDs|
|[**listDataIDsWithMeasurementUUID**](#listdataidswithmeasurementuuid) | **GET** /v1/measurements/{measurement_uuid}/getids | List Data IDs|
|[**listDataPoints**](#listdatapoints) | **GET** /v1/data | List Data Points|
|[**listProjectDataIDs**](#listprojectdataids) | **GET** /v1/projects/{project_uuid}/getids | List Project Edge\&#39;s Data IDs|
|[**listProjectDataIDsWithMeasurementUUID**](#listprojectdataidswithmeasurementuuid) | **GET** /v1/projects/{project_uuid}/measurements/{measurement_uuid}/getids | List Project Data IDs|
|[**listProjectDataPoints**](#listprojectdatapoints) | **GET** /v1/projects/{project_uuid}/data | List Project Data Points|

# **createDataPoints**
> File createDataPoints()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/data` を使用してください）  データポイントを登録します。

### Example

```typescript
import {
    MeasDataPointsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasDataPointsApi(configuration);

let body: File; //このエンドポイント使用時は、 `Content-Type` を以下にしてください。   * `application/protobuf`       * [protocol.proto](https://docs.intdash.jp/api/measurement/v1.17/proto/index.html) の `StoreProto` を参照してください。         * `DataPointProto` の `data_payload`は iSCP v1のデータフォーマットに従います。         * iSCPのデータフォーマットは [詳説 iSCP 1.0](https://docs.intdash.jp/manual/iscp1-essentials/latest/ja/iscp1-essentials-ja.pdf#page=23)を参照してください。 (optional)

const { status, data } = await apiInstance.createDataPoints(
    body
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **body** | **File**| このエンドポイント使用時は、 &#x60;Content-Type&#x60; を以下にしてください。   * &#x60;application/protobuf&#x60;       * [protocol.proto](https://docs.intdash.jp/api/measurement/v1.17/proto/index.html) の &#x60;StoreProto&#x60; を参照してください。         * &#x60;DataPointProto&#x60; の &#x60;data_payload&#x60;は iSCP v1のデータフォーマットに従います。         * iSCPのデータフォーマットは [詳説 iSCP 1.0](https://docs.intdash.jp/manual/iscp1-essentials/latest/ja/iscp1-essentials-ja.pdf#page&#x3D;23)を参照してください。 | |


### Return type

**File**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/protobuf
 - **Accept**: */*


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createProjectDataPoints**
> File createProjectDataPoints()

データポイントを登録します。

### Example

```typescript
import {
    MeasDataPointsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasDataPointsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let body: File; //このエンドポイント使用時は、 `Content-Type` を以下にしてください。   * `application/protobuf`       * [protocol.proto](https://docs.intdash.jp/api/measurement/v1.17/proto/index.html) の `StoreProto` を参照してください。         * `DataPointProto` の `data_payload`は iSCP v1のデータフォーマットに従います。         * iSCPのデータフォーマットは [詳説 iSCP 1.0](https://docs.intdash.jp/manual/iscp1-essentials/latest/ja/iscp1-essentials-ja.pdf#page=23)を参照してください。 (optional)

const { status, data } = await apiInstance.createProjectDataPoints(
    projectUuid,
    body
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **body** | **File**| このエンドポイント使用時は、 &#x60;Content-Type&#x60; を以下にしてください。   * &#x60;application/protobuf&#x60;       * [protocol.proto](https://docs.intdash.jp/api/measurement/v1.17/proto/index.html) の &#x60;StoreProto&#x60; を参照してください。         * &#x60;DataPointProto&#x60; の &#x60;data_payload&#x60;は iSCP v1のデータフォーマットに従います。         * iSCPのデータフォーマットは [詳説 iSCP 1.0](https://docs.intdash.jp/manual/iscp1-essentials/latest/ja/iscp1-essentials-ja.pdf#page&#x3D;23)を参照してください。 | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


### Return type

**File**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/protobuf
 - **Accept**: */*


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listDataIDs**
> DataIDs listDataIDs()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/getids` を使用してください）  エッジを指定し、そのエッジから送信されているデータに含まれるデータ識別子（ `data_type` 、 `channel` 、 `data_id` の組み合わせ）のリストを取得します。

### Example

```typescript
import {
    MeasDataPointsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasDataPointsApi(configuration);

let start: number; //取得対象範囲の始点（マイクロ秒単位のUNIX時刻） (optional) (default to undefined)
let end: number; //取得対象範囲の終点（マイクロ秒単位のUNIX時刻） (optional) (default to undefined)
let edgeUuid: string; //エッジのUUID (optional) (default to undefined)

const { status, data } = await apiInstance.listDataIDs(
    start,
    end,
    edgeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **start** | [**number**] | 取得対象範囲の始点（マイクロ秒単位のUNIX時刻） | (optional) defaults to undefined|
| **end** | [**number**] | 取得対象範囲の終点（マイクロ秒単位のUNIX時刻） | (optional) defaults to undefined|
| **edgeUuid** | [**string**] | エッジのUUID | (optional) defaults to undefined|


### Return type

**DataIDs**

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

# **listDataIDsWithMeasurementUUID**
> DataIDs listDataIDsWithMeasurementUUID()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/measurements/{measurement_uuid}/getids` を使用してください） 計測を指定し、その計測に含まれるデータ識別子（ `data_type` 、 `channel` 、 `data_id` の組み合わせ）のリストを取得します。

### Example

```typescript
import {
    MeasDataPointsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasDataPointsApi(configuration);

let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.listDataIDsWithMeasurementUUID(
    measurementUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **measurementUuid** | [**string**] | 計測のUUID | defaults to undefined|


### Return type

**DataIDs**

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

# **listDataPoints**
> File listDataPoints()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/data` を使用してください）  データポイントのリストを取得します。  返却されるデータポイントはJSON形式です。データポイントごとに改行で区切られます。

### Example

```typescript
import {
    MeasDataPointsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasDataPointsApi(configuration);

let name: string; //どの計測またはどのエッジのデータポイントを取得するかを、以下のいずれかを使って指定します： - 計測UUID - エッジUUID - エッジの名前  最初に、指定されたnameに一致する計測UUIDがあるかが検索されます。なければ一致するエッジUUIDがあるかが検索され、それもなければ一致するエッジの名前があるかが検索されます。 (default to undefined)
let start: string; //取得対象区間の始点（始点は対象区間に含まれます）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let end: string; //取得対象区間の終点（終点は対象区間に含まれません）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let idq: Array<string>; //取得したいデータポイントの条件を以下のフォーマットで指定します。  - `<data_type>:<data_id>`  `data_type` 、 `data_id` は `GET /data_ids` エンドポイントで取得できます。     各セグメントにはワイルドカード(*)を使用することができます。  例:   - データタイプが `string` かつ、データ名が任意のものを取得する -> `string:*` または `string`     - ※ iSCPv1で永続化されたデータはデータタイプが10進数となることに注意してください。詳細は以下の「参考2」を参照してください。  **参考１** iSCP v2形式で保存されたデータの場合    iSCP v2形式で保存されたデータポイントの `data_type` 、 `data_id` は次のようになります。  - `data_type`：<iSCPv2におけるデータ型>  - `data_id`：<iSCPv2におけるデータ名称>   例:    - iSCPv2で永続化された、データ型が「string」のデータポイントを取得する：`string:*` または `string`   - iSCPv2で永続化された、データ型が「string」で、データ名称が「my-data」のデータポイントを取得する：`string:my-data`  **参考２** iSCP v1形式で保存されたデータの場合    iSCP v1形式で保存されたデータポイントの `data_type` 、 `data_id` は次のようになります。  - `data_type`：<iSCPv1におけるデータタイプ(10進数表記)>  - `data_id`：<iSCPv1におけるチャンネル(10進数表記)>/<iSCPv1におけるデータID>  例:    - iSCPv1で永続化された、CAN(データタイプが「1」)のデータポイントを取得する：`1:*_/_*` または `1`   - iSCPv1で永続化された、チャンネル2のCANデータポイントを取得する：`1:2/_*` または `1:2`   - iSCPv1で永続化された、チャンネル2のCANデータポイントのうち、データIDが 「00000001」 のものを取得する：`1:2/00000001` (optional) (default to undefined)
let since: string; //指定した時刻以降に更新された計測のみを取得します。 以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z).   - UNIX時刻（マイクロ秒）(**Deprecated**). (optional) (default to undefined)
let exitOnError: string; //`true` を指定した場合、取得中にエラーが発生すると処理を中断し、中断前までのデータポイントのリストを返します。 (optional) (default to 'false')
let label: Array<string>; //信号定義のラベル (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数。デフォルトは無制限。 (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序。デフォルトは `asc` （昇順） (optional) (default to undefined)
let timeFormat: 'ns' | 'us' | 'ms' | 's' | 'rfc3339'; //レスポンスの時刻表示形式。デフォルトは `us` （マイクロ秒） (optional) (default to undefined)

const { status, data } = await apiInstance.listDataPoints(
    name,
    start,
    end,
    idq,
    since,
    exitOnError,
    label,
    limit,
    order,
    timeFormat
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **name** | [**string**] | どの計測またはどのエッジのデータポイントを取得するかを、以下のいずれかを使って指定します： - 計測UUID - エッジUUID - エッジの名前  最初に、指定されたnameに一致する計測UUIDがあるかが検索されます。なければ一致するエッジUUIDがあるかが検索され、それもなければ一致するエッジの名前があるかが検索されます。 | defaults to undefined|
| **start** | [**string**] | 取得対象区間の始点（始点は対象区間に含まれます）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **end** | [**string**] | 取得対象区間の終点（終点は対象区間に含まれません）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **idq** | **Array&lt;string&gt;** | 取得したいデータポイントの条件を以下のフォーマットで指定します。  - &#x60;&lt;data_type&gt;:&lt;data_id&gt;&#x60;  &#x60;data_type&#x60; 、 &#x60;data_id&#x60; は &#x60;GET /data_ids&#x60; エンドポイントで取得できます。     各セグメントにはワイルドカード(*)を使用することができます。  例:   - データタイプが &#x60;string&#x60; かつ、データ名が任意のものを取得する -&gt; &#x60;string:*&#x60; または &#x60;string&#x60;     - ※ iSCPv1で永続化されたデータはデータタイプが10進数となることに注意してください。詳細は以下の「参考2」を参照してください。  **参考１** iSCP v2形式で保存されたデータの場合    iSCP v2形式で保存されたデータポイントの &#x60;data_type&#x60; 、 &#x60;data_id&#x60; は次のようになります。  - &#x60;data_type&#x60;：&lt;iSCPv2におけるデータ型&gt;  - &#x60;data_id&#x60;：&lt;iSCPv2におけるデータ名称&gt;   例:    - iSCPv2で永続化された、データ型が「string」のデータポイントを取得する：&#x60;string:*&#x60; または &#x60;string&#x60;   - iSCPv2で永続化された、データ型が「string」で、データ名称が「my-data」のデータポイントを取得する：&#x60;string:my-data&#x60;  **参考２** iSCP v1形式で保存されたデータの場合    iSCP v1形式で保存されたデータポイントの &#x60;data_type&#x60; 、 &#x60;data_id&#x60; は次のようになります。  - &#x60;data_type&#x60;：&lt;iSCPv1におけるデータタイプ(10進数表記)&gt;  - &#x60;data_id&#x60;：&lt;iSCPv1におけるチャンネル(10進数表記)&gt;/&lt;iSCPv1におけるデータID&gt;  例:    - iSCPv1で永続化された、CAN(データタイプが「1」)のデータポイントを取得する：&#x60;1:*_/_*&#x60; または &#x60;1&#x60;   - iSCPv1で永続化された、チャンネル2のCANデータポイントを取得する：&#x60;1:2/_*&#x60; または &#x60;1:2&#x60;   - iSCPv1で永続化された、チャンネル2のCANデータポイントのうち、データIDが 「00000001」 のものを取得する：&#x60;1:2/00000001&#x60; | (optional) defaults to undefined|
| **since** | [**string**] | 指定した時刻以降に更新された計測のみを取得します。 以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z).   - UNIX時刻（マイクロ秒）(**Deprecated**). | (optional) defaults to undefined|
| **exitOnError** | [**string**] | &#x60;true&#x60; を指定した場合、取得中にエラーが発生すると処理を中断し、中断前までのデータポイントのリストを返します。 | (optional) defaults to 'false'|
| **label** | **Array&lt;string&gt;** | 信号定義のラベル | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数。デフォルトは無制限。 | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序。デフォルトは &#x60;asc&#x60; （昇順） | (optional) defaults to undefined|
| **timeFormat** | [**&#39;ns&#39; | &#39;us&#39; | &#39;ms&#39; | &#39;s&#39; | &#39;rfc3339&#39;**]**Array<&#39;ns&#39; &#124; &#39;us&#39; &#124; &#39;ms&#39; &#124; &#39;s&#39; &#124; &#39;rfc3339&#39;>** | レスポンスの時刻表示形式。デフォルトは &#x60;us&#x60; （マイクロ秒） | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8, application/protobuf


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  * Transfer-Encoding -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listProjectDataIDs**
> DataIDs listProjectDataIDs()

エッジを指定し、そのエッジから送信されているデータに含まれるデータ識別子（ `data_type` 、 `channel` 、 `data_id` の組み合わせ）のリストを取得します。

### Example

```typescript
import {
    MeasDataPointsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasDataPointsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let start: number; //取得対象範囲の始点（マイクロ秒単位のUNIX時刻） (optional) (default to undefined)
let end: number; //取得対象範囲の終点（マイクロ秒単位のUNIX時刻） (optional) (default to undefined)
let edgeUuid: string; //エッジのUUID (optional) (default to undefined)

const { status, data } = await apiInstance.listProjectDataIDs(
    projectUuid,
    start,
    end,
    edgeUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **start** | [**number**] | 取得対象範囲の始点（マイクロ秒単位のUNIX時刻） | (optional) defaults to undefined|
| **end** | [**number**] | 取得対象範囲の終点（マイクロ秒単位のUNIX時刻） | (optional) defaults to undefined|
| **edgeUuid** | [**string**] | エッジのUUID | (optional) defaults to undefined|


### Return type

**DataIDs**

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

# **listProjectDataIDsWithMeasurementUUID**
> DataIDs listProjectDataIDsWithMeasurementUUID()

計測を指定し、その計測に含まれるデータ識別子（ `data_type` 、 `channel` 、 `data_id` の組み合わせ）のリストを取得します。

### Example

```typescript
import {
    MeasDataPointsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasDataPointsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let measurementUuid: string; //計測のUUID (default to undefined)

const { status, data } = await apiInstance.listProjectDataIDsWithMeasurementUUID(
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

**DataIDs**

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

# **listProjectDataPoints**
> File listProjectDataPoints()

データポイントのリストを取得します。 返却されるデータポイントはJSON形式です。データポイントごとに改行で区切られます。

### Example

```typescript
import {
    MeasDataPointsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasDataPointsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let name: string; //どの計測またはどのエッジのデータポイントを取得するかを、以下のいずれかを使って指定します： - 計測UUID - エッジUUID - エッジの名前  最初に、指定されたnameに一致する計測UUIDがあるかが検索されます。なければ一致するエッジUUIDがあるかが検索され、それもなければ一致するエッジの名前があるかが検索されます。 (default to undefined)
let idq: Array<string>; //取得したいデータポイントの条件を以下のフォーマットで指定します。  - `<data_type>:<data_id>`  `data_type` 、 `data_id` は `GET /data_ids` エンドポイントで取得できます。     各セグメントにはワイルドカード(*)を使用することができます。  例:   - データタイプが `string` かつ、データ名が任意のものを取得する -> `string:*` または `string`     - ※ iSCPv1で永続化されたデータはデータタイプが10進数となることに注意してください。詳細は以下の「参考2」を参照してください。  **参考１** iSCP v2形式で保存されたデータの場合    iSCP v2形式で保存されたデータポイントの `data_type` 、 `data_id` は次のようになります。  - `data_type`：<iSCPv2におけるデータ型>  - `data_id`：<iSCPv2におけるデータ名称>   例:    - iSCPv2で永続化された、データ型が「string」のデータポイントを取得する：`string:*` または `string`   - iSCPv2で永続化された、データ型が「string」で、データ名称が「my-data」のデータポイントを取得する：`string:my-data`  **参考２** iSCP v1形式で保存されたデータの場合    iSCP v1形式で保存されたデータポイントの `data_type` 、 `data_id` は次のようになります。  - `data_type`：<iSCPv1におけるデータタイプ(10進数表記)>  - `data_id`：<iSCPv1におけるチャンネル(10進数表記)>/<iSCPv1におけるデータID>  例:    - iSCPv1で永続化された、CAN(データタイプが「1」)のデータポイントを取得する：`1:*_/_*` または `1`   - iSCPv1で永続化された、チャンネル2のCANデータポイントを取得する：`1:2/_*` または `1:2`   - iSCPv1で永続化された、チャンネル2のCANデータポイントのうち、データIDが 「00000001」 のものを取得する：`1:2/00000001` (optional) (default to undefined)
let start: string; //取得対象区間の始点（始点は対象区間に含まれます）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let end: string; //取得対象区間の終点（終点は対象区間に含まれません）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let since: string; //指定した時刻以降に更新された計測のみを取得します。 以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z).   - UNIX時刻（マイクロ秒）(**Deprecated**). (optional) (default to undefined)
let exitOnError: string; //`true` を指定した場合、取得中にエラーが発生すると処理を中断し、中断前までのデータポイントのリストを返します。 (optional) (default to 'false')
let label: Array<string>; //信号定義のラベル (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)
let order: 'asc' | 'desc'; //並べ替えの順序。デフォルトは `asc` （昇順） (optional) (default to undefined)
let timeFormat: 'ns' | 'us' | 'ms' | 's' | 'rfc3339'; //レスポンスの時刻表示形式。デフォルトは `us` （マイクロ秒） (optional) (default to undefined)

const { status, data } = await apiInstance.listProjectDataPoints(
    projectUuid,
    name,
    idq,
    start,
    end,
    since,
    exitOnError,
    label,
    limit,
    order,
    timeFormat
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **name** | [**string**] | どの計測またはどのエッジのデータポイントを取得するかを、以下のいずれかを使って指定します： - 計測UUID - エッジUUID - エッジの名前  最初に、指定されたnameに一致する計測UUIDがあるかが検索されます。なければ一致するエッジUUIDがあるかが検索され、それもなければ一致するエッジの名前があるかが検索されます。 | defaults to undefined|
| **idq** | **Array&lt;string&gt;** | 取得したいデータポイントの条件を以下のフォーマットで指定します。  - &#x60;&lt;data_type&gt;:&lt;data_id&gt;&#x60;  &#x60;data_type&#x60; 、 &#x60;data_id&#x60; は &#x60;GET /data_ids&#x60; エンドポイントで取得できます。     各セグメントにはワイルドカード(*)を使用することができます。  例:   - データタイプが &#x60;string&#x60; かつ、データ名が任意のものを取得する -&gt; &#x60;string:*&#x60; または &#x60;string&#x60;     - ※ iSCPv1で永続化されたデータはデータタイプが10進数となることに注意してください。詳細は以下の「参考2」を参照してください。  **参考１** iSCP v2形式で保存されたデータの場合    iSCP v2形式で保存されたデータポイントの &#x60;data_type&#x60; 、 &#x60;data_id&#x60; は次のようになります。  - &#x60;data_type&#x60;：&lt;iSCPv2におけるデータ型&gt;  - &#x60;data_id&#x60;：&lt;iSCPv2におけるデータ名称&gt;   例:    - iSCPv2で永続化された、データ型が「string」のデータポイントを取得する：&#x60;string:*&#x60; または &#x60;string&#x60;   - iSCPv2で永続化された、データ型が「string」で、データ名称が「my-data」のデータポイントを取得する：&#x60;string:my-data&#x60;  **参考２** iSCP v1形式で保存されたデータの場合    iSCP v1形式で保存されたデータポイントの &#x60;data_type&#x60; 、 &#x60;data_id&#x60; は次のようになります。  - &#x60;data_type&#x60;：&lt;iSCPv1におけるデータタイプ(10進数表記)&gt;  - &#x60;data_id&#x60;：&lt;iSCPv1におけるチャンネル(10進数表記)&gt;/&lt;iSCPv1におけるデータID&gt;  例:    - iSCPv1で永続化された、CAN(データタイプが「1」)のデータポイントを取得する：&#x60;1:*_/_*&#x60; または &#x60;1&#x60;   - iSCPv1で永続化された、チャンネル2のCANデータポイントを取得する：&#x60;1:2/_*&#x60; または &#x60;1:2&#x60;   - iSCPv1で永続化された、チャンネル2のCANデータポイントのうち、データIDが 「00000001」 のものを取得する：&#x60;1:2/00000001&#x60; | (optional) defaults to undefined|
| **start** | [**string**] | 取得対象区間の始点（始点は対象区間に含まれます）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **end** | [**string**] | 取得対象区間の終点（終点は対象区間に含まれません）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **since** | [**string**] | 指定した時刻以降に更新された計測のみを取得します。 以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z).   - UNIX時刻（マイクロ秒）(**Deprecated**). | (optional) defaults to undefined|
| **exitOnError** | [**string**] | &#x60;true&#x60; を指定した場合、取得中にエラーが発生すると処理を中断し、中断前までのデータポイントのリストを返します。 | (optional) defaults to 'false'|
| **label** | **Array&lt;string&gt;** | 信号定義のラベル | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序。デフォルトは &#x60;asc&#x60; （昇順） | (optional) defaults to undefined|
| **timeFormat** | [**&#39;ns&#39; | &#39;us&#39; | &#39;ms&#39; | &#39;s&#39; | &#39;rfc3339&#39;**]**Array<&#39;ns&#39; &#124; &#39;us&#39; &#124; &#39;ms&#39; &#124; &#39;s&#39; &#124; &#39;rfc3339&#39;>** | レスポンスの時刻表示形式。デフォルトは &#x60;us&#x60; （マイクロ秒） | (optional) defaults to undefined|


### Return type

**File**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8, application/protobuf


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  * Transfer-Encoding -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

