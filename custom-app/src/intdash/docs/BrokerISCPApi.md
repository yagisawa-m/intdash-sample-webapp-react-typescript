# BrokerISCPApi

All URIs are relative to *https://example.intdash.jp/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**connectISCPV1**](#connectiscpv1) | **GET** /v1/ws/measurements | Connect ISCPv1|
|[**connectISCPV2**](#connectiscpv2) | **GET** /iscp/connect | Connect ISCPv2|
|[**connectProjectISCPV1**](#connectprojectiscpv1) | **GET** /v1/projects/{project_uuid}/ws/measurements | Connect Project ISCPv1|
|[**issueISCPTicket**](#issueiscpticket) | **POST** /iscp/tickets | Issue ISCP Ticket|

# **connectISCPV1**
> connectISCPV1()

（Deprecated。このエンドポイントでなく `/projects/00000000-0000-0000-0000-000000000000/ws/measurements` を使用してください）  iSCP v1（WebSocket上でリアルタイムデータを送受信するintdash独自プロトコル）の使用を開始するためのエンドポイントです。    このリクエストを送ることで、プロトコルがWebSocketに切り替えられ、iSCP v1を使用できます。   \"permessage-deflate\" (RFC 7692) が使用できます。    iSCP v1の詳細については、別ドキュメント [詳説iSCP 1.0](https://docs.intdash.jp/manual/iscp1-essentials/latest/ja/iscp1-essentials-ja.pdf) を参照してください。    「詳説iSCP 1.0」に記載されいていない事項ついては、 [アプトポッド](https://www.aptpod.co.jp/contact/) にお問い合わせください。

### Example

```typescript
import {
    BrokerISCPApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPApi(configuration);

const { status, data } = await apiInstance.connectISCPV1();
```

### Parameters
This endpoint does not have any parameters.


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
|**101** | Switching Protocols |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **connectISCPV2**
> connectISCPV2()

iSCP v2（WebSocket上でリアルタイムデータを送受信するintdash独自プロトコル）の使用を開始するためのエンドポイントです。 このリクエストを送ることで、プロトコルがWebSocketに切り替えられ、iSCP v2を使用できます。  iSCP v2の詳細については、 [アプトポッド](https://www.aptpod.co.jp/contact/) にお問い合わせください。

### Example

```typescript
import {
    BrokerISCPApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPApi(configuration);

const { status, data } = await apiInstance.connectISCPV2();
```

### Parameters
This endpoint does not have any parameters.


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
|**101** | Switching Protocols |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **connectProjectISCPV1**
> connectProjectISCPV1()

iSCP v1（WebSocket上でリアルタイムデータを送受信するintdash独自プロトコル）の使用を開始するためのエンドポイントです。  このリクエストを送ることで、プロトコルがWebSocketに切り替えられ、iSCP v1を使用できます。 \"permessage-deflate\" (RFC 7692) が使用できます。  iSCP v1の詳細については、別ドキュメント [詳説iSCP 1.0](https://docs.intdash.jp/manual/iscp1-essentials/latest/ja/iscp1-essentials-ja.pdf) を参照してください。  「詳説iSCP 1.0」に記載されいていない事項ついては、 [アプトポッド](https://www.aptpod.co.jp/contact/) にお問い合わせください。

### Example

```typescript
import {
    BrokerISCPApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPApi(configuration);

let projectUuid: string; //プロジェクトのUUID (default to undefined)

const { status, data } = await apiInstance.connectProjectISCPV1(
    projectUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectUuid** | [**string**] | プロジェクトのUUID | defaults to undefined|


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
|**101** | Switching Protocols |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **issueISCPTicket**
> ISCPTicket issueISCPTicket()

iSCPの認証チケットを発行します。  iSCPの認証チケットは、iSCPv2の接続リクエスト時の拡張用アクセストークンとして使用することができます。 また、認証チケットは有効期限内で一回のみ使用することができます。 一度使用した認証チケットは有効期限に関わらず使用することはできません。

### Example

```typescript
import {
    BrokerISCPApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new BrokerISCPApi(configuration);

const { status, data } = await apiInstance.issueISCPTicket();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**ISCPTicket**

### Authorization

[IntdashToken](../README.md#IntdashToken), [OAuth2TokenInCookie](../README.md#OAuth2TokenInCookie), [OAuth2TokenInHeader](../README.md#OAuth2TokenInHeader)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

