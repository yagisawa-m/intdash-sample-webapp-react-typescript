# CreateMP4Request


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**trimmed** | **boolean** | 時間範囲を指定してその部分のMP4を作成する場合は &#x60;true&#x60; にします。 | [optional] [default to undefined]
**start_offset** | **number** | 動画の開始時刻からのオフセット（マイクロ秒）。trimmedがtrueの場合は必須です。 | [optional] [default to undefined]
**duration** | **number** | 長さ（マイクロ秒）。trimmedがtrueの場合は必須です。 | [optional] [default to undefined]

## Example

```typescript
import { CreateMP4Request } from './api';

const instance: CreateMP4Request = {
    trimmed,
    start_offset,
    duration,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
