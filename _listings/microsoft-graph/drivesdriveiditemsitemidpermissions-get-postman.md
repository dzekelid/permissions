{
  "info": {
    "name": "Microsoft Graph API List Permissions On A Drive Item",
    "_postman_id": "82206bd5-ef88-4549-952b-17ccb35b0fdf",
    "description": "List permissions on a DriveItem List the effective permissions of on a DriveItem.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "list",
      "item": [
        {
          "id": "6a4a6416-8610-4eab-abe7-391c581c99a4",
          "name": "ListPermissionsOnADriveItem",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.microsoft.com",
              "path": [
                "drives/:drive-id/items/:item-id/permissions"
              ],
              "variable": [
                {
                  "id": "drive-id",
                  "value": "drive-id",
                  "type": "string"
                },
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
              "id": "b9e753c0-e4ba-46cb-9460-7efe04c66a2b"
            }
          ]
        }
      ]
    }
  ]
}