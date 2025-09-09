# Request to Process (POST) - WN API DOCS

Documentation of Request to process API - https://api.webnet.mywire.org/process/\[:id\]/request (POST)

## REQUEST

| **HTTP Parameters**   | **Value**                                             |
|-----------------------|-------------------------------------------------------|
| Method:           	| POST                                                  |
| URL:              	| https://api.webnet.mywire.org/process/\[:id\]/request |
| Body:             	| JSON                                                  |

\* _id_: The process ID

| **Body Parameters**  | **Type**  | **Required** | **Description**                              |
|----------------------|-----------|--------------|----------------------------------------------|
|                      |           |              |                                              |

\* Determined by the type of process

## RESPONSE - Code: 200 (OK)

| **Parameters**  | **Type**  | **Description**                                 |
|-----------------|-----------|-------------------------------------------------|
|                 |           |                                                 |

\* Determined by the type of process

## RESPONSE - Code: 404 (Bad Request)

Process is not found

## RESPONSE - Code: 500 (Internal Server Error)

An unexpected server error occurred. Please try again later.

