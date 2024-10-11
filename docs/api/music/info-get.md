# Song Info (GET) - WN API DOCS

Documentation of search songs API - https://api.webnet.mywire.org/music/info (GET)

## REQUEST

| **HTTP Parameters** | **Value**                                |
|---------------------|------------------------------------------|
| Method:             | GET                                      |
| URL:                | https://api.webnet.mywire.org/music/info |
| Body:               | JSON                                     |

| **Body Parameters** | **Type** | **Required** | **Description**       |
|---------------------|----------|--------------|-----------------------|
| id                  | string   | YES          | YouTube Music song ID |

## RESPONSE - Code: 200 (OK)

| **Parameters** | **Type** | **Description**              |
|----------------|----------|------------------------------|
| type           | string   | YouTube video type           |
| videoId        | string   | YouTube Music song ID        |
| name           | string   | Song name                    |
| artist         | json     | Artist name and ID           |
| duration       | int      | Duration of video in seconds |
| thumbnails     | array    | List of song thumbnails      |
| formats        | array    | List of stream formats       |
| formats        | array    | List of stream formats       |

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 404 (Not Found)

Song is not found