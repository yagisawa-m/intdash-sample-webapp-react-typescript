# CheckPasswordResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**valid** | **boolean** | &#x60;true&#x60; の場合、ポリシーに適合しています。 | [default to undefined]
**errors** | [**Array&lt;CheckPasswordResultErrorsInner&gt;**](CheckPasswordResultErrorsInner.md) | ポリシー不適合の場合、その詳細 | [optional] [default to undefined]

## Example

```typescript
import { CheckPasswordResult } from './api';

const instance: CheckPasswordResult = {
    valid,
    errors,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
