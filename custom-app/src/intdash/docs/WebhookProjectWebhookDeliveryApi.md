# WebhookProjectWebhookDeliveryApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getProjectWebhookDelivery**](#getprojectwebhookdelivery) | **GET** /projects/{project_uuid}/hook_deliveries/{hook_delivery_uuid} | Get Project Webhook Delivery|
|[**listProjectWebhookDeliveries**](#listprojectwebhookdeliveries) | **GET** /projects/{project_uuid}/hook_deliveries | List Project Webhook Deliveries|
|[**listProjectWebhookDeliveriesOfHook**](#listprojectwebhookdeliveriesofhook) | **GET** /projects/{project_uuid}/hooks/{hook_uuid}/hook_deliveries | List Project Webhook Deliveries of Hook|
|[**redeliverProjectWebhook**](#redeliverprojectwebhook) | **PUT** /projects/{project_uuid}/hook_deliveries/{hook_delivery_uuid}/redeliver | Redeliver Project Webhook|

# **getProjectWebhookDelivery**
> HookDelivery getProjectWebhookDelivery()


### Example

```typescript
import {
    WebhookProjectWebhookDeliveryApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookDeliveryApi(configuration);

let projectUuid: string; // (default to undefined)
let hookDeliveryUuid: string; // (default to undefined)

const { status, data } = await apiInstance.getProjectWebhookDelivery(
    projectUuid,
    hookDeliveryUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] |  | defaults to undefined|
| **hookDeliveryUuid** | [**string**] |  | defaults to undefined|


### Return type

**HookDelivery**

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

# **listProjectWebhookDeliveries**
> HookDeliveries listProjectWebhookDeliveries()


### Example

```typescript
import {
    WebhookProjectWebhookDeliveryApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookDeliveryApi(configuration);

let projectUuid: string; // (default to undefined)
let hookDeliveryUuid: Array<string>; // (optional) (default to undefined)
let hookUuid: Array<string>; // (optional) (default to undefined)
let hookRedeliveredBy: Array<string>; // (optional) (default to undefined)
let isRedeliver: Array<boolean>; // (optional) (default to undefined)
let isTest: Array<boolean>; // (optional) (default to undefined)
let status: Array<HookDeliveryStatus>; // (optional) (default to undefined)
let page: number; // (optional) (default to 1)
let perPage: number; // (optional) (default to 100)

const { status, data } = await apiInstance.listProjectWebhookDeliveries(
    projectUuid,
    hookDeliveryUuid,
    hookUuid,
    hookRedeliveredBy,
    isRedeliver,
    isTest,
    status,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] |  | defaults to undefined|
| **hookDeliveryUuid** | **Array&lt;string&gt;** |  | (optional) defaults to undefined|
| **hookUuid** | **Array&lt;string&gt;** |  | (optional) defaults to undefined|
| **hookRedeliveredBy** | **Array&lt;string&gt;** |  | (optional) defaults to undefined|
| **isRedeliver** | **Array&lt;boolean&gt;** |  | (optional) defaults to undefined|
| **isTest** | **Array&lt;boolean&gt;** |  | (optional) defaults to undefined|
| **status** | **Array&lt;HookDeliveryStatus&gt;** |  | (optional) defaults to undefined|
| **page** | [**number**] |  | (optional) defaults to 1|
| **perPage** | [**number**] |  | (optional) defaults to 100|


### Return type

**HookDeliveries**

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

# **listProjectWebhookDeliveriesOfHook**
> HookDeliveries listProjectWebhookDeliveriesOfHook()


### Example

```typescript
import {
    WebhookProjectWebhookDeliveryApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookDeliveryApi(configuration);

let projectUuid: string; // (default to undefined)
let hookUuid: string; // (default to undefined)
let hookDeliveryUuid: Array<string>; // (optional) (default to undefined)
let hookRedeliveredBy: Array<string>; // (optional) (default to undefined)
let isRedeliver: Array<boolean>; // (optional) (default to undefined)
let isTest: Array<boolean>; // (optional) (default to undefined)
let status: Array<HookDeliveryStatus>; // (optional) (default to undefined)
let page: number; // (optional) (default to 1)
let perPage: number; // (optional) (default to 100)

const { status, data } = await apiInstance.listProjectWebhookDeliveriesOfHook(
    projectUuid,
    hookUuid,
    hookDeliveryUuid,
    hookRedeliveredBy,
    isRedeliver,
    isTest,
    status,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] |  | defaults to undefined|
| **hookUuid** | [**string**] |  | defaults to undefined|
| **hookDeliveryUuid** | **Array&lt;string&gt;** |  | (optional) defaults to undefined|
| **hookRedeliveredBy** | **Array&lt;string&gt;** |  | (optional) defaults to undefined|
| **isRedeliver** | **Array&lt;boolean&gt;** |  | (optional) defaults to undefined|
| **isTest** | **Array&lt;boolean&gt;** |  | (optional) defaults to undefined|
| **status** | **Array&lt;HookDeliveryStatus&gt;** |  | (optional) defaults to undefined|
| **page** | [**number**] |  | (optional) defaults to 1|
| **perPage** | [**number**] |  | (optional) defaults to 100|


### Return type

**HookDeliveries**

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

# **redeliverProjectWebhook**
> HookDelivery redeliverProjectWebhook()


### Example

```typescript
import {
    WebhookProjectWebhookDeliveryApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookProjectWebhookDeliveryApi(configuration);

let projectUuid: string; // (default to undefined)
let hookDeliveryUuid: string; // (default to undefined)

const { status, data } = await apiInstance.redeliverProjectWebhook(
    projectUuid,
    hookDeliveryUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] |  | defaults to undefined|
| **hookDeliveryUuid** | [**string**] |  | defaults to undefined|


### Return type

**HookDelivery**

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

