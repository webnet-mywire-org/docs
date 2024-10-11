# Search Songs (GET) - WN API DOCS

Documentation of search songs API - https://api.webnet.mywire.org/music/search (GET)

## REQUEST

| **HTTP Parameters** | **Value**                                  |
|---------------------|--------------------------------------------|
| Method:             | POST                                       |
| URL:                | https://api.webnet.mywire.org/music/search |
| Body:               | JSON                                       |

| **Body Parameters** | **Type** | **Required** | **Description** |
|---------------------|----------|--------------|-----------------|
| q                   | string   | YES          | Search query    |

## RESPONSE - Code: 200 (OK)

| **Parameters** | **Type** | **Description**                   |
|----------------|----------|-----------------------------------|
| results        | array    | Query search results list in JSON |

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct