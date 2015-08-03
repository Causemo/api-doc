[Main](https://github.com/Causemo/api-doc/blob/master/README.md) / [Web API](https://github.com/Causemo/api-doc/blob/master/sections/api/1/web/README.md) / Creatives
====================

###  web/creatives
  - **[POST]**
    - Fetches a creative from Causemo server
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
	  - `device`: A JSON object representing the device creative is being fetch for. It should contain a `platform` property which describes the device platform (ie: iPhone OS 8.0.2 or Windows 10, etc...). If the device is using a browser, it should also contain a property called `browser`.
      - `udid`: This is required if the `mobile` flag is not set or set to true; then device `udid` is the device unique identifier.
      - `user`: (optional) JSON object representing a user associated with this request 
    - Params
      - `mobile`: (optional) False if the request is not mobile native
    - Response
      - A JSON object representing the `creative`, `campaign` and `sessionId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"device":{"platform": "Windows 10", "browser": "chrome"}}' "http://localhost:3000/web/creatives?mobile=false"
      ```
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer c8c08dd5bd62b36427c86f6ecb350a1c7da6a8b115fc8cbe357a6f8324c4a52850ed77d9c30b8440b462cbef2a8967ff97e9e43da2a3d7" -d '{"udid": "12379","device":{"platform": "iPhone OS 8.0.2"}}' "http://localhost:3000/web/creatives"
      ```

###  web/creatives/:creativeId/started
  - **[POST]**
    - Notifies Causemo a creative was started
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `sessionId`: The current session `sessionId`
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>"}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/started"
      ```

###  web/creatives/:creativeId/suspended
  - **[POST]**
    - Notifies Causemo a creative was suspended
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `sessionId`: The current session `sessionId`
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>"}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/suspended"
      ```

###  web/creatives/:creativeId/resumed
  - **[POST]**
    - Notifies Causemo a creative was resumed
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `sessionId`: The current session `sessionId`
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>"}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/resumed"
      ```

###  web/creatives/:creativeId/completed
  - **[POST]**
    - Notifies Causemo a creative was completed
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `sessionId`: The current session `sessionId`
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>"}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/completed"
      ```

###  web/creatives/:creativeId/activated
  - **[POST]**
    - Notifies Causemo a creative was activated
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `sessionId`: The current session `sessionId`
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>"}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/activated"
      ```

###  web/creatives/:creativeId/donation/direct
  - **[POST]**
    - Notifies Causemo user was directed to donation screen
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `sessionId`: The current session `sessionId`
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>"}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/donation/direct"
      ```

###  web/creatives/:creativeId/donation/viewed
  - **[POST]**
    - Notifies Causemo user was donation screen was viewed
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `sessionId`: The current session `sessionId`
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>"}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/donation/viewed"
      ```

###  web/creatives/:creativeId/donation/closed
  - **[POST]**
    - Notifies Causemo user was donation screen was closed
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `sessionId`: The current session `sessionId`
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>"}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/donation/closed"
      ```

###  web/creatives/:creativeId/donation/declined
  - **[POST]**
    - Notifies Causemo user was donation screen was declined
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `sessionId`: The current session `sessionId`
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>"}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/donation/declined"
      ```

###  web/creatives/:creativeId/donation
  - **[POST]**
    - Notifies Causemo user was donation screen was completed
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `appProductId`: The AppProduct for which the donation was made for
      - `sessionId`: The current session `creativeId`
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      - Replace `<APP_PRODUCT_ID>` with a valid `AppProduct.id`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "appProductId": "<APP_PRODUCT_ID>"}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/donation"
      ```

###  web/creatives/:creativeId/donation/exited
  - **[POST]**
    - Notifies Causemo user was on the donation screen, it was completed and exited
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `email`: The user email for the donation 
      - `sessionId`: The current session `sessionId`
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "email":"miguel@causemo.com"}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/donation/exited"
      ```

###  web/creatives/:creativeId/pledge
  - **[POST]**
    - Notifies Causemo user made a pledge
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `email`: The user email for pledge
      - `amount`: The amount the user pledged
	  - `device`: (optional) JSON object representing a device associated with this request 
      - `user`: (optional) JSON object representing a user associated with this request 
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `web/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "email":"miguel@causemo.com", "amount": "5.25", "user": {"firstName":"miguel", "lastName":"Doe"}}' "http://dev-api.causemo.com/web/creatives/<CREATIVE_ID>/pledge"
      ```

