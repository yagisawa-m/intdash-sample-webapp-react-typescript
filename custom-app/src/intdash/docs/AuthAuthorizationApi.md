# AuthAuthorizationApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**checkHTTPAuthorization**](#checkhttpauthorization) | **POST** /auth/authorize/http | Check HTTP Authorization|
|[**checkMeHTTPAuthorization**](#checkmehttpauthorization) | **POST** /auth/users/me/authorize/http | Check Me HTTP Authorization|

# **checkHTTPAuthorization**
> CheckAuthorizationResponse checkHTTPAuthorization()


### Example

```typescript
import {
    AuthAuthorizationApi,
    Configuration,
    CheckHTTPAuthorizationRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthAuthorizationApi(configuration);

let checkHTTPAuthorizationRequest: CheckHTTPAuthorizationRequest; // (optional)

const { status, data } = await apiInstance.checkHTTPAuthorization(
    checkHTTPAuthorizationRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **checkHTTPAuthorizationRequest** | **CheckHTTPAuthorizationRequest**|  | |


### Return type

**CheckAuthorizationResponse**

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

# **checkMeHTTPAuthorization**
> CheckAuthorizationResponse checkMeHTTPAuthorization()


### Example

```typescript
import {
    AuthAuthorizationApi,
    Configuration,
    CheckMeHTTPAuthorizationRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new AuthAuthorizationApi(configuration);

let checkMeHTTPAuthorizationRequest: CheckMeHTTPAuthorizationRequest; // (optional)

const { status, data } = await apiInstance.checkMeHTTPAuthorization(
    checkMeHTTPAuthorizationRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **checkMeHTTPAuthorizationRequest** | **CheckMeHTTPAuthorizationRequest**|  | |


### Return type

**CheckAuthorizationResponse**

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

