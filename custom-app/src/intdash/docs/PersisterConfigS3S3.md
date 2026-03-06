# PersisterConfigS3S3


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**region** | **string** |  | [default to undefined]
**bucket_name** | **string** |  | [default to undefined]
**force_path_style** | **boolean** | s3のパススタイルのアドレスを強制します。 | [default to false]
**partition** | [**PersisterConfigAttributeS3Partition**](PersisterConfigAttributeS3Partition.md) |  | [default to undefined]
**endpoint** | **string** | minioなどS3互換のオブジェクトストレージを使用するときに使用します。S3の場合は不要です。 | [default to undefined]

## Example

```typescript
import { PersisterConfigS3S3 } from './api';

const instance: PersisterConfigS3S3 = {
    region,
    bucket_name,
    force_path_style,
    partition,
    endpoint,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
