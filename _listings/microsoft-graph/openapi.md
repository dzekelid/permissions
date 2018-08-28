swagger: "2.0"
x-collection-name: Microsoft Graph
x-complete: 1
info:
  title: Microsoft Graph API
  description: microsoft-graph-exposes-multiple-apis-from-office-365-and-other-microsoft-cloud-services-through-a-single-endpoint-httpsgraph-microsoft-com--microsoft-graph-simplifies-queries-that-would-otherwise-be-more-complex-
  version: 1.0.0
host: graph.microsoft.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /me/drive/items/{item-id}/permissions:
    get:
      summary: List Permissions On A Drive Item
      description: List permissions on a DriveItem List the effective permissions
        of on a DriveItem.
      operationId: ListPermissionsOnADriveItem
      x-api-path-slug: medriveitemsitemidpermissions-get
      parameters:
      - in: header
        name: if-none-match
        description: If this request header is included and the etag provided matches
          the current etag on the item, an HTTP 304 Not Modified response is returned
        type: string
      - in: path
        name: item-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - List
      - Permissions
      - OnDrive
      - Item
  /me/drive/root:/{path}:/permissions:
    get:
      summary: List Permissions On A Drive Item
      description: List permissions on a DriveItem List the effective permissions
        of on a DriveItem.
      operationId: ListPermissionsOnADriveItem
      x-api-path-slug: medriverootpathpermissions-get
      parameters:
      - in: header
        name: if-none-match
        description: If this request header is included and the etag provided matches
          the current etag on the item, an HTTP 304 Not Modified response is returned
        type: string
      - in: path
        name: path
        type: string
      responses:
        200:
          description: OK
      tags:
      - List
      - Permissions
      - OnDrive
      - Item
  /drives/{drive-id}/items/{item-id}/permissions:
    get:
      summary: List Permissions On A Drive Item
      description: List permissions on a DriveItem List the effective permissions
        of on a DriveItem.
      operationId: ListPermissionsOnADriveItem
      x-api-path-slug: drivesdriveiditemsitemidpermissions-get
      parameters:
      - in: path
        name: drive-id
        type: string
      - in: header
        name: if-none-match
        description: If this request header is included and the etag provided matches
          the current etag on the item, an HTTP 304 Not Modified response is returned
        type: string
      - in: path
        name: item-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - List
      - Permissions
      - OnDrive
      - Item
  /groups/{group-id}/drive/items/{item-id}/permissions:
    get:
      summary: List Permissions On A Drive Item
      description: List permissions on a DriveItem List the effective permissions
        of on a DriveItem.
      operationId: ListPermissionsOnADriveItem
      x-api-path-slug: groupsgroupiddriveitemsitemidpermissions-get
      parameters:
      - in: path
        name: group-id
        type: string
      - in: header
        name: if-none-match
        description: If this request header is included and the etag provided matches
          the current etag on the item, an HTTP 304 Not Modified response is returned
        type: string
      - in: path
        name: item-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - List
      - Permissions
      - OnDrive
      - Item
  /me/drive/items/{item-id}/permissions/{perm-id}:
    delete:
      summary: Delete Permission
      description: Delete permission Remove access to a DriveItem.
      operationId: DeletePermission
      x-api-path-slug: medriveitemsitemidpermissionspermid-delete
      parameters:
      - in: header
        name: if-match
        description: If this request header is included and the eTag (or cTag) provided
          does not match the current tag on the item, a 412 Precondition Failed response
          is returned and the item will not be deleted
        type: string
      - in: path
        name: item-id
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission
    get:
      summary: Get Permission
      description: Get permission Retrieve the properties and relationships of permission
        object.
      operationId: GetPermission
      x-api-path-slug: medriveitemsitemidpermissionspermid-get
      parameters:
      - in: path
        name: item-id
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission
    patch:
      summary: Update Permission
      description: Update permission Update the properties of a permission by patching
        the resource.
      operationId: UpdatePermission
      x-api-path-slug: medriveitemsitemidpermissionspermid-patch
      parameters:
      - in: header
        name: if-match
        description: If this request header is included and the eTag (or cTag) provided
          does not match the current tag on the item, a 412 Precondition Failed response
          is returned and the item will not be deleted
        type: string
      - in: path
        name: item-id
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission
  /me/drive/root:/{path}:/permissions/{perm-id}:
    delete:
      summary: Delete Permission
      description: Delete permission Remove access to a DriveItem.
      operationId: DeletePermission
      x-api-path-slug: medriverootpathpermissionspermid-delete
      parameters:
      - in: header
        name: if-match
        description: If this request header is included and the eTag (or cTag) provided
          does not match the current tag on the item, a 412 Precondition Failed response
          is returned and the item will not be deleted
        type: string
      - in: path
        name: path
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission
    get:
      summary: Get Permission
      description: Get permission Retrieve the properties and relationships of permission
        object.
      operationId: GetPermission
      x-api-path-slug: medriverootpathpermissionspermid-get
      parameters:
      - in: path
        name: path
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission
    patch:
      summary: Update Permission
      description: Update permission Update the properties of a permission by patching
        the resource.
      operationId: UpdatePermission
      x-api-path-slug: medriverootpathpermissionspermid-patch
      parameters:
      - in: header
        name: if-match
        description: If this request header is included and the eTag (or cTag) provided
          does not match the current tag on the item, a 412 Precondition Failed response
          is returned and the item will not be deleted
        type: string
      - in: path
        name: path
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission
  /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}:
    delete:
      summary: Delete Permission
      description: Delete permission Remove access to a DriveItem.
      operationId: DeletePermission
      x-api-path-slug: groupsgroupiddriveitemsitemidpermissionspermid-delete
      parameters:
      - in: path
        name: group-id
        type: string
      - in: header
        name: if-match
        description: If this request header is included and the eTag (or cTag) provided
          does not match the current tag on the item, a 412 Precondition Failed response
          is returned and the item will not be deleted
        type: string
      - in: path
        name: item-id
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission
    get:
      summary: Get Permission
      description: Get permission Retrieve the properties and relationships of permission
        object.
      operationId: GetPermission
      x-api-path-slug: groupsgroupiddriveitemsitemidpermissionspermid-get
      parameters:
      - in: path
        name: group-id
        type: string
      - in: path
        name: item-id
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission
    patch:
      summary: Update Permission
      description: Update permission Update the properties of a permission by patching
        the resource.
      operationId: UpdatePermission
      x-api-path-slug: groupsgroupiddriveitemsitemidpermissionspermid-patch
      parameters:
      - in: path
        name: group-id
        type: string
      - in: header
        name: if-match
        description: If this request header is included and the eTag (or cTag) provided
          does not match the current tag on the item, a 412 Precondition Failed response
          is returned and the item will not be deleted
        type: string
      - in: path
        name: item-id
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission
  /drives/{drive-id}/items/{item-id}/permissions/{perm-id}:
    delete:
      summary: Delete Permission
      description: Delete permission Remove access to a DriveItem.
      operationId: DeletePermission
      x-api-path-slug: drivesdriveiditemsitemidpermissionspermid-delete
      parameters:
      - in: path
        name: drive-id
        type: string
      - in: header
        name: if-match
        description: If this request header is included and the eTag (or cTag) provided
          does not match the current tag on the item, a 412 Precondition Failed response
          is returned and the item will not be deleted
        type: string
      - in: path
        name: item-id
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission
    get:
      summary: Get Permission
      description: Get permission Retrieve the properties and relationships of permission
        object.
      operationId: GetPermission
      x-api-path-slug: drivesdriveiditemsitemidpermissionspermid-get
      parameters:
      - in: path
        name: drive-id
        type: string
      - in: path
        name: item-id
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission
    patch:
      summary: Update Permission
      description: Update permission Update the properties of a permission by patching
        the resource.
      operationId: UpdatePermission
      x-api-path-slug: drivesdriveiditemsitemidpermissionspermid-patch
      parameters:
      - in: path
        name: drive-id
        type: string
      - in: header
        name: if-match
        description: If this request header is included and the eTag (or cTag) provided
          does not match the current tag on the item, a 412 Precondition Failed response
          is returned and the item will not be deleted
        type: string
      - in: path
        name: item-id
        type: string
      - in: path
        name: perm-id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permission