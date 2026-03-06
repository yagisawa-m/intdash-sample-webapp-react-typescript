# MeasurementUploadStatusGetResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | 計測アップロードのUUID | [default to undefined]
**meas_uuid** | **string** | 計測のUUID | [default to undefined]
**state** | **string** | 計測への変換ジョブのステータス | [default to undefined]
**message** | **string** | 計測への変換ジョブの結果 | [default to undefined]
**file_name** | **string** | 計測に変換する対象のファイル名。 同じ日に同じ名前のファイルがアップロードされた場合は、 ランダムな接頭辞が付与されます。 | [default to undefined]
**created_at** | **string** | 計測アップロードの作成日時 | [default to undefined]
**updated_at** | **string** | 計測アップロードの最終更新日時 | [default to undefined]

## Example

```typescript
import { MeasurementUploadStatusGetResponse } from './api';

const instance: MeasurementUploadStatusGetResponse = {
    uuid,
    meas_uuid,
    state,
    message,
    file_name,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
