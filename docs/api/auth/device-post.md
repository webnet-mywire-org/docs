# Get devices (POST) - WN API DOCS

Documentation of get devices API - https://api.webnet.mywire.org/auth/deivce (POST)

## REQUEST

| **HTTP Parameters** 	| **Value**                                   |
|-----------------------|---------------------------------------------|
| Method:           	| POST                                          |
| URL:              	| https://api.webnet.mywire.org/auth/device     |
| Body:             	| JSON                                          |

| **Body Parameters**  | **Type**  | **Required** | **Description**       |
|----------------------|-----------|--------------|-----------------------|
| device_key           | string    | YES          | The user's device key |

\* _If both parameters are specified ("device_key" and "session"), the "session" parameter is ignored_

## RESPONSE - Code: 200 (OK)

| **Parameters** | **Type** | **Description**                         |
|----------------|----------|-----------------------------------------|
| devices        | array    | The user's deivces list in JSON         |

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 401 (Unauthorized)

The user's request session or device key is invalid
