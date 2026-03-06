# MeasurementMarkerBase


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | 計測マーカーのUUID | [default to undefined]
**name** | **string** | 計測マーカーの名前 | [default to undefined]
**description** | **string** | 計測マーカーの説明 | [default to undefined]
**type** | **string** | 計測マーカーのタイプ - &#x60;point&#x60; : ポイントマーカー - &#x60;range&#x60; : 範囲マーカー | [default to undefined]
**tag** | **object** | 計測マーカーに付与されたタグ | [default to undefined]
**created_at** | **string** | 計測マーカーの作成日時 | [default to undefined]
**created_by** | **string** | 計測マーカー作成者 | [default to undefined]
**updated_at** | **string** | 計測マーカーの最終更新日時 | [default to undefined]
**updated_by** | **string** | 計測マーカーの最終更新者 | [default to undefined]

## Example

```typescript
import { MeasurementMarkerBase } from './api';

const instance: MeasurementMarkerBase = {
    uuid,
    name,
    description,
    type,
    tag,
    created_at,
    created_by,
    updated_at,
    updated_by,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
