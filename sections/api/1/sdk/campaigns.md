[Main](https://github.com/Causemo/api-doc/blob/master/README.md) / [SDK API](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/README.md) / Campaigns
====================

###  sdk/campaigns/:campaignId/direct
  - **[POST]**
    - Notifies Causemo user was directed to donation screen
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
      - A JSON object with `sessionId` and `campaignId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<SESSION_ID>` with `sessionId` from [session initilization call](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/devices.md#sdkdevices)
      - Replace `<UDID>` with device `udid`
      - Replace `<CAMPAIGN_ID>` with a `creative.campaignId` from a call to `sdk/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "udid": "<UDID>"}' "http://dev-api.causemo.com/sdk/campaigns/<CAMPAIGN_ID>/direct"
      ```

###  sdk/campaigns/:campaignId/viewed
  - **[POST]**
    - Notifies Causemo user was donation screen was viewed
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
      - A JSON object with `sessionId` and `campaignId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<SESSION_ID>` with `sessionId` from [session initilization call](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/devices.md#sdkdevices)
      - Replace `<UDID>` with device `udid`
      - Replace `<CAMPAIGN_ID>` with a `creative.campaignId` from a call to `sdk/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "udid": "<UDID>"}' "http://dev-api.causemo.com/sdk/campaigns/<CAMPAIGN_ID>/viewed"
      ```

###  sdk/campaigns/:campaignId/closed
  - **[POST]**
    - Notifies Causemo user was donation screen was closed
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
      - A JSON object with `sessionId` and `campaignId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<SESSION_ID>` with `sessionId` from [session initilization call](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/devices.md#sdkdevices)
      - Replace `<UDID>` with device `udid`
      - Replace `<CAMPAIGN_ID>` with a `creative.campaignId` from a call to `sdk/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "udid": "<UDID>"}' "http://dev-api.causemo.com/sdk/campaigns/<CAMPAIGN_ID>/closed"
      ```

###  sdk/campaigns/:campaignId/declined
  - **[POST]**
    - Notifies Causemo user was donation screen was declined
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
      - A JSON object with `sessionId` and `campaignId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<SESSION_ID>` with `sessionId` from [session initilization call](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/devices.md#sdkdevices)
      - Replace `<UDID>` with device `udid`
      - Replace `<CAMPAIGN_ID>` with a `creative.campaignId` from a call to `sdk/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "udid": "<UDID>"}' "http://dev-api.causemo.com/sdk/campaigns/<CAMPAIGN_ID>/declined"
      ```

###  sdk/campaigns/:campaignId/activated
  - **[POST]**
    - Notifies Causemo user was donation screen was activated
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
      - A JSON object with `sessionId` and `campaignId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<SESSION_ID>` with `sessionId` from [session initilization call](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/devices.md#sdkdevices)
      - Replace `<UDID>` with device `udid`
      - Replace `<CAMPAIGN_ID>` with a `creative.campaignId` from a call to `sdk/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "udid": "<UDID>"}' "http://dev-api.causemo.com/sdk/campaigns/<CAMPAIGN_ID>/activated"
      ```

###  sdk/campaigns/:campaignId/completed
  - **[POST]**
    - Notifies Causemo user was donation screen was completed
    - Header fields
      - `api-version: 1`
      - `client-version: <SDK_VERSION>`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `appProductId`: The AppProduct for which the donation was made for
      - `creativeId`: The identifier of the creative which generated the donation
      - `sessionId`: The current session `sessionId`
      - `udid`: The device `udid` used to initialize session with
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `campaignId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<SESSION_ID>` with `sessionId` from [session initilization call](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/devices.md#sdkdevices)
      - Replace `<UDID>` with device `udid`
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `sdk/creatives`
      - Replace `<CAMPAIGN_ID>` with a `creative.campaignId` from a call to `sdk/creatives`
      - Replace `<APP_PRODUCT_ID>` with a valid `AppProduct.id`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "udid": "<UDID>", "appProductId": "<APP_PRODUCT_ID>", "creativeId": "<CREATIVE_ID>"}' "http://dev-api.causemo.com/sdk/campaigns/<CAMPAIGN_ID>/completed"
      ```

###  sdk/campaigns/:campaignId/exited
  - **[POST]**
    - Notifies Causemo user was donation screen was completed and exited
    - Header fields
      - `api-version: 1`
      - `client-version: <SDK_VERSION>`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `email`: The user email for the donation 
      - `sessionId`: The current session `sessionId`
      - `udid`: The device `udid` used to initialize session with
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `campaignId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<SESSION_ID>` with `sessionId` from [session initilization call](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/devices.md#sdkdevices)
      - Replace `<UDID>` with device `udid`
      - Replace `<CAMPAIGN_ID>` with a `creative.campaignId` from a call to `sdk/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "udid": "<UDID>"}' "http://dev-api.causemo.com/sdk/campaigns/<CAMPAIGN_ID>/exited"
      ```

###  sdk/campaigns/:campaignId/pledge
  - **[POST]**
    - Notifies Causemo user made a pledge
    - Header fields
      - `api-version: 1`
      - `client-version: <SDK_VERSION>`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `email`: The user email for pledge
      - `amount`: The amount the user pledged
      - `creativeId`: The creative id the pledge was generated from
      - `sessionId`: The current session `sessionId`
      - `udid`: The device `udid` used to initialize session with
    - Params
      - _none_ 
    - Response
      - A JSON object with `sessionId` and `campaignId`.
    - Try it:
      - Replace `<AUTH_TOKEN>` with authenticated token provided
      - Replace `<SESSION_ID>` with `sessionId` from [session initilization call](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/devices.md#sdkdevices)
      - Replace `<UDID>` with device `udid`
      - Replace `<CAMPAIGN_ID>` with a `creative.campaignId` from a call to `sdk/creatives`
      - Replace `<CREATIVE_ID>` with a `creative.id` from a call to `sdk/creatives`
      ```
      curl -X POST -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" -d '{"sessionId": "<SESSION_ID>", "udid": "<UDID>", "creativeId": "<CREATIVE_ID>", "email":"miguel@causemo.com", "amount": "5.25"}' "http://dev-api.causemo.com/sdk/campaigns/<CAMPAIGN_ID>/pledge"
      ```

