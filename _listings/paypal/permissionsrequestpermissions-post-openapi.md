---
swagger: "2.0"
x-collection-name: PayPal
x-complete: 0
info:
  title: Paypal Request Permissions
  description: Use the RequestPermissions API operation to request permissions to
    execute API operations on a PayPal account holder???s behalf.
  version: 1.0.0
host: svcs.sandbox.paypal.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Permissions/CancelPermissions:
    post:
      summary: Cancel Permissions
      description: Use the CancelPermissions API operation to cancel access to a set
        of permissions.
      operationId: Permissions.CancelPermissions.post
      x-api-path-slug: permissionscancelpermissions-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Permissions
  /Permissions/GetPermissions:
    post:
      summary: Get Permissions
      description: Use the GetPermissons API operation to obtain the permissions associated
        with an access token.
      operationId: Permissions.GetPermissions.post
      x-api-path-slug: permissionsgetpermissions-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Permissions
  /Permissions/RequestPermissions:
    post:
      summary: Request Permissions
      description: Use the RequestPermissions API operation to request permissions
        to execute API operations on a PayPal account holder???s behalf.
      operationId: Permissions.RequestPermissions.post
      x-api-path-slug: permissionsrequestpermissions-post
      responses:
        200:
          description: OK
      tags:
      - Payments
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