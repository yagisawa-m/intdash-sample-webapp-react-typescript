# HookCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | WebhookのURL | [default to undefined]
**secret** | **string** | シークレット。 ペイロードの署名に使用します。詳細は [Hooks Request](/#tag/model/Hooks-Request) を参照してください。 空の場合はサーバーが鍵を生成します。  | [optional] [default to undefined]
**edges_events** | **boolean** | エッジイベントを表します。 エッジイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;edge&#x60; を参照してください。  | [optional] [default to false]
**measurements_events** | **boolean** | 計測イベントを表します。 計測イベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;measurement&#x60; を参照してください。  | [optional] [default to false]
**users_events** | **boolean** | ユーザーイベントを表します。 ユーザーイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;user&#x60; を参照してください。  | [optional] [default to false]
**edge_connections_events** | **boolean** | エッジ接続イベントを表します。 エッジ接続イベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;edge_connection&#x60; を参照してください。  | [optional] [default to false]
**project_edges_events** | **boolean** | プロジェクトエッジのイベントを表します。 プロジェクトエッジイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;project_edge&#x60; を参照してください。  | [optional] [default to false]
**project_members_events** | **boolean** | プロジェクトメンバーのイベントを表します。 プロジェクトメンバーイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;project_member&#x60; を参照してください。  | [optional] [default to false]

## Example

```typescript
import { HookCreateRequest } from './api';

const instance: HookCreateRequest = {
    url,
    secret,
    edges_events,
    measurements_events,
    users_events,
    edge_connections_events,
    project_edges_events,
    project_members_events,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
