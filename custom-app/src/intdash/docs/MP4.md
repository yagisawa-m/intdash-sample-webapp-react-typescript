# MP4


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | MP4のUUID | [default to undefined]
**start_offset** | **number** | 動画の開始時刻からのオフセット（マイクロ秒） | [default to undefined]
**duration** | **number** | 長さ（マイクロ秒） | [default to undefined]
**trimmed** | **boolean** | 指定された時間範囲のみを抽出したものである場合は &#x60;true&#x60; 。 | [default to undefined]
**file_path** | **string** | メディアファイルのパス | [optional] [default to undefined]
**status** | [**MP4Status**](MP4Status.md) |  | [default to undefined]
**created_at** | **string** | 作成された日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]

## Example

```typescript
import { MP4 } from './api';

const instance: MP4 = {
    uuid,
    start_offset,
    duration,
    trimmed,
    file_path,
    status,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
