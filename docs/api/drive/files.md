# Get files and folders (POST) - WN API DOCS

Documentation of get files and folders API - https://api.webnet.mywire.org/drive/\[:drive\]/files (POST)

## REQUEST

| **HTTP Parameters**   | **Value**                                            |
|-----------------------|------------------------------------------------------|
| Method:           	| POST                                                 |
| URL:              	| https://api.webnet.mywire.org/drive/\[:drive\]/files |
| Body:             	| JSON                                                 |

\* _drive_: The drive name: "disk", "media", "photos", App ID, Share ID, etc.

| **Body Parameters**  | **Type**  | **Required** | **Description**                       |
|----------------------|-----------|--------------|---------------------------------------|
| session              | string    | YES          | The user's session                    |
| path                 | string    | YES          | The folder path in drive              |
| sort*                | string    | NO           | Sort order: "desc" ro "asc" (by name) |

\* _sort_: If not specified, the default is "asc" by name.

## RESPONSE - Code: 200 (OK)

| **Parameters**  | **Type** | **Description**                         |
|-----------------|----------|-----------------------------------------|
| total           | integer  | Total number of files and folders found |
| sort_order      | string   | Sort order used: "desc" or "asc"        |
| files*          | array    | Array of files and folders              |

\* _files_: Each file or folder object contains:
  - **name**: string - Name of the file or folder
  - **ext**: string - File extension (empty for folders)
  - **isDirectory**: boolean - True if it's a folder, else false
  - **isSymlink**: boolean - True if it's a symlink, else false

## RESPONSE - Code: 400 (Bad Request)

Bad request missing or invalid parameters.

## RESPONSE - Code: 401 (Unauthorized)

Unauthorized if the session is invalid or expired.

## RESPONSE - Code: 403 (Forbidden)

Forbidden if the user does not have permission to access the specified drive or folder.