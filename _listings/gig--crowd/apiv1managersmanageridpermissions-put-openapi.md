---
swagger: "2.0"
x-collection-name: GIG & CROWD
x-complete: 0
info:
  title: GIGANDCROWD Put Managers Managerid Permissions
  version: 1.0.0
  description: Put managers managerid permissions.
host: gigandcrowd.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/managers/{managerId}/permissions:
    put:
      summary: Put Managers Managerid Permissions
      description: Put managers managerid permissions.
      operationId: putApiV1ManagersManagerPermissions
      x-api-path-slug: apiv1managersmanageridpermissions-put
      parameters:
      - in: header
        name: Authorization
      - in: path
        name: managerId
      - in: body
        name: model
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Managers
      - Managerid
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