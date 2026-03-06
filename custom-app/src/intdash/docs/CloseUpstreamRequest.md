# CloseUpstreamRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**close_session** | **boolean** | セッションをクローズします。 intdashではセッションは計測と紐づいており、&#x60;close_session&#x3D;true&#x60; とした場合は紐づく計測は &#x60;complete&#x60; 状態に遷移させます。 永続化フラグが &#x60;false&#x60; であるストリームに対しては &#x60;close_session&#x60; の属性はtrue/falseに関わらず無視されます。 | [default to false]

## Example

```typescript
import { CloseUpstreamRequest } from './api';

const instance: CloseUpstreamRequest = {
    close_session,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
