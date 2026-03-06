# HookProjectCreateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [default to undefined]
**url** | **string** | WebhookのURL | [default to undefined]
**measurements_event** | **boolean** | 計測イベントを表します。 計測イベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;measurement&#x60; を参照してください。  | [default to false]
**edge_connections_event** | **boolean** | エッジ接続イベントを表します。 エッジ接続イベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;edge_connection&#x60; を参照してください。  | [default to false]
**project_edges_event** | **boolean** | プロジェクトエッジのイベントを表します。 プロジェクトエッジイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;project_edge&#x60; を参照してください。  | [default to false]
**project_members_event** | **boolean** | プロジェクトメンバーのイベントを表します。 プロジェクトメンバーイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;project_member&#x60; を参照してください。  | [default to false]
**enabled** | **boolean** | Webhookが有効かどうか | [default to undefined]
**created_at** | **string** | 作成時刻 | [default to undefined]
**updated_at** | **string** | 更新時刻 | [default to undefined]
**secret** | **string** | シークレット。リクエストでシークレットの指定がなかったときに表示します。  | [optional] [default to undefined]

## Example

```typescript
import { HookProjectCreateResponse } from './api';

const instance: HookProjectCreateResponse = {
    uuid,
    url,
    measurements_event,
    edge_connections_event,
    project_edges_event,
    project_members_event,
    enabled,
    created_at,
    updated_at,
    secret,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
