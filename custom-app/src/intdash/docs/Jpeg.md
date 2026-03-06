# Jpeg


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | JPEGのUUID | [default to undefined]
**start_offset** | **number** | 計測開始からのオフセット（マイクロ秒） | [default to undefined]
**duration** | **number** | 長さ（マイクロ秒） | [default to undefined]
**trimmed** | **boolean** | 指定された時間範囲のみを抽出したものである場合は &#x60;true&#x60; 。 | [default to undefined]
**fps** | **number** | フレームレート（fps） | [default to undefined]
**quality** | [**JpegQuality**](JpegQuality.md) |  | [default to undefined]
**status** | [**JpegStatus**](JpegStatus.md) |  | [default to undefined]
**created_at** | **string** | 作成された日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]

## Example

```typescript
import { Jpeg } from './api';

const instance: Jpeg = {
    uuid,
    start_offset,
    duration,
    trimmed,
    fps,
    quality,
    status,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
