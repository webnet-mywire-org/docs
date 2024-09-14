# Login (POST) - WN API DOCS

Documentation of login API - https://api.webnet.mywire.org/auth/login (POST)

## REQUEST

| **HTTP Parametars** 	| **Value**                                 	|
|-----------------------|-----------------------------------------------|
| Method:           	| POST                                      	|
| URL:              	| https://api.webnet.mywire.org/auth/login   	|
| Body:             	| JSON                                      	|

| **Body Parameters** 	| **Type** 	| **Required** 	    | **Description**                                                                     	|
|-----------------------|-----------|-------------------|---------------------------------------------------------------------------------------|
| username          	| string   	| YES           	| The user's username                                                                 	|
| password          	| string   	| YES           	| The user's password                                                                 	|
| domain            	| string   	| NO            	| The domain the user belongs to (default: webnet.mywire.org)                         	|
| device_key        	| boolean  	| YES           	| If set to TRUE, a session device key will also be generated                         	|
| device_name       	| string   	| YES           	| The name of the user's device or application from which authentication is performed 	|

## RESPONSE - Code: 200 (OK)

| **Parameters** 	| **Type**      	| **Description**                                           	|
|-------------------|-------------------|---------------------------------------------------------------|
| username       	| string        	| The user's username                                       	|
| domain         	| string        	| The user's domain                                         	|
| display_name   	| string        	| The user's display name                                   	|
| session        	| string        	| The user's temporary session key for WebNet API requests  	|
| device_name*   	| string / null 	| The user's device name                                    	|
| device_key*    	| string / null 	| The user's device key to generate new sessions key        	|

\* _"device_name" and "device_key" are set to the value null, if the request parameter "device_key" was set to FALSE_

## RESPONSE - Code: 400 (Bad Request)

Request does not have all required parameters or they are not correct

## RESPONSE - Code: 401 (Unauthorized)

The login for the user is incorrect, the combination of user credentials (username, password, domain) is incorrect

## RESPONSE - Code: 429 (Too Many Requests)

Too many failed user authorization attempts (try again later)
