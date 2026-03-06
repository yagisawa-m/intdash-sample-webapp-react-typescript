# BrokerISCPPersistersApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createPersisterConfigs**](#createpersisterconfigs) | **POST** /iscp/persister_configs | Create Persister Configs|
|[**deletePersisterConfig**](#deletepersisterconfig) | **DELETE** /iscp/persister_configs/{persister_config_uuid} | Delete Persister Config|
|[**disablePersisterConfig**](#disablepersisterconfig) | **PUT** /iscp/persister_configs/{persister_config_uuid}/disable | Disable Persister Config|
|[**enablePersisterConfig**](#enablepersisterconfig) | **PUT** /iscp/persister_configs/{persister_config_uuid}/enable | Enable Persister Config|
|[**getPersisterConfig**](#getpersisterconfig) | **GET** /iscp/persister_configs/{persister_config_uuid} | Get Persister Config|
|[**listPersisterConfigs**](#listpersisterconfigs) | **GET** /iscp/persister_configs | List Persister Configs|
|[**testPersisterConfigs**](#testpersisterconfigs) | **POST** /iscp/persister_configs/test | Test Persister Configs|
|[**testSavedPersisterConfig**](#testsavedpersisterconfig) | **POST** /iscp/persister_configs/{persister_config_uuid}/test | Test Saved Persister Config|
|[**updatePersisterConfig**](#updatepersisterconfig) | **PATCH** /iscp/persister_configs/{persister_config_uuid} | Update Persister Config|

# **createPersisterConfigs**
> PersisterConfig createPersisterConfigs()

永続化拡張モジュール設定を作成します。

### Example

```typescript
import {
    BrokerISCPPersistersApi,
    Configuration,
    PersisterConfigCreateRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPPersistersApi(configuration);

let persisterConfigCreateRequest: PersisterConfigCreateRequest; // (optional)

const { status, data } = await apiInstance.createPersisterConfigs(
    persisterConfigCreateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **persisterConfigCreateRequest** | **PersisterConfigCreateRequest**|  | |


### Return type

**PersisterConfig**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8, text/plain; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created |  -  |
|**409** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deletePersisterConfig**
> deletePersisterConfig()

永続化拡張モジュール設定を削除します。

### Example

```typescript
import {
    BrokerISCPPersistersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPPersistersApi(configuration);

let persisterConfigUuid: string; //永続化モジュール設定のUUID (default to undefined)

const { status, data } = await apiInstance.deletePersisterConfig(
    persisterConfigUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **persisterConfigUuid** | [**string**] | 永続化モジュール設定のUUID | defaults to undefined|


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

# **disablePersisterConfig**
> PersisterConfig disablePersisterConfig()

永続化拡張モジュールを有効化します。

### Example

```typescript
import {
    BrokerISCPPersistersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPPersistersApi(configuration);

let persisterConfigUuid: string; //永続化モジュール設定のUUID (default to undefined)

const { status, data } = await apiInstance.disablePersisterConfig(
    persisterConfigUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **persisterConfigUuid** | [**string**] | 永続化モジュール設定のUUID | defaults to undefined|


### Return type

**PersisterConfig**

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

# **enablePersisterConfig**
> PersisterConfig enablePersisterConfig()

永続化拡張モジュールを無効化します。

### Example

```typescript
import {
    BrokerISCPPersistersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPPersistersApi(configuration);

let persisterConfigUuid: string; //永続化モジュール設定のUUID (default to undefined)

const { status, data } = await apiInstance.enablePersisterConfig(
    persisterConfigUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **persisterConfigUuid** | [**string**] | 永続化モジュール設定のUUID | defaults to undefined|


### Return type

**PersisterConfig**

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

# **getPersisterConfig**
> PersisterConfig getPersisterConfig()

永続化拡張モジュール設定を取得します。

### Example

```typescript
import {
    BrokerISCPPersistersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPPersistersApi(configuration);

let persisterConfigUuid: string; //永続化モジュール設定のUUID (default to undefined)

const { status, data } = await apiInstance.getPersisterConfig(
    persisterConfigUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **persisterConfigUuid** | [**string**] | 永続化モジュール設定のUUID | defaults to undefined|


### Return type

**PersisterConfig**

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

# **listPersisterConfigs**
> PersisterConfigs listPersisterConfigs()

永続化拡張モジュール設定のリストを取得します。

### Example

```typescript
import {
    BrokerISCPPersistersApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPPersistersApi(configuration);

const { status, data } = await apiInstance.listPersisterConfigs();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**PersisterConfigs**

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

# **testPersisterConfigs**
> testPersisterConfigs()

永続化拡張モジュール設定をテストします。リソースは作成しません。

### Example

```typescript
import {
    BrokerISCPPersistersApi,
    Configuration,
    PersisterConfigCreateRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPPersistersApi(configuration);

let persisterConfigCreateRequest: PersisterConfigCreateRequest; // (optional)

const { status, data } = await apiInstance.testPersisterConfigs(
    persisterConfigCreateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **persisterConfigCreateRequest** | **PersisterConfigCreateRequest**|  | |


### Return type

void (empty response body)

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | Created |  -  |
|**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **testSavedPersisterConfig**
> testSavedPersisterConfig()

永続化拡張モジュール設定をテストします。

### Example

```typescript
import {
    BrokerISCPPersistersApi,
    Configuration,
    PersisterConfigUpdateRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPPersistersApi(configuration);

let persisterConfigUuid: string; //永続化モジュール設定のUUID (default to undefined)
let persisterConfigUpdateRequest: PersisterConfigUpdateRequest; // (optional)

const { status, data } = await apiInstance.testSavedPersisterConfig(
    persisterConfigUuid,
    persisterConfigUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **persisterConfigUpdateRequest** | **PersisterConfigUpdateRequest**|  | |
| **persisterConfigUuid** | [**string**] | 永続化モジュール設定のUUID | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | OK |  -  |
|**400** | Service Unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePersisterConfig**
> PersisterConfig updatePersisterConfig()

永続化拡張モジュール設定を更新します。

### Example

```typescript
import {
    BrokerISCPPersistersApi,
    Configuration,
    PersisterConfigUpdateRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPPersistersApi(configuration);

let persisterConfigUuid: string; //永続化モジュール設定のUUID (default to undefined)
let persisterConfigUpdateRequest: PersisterConfigUpdateRequest; // (optional)

const { status, data } = await apiInstance.updatePersisterConfig(
    persisterConfigUuid,
    persisterConfigUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **persisterConfigUpdateRequest** | **PersisterConfigUpdateRequest**|  | |
| **persisterConfigUuid** | [**string**] | 永続化モジュール設定のUUID | defaults to undefined|


### Return type

**PersisterConfig**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8, text/plain; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |
|**409** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

