[Main](https://github.com/Causemo/api-doc/blob/master/README.md) / [SDK API](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/README.md) / Creatives
====================
- `sdk/creatives` 
  - **[GET]**
    - Fetches a creative from Causemo server
    - Header fields
      - `api-version: 1`
      - `client-version: <SDK_VERSION>`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - _none_ 
    - Params
      - transactionId
    - Try it:
    
      ```
      curl -X GET -H "Content-Type: application/json" -H "api-version: 1" -H "Authorization: Bearer <AUTH_TOKEN>" "http://localhost:3000/sdk/creatives?transactionId=<TRANSACTION_ID>"
      ```
