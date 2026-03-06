# HLS


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**edge_uuid** | **string** | エッジのUUID | [default to undefined]
**measurement_uuid** | **string** | 計測のUUID | [default to undefined]
**basetime** | **string** | 基準時刻 | [default to undefined]
**basetime_type** | **string** | 基準時刻タイプ | [default to undefined]
**playlist** | **string** | プレイリスト | [default to undefined]
**channel** | **number** | チャンネル | [default to undefined]
**offset_time** | **number** | 計測開始から動画の開始までのオフセット（マイクロ秒） | [default to undefined]
**duration** | **number** | 長さ（マイクロ秒） | [default to undefined]

## Example

```typescript
import { HLS } from './api';

const instance: HLS = {
    edge_uuid,
    measurement_uuid,
    basetime,
    basetime_type,
    playlist,
    channel,
    offset_time,
    duration,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
