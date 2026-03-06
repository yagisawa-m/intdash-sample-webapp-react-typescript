# AddGroupMemberRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_email_address** | **string** | ユーザーのメールアドレス。&#x60;user_uuid&#x60; といずれか必須です。&#x60;user_uuid&#x60; を優先します。 | [optional] [default to undefined]
**user_uuid** | **string** | ユーザーのUUID。&#x60;user_email_address&#x60; といずれか必須です。&#x60;user_uuid&#x60; を優先します。 | [optional] [default to undefined]
**role_uuids** | **Array&lt;string&gt;** | ユーザーに割り当てるロールのUUID。オーナーのロールUUIDは変更できません。 | [default to undefined]

## Example

```typescript
import { AddGroupMemberRequest } from './api';

const instance: AddGroupMemberRequest = {
    user_email_address,
    user_uuid,
    role_uuids,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
