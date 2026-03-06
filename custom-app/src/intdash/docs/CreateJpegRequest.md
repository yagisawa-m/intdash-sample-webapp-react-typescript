# CreateJpegRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**trim** | **boolean** | 時間範囲を指定してその部分のJPEGを作成する場合は &#x60;true&#x60; にします。 | [optional] [default to undefined]
**start_offset** | **number** | 計測開始からのオフセット（マイクロ秒）。trimがtrueの場合は必須です。 | [optional] [default to undefined]
**duration** | **number** | 長さ（マイクロ秒）。trimがtrueの場合は必須です。 | [optional] [default to undefined]
**fps** | **number** | フレームレート。値が省略された場合は、元のデータと同じフレームレートが使用されます。 | [optional] [default to undefined]
**quality** | [**JpegQuality**](JpegQuality.md) |  | [optional] [default to undefined]

## Example

```typescript
import { CreateJpegRequest } from './api';

const instance: CreateJpegRequest = {
    trim,
    start_offset,
    duration,
    fps,
    quality,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
