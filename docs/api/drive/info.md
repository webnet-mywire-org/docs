# Get file or folder information (POST) - WN API DOCS

Documentation of get file or folder information API - https://api.webnet.mywire.org/drive/\[:drive\]/info (POST)

## REQUEST

| **HTTP Parameters**   | **Value**                                            |
|-----------------------|------------------------------------------------------|
| Method:           	| POST                                                 |
| URL:              	| https://api.webnet.mywire.org/drive/\[:drive\]/info  |
| Body:             	| JSON                                                 |

\* _drive_: The drive name: "disk", "media", "photos", App ID, Share ID, etc.

| **Body Parameters**  | **Type**  | **Required** | **Description**                       |
|----------------------|-----------|--------------|---------------------------------------|
| session              | string    | YES          | The user's session                    |
| path                 | string    | YES          | The folder path in drive              |

## RESPONSE - Code: 200 (OK)


| **Parameters**  | **Type**  | **Description**                        |
|-----------------|-----------|----------------------------------------|
| name            | string    | The display name of the file or folder |
| full_name       | string    | The full name (with extension)         |
| ext             | string    | File extension, empty for folders      |
| mimeType        | string    | MIME type of the file                  |
| size            | integer   | Size in bytes (0 for folders)          |
| modified        | string    | Last modified timestamp (ISO 8601)     |
| created         | string    | Creation timestamp (ISO 8601)          |
| accessed        | string    | Last accessed timestamp (ISO 8601)     |
| isDirectory     | boolean   | True if this is a directory            |
| isSymlink       | boolean   | True if this is a symbolic link        |


## RESPONSE - Code: 400 (Bad Request)

Bad request missing or invalid parameters.

## RESPONSE - Code: 401 (Unauthorized)

Unauthorized if the session is invalid or expired.

## RESPONSE - Code: 403 (Forbidden)

Forbidden if the user does not have permission to access the specified drive folder of file.

## RESPONSE - Code: 404 (Not found)

Directory or file doesn't exist
 
## RESPONSE - Code: 500 (Internal Server Error)

An unexpected server error occurred. Please try again later.

