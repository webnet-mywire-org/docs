# Logout session (DELETE) - WN API DOCS

Documentation of logout session API - https://api.webnet.mywire.org/auth/session (delete)

## REQUEST

| **HTTP Parametars** 	| **Value**                                 	|
|-----------------------|-----------------------------------------------|
| Method:           	| DELETE                                      	|
| URL:              	| https://api.webnet.mywire.org/auth/session   	|
| Body:             	| JSON                                      	|

| **Body Parameters** | **Type** | **Required**  | **Description**    |
|---------------------|----------|---------------|--------------------|
| session             | string   | YES           | The user's session |

## RESPONSE - Code: 200 (OK)

| **Parameters** | **Type** | **Description**                              |
|----------------|----------|----------------------------------------------|
| session        | string   | The user's session                           |
| success        | boolean  | If TRUE, the session was closed successfully |

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 401 (Unauthorized)

The user's request session is invalid
