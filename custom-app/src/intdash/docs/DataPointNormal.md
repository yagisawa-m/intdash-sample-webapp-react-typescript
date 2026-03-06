# DataPointNormal

改行で区切られたJSON文字列です。

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**time** | [**DataPointTime**](DataPointTime.md) |  | [default to undefined]
**measurement_uuid** | **string** | このデータポイントが含まれる計測のUUID | [default to undefined]
**created_at** | **string** | このデータポイントが作成された日時 | [default to undefined]
**data_type** | **string** | データタイプ | [default to undefined]
**data_id** | **string** | データID | [default to undefined]
**data** | **object** | データのペイロード。ペイロードのJSON表現はデータタイプによって異なります。 [詳説iSCP 1.0](https://docs.intdash.jp/manual/iscp1-essentials/latest/ja/iscp1-essentials-ja.pdf) の「付録: データタイプとペイロードの定義」を参照してください。 iscpv1に当てはまらない場合、下記のフォーマットで固定となります。  &#x60;&#x60;&#x60; {   \&quot;d\&quot;: \&quot;データ本体のBase64表記\&quot; } &#x60;&#x60;&#x60; | [default to undefined]

## Example

```typescript
import { DataPointNormal } from './api';

const instance: DataPointNormal = {
    time,
    measurement_uuid,
    created_at,
    data_type,
    data_id,
    data,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
