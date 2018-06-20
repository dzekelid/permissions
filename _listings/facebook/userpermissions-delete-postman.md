{
  "info": {
    "name": "Facebook Delete User Permissions",
    "_postman_id": "e4e08055-f5ec-48ad-8198-be21f33bc4be",
    "description": "De-authorizes an application or revokes a specific extended permissions on behalf of a user",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "User",
      "item": [
        {
          "id": "051f4db3-25af-407d-942c-9e743f346e4e",
          "name": "getUserPermissions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/permissions"
              ],
              "variable": [
                {
                  "id": "user",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The permissions that user has granted the application."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ff0b19b5-726b-4cd8-92f2-0091aadb47c5"
            }
          ]
        },
        {
          "id": "e2a1d594-55c2-4095-ae50-3910ef1fe51c",
          "name": "deleteUserPermissions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/permissions"
              ],
              "query": [
                {
                  "key": "permission",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "user",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "De-authorizes an application or revokes a specific extended permissions on behalf of a user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f528e736-a237-4951-a6df-21b094b8f45f"
            }
          ]
        }
      ]
    }
  ]
}