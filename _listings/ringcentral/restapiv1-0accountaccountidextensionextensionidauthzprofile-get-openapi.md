---
swagger: "2.0"
x-collection-name: RingCentral
x-complete: 0
info:
  title: RingCentral Get User Permissions
  description: "Returns a list of user permissions granted at authorization procedure.
    Please note: Some permissions may be restricted by extension type.\nUsage Plan
    Group\nMedium\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error Message\n
    \  \n \n\n403\nCMN-404\nAttempt to access another extension\n\n\n404\nCMN-102\nResource
    for parameter [accountId] is not found"
  version: 1.0.0
host: platform.ringcentral.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/authz-profile:
    get:
      summary: Get User Permissions
      description: "Returns a list of user permissions granted at authorization procedure.
        Please note: Some permissions may be restricted by extension type.\nUsage
        Plan Group\nMedium\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n403\nCMN-404\nAttempt to access another extension\n\n\n404\nCMN-102\nResource
        for parameter [accountId] is not found"
      operationId: getAuthorizationProfile
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidauthzprofile-get
      parameters:
      - in: path
        name: accountId
      - in: path
        name: extensionId
      responses:
        200:
          description: OK
      tags:
      - User
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