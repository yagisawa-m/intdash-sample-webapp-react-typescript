# JSONWebKey

See [JSON Web Key (JWK)](https://datatracker.ietf.org/doc/html/rfc7517)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**use** | **string** |  | [optional] [default to undefined]
**kty** | **string** |  | [optional] [default to undefined]
**kid** | **string** |  | [optional] [default to undefined]
**crv** | **string** |  | [optional] [default to undefined]
**alg** | **string** |  | [optional] [default to undefined]
**k** | **string** |  | [optional] [default to undefined]
**x** | **string** |  | [optional] [default to undefined]
**y** | **string** |  | [optional] [default to undefined]
**n** | **string** |  | [optional] [default to undefined]
**e** | **string** |  | [optional] [default to undefined]
**d** | **string** |  | [optional] [default to undefined]
**p** | **string** |  | [optional] [default to undefined]
**q** | **string** |  | [optional] [default to undefined]
**dp** | **string** |  | [optional] [default to undefined]
**dq** | **string** |  | [optional] [default to undefined]
**qi** | **string** |  | [optional] [default to undefined]
**x5c** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**x5u** | **string** |  | [optional] [default to undefined]
**x5t** | **string** |  | [optional] [default to undefined]
**x5tS256** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { JSONWebKey } from './api';

const instance: JSONWebKey = {
    use,
    kty,
    kid,
    crv,
    alg,
    k,
    x,
    y,
    n,
    e,
    d,
    p,
    q,
    dp,
    dq,
    qi,
    x5c,
    x5u,
    x5t,
    x5tS256,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
