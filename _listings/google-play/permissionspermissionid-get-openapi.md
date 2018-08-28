---
swagger: "2.0"
x-collection-name: Google Play
x-complete: 0
info:
  title: Google Play Get Permissions
  version: 1.0.0
  description: Retrieves details of an Android app permission for display to an enterprise
    admin.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /enterprises/{enterpriseId}/products/{productId}/permissions:
    get:
      summary: Retrieves the Android App Permission
      description: Retrieves the Android app permissions required by this app.
      operationId: androidenterprise.products.getPermissions
      x-api-path-slug: enterprisesenterpriseidproductsproductidpermissions-get
      parameters:
      - in: path
        name: enterpriseId
        description: The ID of the enterprise
      - in: path
        name: productId
        description: The ID of the product
      responses:
        200:
          description: OK
      tags:
      - Permission
  /permissions/{permissionId}:
    get:
      summary: Get Permissions
      description: Retrieves details of an Android app permission for display to an
        enterprise admin.
      operationId: androidenterprise.permissions.get
      x-api-path-slug: permissionspermissionid-get
      parameters:
      - in: query
        name: language
        description: The BCP47 tag for the users preferred language (e
      - in: path
        name: permissionId
        description: The ID of the permission
      responses:
        200:
          description: OK
      tags:
      - Permission
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