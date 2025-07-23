# Get Image Poster (GET) - WN API DOCS

Documentation of get image poster API - https://api.webnet.mywire.org/image/poster (GET)

## REQUEST

| **HTTP Parameters** | **Value**                                  |
|---------------------|--------------------------------------------|
| Method:             | GET                                        |
| URL:                | https://api.webnet.mywire.org/image/poster |
| Body:               | Query                                      |

| **Body Parameters** | **Type** | **Required** | **Description**       |
|---------------------|----------|--------------|-----------------------|
| name                | string   | YES          | Name of media         |

## RESPONSE - Code: 200 (OK)

File buffer

## RESPONSE - Code: 400 (Bad Request)

Bad request missing or invalid parameters.
