---
swagger: "2.0"
x-collection-name: AWS Simple Queue Service
x-complete: 0
info:
  title: AWS Simple Queue Service API Remove Permission
  version: 1.0.0
  description: Revokes any permissions in the queue policy that matches the specified
    Label parameter.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AddPermission:
    get:
      summary: Add Permission
      description: Adds a permission to a queue for a specific.
      operationId: addPermission
      x-api-path-slug: actionaddpermission-get
      parameters:
      - in: query
        name: ActionName.N
        description: The action the client wants to allow for the specified principal
        type: string
      - in: query
        name: AWSAccountId.N
        description: The AWS account number of the principal who is given permission
        type: string
      - in: query
        name: Label
        description: The unique identification of the permission youre setting (for
          example, AliceSendMessage)
        type: string
      - in: query
        name: QueueUrl
        description: The URL of the Amazon SQS queue to which permissions are added
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions
  /?Action=RemovePermission:
    get:
      summary: Remove Permission
      description: Revokes any permissions in the queue policy that matches the specified
        Label parameter.
      operationId: removePermission
      x-api-path-slug: actionremovepermission-get
      parameters:
      - in: query
        name: Label
        description: The identification of the permission to remove
        type: string
      - in: query
        name: QueueUrl
        description: The URL of the Amazon SQS queue from which permissions are removed
        type: string
      responses:
        200:
          description: OK
      tags:
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