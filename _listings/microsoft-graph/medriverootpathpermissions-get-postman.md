{
  "info": {
    "name": "Microsoft Graph API List Permissions On A Drive Item",
    "_postman_id": "7d2e221a-c326-4eae-aa0e-86786e10ce03",
    "description": "List permissions on a DriveItem List the effective permissions of on a DriveItem.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "list",
      "item": [
        {
          "id": "696a20e7-fc52-45ca-aa4b-ce4a868ac6ee",
          "name": "ListPermissionsOnADriveItem",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.microsoft.com",
              "path": [
                "me/drive/root:/:path:/permissions"
              ],
              "variable": [
                {
                  "id": "path",
                  "value": "path",
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
              "id": "4f851dc5-6584-48e6-8095-08ceb78cf1bd"
            }
          ]
        }
      ]
    }
  ]
}