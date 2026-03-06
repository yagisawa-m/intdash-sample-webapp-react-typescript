# EdgeConnectionItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | エッジ接続のUUID | [default to undefined]
**last_lived_at** | **string** | サーバーがこのエッジ接続を確認できた最後の日時。 エッジとサーバーがWebSocketで接続されている間、この値は数秒おきに最新の日時に更新されます。 WebSocketが切断されると、それ以上更新されなくなります。 更新は数秒おきであるため、WebSocketが切断された場合に その切断の時刻が正確に記録されるわけではありません。 | [default to undefined]
**edge** | [**EdgeConnectionEdge**](EdgeConnectionEdge.md) |  | [default to undefined]
**created_at** | **string** | エッジ接続が作成された日時 | [default to undefined]
**updated_at** | **string** | エッジ接続の最終更新日時 | [default to undefined]

## Example

```typescript
import { EdgeConnectionItem } from './api';

const instance: EdgeConnectionItem = {
    uuid,
    last_lived_at,
    edge,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
