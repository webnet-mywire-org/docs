# File/Make (POST) - WN API DOCS

Documentation of making mp3 file  API - https://api.webnet.mywire.org/music/file/make (POST)

## REQUEST

| **HTTP Parameters** | **Value**                                     |
|---------------------|-----------------------------------------------|
| Method:             | POST                                          |
| URL:                | https://api.webnet.mywire.org/music/file/make |
| Body:               | JSON                                          |

| **Body Parameters** | **Type** | **Required** | **Description**        |
|---------------------|----------|--------------|------------------------|
| id                  | string   | YES          | YouTube Music song ID  |
| album               | string   | YES          | YouTube Music album ID |

## RESPONSE - Code: 200 (OK)

| **Parameters** | **Type** | **Description**          |
|----------------|----------|--------------------------|
| url            | string   | Download URL of mp3 file |

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 404 (Not Found)

Album is not found