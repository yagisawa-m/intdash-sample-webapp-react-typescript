# PersisterConfigAttributeS3


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**region** | **string** |  | [default to undefined]
**bucket_name** | **string** |  | [default to undefined]
**force_path_style** | **boolean** | s3のパススタイルのアドレスを強制します。 | [optional] [default to false]
**partition** | [**PersisterConfigAttributeS3Partition**](PersisterConfigAttributeS3Partition.md) |  | [default to undefined]
**endpoint** | **string** | minioなどS3互換のオブジェクトストレージを使用するときに使用します。S3の場合は不要です。 | [optional] [default to undefined]
**access_key_id** | **string** | AWSのアクセスキーIDです。 | [optional] [default to undefined]
**secret_access_key** | **string** | AWSのシークレットアクセスキーです。 | [optional] [default to undefined]

## Example

```typescript
import { PersisterConfigAttributeS3 } from './api';

const instance: PersisterConfigAttributeS3 = {
    region,
    bucket_name,
    force_path_style,
    partition,
    endpoint,
    access_key_id,
    secret_access_key,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
