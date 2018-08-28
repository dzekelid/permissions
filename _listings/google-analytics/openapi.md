swagger: "2.0"
x-collection-name: Google Analytics
x-complete: 1
info:
  title: Google Analytics
  description: views-and-manages-your-google-analytics-data-
  contact:
    name: Google
    url: https://google.com
  version: v3
host: www.googleapis.com
basePath: /analytics/v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /management/accounts/{accountId}/entityUserLinks/{linkId}:
    put:
      summary: Update Permissions
      description: Updates permissions for an existing user on the given account.
      operationId: analytics.management.accountUserLinks.update
      x-api-path-slug: managementaccountsaccountidentityuserlinkslinkid-put
      parameters:
      - in: path
        name: accountId
        description: Account ID to update the account-user link for
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: linkId
        description: Link ID to update the account-user link for
      responses:
        200:
          description: OK
      tags:
      - Permission
  /management/accounts/{accountId}/webproperties/{webPropertyId}/entityUserLinks/{linkId}:
    put:
      summary: Update Permission
      description: Updates permissions for an existing user on the given web property.
      operationId: analytics.management.webpropertyUserLinks.update
      x-api-path-slug: managementaccountsaccountidwebpropertieswebpropertyidentityuserlinkslinkid-put
      parameters:
      - in: path
        name: accountId
        description: Account ID to update the account-user link for
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: linkId
        description: Link ID to update the account-user link for
      - in: path
        name: webPropertyId
        description: Web property ID to update the account-user link for
      responses:
        200:
          description: OK
      tags:
      - Permission
  /management/accounts/{accountId}/webproperties/{webPropertyId}/profiles/{profileId}/entityUserLinks/{linkId}:
    put:
      summary: Update Permissions
      description: Updates permissions for an existing user on the given view (profile).
      operationId: analytics.management.profileUserLinks.update
      x-api-path-slug: managementaccountsaccountidwebpropertieswebpropertyidprofilesprofileidentityuserlinkslinkid-put
      parameters:
      - in: path
        name: accountId
        description: Account ID to update the user link for
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: linkId
        description: Link ID to update the user link for
      - in: path
        name: profileId
        description: View (Profile ID) to update the user link for
      - in: path
        name: webPropertyId
        description: Web Property ID to update the user link for
      responses:
        200:
          description: OK
      tags:
      - Permission