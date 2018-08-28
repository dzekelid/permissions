---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez This returns security permissions that a group has on other groups
  version: 1.0.0
  description: This returns security permissions that a group has on other groups.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/teamsecurity/permissionsforgroup:
    get:
      summary: This returns security permissions that a group has on other groups
      description: This returns security permissions that a group has on other groups.
      operationId: TeamGroupSecurity_GetSecurityPermissionsForGroupByteamId
      x-api-path-slug: apiteamsecuritypermissionsforgroup-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: teamId
        description: The id of the group to find permissions for
      responses:
        200:
          description: OK
      tags:
      - This
      - Returns
      - Security
      - Permissions
      - That
      - Group
      - Has
      - "On"
      - Other
      - Groups
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