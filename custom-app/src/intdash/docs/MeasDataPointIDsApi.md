# MeasDataPointIDsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listDataPointDataIDs**](#listdatapointdataids) | **GET** /v1/data_ids | List Data Point Data IDs|
|[**listProjectDataPointDataIDs**](#listprojectdatapointdataids) | **GET** /v1/projects/{project_uuid}/data_ids | List Project Data Point Data IDs|

# **listDataPointDataIDs**
> DataPointDataIDs listDataPointDataIDs()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/data_ids` を使用してください）  データポイントのデータID（ `data_type`, `data_id` ）のリストを取得します。    `name` で計測UUIDを指定した場合、 `start` / `end` パラメーターは無視されます。    `name` でエッジUUIDまたはエッジの名前を指定した場合、 `start` / `end` パラメーターを使ってそのエッジの計測をさらに絞り込むことができます。  この場合、 `start` / `end` で指定された区間内に基準時刻を持つ計測のみが対象となり、その計測に含まれるデータIDが取得されます。

### Example

```typescript
import {
    MeasDataPointIDsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasDataPointIDsApi(configuration);

let name: string; //どの計測またはどのエッジのデータポイントを取得するかを、以下のいずれかを使って指定します： - 計測UUID - エッジUUID - エッジの名前  最初に、指定されたnameに一致する計測UUIDがあるかが検索されます。なければ一致するエッジUUIDがあるかが検索され、それもなければ一致するエッジの名前があるかが検索されます。 (default to undefined)
let start: string; //取得対象区間の始点（始点は対象区間に含まれます）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let end: string; //取得対象区間の終点（終点は対象区間に含まれません）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)

const { status, data } = await apiInstance.listDataPointDataIDs(
    name,
    start,
    end
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **name** | [**string**] | どの計測またはどのエッジのデータポイントを取得するかを、以下のいずれかを使って指定します： - 計測UUID - エッジUUID - エッジの名前  最初に、指定されたnameに一致する計測UUIDがあるかが検索されます。なければ一致するエッジUUIDがあるかが検索され、それもなければ一致するエッジの名前があるかが検索されます。 | defaults to undefined|
| **start** | [**string**] | 取得対象区間の始点（始点は対象区間に含まれます）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **end** | [**string**] | 取得対象区間の終点（終点は対象区間に含まれません）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|


### Return type

**DataPointDataIDs**

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

# **listProjectDataPointDataIDs**
> DataPointDataIDs listProjectDataPointDataIDs()

データポイントのデータID（ `data_type`, `data_id` ）のリストを取得します。  `name` で計測UUIDを指定した場合、 `start` / `end` パラメーターは無視されます。  `name` でエッジUUIDまたはエッジの名前を指定した場合、 `start` / `end` パラメーターを使ってそのエッジの計測をさらに絞り込むことができます。 この場合、 `start` / `end` で指定された区間内に基準時刻を持つ計測のみが対象となり、その計測に含まれるデータIDが取得されます。

### Example

```typescript
import {
    MeasDataPointIDsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MeasDataPointIDsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let name: string; //どの計測またはどのエッジのデータポイントを取得するかを、以下のいずれかを使って指定します： - 計測UUID - エッジUUID - エッジの名前  最初に、指定されたnameに一致する計測UUIDがあるかが検索されます。なければ一致するエッジUUIDがあるかが検索され、それもなければ一致するエッジの名前があるかが検索されます。 (default to undefined)
let start: string; //取得対象区間の始点（始点は対象区間に含まれます）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)
let end: string; //取得対象区間の終点（終点は対象区間に含まれません）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) (optional) (default to undefined)

const { status, data } = await apiInstance.listProjectDataPointDataIDs(
    projectUuid,
    name,
    start,
    end
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **name** | [**string**] | どの計測またはどのエッジのデータポイントを取得するかを、以下のいずれかを使って指定します： - 計測UUID - エッジUUID - エッジの名前  最初に、指定されたnameに一致する計測UUIDがあるかが検索されます。なければ一致するエッジUUIDがあるかが検索され、それもなければ一致するエッジの名前があるかが検索されます。 | defaults to undefined|
| **start** | [**string**] | 取得対象区間の始点（始点は対象区間に含まれます）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|
| **end** | [**string**] | 取得対象区間の終点（終点は対象区間に含まれません）。以下のいずれかの形式で指定します。   - rfc3339(ex 2019-10-29T03:04:05.341268Z)   - UNIX時刻（マイクロ秒）(**Deprecated**) | (optional) defaults to undefined|


### Return type

**DataPointDataIDs**

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

