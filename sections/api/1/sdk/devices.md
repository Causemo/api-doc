[Main](https://github.com/Causemo/api-doc/blob/master/README.md) / [SDK API](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/README.md) / Devices
====================
- `sdk/devices/` 
  - **[POST]**
    - Initializes a device with Causemo server. 
    - Header fields
      - `api-version: 1`
      - `Authorization: Bearer <AUTH_TOKEN>`
    - Body
      - `app`
        - `appStoreId`: The app store id of app running SDK 
      - `device`
        - `udid`: The device unique identifier
        - `platform`: The device platform name
        - `model`: The device name
    - Params
      - _none_ 
