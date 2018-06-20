{
  "info": {
    "name": "Microsoft Graph API List Permissions On A Drive Item",
    "_postman_id": "a200eeba-d363-48b7-8312-dba2e31709cf",
    "description": "List permissions on a DriveItem List the effective permissions of on a DriveItem.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "list",
      "item": [
        {
          "id": "5d36a8ea-1841-45e5-bdc5-6483eedc56a8",
          "name": "ListPermissionsOnADriveItem",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.microsoft.com",
              "path": [
                "me/drive/items/:item-id/permissions"
              ],
              "variable": [
                {
                  "id": "item-id",
                  "value": "item-id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "if-none-match",
                "value": "if-none-match",
                "description": "If this request header is included and the etag provided matches the current etag on the item, an HTTP 304 Not Modified response is returned",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "List permissions on a DriveItem List the effective permissions of on a DriveItem"
          },
          "response": [
            {
              "code": 200,
              "name": "Response_200",
              "id": "84ba2fda-dec3-4a40-b777-1d7629f6f9ee"
            }
          ]
        }
      ]
    }
  ]
}