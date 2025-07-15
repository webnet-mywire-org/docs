# Create file or folder (POST) - WN API DOCS

Documentation of create file or folder API - https://api.webnet.mywire.org/drive/\[:drive\]/create (POST)

## REQUEST

| **HTTP Parameters**   | **Value**                                             |
|-----------------------|-------------------------------------------------------|
| Method:           	| POST                                                  |
| URL:              	| https://api.webnet.mywire.org/drive/\[:drive\]/create |
| Body:             	| JSON                                                  |

\* _drive_: The drive name: "disk", "media", "photos", App ID, Share ID, etc.

| **Body Parameters**  | **Type**  | **Required** | **Description**                       |
|----------------------|-----------|--------------|---------------------------------------|
| session              | string    | YES          | The user's session                    |
| path                 | string    | YES          | The folder path in drive              |
| type                 | string    | YES          | Type of creation needed               |

## RESPONSE - Code: 200 (OK)


| **Parameters**  | **Type**  | **Description**                         |
|-----------------|-----------|-----------------------------------------|
| path            | string    | YES          | The folder path in drive |
| type            | string    | YES          | Type of creation         |


## RESPONSE - Code: 400 (Bad Request)

Bad request missing or invalid parameters.

## RESPONSE - Code: 401 (Unauthorized)

Unauthorized if the session is invalid or expired.

## RESPONSE - Code: 403 (Forbidden)

Forbidden if the user does not have permission to access the specified drive folder of file.
 
## RESPONSE - Code: 500 (Internal Server Error)

An unexpected server error occurred. Please try again later.

