---
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
---