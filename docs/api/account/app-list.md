# App list (POST) - WN API DOCS

Documentation of user app list API - https://api.webnet.mywire.org/account/app-list (POST)

## REQUEST

| **HTTP Parameters** | **Value**                                      |
|---------------------|------------------------------------------------|
| Method:           	| POST                                           |
| URL:              	| https://api.webnet.mywire.org/account/app-list |
| Body:             	| JSON                                           |

| **Body Parameters**  | **Type**  | **Required** | **Description**    |
|----------------------|-----------|--------------|--------------------|
| session              | string    | NO           | The user's session |

## RESPONSE - Code: 200 (OK)

| **Parameters** | **Type** | **Description**                         |
|----------------|----------|-----------------------------------------|
| apps           | array    | The user's or default apps list in JSON |

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct
