# Album Info (GET) - WN API DOCS

Documentation of album info  API - https://api.webnet.mywire.org/music/album (GET)

## REQUEST

| **HTTP Parameters** | **Value**                                 |
|---------------------|-------------------------------------------|
| Method:             | GET                                       |
| URL:                | https://api.webnet.mywire.org/music/album |
| Body:               | JSON                                      |

| **Body Parameters** | **Type** | **Required** | **Description**       |
|---------------------|----------|--------------|-----------------------|
| id                  | string   | YES          | YouTube Music song ID |

## RESPONSE - Code: 200 (OK)

| **Parameters** | **Type** | **Description**          |
|----------------|----------|--------------------------|
| type           | string   | YouTube video type       |
| albumId        | string   | YouTube Music album ID   |
| name           | string   | Album name               |
| artist         | json     | Artist name and ID       |
| year           | int      | Album year               |
| thumbnails     | array    | List of album thumbnails |
| songs          | array    | List of songs in album   |

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 404 (Not Found)

Song is not found