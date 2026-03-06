# WebhookWebhookApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createWebhook**](#createwebhook) | **POST** /hooks | Create Webhook|
|[**deleteWebhook**](#deletewebhook) | **DELETE** /hooks/{hook_uuid} | Delete Webhook|
|[**disableWebhook**](#disablewebhook) | **PUT** /hooks/{hook_uuid}/disable | Disable Webhook|
|[**enableWebhook**](#enablewebhook) | **PUT** /hooks/{hook_uuid}/enable | Enable Webhook|
|[**getWebhook**](#getwebhook) | **GET** /hooks/{hook_uuid} | Get Webhook|
|[**listWebhooks**](#listwebhooks) | **GET** /hooks | List Webhooks|
|[**testWebhook**](#testwebhook) | **PUT** /hooks/{hook_uuid}/test | Test Webhook|
|[**updateWebhook**](#updatewebhook) | **PATCH** /hooks/{hook_uuid} | Update Webhook|

# **createWebhook**
> HookCreateResponse createWebhook()


### Example

```typescript
import {
    WebhookWebhookApi,
    Configuration,
    HookCreateRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookApi(configuration);

let hookCreateRequest: HookCreateRequest; // (optional)

const { status, data } = await apiInstance.createWebhook(
    hookCreateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hookCreateRequest** | **HookCreateRequest**|  | |


### Return type

**HookCreateResponse**

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

# **deleteWebhook**
> deleteWebhook()


### Example

```typescript
import {
    WebhookWebhookApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookApi(configuration);

let hookUuid: string; // (default to undefined)

const { status, data } = await apiInstance.deleteWebhook(
    hookUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

# **disableWebhook**
> Hook disableWebhook()


### Example

```typescript
import {
    WebhookWebhookApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookApi(configuration);

let hookUuid: string; // (default to undefined)

const { status, data } = await apiInstance.disableWebhook(
    hookUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hookUuid** | [**string**] |  | defaults to undefined|


### Return type

**Hook**

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

# **enableWebhook**
> Hook enableWebhook()


### Example

```typescript
import {
    WebhookWebhookApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookApi(configuration);

let hookUuid: string; // (default to undefined)

const { status, data } = await apiInstance.enableWebhook(
    hookUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hookUuid** | [**string**] |  | defaults to undefined|


### Return type

**Hook**

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

# **getWebhook**
> Hook getWebhook()


### Example

```typescript
import {
    WebhookWebhookApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookApi(configuration);

let hookUuid: string; // (default to undefined)

const { status, data } = await apiInstance.getWebhook(
    hookUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hookUuid** | [**string**] |  | defaults to undefined|


### Return type

**Hook**

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

# **listWebhooks**
> Hooks listWebhooks()


### Example

```typescript
import {
    WebhookWebhookApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookApi(configuration);

let hookUuid: Array<string>; // (optional) (default to undefined)
let enabled: Array<boolean>; // (optional) (default to undefined)
let page: number; // (optional) (default to 1)
let perPage: number; // (optional) (default to 100)

const { status, data } = await apiInstance.listWebhooks(
    hookUuid,
    enabled,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hookUuid** | **Array&lt;string&gt;** |  | (optional) defaults to undefined|
| **enabled** | **Array&lt;boolean&gt;** |  | (optional) defaults to undefined|
| **page** | [**number**] |  | (optional) defaults to 1|
| **perPage** | [**number**] |  | (optional) defaults to 100|


### Return type

**Hooks**

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

# **testWebhook**
> HookDelivery testWebhook()


### Example

```typescript
import {
    WebhookWebhookApi,
    Configuration,
    HookTestRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookApi(configuration);

let hookUuid: string; // (default to undefined)
let hookTestRequest: HookTestRequest; // (optional)

const { status, data } = await apiInstance.testWebhook(
    hookUuid,
    hookTestRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hookTestRequest** | **HookTestRequest**|  | |
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

# **updateWebhook**
> Hook updateWebhook()


### Example

```typescript
import {
    WebhookWebhookApi,
    Configuration,
    HookUpdateRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookApi(configuration);

let hookUuid: string; // (default to undefined)
let hookUpdateRequest: HookUpdateRequest; // (optional)

const { status, data } = await apiInstance.updateWebhook(
    hookUuid,
    hookUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hookUpdateRequest** | **HookUpdateRequest**|  | |
| **hookUuid** | [**string**] |  | defaults to undefined|


### Return type

**Hook**

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

