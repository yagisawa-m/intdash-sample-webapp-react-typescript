# MeasurementMarkerPutRequestRange


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | 計測マーカーの名前 | [optional] [default to undefined]
**description** | **string** | 計測マーカーの説明 | [optional] [default to undefined]
**type** | **string** | 計測マーカーのタイプ - &#x60;point&#x60; : ポイントマーカー - &#x60;range&#x60; : 範囲マーカー | [optional] [default to undefined]
**tag** | **object** | この計測マーカーに付与するタグ。タグはキーと値からなるペア（いずれもstring）で設定します。 複数のタグを一度に設定することができます。 値の中にオブジェクトを入れる（ネストする）ことはできません。 &#x60;&#x60;&#x60; // Not good {   \&quot;tagkey\&quot; : {     \&quot;nestKey\&quot;: \&quot;not allowed\&quot;   } } &#x60;&#x60;&#x60;  &#x60;&#x60;&#x60; // OK {   \&quot;tagkey1\&quot; : \&quot;ok1\&quot;,   \&quot;tagkey2\&quot; : \&quot;ok2\&quot; } &#x60;&#x60;&#x60; | [optional] [default to undefined]
**detail** | [**MeasurementMarkerDetailRange**](MeasurementMarkerDetailRange.md) |  | [optional] [default to undefined]

## Example

```typescript
import { MeasurementMarkerPutRequestRange } from './api';

const instance: MeasurementMarkerPutRequestRange = {
    name,
    description,
    type,
    tag,
    detail,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
