# Get Image Avatar (GET) - WN API DOCS

Documentation of get image avatar API - https://api.webnet.mywire.org/image/avatar (GET)

## REQUEST

| **HTTP Parameters** | **Value**                                  |
|---------------------|--------------------------------------------|
| Method:             | GET                                        |
| URL:                | https://api.webnet.mywire.org/image/avatar |
| Body:               | Query                                      |

| **Body Parameters** | **Type** | **Required** | **Description**       |
|---------------------|----------|--------------|-----------------------|
| name                | string   | YES          | Name of person        |

## RESPONSE - Code: 200 (OK)

File buffer

## RESPONSE - Code: 400 (Bad Request)

Bad request missing or invalid parameters.
