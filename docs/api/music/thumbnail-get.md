# Song Thumbnail (GET) - WN API DOCS

Documentation of song thumbnail API - https://api.webnet.mywire.org/music/thumbnail (GET)

## REQUEST

| **HTTP Parameters** | **Value**                                     |
|---------------------|-----------------------------------------------|
| Method:             | GET                                           |
| URL:                | https://api.webnet.mywire.org/music/thumbnail |
| Body:               | JPG                                           |

| **Body Parameters** | **Type** | **Required** | **Description**       |
|---------------------|----------|--------------|-----------------------|
| id                  | string   | YES          | YouTube Music song ID |

## RESPONSE - Code: 200 (OK)

| **Parameters** | **Type** | **Description**                   |
|----------------|----------|-----------------------------------|
| results        | array    | Query search results list in JSON |

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 404 (Not Found)

Song thumbnail is not found