# Delete file or folder (POST) - WN API DOCS

Documentation of Delete file or folder API - https://api.webnet.mywire.org/drive/\[:drive\]/delete (POST)

## REQUEST

| **HTTP Parameters**   | **Value**                                             |
|-----------------------|-------------------------------------------------------|
| Method:           	| POST                                                  |
| URL:              	| https://api.webnet.mywire.org/drive/\[:drive\]/delete |
| Body:             	| JSON                                                  |

\* _drive_: The drive name: "disk", "media", "photos", App ID, Share ID, etc.

| **Body Parameters**  | **Type**  | **Required** | **Description**                              |
|----------------------|-----------|--------------|----------------------------------------------|
| session              | string    | YES          | The user's session                           |
| files                | array     | YES          | The folders and files absolute path in drive |

## RESPONSE - Code: 200 (OK)


| **Parameters**  | **Type**  | **Description**                                 |
|-----------------|-----------|-------------------------------------------------|
| process_id      | string    | Process ID for handling file or folder deletion |

* _process request_ (get-progress): Get state of deleting progress
  - **action**: string - "get-progress"
  

## RESPONSE - Code: 400 (Bad Request)

Bad request: missing or invalid parameters.

## RESPONSE - Code: 401 (Unauthorized)

Unauthorized if the session is invalid or expired.

## RESPONSE - Code: 403 (Forbidden)

Forbidden if the user does not have permission to access the specified drive folder of file.
 
## RESPONSE - Code: 500 (Internal Server Error)

An unexpected server error occurred. Please try again later.

