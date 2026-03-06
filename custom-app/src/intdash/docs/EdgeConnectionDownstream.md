# EdgeConnectionDownstream


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stream_id** | **number** | ダウンストリームのストリームID | [default to undefined]
**src_edge_uuid** | **string** | ダウンストリームの送信元エッジUUID | [default to undefined]
**dst_edge_uuid** | **string** | ダウンストリームの宛先エッジUUID | [default to undefined]
**last_received_at** | **string** | ダウンストリームで最後にデータポイントが受信された日時。 実際の最後のデータポイントの受信よりも最大で10秒後の値となる場合があります。 | [default to undefined]
**received_close_request** | **boolean** | * &#x60;true&#x60; : このダウンストリームについてのclose requestを受信済みです。 * &#x60;false&#x60; : このダウンストリームについてのclose requestを受信していません。 | [default to undefined]
**created_at** | **string** | ダウンストリームが作成された日時 | [default to undefined]
**updated_at** | **string** | ダウンストリームの最終更新日時 | [default to undefined]

## Example

```typescript
import { EdgeConnectionDownstream } from './api';

const instance: EdgeConnectionDownstream = {
    stream_id,
    src_edge_uuid,
    dst_edge_uuid,
    last_received_at,
    received_close_request,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
