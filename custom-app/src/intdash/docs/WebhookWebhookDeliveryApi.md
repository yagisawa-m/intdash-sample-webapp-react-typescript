# WebhookWebhookDeliveryApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getWebhookDelivery**](#getwebhookdelivery) | **GET** /hook_deliveries/{hook_delivery_uuid} | Get Webhook Delivery|
|[**listWebhookDeliveries**](#listwebhookdeliveries) | **GET** /hook_deliveries | List Webhook Deliveries|
|[**listWebhookDeliveriesOfHook**](#listwebhookdeliveriesofhook) | **GET** /hooks/{hook_uuid}/hook_deliveries | List Webhook Deliveries of Hook|
|[**redeliverWebhook**](#redeliverwebhook) | **PUT** /hook_deliveries/{hook_delivery_uuid}/redeliver | Redeliver Webhook|

# **getWebhookDelivery**
> HookDelivery getWebhookDelivery()


### Example

```typescript
import {
    WebhookWebhookDeliveryApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookDeliveryApi(configuration);

let hookDeliveryUuid: string; // (default to undefined)

const { status, data } = await apiInstance.getWebhookDelivery(
    hookDeliveryUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

# **listWebhookDeliveries**
> HookDeliveries listWebhookDeliveries()


### Example

```typescript
import {
    WebhookWebhookDeliveryApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookDeliveryApi(configuration);

let hookDeliveryUuid: Array<string>; // (optional) (default to undefined)
let hookUuid: Array<string>; // (optional) (default to undefined)
let hookRedeliveredBy: Array<string>; // (optional) (default to undefined)
let isRedeliver: Array<boolean>; // (optional) (default to undefined)
let isTest: Array<boolean>; // (optional) (default to undefined)
let status: Array<HookDeliveryStatus>; // (optional) (default to undefined)
let page: number; // (optional) (default to 1)
let perPage: number; // (optional) (default to 100)

const { status, data } = await apiInstance.listWebhookDeliveries(
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

# **listWebhookDeliveriesOfHook**
> HookDeliveries listWebhookDeliveriesOfHook()


### Example

```typescript
import {
    WebhookWebhookDeliveryApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookDeliveryApi(configuration);

let hookUuid: string; // (default to undefined)
let hookDeliveryUuid: Array<string>; // (optional) (default to undefined)
let hookRedeliveredBy: Array<string>; // (optional) (default to undefined)
let isRedeliver: Array<boolean>; // (optional) (default to undefined)
let isTest: Array<boolean>; // (optional) (default to undefined)
let status: Array<HookDeliveryStatus>; // (optional) (default to undefined)
let page: number; // (optional) (default to 1)
let perPage: number; // (optional) (default to 100)

const { status, data } = await apiInstance.listWebhookDeliveriesOfHook(
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

# **redeliverWebhook**
> HookDelivery redeliverWebhook()


### Example

```typescript
import {
    WebhookWebhookDeliveryApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new WebhookWebhookDeliveryApi(configuration);

let hookDeliveryUuid: string; // (default to undefined)

const { status, data } = await apiInstance.redeliverWebhook(
    hookDeliveryUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

