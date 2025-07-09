# Song Lyrics (GET) - WN API DOCS

Documentation of song lyrics API - https://api.webnet.mywire.org/music/lyrics (GET)

## REQUEST

| **HTTP Parameters** | **Value**                                  |
|---------------------|--------------------------------------------|
| Method:             | GET                                        |
| URL:                | https://api.webnet.mywire.org/music/lyrics |
| Body:               | TEXT                                       |

| **Body Parameters** | **Type** | **Required** | **Description**       |
|---------------------|----------|--------------|-----------------------|
| id                  | string   | YES          | YouTube Music song ID |

## RESPONSE - Code: 200 (OK)

Lyrics text

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 404 (Not Found)

Lyrics are not found