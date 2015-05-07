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
    - Response
```json
      {
    "app": {
        "id": 1241588087,
        "appStoreId": "test-publisher-1-app",
        "name": "test publisher 1 app",
        "color": "ff8000",
        "imageUri": "https://causemo-staging.s3.amazonaws.com/app/4/app.imageUri4.jpg",
        "createdAt": "2015-05-06T02:11:48.115Z",
        "updatedAt": "2015-05-06T02:11:48.115Z",
        "deletedAt": null,
        "publisherId": 1241588087,
        "storeId": 1,
        "clientId": 2,
        "AppProducts": [
            {
                "id": 1241588087,
                "name": "test-publisher-1-product-1",
                "description": null,
                "portionOfProceeds": "0",
                "donationPrice": "0",
                "donationPriceTier": 0,
                "donationRewardUnits": 0,
                "donationRewardType": null,
                "donationRewardUri": null,
                "donationRewardCopy": null,
                "autoRewardUnits": 0,
                "autoRewardType": null,
                "actionButtonCopy": null,
                "headerCopy": null,
                "subHeaderCopy": null,
                "createdAt": "2015-05-06T02:11:48.122Z",
                "updatedAt": "2015-05-06T02:11:48.122Z",
                "deletedAt": null,
                "appId": 1241588087,
                "Triggers": []
            },
            {
                "id": 1500453386,
                "name": "test-publisher-1-product-2",
                "description": null,
                "portionOfProceeds": "0",
                "donationPrice": "0",
                "donationPriceTier": 0,
                "donationRewardUnits": 0,
                "donationRewardType": null,
                "donationRewardUri": null,
                "donationRewardCopy": null,
                "autoRewardUnits": 0,
                "autoRewardType": null,
                "actionButtonCopy": null,
                "headerCopy": null,
                "subHeaderCopy": null,
                "createdAt": "2015-05-06T02:12:39.672Z",
                "updatedAt": "2015-05-06T02:12:39.672Z",
                "deletedAt": null,
                "appId": 1241588087,
                "Triggers": [
                    {
                        "id": 2,
                        "key": "ad_view_help_now",
                        "behavior": "donation_screen",
                        "createdAt": "2015-05-06T02:11:48.101Z",
                        "updatedAt": "2015-05-06T02:11:48.101Z",
                        "deletedAt": null,
                        "AppProductTrigger": {
                            "createdAt": "2015-05-06T02:12:39.684Z",
                            "updatedAt": "2015-05-06T02:12:39.684Z",
                            "deletedAt": null,
                            "triggerId": 2,
                            "appProductId": 1500453386
                        }
                    },
                    {
                        "id": 3,
                        "key": "direct_donation",
                        "behavior": "donation_screen",
                        "createdAt": "2015-05-06T02:11:48.108Z",
                        "updatedAt": "2015-05-06T02:11:48.108Z",
                        "deletedAt": null,
                        "AppProductTrigger": {
                            "createdAt": "2015-05-06T02:12:39.684Z",
                            "updatedAt": "2015-05-06T02:12:39.684Z",
                            "deletedAt": null,
                            "triggerId": 3,
                            "appProductId": 1500453386
                        }
                    }
                ]
            },
            {
                "id": 1755259484,
                "name": "test-publisher-1-product-3",
                "description": null,
                "portionOfProceeds": "0",
                "donationPrice": "0",
                "donationPriceTier": 0,
                "donationRewardUnits": 0,
                "donationRewardType": null,
                "donationRewardUri": null,
                "donationRewardCopy": null,
                "autoRewardUnits": 0,
                "autoRewardType": null,
                "actionButtonCopy": null,
                "headerCopy": null,
                "subHeaderCopy": null,
                "createdAt": "2015-05-06T02:12:39.692Z",
                "updatedAt": "2015-05-06T02:12:39.692Z",
                "deletedAt": null,
                "appId": 1241588087,
                "Triggers": [
                    {
                        "id": 1,
                        "key": "incentivized_ad_view",
                        "behavior": "creative_player",
                        "createdAt": "2015-05-06T02:11:48.092Z",
                        "updatedAt": "2015-05-06T02:11:48.092Z",
                        "deletedAt": null,
                        "AppProductTrigger": {
                            "createdAt": "2015-05-06T02:12:39.696Z",
                            "updatedAt": "2015-05-06T02:12:39.696Z",
                            "deletedAt": null,
                            "triggerId": 1,
                            "appProductId": 1755259484
                        }
                    },
                    {
                        "id": 3,
                        "key": "direct_donation",
                        "behavior": "donation_screen",
                        "createdAt": "2015-05-06T02:11:48.108Z",
                        "updatedAt": "2015-05-06T02:11:48.108Z",
                        "deletedAt": null,
                        "AppProductTrigger": {
                            "createdAt": "2015-05-06T02:12:39.697Z",
                            "updatedAt": "2015-05-06T02:12:39.697Z",
                            "deletedAt": null,
                            "triggerId": 3,
                            "appProductId": 1755259484
                        }
                    }
                ]
            }
        ]
    },
    "deviceCreated": false,
    "deviceId": 1,
    "transactionId": 4,
    "features": []
}
```
