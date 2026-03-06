# ErrorConverted


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **string** | エラーのタイプ。エラーのタイプが &#x60;unexpected&#x60; の場合は、直ちに処理が中断されます。 | [default to undefined]
**error_description** | **string** | エラーの説明 | [default to undefined]
**error_extra** | [**ErrorConvertedAllOfErrorExtra**](ErrorConvertedAllOfErrorExtra.md) |  | [default to undefined]

## Example

```typescript
import { ErrorConverted } from './api';

const instance: ErrorConverted = {
    error,
    error_description,
    error_extra,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
