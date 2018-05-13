{
  "info": {
    "name": "Slack App Permissions",
    "_postman_id": "22d2e50d-bf6e-423a-aa0c-1f7f5eaef260",
    "description": "Returns list of permissions this app has on a team.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "cf1661f4-3374-450d-9212-c76155bc09c6",
          "name": "apps_permissions_info",
          "request": {
            "url": "http://slack.com/api/apps.permissions.info?token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns list of permissions this app has on a team"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "97498d07-e2a1-40de-9048-8284f96ca6e6"
            }
          ]
        }
      ]
    }
  ]
}