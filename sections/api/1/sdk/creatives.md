[Main](https://github.com/Causemo/api-doc/blob/master/README.md) / [SDK API](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/README.md) / Creatives
====================

###  sdk/creatives
  - **[GET]**
    - Fetches a creative from Causemo server
    - Header fields
      - `api-version: 1`
      - `client-version: <SDK_VERSION>`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - _none_ 
    - Params
      - `sessionId`: The current session `sessionId`
      - `udid`: The device `udid` used to initialize session with
    - Response
      - A JSON object representing the `creative`. It will also return a `sessionId` passed in.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<SESSION_ID>` with `sessionId` from [session initilization call](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/devices.md#sdkdevices)
      - Replace `<UDID>` with device `udid`
      ```
      curl -X GET -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" "http://localhost:3000/sdk/creatives?transactionId=<SESSION_ID>&udid=<UDID>"
      ```

###  sdk/creatives/:creativeId/started
  - **[POST]**
    - Notifies Causemo a creative was started
    - Header fields
      - `api-version: 1`
      - `client-version: <SDK_VERSION>`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `sessionId`: The current session `sessionId`
      - `udid`: The device `udid` used to initialize session with
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `creativeId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<SESSION_ID>` with `sessionId` from [session initilization call](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/devices.md#sdkdevices)
      - Replace `<UDID>` with device `udid`
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `sdk/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "udid": "<UDID>"}' "http://dev-api.causemo.com/sdk/creatives/<CREATIVE_ID>/started"
      ```
