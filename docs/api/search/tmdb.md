# Search for Movies and TV shows (POST) - WN API DOCS

Documentation of search for movies and TV shows API - https://api.webnet.mywire.org/search/tmdb (POST)

## REQUEST

| **HTTP Parameters** | **Value**                                 |
|---------------------|-------------------------------------------|
| Method:             | POST                                      |
| URL:                | https://api.webnet.mywire.org/search/tmdb |
| Body:               | JSON                                      |

| **Body Parameters** | **Type** | **Required** | **Description**       |
|---------------------|----------|--------------|-----------------------|
| q                   | string   | YES          | Search query          |
| lang                | string   | YES          | Language of search    |
| page                | string   | YES          | Page of search        |

## RRESPONSE

See TMDB documenta on [this](https://developer.themoviedb.org/reference/search-multi) ink