# DataPointGroupsInnerDataPointsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**string** | **string** | data_typeが &#x60;string&#x60; または, &#x60;string/&#x60; で始まるデータのときに使用します。ただし、&#x60;stirng/json&#x60; については &#x60;json&#x60; 属性名が優先されます。 | [optional] [default to undefined]
**json** | **object** | data_typeが &#x60;string/json&#x60; または, &#x60;string/json&#x60; で始まるデータのときに使用します。 &#x60;string/json&#x60; のときに本属性がない場合は &#x60;string&#x60; 属性を代わりに使用します。 | [optional] [default to undefined]
**bool** | **boolean** | data_typeが &#x60;bool&#x60; または, &#x60;bool/&#x60; で始まるデータのときに必須です。 | [optional] [default to undefined]
**float64** | **number** | data_typeが &#x60;float64&#x60; または, &#x60;float64/&#x60; で始まるデータのときに必須です。 | [optional] [default to undefined]
**float64_array** | **Array&lt;number&gt;** | data_typeが &#x60;float64_array&#x60; または, &#x60;float64_array/&#x60; で始まるデータのときに必須です。 | [optional] [default to undefined]
**int64** | **number** | data_typeが &#x60;int64&#x60; または, &#x60;int64/&#x60; で始まるデータのときに必須です。 | [optional] [default to undefined]
**int64_array** | **Array&lt;number&gt;** | data_typeが &#x60;int64_array&#x60; または, &#x60;int64_array/&#x60; で始まるデータのときに必須です。 | [optional] [default to undefined]
**vector_2d** | [**DataTypeVector2dVector2d**](DataTypeVector2dVector2d.md) |  | [optional] [default to undefined]
**vector_3d** | [**DataTypeVector3dVector3d**](DataTypeVector3dVector3d.md) |  | [optional] [default to undefined]
**vector_4d** | [**DataTypeVector4dVector4d**](DataTypeVector4dVector4d.md) |  | [optional] [default to undefined]
**payload** | **File** | data_typeが他の属性に該当しない場合に必須です。バイナリをBase64形式で指定します。 | [optional] [default to undefined]
**elapsed_time** | **number** | 経過時間[UnixNano秒]です。 | [default to undefined]

## Example

```typescript
import { DataPointGroupsInnerDataPointsInner } from './api';

const instance: DataPointGroupsInnerDataPointsInner = {
    string,
    json,
    bool,
    float64,
    float64_array,
    int64,
    int64_array,
    vector_2d,
    vector_3d,
    vector_4d,
    payload,
    elapsed_time,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
