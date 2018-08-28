{
  "info": {
    "name": "RingCentral Check User Permissions",
    "_postman_id": "030f3cd6-db3c-4ad6-a595-3ac9de523ef0",
    "description": "Checks if a certain user permission is activated for a particular extension.\nUsage Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter [targetExtensionId] value is invalid\n\n\n403\nCMN-404\nAttempt to access another extension\n\n\n404\nCMN-102\nResource for parameter [accountId] is not found",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Check",
      "item": [
        {
          "id": "0fcf3285-5103-4fee-920a-b260e3ce351c",
          "name": "checkUserPermission",
          "request": {
            "url": {
              "protocol": "http",
              "host": "platform.ringcentral.com",
              "path": [
                "restapi/v1.0/account/:accountId/extension/:extensionId/authz-profile/check"
              ],
              "query": [
                {
                  "key": "permissionId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "targetExtensionId",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "accountId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "extensionId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Checks if a certain user permission is activated for a particular extension.\nUsage Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter [targetExtensionId] value is invalid\n\n\n403\nCMN-404\nAttempt to access another extension\n\n\n404\nCMN-102\nResource for parameter [accountId] is not found"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "68d82776-4280-4a8d-90f9-4b58312717ae"
            }
          ]
        }
      ]
    }
  ]
}