# Search for Web (POST) - WN API DOCS

Documentation of search for web API - https://api.webnet.mywire.org/search/web (POST)

## REQUEST

| **HTTP Parameters** | **Value**                                |
|---------------------|------------------------------------------|
| Method:             | POST                                     |
| URL:                | https://api.webnet.mywire.org/search/web |
| Body:               | JSON                                     |

| **Body Parameters** | **Type** | **Required** | **Description**       |
|---------------------|----------|--------------|-----------------------|
| q                   | string   | YES          | Search query          |
| lang                | string   | YES          | Language of search    |
| page                | string   | YES          | Page of search        |
| country             | string   | NO           | Country of search     |

## RRESPONSE - Code: 200 (OK)

| **Parameters**       | **Type**  | **Description**                        |
|----------------------|-----------|----------------------------------------|
| query                | string    | Search query                           |
| results*             | array     | Array of search result                 |
| number_of_results    | integer   | Number of search result                |
| answers              | array     | Array of answer                        |
| corrections          | array     | Array of correction                    |
| infoboxes            | array     | Array of infobox                       |
| suggestions          | array     | Array of suggestion                    |
| unresponsive_engines | array     | Array of unresponsive engine           |

\* _results_: Each result is an object with the following properties:
  - **url**: The URL of the search result.
  - **title**: The title of the search result.
  - **content**: The content of the search result.
  - **thumbnail**: The thumbnail URL of the search result.
  - **engine**: The name of the engine that generated the search result.
  - **template**: The template used to generate the search result.
  - **parsed_url**: The parsed URL of the search result.
  - **img_src**: The source image URL of the search result.
  - **priority**: The priority level of the search result.
  - **engines**: An array of engines that generated the search result
  - **positions**: An array of positions for the search result pre engine.
  - **score**: The score of the search result.
  - **category**: The category of the search result.

## RESPONSE - Code: 400 (Bad Request)

Invalid query parameter(s).

## RRESPONSE - Code: 500 (Internal Server Error)

An unexpected server error occurred. Please try again later.