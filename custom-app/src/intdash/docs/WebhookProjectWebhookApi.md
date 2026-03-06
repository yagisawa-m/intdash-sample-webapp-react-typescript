# WebhookProjectWebhookApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createProjectWebhook**](#createprojectwebhook) | **POST** /projects/{project_uuid}/hooks | Create Project Webhook|
|[**deleteProjectWebhook**](#deleteprojectwebhook) | **DELETE** /projects/{project_uuid}/hooks/{hook_uuid} | Delete Project Webhook|
|[**disableProjectWebhook**](#disableprojectwebhook) | **PUT** /projects/{project_uuid}/hooks/{hook_uuid}/disable | Disable Project Webhook|
|[**enableProjectWebhook**](#enableprojectwebhook) | **PUT** /projects/{project_uuid}/hooks/{hook_uuid}/enable | Enable Project Webhook|
|[**getProjectWebhook**](#getprojectwebhook) | **GET** /projects/{project_uuid}/hooks/{hook_uuid} | Get Project Webhook|
|[**listProjectWebhooks**](#listprojectwebhooks) | **GET** /projects/{project_uuid}/hooks | List Project Webhooks|
|[**testProjectWebhook**](#testprojectwebhook) | **PUT** /projects/{project_uuid}/hooks/{hook_uuid}/test | Test Project Webhook|
|[**updateProjectWebhook**](#updateprojectwebhook) | **PATCH** /projects/{project_uuid}/hooks/{hook_uuid} | Update Project Webhook|

# **createProjectWebhook**
> HookProjectCreateResponse createProjectWebhook()


### Example

```typescript
import {
    WebhookProjectWebhookApi,
    Configuration,
    HookProjectCreateRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookApi(configuration);

let projectUuid: string; // (default to undefined)
let hookProjectCreateRequest: HookProjectCreateRequest; // (optional)

const { status, data } = await apiInstance.createProjectWebhook(
    projectUuid,
    hookProjectCreateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hookProjectCreateRequest** | **HookProjectCreateRequest**|  | |
| **projectUuid** | [**string**] |  | defaults to undefined|


### Return type

**HookProjectCreateResponse**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json; charset:utf-8
 - **Accept**: application/json; charset:utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteProjectWebhook**
> deleteProjectWebhook()


### Example

```typescript
import {
    WebhookProjectWebhookApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookApi(configuration);

let projectUuid: string; // (default to undefined)
let hookUuid: string; // (default to undefined)

const { status, data } = await apiInstance.deleteProjectWebhook(
    projectUuid,
    hookUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] |  | defaults to undefined|
| **hookUuid** | [**string**] |  | defaults to undefined|


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

# **disableProjectWebhook**
> HookProject disableProjectWebhook()


### Example

```typescript
import {
    WebhookProjectWebhookApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookApi(configuration);

let projectUuid: string; // (default to undefined)
let hookUuid: string; // (default to undefined)

const { status, data } = await apiInstance.disableProjectWebhook(
    projectUuid,
    hookUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] |  | defaults to undefined|
| **hookUuid** | [**string**] |  | defaults to undefined|


### Return type

**HookProject**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset:utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enableProjectWebhook**
> HookProject enableProjectWebhook()


### Example

```typescript
import {
    WebhookProjectWebhookApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookApi(configuration);

let projectUuid: string; // (default to undefined)
let hookUuid: string; // (default to undefined)

const { status, data } = await apiInstance.enableProjectWebhook(
    projectUuid,
    hookUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] |  | defaults to undefined|
| **hookUuid** | [**string**] |  | defaults to undefined|


### Return type

**HookProject**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset:utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProjectWebhook**
> HookProject getProjectWebhook()


### Example

```typescript
import {
    WebhookProjectWebhookApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookApi(configuration);

let projectUuid: string; // (default to undefined)
let hookUuid: string; // (default to undefined)

const { status, data } = await apiInstance.getProjectWebhook(
    projectUuid,
    hookUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] |  | defaults to undefined|
| **hookUuid** | [**string**] |  | defaults to undefined|


### Return type

**HookProject**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset:utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listProjectWebhooks**
> HookProjects listProjectWebhooks()


### Example

```typescript
import {
    WebhookProjectWebhookApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookApi(configuration);

let projectUuid: string; // (default to undefined)
let hookUuid: Array<string>; // (optional) (default to undefined)
let enabled: Array<boolean>; // (optional) (default to undefined)
let page: number; // (optional) (default to 1)
let perPage: number; // (optional) (default to 100)

const { status, data } = await apiInstance.listProjectWebhooks(
    projectUuid,
    hookUuid,
    enabled,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] |  | defaults to undefined|
| **hookUuid** | **Array&lt;string&gt;** |  | (optional) defaults to undefined|
| **enabled** | **Array&lt;boolean&gt;** |  | (optional) defaults to undefined|
| **page** | [**number**] |  | (optional) defaults to 1|
| **perPage** | [**number**] |  | (optional) defaults to 100|


### Return type

**HookProjects**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset:utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **testProjectWebhook**
> HookDelivery testProjectWebhook()


### Example

```typescript
import {
    WebhookProjectWebhookApi,
    Configuration,
    HookTestRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookApi(configuration);

let projectUuid: string; // (default to undefined)
let hookUuid: string; // (default to undefined)
let hookTestRequest: HookTestRequest; // (optional)

const { status, data } = await apiInstance.testProjectWebhook(
    projectUuid,
    hookUuid,
    hookTestRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hookTestRequest** | **HookTestRequest**|  | |
| **projectUuid** | [**string**] |  | defaults to undefined|
| **hookUuid** | [**string**] |  | defaults to undefined|


### Return type

**HookDelivery**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json; charset:utf-8
 - **Accept**: application/json; charset:utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProjectWebhook**
> HookProject updateProjectWebhook()


### Example

```typescript
import {
    WebhookProjectWebhookApi,
    Configuration,
    HookProjectUpdateRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookApi(configuration);

let projectUuid: string; // (default to undefined)
let hookUuid: string; // (default to undefined)
let hookProjectUpdateRequest: HookProjectUpdateRequest; // (optional)

const { status, data } = await apiInstance.updateProjectWebhook(
    projectUuid,
    hookUuid,
    hookProjectUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hookProjectUpdateRequest** | **HookProjectUpdateRequest**|  | |
| **projectUuid** | [**string**] |  | defaults to undefined|
| **hookUuid** | [**string**] |  | defaults to undefined|


### Return type

**HookProject**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: application/json; charset:utf-8
 - **Accept**: application/json; charset:utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

