{
  "info": {
    "name": "Microsoft Graph API List Permissions On A Drive Item",
    "_postman_id": "1da5d3a0-178f-4402-b517-26c4a8598679",
    "description": "List permissions on a DriveItem List the effective permissions of on a DriveItem.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "list",
      "item": [
        {
          "id": "d7f29413-299e-40b8-991b-c57145ba6096",
          "name": "ListPermissionsOnADriveItem",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.microsoft.com",
              "path": [
                "groups/:group-id/drive/items/:item-id/permissions"
              ],
              "variable": [
                {
                  "id": "group-id",
                  "value": "group-id",
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
              "id": "0ee87d67-2299-4e45-a5f4-431cd3df9b7f"
            }
          ]
        }
      ]
    }
  ]
}