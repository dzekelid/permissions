swagger: "2.0"
x-collection-name: GIG & CROWD
x-complete: 1
info:
  title: GIG & Crowd
  version: 1.0.0
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