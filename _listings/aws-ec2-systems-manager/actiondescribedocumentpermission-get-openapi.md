---
swagger: "2.0"
x-collection-name: AWS EC2 Systems Manager
x-complete: 0
info:
  title: Amazon EC2 Systems Manager API Describe Document Permission
  version: 1.0.0
  description: Describes the permissions for an SSM document.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeDocumentPermission:
    get:
      summary: Describe Document Permission
      description: Describes the permissions for an SSM document.
      operationId: describeDocumentPermission
      x-api-path-slug: actiondescribedocumentpermission-get
      parameters:
      - in: query
        name: Name
        description: The name of the document for which you are the owner
        type: string
      - in: query
        name: PermissionType
        description: The permission type for the document
        type: string
      responses:
        200:
          description: OK
      tags:
      - Document
      - Permission
  /?Action=ModifyDocumentPermission:
    get:
      summary: Modify Document Permission
      description: Share a document publicly or privately.
      operationId: modifyDocumentPermission
      x-api-path-slug: actionmodifydocumentpermission-get
      parameters:
      - in: query
        name: AccountIdsToAdd
        description: The AWS user accounts that should have access to the document
        type: string
      - in: query
        name: AccountIdsToRemove
        description: The AWS user accounts that should no longer have access to the
          document
        type: string
      - in: query
        name: Name
        description: The name of the document that you want to share
        type: string
      - in: query
        name: PermissionType
        description: The permission type for the document
        type: string
      responses:
        200:
          description: OK
      tags:
      - Modify
      - Document
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