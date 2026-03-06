# CheckHTTPAuthorizationRequest

アクセス制御可能かどうかを判定します。 ###  サブジェクト指定なしの場合 リクエストのスコープのみでアクセス判定を行います。 ###  サブジェクト指定ありの場合 パスを分類し、分類した結果によって処理が変わります。 ####  パスがプロジェクトコンテキストの場合 サブジェクトがプロジェクトに所属しているかを確認し、所属している場合は、サブジェクトがメンバーの場合そのプロジェクトにおけるスコープからアクセス判定を行います。サブジェクトがエッジの場合はリクエストのスコープからアクセス判定を行います。  ###  パスがグループコンテキストの場合 サブジェクトがプロジェクトに所属しているかを確認し、所属している場合は、そのプロジェクトにおけるスコープからアクセス判定を行います。 ###  パスがその他の場合 リクエストのスコープからアクセス判定を行います。

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subject** | **string** | 認証主体を指定します。通常アクセスユーザーのUUIDかアクセスエッジのUUIDを指定します。 | [optional] [default to undefined]
**scopes** | **Array&lt;string&gt;** | スコープを指定します。前述の説明を参照ください。 | [default to undefined]
**path** | **string** |  | [default to undefined]
**method** | **string** |  | [default to undefined]

## Example

```typescript
import { CheckHTTPAuthorizationRequest } from './api';

const instance: CheckHTTPAuthorizationRequest = {
    subject,
    scopes,
    path,
    method,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
