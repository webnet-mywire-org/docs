# Logout Device (GET) - WN API DOCS

Documentation of logout device API - https://api.webnet.mywire.org/auth/device (GET)

## REQUEST

| **HTTP Parametars** 	| **Value**                                         |
|-----------------------|---------------------------------------------------|
| Method:           	| GET                                               |
| URL:              	| https://api.webnet.mywire.org/auth/logout-device  |
| Body:             	| JSON                                              |

| **Body Parameters** | **Type** | **Required** | **Description**       |
|---------------------|----------|--------------|-----------------------|
| device_key          | string   | YES          | The user's device key |

## RESPONSE - Code: 200 (OK)

| **Parameters** | **Type** | **Description**                                     |
|----------------|----------|-----------------------------------------------------|
| device_name    | string   | The user's device name that is removed              |
| device_key     | string   | The user's device key that is removed               |
| success        | boolean  | If TRUE, the user's device was removed successfully |

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 401 (Unauthorized)

The user's request device key is invalid
