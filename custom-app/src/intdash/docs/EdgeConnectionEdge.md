# EdgeConnectionEdge


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | エッジのUUID | [default to undefined]
**name** | **string** | エッジの名前 | [default to undefined]
**nickname** | **string** | エッジの表示名 | [default to undefined]
**description** | **string** | エッジの説明 | [default to undefined]
**disabled** | **boolean** | * &#x60;true&#x60; : このエッジは無効化されています。 * &#x60;false&#x60; : このエッジは有効です。 | [default to undefined]
**internal** | **boolean** | * &#x60;true&#x60; : このエッジは内部エッジ（システム内部で使用される特別なエッジ）です。   このエッジの変更や削除はできません。 * &#x60;false&#x60; : このエッジは内部エッジではありません。 | [default to undefined]
**_protected** | **boolean** | * &#x60;true&#x60; : このエッジは保護されています。このエッジの変更や削除はできません。 * &#x60;false&#x60; : このエッジは保護されていません。 | [default to undefined]
**type** | **string** | エッジのタイプ | [default to undefined]
**last_login_at** | **string** | エッジが最後にログインした日時 | [default to undefined]
**last_lived_at** | **string** | サーバーがこのエッジ接続を確認できた最後の日時。 エッジとサーバーがWebSocketで接続されている間、この値は数秒おきに最新の日時に更新されます。 WebSocketが切断されると、それ以上更新されなくなります。 更新は数秒おきであるため、WebSocketが切断された場合に その切断の時刻が正確に記録されるわけではありません。 | [default to undefined]
**created_at** | **string** | エッジが作成された日時 | [default to undefined]
**updated_at** | **string** | エッジの最終更新日時 | [default to undefined]

## Example

```typescript
import { EdgeConnectionEdge } from './api';

const instance: EdgeConnectionEdge = {
    uuid,
    name,
    nickname,
    description,
    disabled,
    internal,
    _protected,
    type,
    last_login_at,
    last_lived_at,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
