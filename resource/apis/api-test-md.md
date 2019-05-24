# Api Test Import

## Edgehog Public API, Devices

### About

| Url | Version | Contact | Terms of Service | License |
| :--- | :--- | :--- | :--- | :--- |
|  | 2019-03-14 |  |  |  |

### Schemes

| Scheme |
| :--- |


## Endpoints

## auth/login

## POST

Requests a JWT token

### Expected Response Types

| Response | Reason |
| :--- | :--- |
|  |  |
| 200 | OK |
| 401 | Login failed |
| 429 | Too many login attempts |

### Parameters

| Name | In | Description | Required? | Type |
| :--- | :--- | :--- | :--- | :--- |


### Content Types Produced

| Produces |
| :--- |
| None |

### Content Types Consumed

| Consumes |
| :--- |
| None |

### Security

| Id | Scopes |
| :--- | :--- |
| None | None |

## auth/logout

## POST

Invalidates a JWT token

### Expected Response Types

| Response | Reason |
| :--- | :--- |
|  |  |
| 200 | OK |

### Parameters

| Name | In | Description | Required? | Type |
| :--- | :--- | :--- | :--- | :--- |


### Content Types Produced

| Produces |
| :--- |
| None |

### Content Types Consumed

| Consumes |
| :--- |
| None |

### Security

| Id | Scopes |
| :--- | :--- |
|  |  |

## auth/refresh

## POST

Refreshes a JWT token

### Expected Response Types

| Response | Reason |
| :--- | :--- |
|  |  |
| 200 | OK |

### Parameters

| Name | In | Description | Required? | Type |
| :--- | :--- | :--- | :--- | :--- |


### Content Types Produced

| Produces |
| :--- |
| None |

### Content Types Consumed

| Consumes |
| :--- |
| None |

### Security

| Id | Scopes |
| :--- | :--- |
|  |  |

## management/devices

## GET

Gets a list of registered devices Requires `devices.list` permission.

### Expected Response Types

| Response | Reason |
| :--- | :--- |
| 200 | OK |
| 4XX | Invalid request |

### Parameters

| Name | In | Description | Required? | Type |
| :--- | :--- | :--- | :--- | :--- |
| $top | query | maximum number of records to retrieve | false | integer |
| $skip | query | skip this number of records \(e.g. for pagination\) | false | integer |

### Content Types Produced

| Produces |
| :--- |
| None |

### Content Types Consumed

| Consumes |
| :--- |
| None |

### Security

| Id | Scopes |
| :--- | :--- |
| None | None |

## POST

Registers a device Requires `devices.create` permission.

### Expected Response Types

| Response | Reason |
| :--- | :--- |
| 200 | OK |
| 4XX | Invalid request |

### Parameters

| Name | In | Description | Required? | Type |
| :--- | :--- | :--- | :--- | :--- |


### Content Types Produced

| Produces |
| :--- |
| None |

### Content Types Consumed

| Consumes |
| :--- |
| None |

### Security

| Id | Scopes |
| :--- | :--- |
| None | None |

## management/devices/{id}

## GET

Reads a device Requires `devices.read` permission.

### Expected Response Types

| Response | Reason |
| :--- | :--- |
| 200 | OK |
| 4XX | Invalid request |

### Parameters

| Name | In | Description | Required? | Type |
| :--- | :--- | :--- | :--- | :--- |
| id | path | Device ID | true | integer |

### Content Types Produced

| Produces |
| :--- |
| None |

### Content Types Consumed

| Consumes |
| :--- |
| None |

### Security

| Id | Scopes |
| :--- | :--- |
| None | None |

## PUT

Updates a device Requires `devices.update` permission.

### Expected Response Types

| Response | Reason |
| :--- | :--- |
| 200 | OK |
| 4XX | Invalid request |

### Parameters

| Name | In | Description | Required? | Type |
| :--- | :--- | :--- | :--- | :--- |
| id | path | Device ID | true | integer |

### Content Types Produced

| Produces |
| :--- |
| None |

### Content Types Consumed

| Consumes |
| :--- |
| None |

### Security

| Id | Scopes |
| :--- | :--- |
| None | None |

## management/devices/{id}/export-sensors

## GET

Reads sensors observations in the specified time interval Requires `devices.read` permission.

### Expected Response Types

| Response | Reason |
| :--- | :--- |
| 200 | OK |
| 4XX | Invalid request |

### Parameters

| Name | In | Description | Required? | Type |
| :--- | :--- | :--- | :--- | :--- |
| id | path | Device ID | true | integer |
| from | query | Interval start date time, in user format | true | string |
| to | query | Interval stop date time, in user format | true | string |
| format | query | Export format | true | string |

### Content Types Produced

| Produces |
| :--- |
| None |

### Content Types Consumed

| Consumes |
| :--- |
| None |

### Security

| Id | Scopes |
| :--- | :--- |
| None | None |

## management/devices/{id}/sensors

## GET

Reads the last known sensor values Requires `devices.read` permission. If the device has never transmitted telemetry data \(eg. the shadow is empty\), it returns an empty array.

### Expected Response Types

| Response | Reason |
| :--- | :--- |
| 200 | OK |
| 4XX | Invalid request |

### Parameters

| Name | In | Description | Required? | Type |
| :--- | :--- | :--- | :--- | :--- |
| id | path | Device ID | true | integer |

### Content Types Produced

| Produces |
| :--- |
| None |

### Content Types Consumed

| Consumes |
| :--- |
| None |

### Security

| Id | Scopes |
| :--- | :--- |
| None | None |

## Security Definitions

| Id | Type | Flow | Authorization Url | Name | In | Scopes |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |


| Scope | Description |
| :--- | :--- |


## Definitions

## Additional Resources

