swagger: "2.0"
x-collection-name: RingCentral
x-complete: 1
info:
  title: RingCentral Connect Platform API Explorer
  description: this-is-an-interactive-api-explorer-for-the-ringcentral-connect-platform--to-use-this-service-you-will-need-to-have-a-developer-account---links--a-hrefhttpsnetstorage-ringcentral-comdpwapiexplorerrcplatform-basic-ymlv20180514092722-target-blankringcentral-api-specaspannbspnbspopenapi-fka-swagger-formatnbspnbspnbspnbspspana-hrefhttpsgithub-comoaiopenapispecification-target-blanklearn-more-about-openapia
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
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/authz-profile/check:
    get:
      summary: Check User Permissions
      description: "Checks if a certain user permission is activated for a particular
        extension.\nUsage Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n
        \  Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter [targetExtensionId]
        value is invalid\n\n\n403\nCMN-404\nAttempt to access another extension\n\n\n404\nCMN-102\nResource
        for parameter [accountId] is not found"
      operationId: checkUserPermission
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidauthzprofilecheck-get
      parameters:
      - in: path
        name: accountId
      - in: path
        name: extensionId
      - in: query
        name: permissionId
      - in: query
        name: targetExtensionId
      responses:
        200:
          description: OK
      tags:
      - Check
      - User
      - Permissions