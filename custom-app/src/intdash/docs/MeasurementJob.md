# MeasurementJob


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | ジョブのUUID | [default to undefined]
**meas_uuid** | **string** | 計測のUUID | [default to undefined]
**measurement** | [**Measurement**](Measurement.md) |  | [default to undefined]
**status** | [**MeasurementJobStatus**](MeasurementJobStatus.md) |  | [default to undefined]
**message** | **string** | ジョブの結果を表すメッセージ。 ジョブのステータスが &#x60;failed&#x60; の場合、メッセージが以下の形式で表示されます。  &#x60;&lt;row_number&gt;:&lt;column_number&gt;:&lt;column_name&gt;:&lt;cell_value&gt;:&lt;error_message&gt;&#x60;  行番号や列番号が不明の場合は &#x60;0&#x60; が出力されます。 * ex.1 &#x60;2:1:time:1539263580:A time must be after the base_time\\: BaseTime&#x3D;2018-10-11 13\\:13\\:03 +0000 UTC&#x60; * ex.2 &#x60;4:0:::Wrong number of fields&#x60; * ex.3 &#x60;0:0:::Unexpected Error&#x60;  &#x60;:&#x60; と &#x60;\\&#x60; はエスケープされ、 &#x60;\\:&#x60; と &#x60;\\\\&#x60; として出力されます。 | [default to undefined]
**file_name** | **string** | ジョブの対象のファイル名。 同じ日に同じ名前のファイルがアップロードされた場合は、ランダムな接頭辞が付与されます。 | [default to undefined]
**created_at** | **string** | ジョブの作成日時 | [default to undefined]
**updated_at** | **string** | ジョブの最終更新日時 | [default to undefined]

## Example

```typescript
import { MeasurementJob } from './api';

const instance: MeasurementJob = {
    uuid,
    meas_uuid,
    measurement,
    status,
    message,
    file_name,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
