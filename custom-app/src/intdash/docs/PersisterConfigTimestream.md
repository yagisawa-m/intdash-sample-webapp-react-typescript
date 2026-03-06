# PersisterConfigTimestream


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [default to undefined]
**name** | **string** |  | [default to undefined]
**type** | [**PersisterConfigAttributeType**](PersisterConfigAttributeType.md) |  | [default to undefined]
**timestream** | [**PersisterConfigTimestreamTimestream**](PersisterConfigTimestreamTimestream.md) |  | [default to undefined]
**format** | [**PersisterConfigAttributeTimestreamFormat**](PersisterConfigAttributeTimestreamFormat.md) |  | [default to undefined]
**is_shared_global** | **boolean** | アプリケーション全体で共有されているかどうか。この値が &#x60;true&#x60; の場合、編集や削除はできません。 | [default to undefined]
**data_filters** | [**Array&lt;PersisterConfigDataFilter&gt;**](PersisterConfigDataFilter.md) |  | [default to undefined]
**nodes** | [**Array&lt;PersisterConfigNode&gt;**](PersisterConfigNode.md) | 対象ノードIDを指定します。空の場合は全てのノードを対象とします。本属性と &#x60;ignore_nodes&#x60; 属性の両方に同じノードIDを指定した場合は、&#x60;ignore_nodes&#x60; 属性が優先されます。 | [default to undefined]
**ignore_data_filters** | [**Array&lt;PersisterConfigIgnoreDataFilter&gt;**](PersisterConfigIgnoreDataFilter.md) |  | [optional] [default to undefined]
**ignore_nodes** | [**Array&lt;PersisterConfigIgnoreNode&gt;**](PersisterConfigIgnoreNode.md) | 場外するノードIDを指定します。 本属性と &#x60;nodes&#x60; 属性の両方に同じノードIDを指定した場合は、本属性が優先されます。 | [default to undefined]
**created_at** | **string** | 作成日時 | [default to undefined]
**updated_at** | **string** | 更新日時 | [default to undefined]

## Example

```typescript
import { PersisterConfigTimestream } from './api';

const instance: PersisterConfigTimestream = {
    uuid,
    name,
    type,
    timestream,
    format,
    is_shared_global,
    data_filters,
    nodes,
    ignore_data_filters,
    ignore_nodes,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
