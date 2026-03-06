# BrokerPage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**first** | **boolean** | &#x60;true&#x60; の場合、現在のページが最初のページです。 | [default to undefined]
**last** | **boolean** | &#x60;true&#x60; の場合、現在のページが最後のページです。 | [default to undefined]
**next** | **string** | 次のページのパス。現在のページが最後のページの場合は空文字列です。 | [default to undefined]
**previous** | **string** | 前のページのパス。現在のページが最初のページの場合は空文字列です。 | [default to undefined]
**total_count** | **number** | 取得対象の総件数 | [default to undefined]

## Example

```typescript
import { BrokerPage } from './api';

const instance: BrokerPage = {
    first,
    last,
    next,
    previous,
    total_count,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
