swagger: "2.0"
x-collection-name: AWS EC2 Systems Manager
x-complete: 1
info:
  title: AWS EC2 Systems Manager API
  version: 1.0.0
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