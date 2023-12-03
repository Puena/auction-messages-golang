# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [proto/product.proto](#proto_product-proto)
    - [GetProductByIdRequest](#auction-GetProductByIdRequest)
    - [GetProductsByNameRequest](#auction-GetProductsByNameRequest)
    - [ProductCreateRequest](#auction-ProductCreateRequest)
    - [ProductCreatedResponse](#auction-ProductCreatedResponse)
    - [ProductDeleteRequest](#auction-ProductDeleteRequest)
    - [ProductDeletedResponse](#auction-ProductDeletedResponse)
    - [ProductErrorResponse](#auction-ProductErrorResponse)
    - [ProductResponse](#auction-ProductResponse)
    - [ProductUpdateRequest](#auction-ProductUpdateRequest)
    - [ProductUpdatedResponse](#auction-ProductUpdatedResponse)
  
- [proto/user.proto](#proto_user-proto)
    - [EventUserData](#auction-EventUserData)
    - [EventUserError](#auction-EventUserError)
    - [EventUserRevoked](#auction-EventUserRevoked)
    - [EventUserUpdated](#auction-EventUserUpdated)
    - [EventUserVerified](#auction-EventUserVerified)
    - [User](#auction-User)
    - [UserId](#auction-UserId)
    - [UserMessageError](#auction-UserMessageError)
  
- [Scalar Value Types](#scalar-value-types)



<a name="proto_product-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## proto/product.proto



<a name="auction-GetProductByIdRequest"></a>

### GetProductByIdRequest
GetProductByIdRequest represent event message to get product by id.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) |  |  |






<a name="auction-GetProductsByNameRequest"></a>

### GetProductsByNameRequest
GetProductsByNameRequest represent event message to get products by name.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) | repeated |  |






<a name="auction-ProductCreateRequest"></a>

### ProductCreateRequest
ProductCreateRequest represent event message to create products.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |
| media | [string](#string) | repeated |  |
| description | [string](#string) |  |  |






<a name="auction-ProductCreatedResponse"></a>

### ProductCreatedResponse
ProductCreatedResponse represent event message after create product.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| product | [ProductResponse](#auction-ProductResponse) |  |  |






<a name="auction-ProductDeleteRequest"></a>

### ProductDeleteRequest
ProductDeleteRequest represent event message to delete product.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) |  |  |






<a name="auction-ProductDeletedResponse"></a>

### ProductDeletedResponse
ProductDeletedResponse represent event message after delete product.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| product | [ProductResponse](#auction-ProductResponse) |  |  |






<a name="auction-ProductErrorResponse"></a>

### ProductErrorResponse
ProductErrorResponse represent event message of product error.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [string](#string) |  |  |
| message | [string](#string) |  |  |
| details | [string](#string) |  |  |






<a name="auction-ProductResponse"></a>

### ProductResponse
ProductResponse represent message data of product.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) |  |  |
| name | [string](#string) |  |  |
| media | [string](#string) | repeated |  |
| description | [string](#string) |  |  |
| created_by | [string](#string) |  |  |
| created_at | [string](#string) |  |  |






<a name="auction-ProductUpdateRequest"></a>

### ProductUpdateRequest
ProductUpdateRequest represent event message to update product.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) |  |  |
| media | [string](#string) | repeated |  |
| description | [string](#string) | optional |  |






<a name="auction-ProductUpdatedResponse"></a>

### ProductUpdatedResponse
ProductUpdatedResponse represent event message after update product.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| product | [ProductResponse](#auction-ProductResponse) |  |  |





 

 

 

 



<a name="proto_user-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## proto/user.proto



<a name="auction-EventUserData"></a>

### EventUserData
EventUserData message represent event after user data request.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| data | [User](#auction-User) |  |  |






<a name="auction-EventUserError"></a>

### EventUserError
EventUserError message represent event after user message error.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| data | [UserMessageError](#auction-UserMessageError) |  |  |






<a name="auction-EventUserRevoked"></a>

### EventUserRevoked
EventUserRevoked message represent event after user revocation.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| data | [UserId](#auction-UserId) |  |  |






<a name="auction-EventUserUpdated"></a>

### EventUserUpdated
EventUserUpdated message represent event after user update.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| data | [User](#auction-User) |  |  |






<a name="auction-EventUserVerified"></a>

### EventUserVerified
EventUserVerified message represent event after user verification.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| data | [UserId](#auction-UserId) |  |  |






<a name="auction-User"></a>

### User
User messages represent user data.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) |  |  |
| name | [string](#string) |  |  |
| email | [string](#string) |  |  |
| phone | [string](#string) |  |  |
| photo | [string](#string) |  |  |
| createdAt | [string](#string) |  |  |
| lastLogin | [string](#string) |  |  |
| disabled | [bool](#bool) |  |  |






<a name="auction-UserId"></a>

### UserId
UserID message represent user id data.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) |  |  |






<a name="auction-UserMessageError"></a>

### UserMessageError
UserMessageError message represent data of user message error.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| msgId | [string](#string) |  |  |
| user | [User](#auction-User) |  |  |
| userId | [UserId](#auction-UserId) |  |  |
| msgCreatedAt | [string](#string) |  |  |





 

 

 

 



## Scalar Value Types

| .proto Type | Notes | C++ | Java | Python | Go | C# | PHP | Ruby |
| ----------- | ----- | --- | ---- | ------ | -- | -- | --- | ---- |
| <a name="double" /> double |  | double | double | float | float64 | double | float | Float |
| <a name="float" /> float |  | float | float | float | float32 | float | float | Float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum or Fixnum (as required) |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="bool" /> bool |  | bool | boolean | boolean | bool | bool | boolean | TrueClass/FalseClass |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode | string | string | string | String (UTF-8) |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str | []byte | ByteString | string | String (ASCII-8BIT) |

