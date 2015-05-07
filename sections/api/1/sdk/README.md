[Main](https://github.com/Causemo/api-doc/blob/master/README.md) / SDK API
====================
All API endpoints for SDK. 

**IMPORTANT:** Every session needs to be initialized by posting to `/sdk/devices/`. This will then return you an object which contains a `transactionId`. This `transactionId` is needed for subsequent calls, chaining the calls together to a single transaction. When a new session is started on a device, another call to initialize should occour to receive a new transactionId.

- Client Scope
  - `sdk`
- API 
  - [Devices](https://github.com/Causemo/api-doc/blob/master/sections/api/1/sdk/devices.md)

