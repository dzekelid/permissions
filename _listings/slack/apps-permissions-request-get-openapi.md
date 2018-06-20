---
swagger: "2.0"
x-collection-name: Slack
x-complete: 0
info:
  title: Slack Request App Permissions
  description: Allows an app to request additional scopes
  version: 1.0.3
host: slack.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /apps.permissions.info:
    get:
      summary: App Permissions
      description: Returns list of permissions this app has on a team.
      operationId: apps_permissions_info
      x-api-path-slug: apps-permissions-info-get
      parameters:
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Permissions
  /apps.permissions.request:
    get:
      summary: Request App Permissions
      description: Allows an app to request additional scopes
      operationId: apps_permissions_request
      x-api-path-slug: apps-permissions-request-get
      parameters:
      - in: query
        name: scopes
        description: A comma separated list of scopes to request for
      - in: query
        name: token
        description: Authentication token
      - in: query
        name: trigger_id
        description: Token used to trigger the permissions API
      responses:
        200:
          description: OK
      tags:
      - Messaging
      - Permissions
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---