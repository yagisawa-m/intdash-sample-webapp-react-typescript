# Scope


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | スコープのUUID | [default to undefined]
**name** | **string** | スコープの名前 | [default to undefined]
**allowed_endpoints** | [**Array&lt;AllowedEndpoint&gt;**](AllowedEndpoint.md) | 許可されているエンドポイント | [default to undefined]
**allowed_iscp_messages** | [**Array&lt;AllowedISCPMessage&gt;**](AllowedISCPMessage.md) | 許可されているiSCPメッセージ | [default to undefined]
**denied_endpoints** | [**Array&lt;DeniedEndpoint&gt;**](DeniedEndpoint.md) | 拒否されているエンドポイント | [default to undefined]
**created_at** | **string** | 作成日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]

## Example

```typescript
import { Scope } from './api';

const instance: Scope = {
    uuid,
    name,
    allowed_endpoints,
    allowed_iscp_messages,
    denied_endpoints,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
