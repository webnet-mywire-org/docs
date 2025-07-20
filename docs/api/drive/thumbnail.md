# File thumbnail (GET) - WN API DOCS

Documentation of file thumbnail API - https://api.webnet.mywire.org/drive/\[:drive\]/thumbnail (GET)

## REQUEST

| **HTTP Parameters**   | **Value**                                                 |
|-----------------------|-----------------------------------------------------------|
| Method:           	| GET                                                       |
| URL:              	| https://api.webnet.mywire.org/drive/\[:drive\]/thumbnail  |
| Params:             	| JSON                                                      |

\* _drive_: The drive name: "disk", "media", "photos", App ID, Share ID, etc.

| **Body Parameters**  | **Type**  | **Required** | **Description**                            |
|----------------------|-----------|--------------|--------------------------------------------|
| session              | string    | YES          | The user's session                         |
| path                 | string    | YES          | The file path in drive                     |

## RESPONSE - Code: 200 (OK)

File thumbnail buffer in jpg format

## RESPONSE - Code: 400 (Bad Request)

Bad request missing or invalid parameters.

## RESPONSE - Code: 401 (Unauthorized)

Unauthorized if the session is invalid or expired.

## RESPONSE - Code: 403 (Forbidden)

Forbidden if the user does not have permission to access the specified file.

## RESPONSE - Code: 404 (Not found)

File doesn't exist
 
## RESPONSE - Code: 500 (Internal Server Error)

An unexpected server error occurred. Please try again later.

