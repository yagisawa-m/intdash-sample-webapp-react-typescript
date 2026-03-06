# HookPage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**next** | **boolean** | 次のページがあるかどうか | [default to undefined]
**prev** | **boolean** | 前のページがあるかどうか | [default to undefined]
**next_page** | **number** | 取得対象の次のページ番号。&#x60;next&#x60; がtrueの場合のみ表示。 | [optional] [default to undefined]
**prev_page** | **number** | 取得対象の前のページ番号。&#x60;next&#x60; がtrueの場合のみ表示。 | [optional] [default to undefined]
**total_page** | **number** | 取得対象の総ページ数 | [default to undefined]
**total_count** | **number** | 取得対象の総件数 | [default to undefined]

## Example

```typescript
import { HookPage } from './api';

const instance: HookPage = {
    next,
    prev,
    next_page,
    prev_page,
    total_page,
    total_count,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
