# Song Stream (GET) - WN API DOCS

Documentation of stream song API - https://api.webnet.mywire.org/music/stream (GET)

## REQUEST

| **HTTP Parameters** | **Value**                                  |
|---------------------|--------------------------------------------|
| Method:             | GET                                        |
| URL:                | https://api.webnet.mywire.org/music/stream |
| Body:               | STREAM                                     |

| **Body Parameters** | **Type** | **Required** | **Description**       |
|---------------------|----------|--------------|-----------------------|
| id                  | string   | YES          | YouTube Music song ID |

## RESPONSE - Code: 200 (OK)

Song stream

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 404 (Not Found)

Stream is not found