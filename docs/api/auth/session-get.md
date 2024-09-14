# Renew session (GET) - WN API DOCS

Documentation of renew session API - https://api.webnet.mywire.org/auth/session (GET)

## REQUEST

| **HTTP Parametars** 	| **Value**                                   |
|-----------------------|---------------------------------------------|
| Method:           	| GET                                         |
| URL:              	| https://api.webnet.mywire.org/auth/session  |
| Body:             	| JSON                                        |

| **Body Parameters**  | **Type**        | **Required** | **Description**                  |
|----------------------|-----------------|--------------|----------------------------------|
| device_key / session | string / string | YES          | The user's session or device key |

\* _If both parameters are specified ("device_key" and "session"), the "session" parameter is ignored_

## RESPONSE - Code: 200 (OK)

| **Parameters** | **Type**       | **Description**                         |
|----------------|----------------|-----------------------------------------|
| session        | string         | The user's new session                  |
| session_old*   | string / null  | The user's old, no longer valid session |

\* _"session_old" is set to null if "device_key" was used in the request_

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 401 (Unauthorized)

The user's request session or device key is invalid
