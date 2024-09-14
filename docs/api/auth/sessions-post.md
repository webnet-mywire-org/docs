# Get sessions (POST) - WN API DOCS

Documentation of get sessions API - https://api.webnet.mywire.org/auth/sessions (POST)

## REQUEST

| **HTTP Parametars** 	| **Value**                                    |
|-----------------------|----------------------------------------------|
| Method:           	| POST                                         |
| URL:              	| https://api.webnet.mywire.org/auth/sessions  |
| Body:             	| JSON                                         |

| **Body Parameters**  | **Type**        | **Required** | **Description**                  |
|----------------------|-----------------|--------------|----------------------------------|
| device_key / session | string / string | YES          | The user's session or device key |

\* _If both parameters are specified ("device_key" and "session"), the "session" parameter is ignored_

## RESPONSE - Code: 200 (OK)

| **Parameters**  | **Type** | **Description**                         |
|-----------------|----------|-----------------------------------------|
| sessions        | array    | The user's sessions list in JSON        |

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 401 (Unauthorized)

The user's request session or device key is invalid
