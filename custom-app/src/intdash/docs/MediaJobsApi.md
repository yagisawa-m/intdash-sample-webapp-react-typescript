# MediaJobsApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createJob**](#createjob) | **POST** /media/jobs | Create Job|
|[**createProjectJob**](#createprojectjob) | **POST** /media/projects/{project_uuid}/jobs | Create Project Job|
|[**getJobs**](#getjobs) | **GET** /media/jobs | List Jobs|
|[**getProjectJobs**](#getprojectjobs) | **GET** /media/projects/{project_uuid}/jobs | List Project Jobs|

# **createJob**
> Job createJob()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） HLSへの変換ジョブを作成します。

### Example

```typescript
import {
    MediaJobsApi,
    Configuration,
    CreateJobRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaJobsApi(configuration);

let createJobRequest: CreateJobRequest; // (optional)

const { status, data } = await apiInstance.createJob(
    createJobRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createJobRequest** | **CreateJobRequest**|  | |


### Return type

**Job**

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
|**409** | Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createProjectJob**
> Job createProjectJob()

HLSへの変換ジョブを作成します。

### Example

```typescript
import {
    MediaJobsApi,
    Configuration,
    CreateJobRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaJobsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let createJobRequest: CreateJobRequest; // (optional)

const { status, data } = await apiInstance.createProjectJob(
    projectUuid,
    createJobRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createJobRequest** | **CreateJobRequest**|  | |
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


### Return type

**Job**

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
|**409** | Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getJobs**
> JobList getJobs()

（Deprecated。代わりに Prefix(`/projects/00000000-0000-0000-0000-000000000000/`)が付いたエンドポイントを使用してください） HLSへの変換ジョブのリストを取得します。

### Example

```typescript
import {
    MediaJobsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaJobsApi(configuration);

let uuid: Array<string>; //取得したいジョブのUUID (optional) (default to undefined)
let measUuid: Array<string>; //計測のUUID (optional) (default to undefined)
let type: Array<JobType>; //- update   - 計測内の動画データのうち、新しくサーバーが受信した部分（HLSにまだ変換されていない部分）を     HLSに変換するジョブ。通常は計測実行中に行います。 - finalize   - 計測全体をサーバーに回収した後に、動画データ全体をHLSに変換するジョブ - delete   - 変換によって作成されたHLSデータを削除するジョブ。     このジョブを実行すると、HLSプレイリスト、セグメントファイル、     データベース内のHLSに関する情報が削除され、この動画のHLSによる再生はできなくなります。 (optional) (default to undefined)
let status: Array<JobStatus>; //ジョブのステータス (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)
let page: number; //取得するページ番号 (optional) (default to 1)
let sort: 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'created_at')
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)

const { status, data } = await apiInstance.getJobs(
    uuid,
    measUuid,
    type,
    status,
    limit,
    page,
    sort,
    order
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uuid** | **Array&lt;string&gt;** | 取得したいジョブのUUID | (optional) defaults to undefined|
| **measUuid** | **Array&lt;string&gt;** | 計測のUUID | (optional) defaults to undefined|
| **type** | **Array&lt;JobType&gt;** | - update   - 計測内の動画データのうち、新しくサーバーが受信した部分（HLSにまだ変換されていない部分）を     HLSに変換するジョブ。通常は計測実行中に行います。 - finalize   - 計測全体をサーバーに回収した後に、動画データ全体をHLSに変換するジョブ - delete   - 変換によって作成されたHLSデータを削除するジョブ。     このジョブを実行すると、HLSプレイリスト、セグメントファイル、     データベース内のHLSに関する情報が削除され、この動画のHLSによる再生はできなくなります。 | (optional) defaults to undefined|
| **status** | **Array&lt;JobStatus&gt;** | ジョブのステータス | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページ番号 | (optional) defaults to 1|
| **sort** | [**&#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'created_at'|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|


### Return type

**JobList**

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

# **getProjectJobs**
> JobList getProjectJobs()

HLSへの変換ジョブのリストを取得します。

### Example

```typescript
import {
    MediaJobsApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new MediaJobsApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)
let uuid: Array<string>; //取得したいジョブのUUID (optional) (default to undefined)
let measUuid: Array<string>; //計測のUUID (optional) (default to undefined)
let type: Array<JobType>; //- update   - 計測内の動画データのうち、新しくサーバーが受信した部分（HLSにまだ変換されていない部分）を     HLSに変換するジョブ。通常は計測実行中に行います。 - finalize   - 計測全体をサーバーに回収した後に、動画データ全体をHLSに変換するジョブ - delete   - 変換によって作成されたHLSデータを削除するジョブ。     このジョブを実行すると、HLSプレイリスト、セグメントファイル、     データベース内のHLSに関する情報が削除され、この動画のHLSによる再生はできなくなります。 (optional) (default to undefined)
let status: Array<JobStatus>; //ジョブのステータス (optional) (default to undefined)
let limit: number; //1回のリクエストで取得する件数 (optional) (default to undefined)
let page: number; //取得するページ番号 (optional) (default to 1)
let sort: 'created_at' | 'updated_at'; //並べ替えに使用するキー (optional) (default to 'created_at')
let order: 'asc' | 'desc'; //並べ替えの順序 (optional) (default to undefined)

const { status, data } = await apiInstance.getProjectJobs(
    projectUuid,
    uuid,
    measUuid,
    type,
    status,
    limit,
    page,
    sort,
    order
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|
| **uuid** | **Array&lt;string&gt;** | 取得したいジョブのUUID | (optional) defaults to undefined|
| **measUuid** | **Array&lt;string&gt;** | 計測のUUID | (optional) defaults to undefined|
| **type** | **Array&lt;JobType&gt;** | - update   - 計測内の動画データのうち、新しくサーバーが受信した部分（HLSにまだ変換されていない部分）を     HLSに変換するジョブ。通常は計測実行中に行います。 - finalize   - 計測全体をサーバーに回収した後に、動画データ全体をHLSに変換するジョブ - delete   - 変換によって作成されたHLSデータを削除するジョブ。     このジョブを実行すると、HLSプレイリスト、セグメントファイル、     データベース内のHLSに関する情報が削除され、この動画のHLSによる再生はできなくなります。 | (optional) defaults to undefined|
| **status** | **Array&lt;JobStatus&gt;** | ジョブのステータス | (optional) defaults to undefined|
| **limit** | [**number**] | 1回のリクエストで取得する件数 | (optional) defaults to undefined|
| **page** | [**number**] | 取得するページ番号 | (optional) defaults to 1|
| **sort** | [**&#39;created_at&#39; | &#39;updated_at&#39;**]**Array<&#39;created_at&#39; &#124; &#39;updated_at&#39;>** | 並べ替えに使用するキー | (optional) defaults to 'created_at'|
| **order** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | 並べ替えの順序 | (optional) defaults to undefined|


### Return type

**JobList**

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

