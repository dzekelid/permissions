{
  "info": {
    "name": "Slack Request App Permissions",
    "_postman_id": "ee8b3af6-0a6b-478d-8c8e-079ca2aa7533",
    "description": "Allows an app to request additional scopes",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "messaging",
      "item": [
        {
          "id": "e899b61a-baf2-4020-9367-19ae4d61df22",
          "name": "apps_permissions_request",
          "request": {
            "url": "http://slack.com/api/apps.permissions.request?scopes=%7B%7D&token=%7B%7D&trigger_id=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Allows an app to request additional scopes"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "07973a2a-9d44-402a-871e-c63bf462fa40"
            }
          ]
        }
      ]
    }
  ]
}