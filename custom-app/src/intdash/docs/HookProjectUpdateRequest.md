# HookProjectUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | WebhookのURL | [optional] [default to undefined]
**secret** | **string** | シークレット。 ペイロードの署名に使用します。詳細は [Hooks Request](/#tag/model/Hooks-Request) を参照してください。 空の場合はサーバーが鍵を生成します。  | [optional] [default to undefined]
**measurements_event** | **boolean** | 計測イベントを表します。 計測イベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;measurement&#x60; を参照してください。  | [optional] [default to false]
**edge_connections_event** | **boolean** | エッジ接続イベントを表します。 エッジ接続イベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;edge_connection&#x60; を参照してください。  | [optional] [default to false]
**project_edges_event** | **boolean** | プロジェクトエッジのイベントを表します。 プロジェクトエッジイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;project_edge&#x60; を参照してください。  | [optional] [default to false]
**project_members_event** | **boolean** | プロジェクトメンバーのイベントを表します。 プロジェクトメンバーイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;project_member&#x60; を参照してください。  | [optional] [default to false]

## Example

```typescript
import { HookProjectUpdateRequest } from './api';

const instance: HookProjectUpdateRequest = {
    url,
    secret,
    measurements_event,
    edge_connections_event,
    project_edges_event,
    project_members_event,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
