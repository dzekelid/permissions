swagger: "2.0"
x-collection-name: Google Drive
x-complete: 1
info:
  title: Google Drive
  description: manages-files-in-drive-including-uploading-downloading-searching-detecting-changes-and-updating-sharing-permissions-
  termsOfService: https://developers.google.com/terms/
  contact:
    name: Google
    url: https://google.com
  version: v3
host: www.googleapis.com
basePath: /drive/v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /files/{fileId}/permissions:
    get:
      summary: Get File Permissions
      description: Lists a file's or Team Drive's permissions.
      operationId: drive.permissions.list
      x-api-path-slug: filesfileidpermissions-get
      parameters:
      - in: path
        name: fileId
        description: The ID of the file or Team Drive
      - in: query
        name: pageSize
        description: The maximum number of permissions to return per page
      - in: query
        name: pageToken
        description: The token for continuing a previous list request on the next
          page
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      - in: query
        name: useDomainAdminAccess
        description: Whether the request should be treated as if it was issued by
          a domain administrator; if set to true, then the requester will be granted
          access if they are an administrator of the domain to which the item belongs
      responses:
        200:
          description: OK
      tags:
      - Permission
    post:
      summary: Create File Permission
      description: Creates a permission for a file or Team Drive.
      operationId: drive.permissions.create
      x-api-path-slug: filesfileidpermissions-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: emailMessage
        description: A custom message to include in the notification email
      - in: path
        name: fileId
        description: The ID of the file or Team Drive
      - in: query
        name: sendNotificationEmail
        description: Whether to send a notification email when sharing to users or
          groups
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      - in: query
        name: transferOwnership
        description: Whether to transfer ownership to the specified user and downgrade
          the current owner to a writer
      - in: query
        name: useDomainAdminAccess
        description: Whether the request should be treated as if it was issued by
          a domain administrator; if set to true, then the requester will be granted
          access if they are an administrator of the domain to which the item belongs
      responses:
        200:
          description: OK
      tags:
      - Permission
  /files/{fileId}/permissions/{permissionId}:
    delete:
      summary: Delete File Permission
      description: Deletes a permission.
      operationId: drive.permissions.delete
      x-api-path-slug: filesfileidpermissionspermissionid-delete
      parameters:
      - in: path
        name: fileId
        description: The ID of the file or Team Drive
      - in: path
        name: permissionId
        description: The ID of the permission
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      - in: query
        name: useDomainAdminAccess
        description: Whether the request should be treated as if it was issued by
          a domain administrator; if set to true, then the requester will be granted
          access if they are an administrator of the domain to which the item belongs
      responses:
        200:
          description: OK
      tags:
      - Permission
    get:
      summary: Get File Permission
      description: Gets a permission by ID.
      operationId: drive.permissions.get
      x-api-path-slug: filesfileidpermissionspermissionid-get
      parameters:
      - in: path
        name: fileId
        description: The ID of the file
      - in: path
        name: permissionId
        description: The ID of the permission
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      - in: query
        name: useDomainAdminAccess
        description: Whether the request should be treated as if it was issued by
          a domain administrator; if set to true, then the requester will be granted
          access if they are an administrator of the domain to which the item belongs
      responses:
        200:
          description: OK
      tags:
      - Permission
    patch:
      summary: Update File Permission
      description: Updates a permission with patch semantics.
      operationId: drive.permissions.update
      x-api-path-slug: filesfileidpermissionspermissionid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: fileId
        description: The ID of the file or Team Drive
      - in: path
        name: permissionId
        description: The ID of the permission
      - in: query
        name: removeExpiration
        description: Whether to remove the expiration date
      - in: query
        name: supportsTeamDrives
        description: Whether the requesting application supports Team Drives
      - in: query
        name: transferOwnership
        description: Whether to transfer ownership to the specified user and downgrade
          the current owner to a writer
      - in: query
        name: useDomainAdminAccess
        description: Whether the request should be treated as if it was issued by
          a domain administrator; if set to true, then the requester will be granted
          access if they are an administrator of the domain to which the item belongs
      responses:
        200:
          description: OK
      tags:
      - Permission