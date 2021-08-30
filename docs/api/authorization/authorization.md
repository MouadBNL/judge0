# Group Authorization
To issue some API calls you need to be authorized. For example, you need to be authorized to
[list all submissions](#submissions-submission-get-1) on Judge0.

## Authorize 
* With this API call you can check if your authorization token is valid. If authentication is enabled you should also authenticate in this API call.
---
### Note
* `X-Auth-Token` is default header field name, but administrators of Judge0 instance you are using
   can change this default field name.
* Contact administrator of Judge0 instance you are using to get your authentication token.
---
### Security Warning
* Although you can send authentication token as URI parameter, **always** send authentication token through headers.
---
- **URL** `/authorize{?X-Auth-User}`
  
- **Method:** `POST`
  
- **Headers:**
  ```
  X-Auth-Token: f6583e60-b13b-4228-b554-2eb332ca64e7
  ```

- **Success Response:**
  Response 200 If your authorization token is valid.
  * **Code:** 200

- **Error Response:**
  Response 403 Authorization failed because your authorization token is invalid.
  * **Code:** 401