{
  "info": {
    "name": "Facebook Get User Permissions",
    "_postman_id": "e23d1fe3-9084-455e-b4ed-74c9442ebf28",
    "description": "The permissions that user has granted the application.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "User",
      "item": [
        {
          "id": "301d227c-d3ac-4092-9779-e0e5e7d2458e",
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
              "id": "067ba596-ef53-4fbe-8897-03eeb1a25780"
            }
          ]
        }
      ]
    }
  ]
}