# Start Process (POST) - WN API DOCS

Documentation of Start process API - https://api.webnet.mywire.org/process/\[:id\]/start (POST)

## REQUEST

| **HTTP Parameters**   | **Value**                                             |
|-----------------------|-------------------------------------------------------|
| Method:           	| POST                                                  |
| URL:              	| https://api.webnet.mywire.org/process/\[:id\]/start   |
| Body:             	| JSON                                                  |

\* _id_: The process ID

| **Body Parameters**  | **Type**  | **Required** | **Description**                              |
|----------------------|-----------|--------------|----------------------------------------------|

## RESPONSE - Code: 200 (OK)

| **Parameters**  | **Type**  | **Description**                                 |
|-----------------|-----------|-------------------------------------------------|
| process_id      | string    | Process ID for handling file or folder deletion |
| started         | Boolean   | Is process started?                             |

## RESPONSE - Code: 404 (Bad Request)

Process is not found
 
## RESPONSE - Code: 500 (Internal Server Error)

An unexpected server error occurred. Please try again later.

