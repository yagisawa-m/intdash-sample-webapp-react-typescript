# Edge


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | エッジのUUID | [default to undefined]
**name** | **string** | エッジの名前 | [default to undefined]
**nickname** | **string** | エッジの表示名 | [default to undefined]
**description** | **string** | エッジの説明 | [default to undefined]
**owner** | [**EdgeOwner**](EdgeOwner.md) |  | [optional] [default to undefined]
**created_at** | **string** | 作成日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]
**client_secret** | **string** | エッジのクライアントシークレット | [optional] [default to undefined]

## Example

```typescript
import { Edge } from './api';

const instance: Edge = {
    uuid,
    name,
    nickname,
    description,
    owner,
    created_at,
    updated_at,
    client_secret,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
