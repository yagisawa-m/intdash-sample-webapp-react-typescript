# PersisterConfigCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**type** | [**PersisterConfigAttributeType**](PersisterConfigAttributeType.md) |  | [default to undefined]
**s3** | [**PersisterConfigAttributeS3**](PersisterConfigAttributeS3.md) |  | [optional] [default to undefined]
**format** | [**PersisterConfigAttributeTimestreamFormat**](PersisterConfigAttributeTimestreamFormat.md) |  | [default to undefined]
**data_filters** | [**Array&lt;PersisterConfigDataFilter&gt;**](PersisterConfigDataFilter.md) |  | [optional] [default to undefined]
**ignore_data_filters** | [**Array&lt;PersisterConfigIgnoreDataFilter&gt;**](PersisterConfigIgnoreDataFilter.md) |  | [optional] [default to undefined]
**nodes** | [**Array&lt;PersisterConfigNode&gt;**](PersisterConfigNode.md) | 対象ノードIDを指定します。空の場合は全てのノードを対象とします。本属性と &#x60;ignore_nodes&#x60; 属性の両方に同じノードIDを指定した場合は、&#x60;ignore_nodes&#x60; 属性が優先されます。 | [optional] [default to undefined]
**ignore_nodes** | [**Array&lt;PersisterConfigIgnoreNode&gt;**](PersisterConfigIgnoreNode.md) | 場外するノードIDを指定します。 本属性と &#x60;nodes&#x60; 属性の両方に同じノードIDを指定した場合は、本属性が優先されます。 | [optional] [default to undefined]
**http** | [**PersisterConfigCreateRequestAttributeHTTP**](PersisterConfigCreateRequestAttributeHTTP.md) |  | [optional] [default to undefined]
**timestream** | [**PersisterConfigAttributeTimestream**](PersisterConfigAttributeTimestream.md) |  | [optional] [default to undefined]

## Example

```typescript
import { PersisterConfigCreateRequest } from './api';

const instance: PersisterConfigCreateRequest = {
    name,
    description,
    type,
    s3,
    format,
    data_filters,
    ignore_data_filters,
    nodes,
    ignore_nodes,
    http,
    timestream,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
