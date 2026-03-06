# Video


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | 動画（video）のUUID | [default to undefined]
**measurement_uuid** | **string** | 計測のUUID | [default to undefined]
**measurement** | [**MediaMeasurement**](MediaMeasurement.md) |  | [optional] [default to undefined]
**edge_uuid** | **string** | エッジのUUID | [default to undefined]
**channel** | **number** | 計測のチャンネル。チャンネルが存在しない計測データ（iscp-v2）の場合は0が設定されます。 | [default to undefined]
**codec** | [**VideoCodecs**](VideoCodecs.md) |  | [default to undefined]
**source_data_type** | **string** | 通常、計測のdata_typeが用いられます。 | [default to undefined]
**source_data_name** | **string** | 通常、計測のdata_nameが用いられます。 | [default to undefined]
**offset_time** | **number** | 計測開始からのオフセット（マイクロ秒） | [default to undefined]
**duration** | **number** | 長さ（マイクロ秒） | [default to undefined]
**fps** | **number** | フレームレート（fps） | [default to undefined]
**width** | **number** | 動画の幅 | [default to undefined]
**height** | **number** | 動画の高さ | [default to undefined]
**status** | [**VideoStatus**](VideoStatus.md) |  | [default to undefined]
**hls** | [**Playlist**](Playlist.md) |  | [optional] [default to undefined]
**mp4s** | [**Array&lt;MP4&gt;**](MP4.md) | この動画を変換して作成されたMP4のリスト | [default to undefined]
**jpegs** | [**Array&lt;Jpeg&gt;**](Jpeg.md) | この動画を変換して作成されたJPEGのリスト | [default to undefined]
**created_at** | **string** | 作成された日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]

## Example

```typescript
import { Video } from './api';

const instance: Video = {
    uuid,
    measurement_uuid,
    measurement,
    edge_uuid,
    channel,
    codec,
    source_data_type,
    source_data_name,
    offset_time,
    duration,
    fps,
    width,
    height,
    status,
    hls,
    mp4s,
    jpegs,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
