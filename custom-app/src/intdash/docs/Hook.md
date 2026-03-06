# Hook


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [default to undefined]
**url** | **string** | WebhookのURL | [default to undefined]
**edges_event** | **boolean** | エッジイベントを表します。 エッジイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;edge&#x60; を参照してください。  | [default to false]
**measurements_event** | **boolean** | 計測イベントを表します。 計測イベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;measurement&#x60; を参照してください。  | [default to false]
**users_event** | **boolean** | ユーザーイベントを表します。 ユーザーイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;user&#x60; を参照してください。  | [default to false]
**edge_connections_event** | **boolean** | エッジ接続イベントを表します。 エッジ接続イベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;edge_connection&#x60; を参照してください。  | [default to false]
**project_edges_event** | **boolean** | プロジェクトエッジのイベントを表します。 プロジェクトエッジイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;project_edge&#x60; を参照してください。  | [default to false]
**project_members_event** | **boolean** | プロジェクトメンバーのイベントを表します。 プロジェクトメンバーイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;project_member&#x60; を参照してください。  | [default to false]
**tenants_event** | **boolean** | テナントイベントを表します。 テナントイベントは [Hooks Request](/#tag/model/Hooks-Request) の &#x60;resource_type&#x60; が &#x60;tenant&#x60; を参照してください。 この値はデフォルトテナントのみに作成される共有グローバルフックに対して設定可能です。  | [optional] [default to false]
**is_shared_global** | **boolean** | 共有グローバルフックかどうか。共有グローバルフックである場合は削除や編集はできません。 | [default to undefined]
**enabled** | **boolean** | Webhookが有効かどうか | [default to undefined]
**created_at** | **string** | 作成時刻 | [default to undefined]
**updated_at** | **string** | 更新時刻 | [default to undefined]

## Example

```typescript
import { Hook } from './api';

const instance: Hook = {
    uuid,
    url,
    edges_event,
    measurements_event,
    users_event,
    edge_connections_event,
    project_edges_event,
    project_members_event,
    tenants_event,
    is_shared_global,
    enabled,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
