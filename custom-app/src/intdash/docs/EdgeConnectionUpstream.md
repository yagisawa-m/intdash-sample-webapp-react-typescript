# EdgeConnectionUpstream


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stream_id** | **number** | アップストリームのストリームID | [default to undefined]
**measurement_uuid** | **string** | アップストリームの計測UUID | [default to undefined]
**src_edge_uuid** | **string** | アップストリームの送信元エッジUUID | [default to undefined]
**resend** | **boolean** | * &#x60;true&#x60; : このアップストリームは再送です。 * &#x60;false&#x60; : このアップストリームは再送ではありません。 | [default to undefined]
**store** | **boolean** | * &#x60;true&#x60; : このアップストリームで送信されたデータポイントはサーバーに保存されます。 * &#x60;false&#x60; : このアップストリームで送信されたデータポイントはサーバーに保存されません。 | [default to undefined]
**last_received_at** | **string** | アップストリームで最後にデータポイントが送信された日時。 実際の最後のデータポイント送信よりも最大で10秒後の値となる場合があります。 | [default to undefined]
**received_close_request** | **boolean** | * &#x60;true&#x60; : このアップストリームについてのclose requestを受信済みです。 * &#x60;false&#x60; : このアップストリームについてのclose requestは受信していません。 | [default to undefined]
**created_at** | **string** | アップストリームが作成された日時 | [default to undefined]
**updated_at** | **string** | アップストリームの最終更新日時 | [default to undefined]

## Example

```typescript
import { EdgeConnectionUpstream } from './api';

const instance: EdgeConnectionUpstream = {
    stream_id,
    measurement_uuid,
    src_edge_uuid,
    resend,
    store,
    last_received_at,
    received_close_request,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
