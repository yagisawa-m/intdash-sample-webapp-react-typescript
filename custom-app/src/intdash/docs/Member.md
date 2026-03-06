# Member


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_uuid** | **string** | メンバーのユーザーUUID | [default to undefined]
**name** | **string** | メンバーの名前 | [default to undefined]
**emails** | [**Array&lt;UserEmail&gt;**](UserEmail.md) |  | [default to undefined]
**inherited_role_uuids** | **Array&lt;string&gt;** | 親グループから継承されたメンバーのロールUUID | [default to undefined]
**role_uuids** | **Array&lt;string&gt;** | メンバーのロールUUID | [default to undefined]
**is_owner** | **boolean** | &#x60;true&#x60; の場合、このメンバーはオーナーです。 | [default to undefined]
**created_at** | **string** | 作成日時 | [default to undefined]
**updated_at** | **string** | 最終更新日時 | [default to undefined]

## Example

```typescript
import { Member } from './api';

const instance: Member = {
    user_uuid,
    name,
    emails,
    inherited_role_uuids,
    role_uuids,
    is_owner,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
