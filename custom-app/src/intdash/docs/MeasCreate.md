# MeasCreate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | 計測の名前 | [optional] [default to undefined]
**description** | **string** | 計測の説明 | [optional] [default to undefined]
**basetime** | **string** | 計測の基準時刻（計測が開始された時刻） | [default to undefined]
**basetime_type** | [**MeasurementBaseTimeType**](MeasurementBaseTimeType.md) | 計測の基準時刻タイプ。この属性に加えて、 &#x60;basetime_priority&#x60; と 任意の &#x60;basetime_name&#x60; も同時に設定することを推奨します。 &#x60;undefined&#x60; を指定した場合は、接頭辞 &#x60;basetime_&#x60; 及び &#x60;basetime&#x60; の属性は無視される事にご注意ください。 | [default to undefined]
**basetime_priority** | **number** | 基準時刻の優先度 | [optional] [default to undefined]
**basetime_name** | **string** | 基準時刻の名前 | [optional] [default to undefined]
**basetime_elapsed_time** | **number** | 基準時刻を受信した基準時刻からの経過時間（ナノ秒）。 | [optional] [default to undefined]
**edge_uuid** | **string** | この計測に関連付けられたエッジのUUID | [default to undefined]
**_protected** | **boolean** | &#x60;true&#x60; の場合、計測は保護されます。保護されている計測は削除できません。 | [default to undefined]

## Example

```typescript
import { MeasCreate } from './api';

const instance: MeasCreate = {
    name,
    description,
    basetime,
    basetime_type,
    basetime_priority,
    basetime_name,
    basetime_elapsed_time,
    edge_uuid,
    _protected,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
