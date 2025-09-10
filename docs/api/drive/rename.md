# Rename file or folder (POST) - WN API DOCS

Documentation of Rename file or folder API - https://api.webnet.mywire.org/drive/\[:drive\]/rename (POST)

## REQUEST

| **HTTP Parameters**   | **Value**                                             |
|-----------------------|-------------------------------------------------------|
| Method:              	| POST                                                  |
| URL:                	| https://api.webnet.mywire.org/drive/\[:drive\]/rename |
| Body:               	| JSON                                                  |

\* _drive_: The drive name: "disk", "media", "photos", App ID, Share ID, etc.

| **Body Parameters**  | **Type**  | **Required** | **Description**                              |
|----------------------|-----------|--------------|----------------------------------------------|
| session              | string    | YES          | The user's session                           |
| file                 | string    | YES          | Old file or folder name                      |
| file_new             | string    | YES          | New file or folder name                      |
| directory            | string    | YES          | The file or folder perent directory path     |

## RESPONSE - Code: 200 (OK)


| **Parameters**  | **Type**  | **Description**                                 |
|-----------------|-----------|-------------------------------------------------|
| process_id      | string    | Process ID for handling file or folder renaming |

* _process request_ (get-status): Get state of deleting progress
  - **action**: string - "get-status"
  

## RESPONSE - Code: 400 (Bad Request)

Bad request: missing or invalid parameters.

## RESPONSE - Code: 404 (File not found)

File or folder not found, please check your input.

## RESPONSE - Code: 401 (Unauthorized)

Unauthorized if the session is invalid or expired.

## RESPONSE - Code: 403 (Forbidden)

Forbidden if the user does not have permission to access the specified drive folder of file.
 
## RESPONSE - Code: 500 (Internal Server Error)

An unexpected server error occurred. Please try again later.

