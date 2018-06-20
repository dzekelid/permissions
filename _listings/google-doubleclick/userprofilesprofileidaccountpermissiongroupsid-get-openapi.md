---
swagger: "2.0"
x-collection-name: Google Doubleclick
x-complete: 0
info:
  title: Google Doubleclick API Get Account Permission Group
  version: 1.0.0
  description: Gets one account permission group by ID.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /userprofiles/{profileId}/accountPermissionGroups:
    get:
      summary: Get Account Permission Groups
      description: Retrieves the list of account permission groups.
      operationId: dfareporting.accountPermissionGroups.list
      x-api-path-slug: userprofilesprofileidaccountpermissiongroups-get
      parameters:
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Permissions Group
  /userprofiles/{profileId}/accountPermissionGroups/{id}:
    get:
      summary: Get Account Permission Group
      description: Gets one account permission group by ID.
      operationId: dfareporting.accountPermissionGroups.get
      x-api-path-slug: userprofilesprofileidaccountpermissiongroupsid-get
      parameters:
      - in: path
        name: id
        description: Account permission group ID
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Permissions Group
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