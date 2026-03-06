# MeasurementSectionGetResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**serial_number** | **number** | 計測セクションのシリアルナンバー | [default to undefined]
**processed** | **boolean** | &#x60;true&#x60; の場合、計測セクションは処理済みです。 | [default to undefined]
**created_at** | **string** | 計測セクションの作成日時。 &#x60;processed&#x60; が &#x60;false&#x60; の場合は、この属性はありません。 | [default to undefined]
**updated_at** | **string** | 計測セクションの最終更新日時。 &#x60;processed&#x60; が &#x60;false&#x60; の場合は、この属性はありません。 | [default to undefined]

## Example

```typescript
import { MeasurementSectionGetResponse } from './api';

const instance: MeasurementSectionGetResponse = {
    serial_number,
    processed,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
