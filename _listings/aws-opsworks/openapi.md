swagger: "2.0"
x-collection-name: AWS OpsWorks
x-complete: 1
info:
  title: AWS OpsWorks API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribePermissions:
    get:
      summary: Describe Permissions
      description: Describes the permissions for a specified stack.
      operationId: describePermissions
      x-api-path-slug: actiondescribepermissions-get
      parameters:
      - in: query
        name: IamUserArn
        description: The users IAM ARN
        type: string
      - in: query
        name: StackId
        description: The stack ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Describe
      - Permissions
  /?Action=SetPermission:
    get:
      summary: Set Permission
      description: Specifies a user's permissions.
      operationId: setPermission
      x-api-path-slug: actionsetpermission-get
      parameters:
      - in: query
        name: AllowSsh
        description: The user is allowed to use SSH to communicate with the instance
        type: string
      - in: query
        name: AllowSudo
        description: The user is allowed to use sudo to elevate privileges
        type: string
      - in: query
        name: IamUserArn
        description: The users IAM ARN
        type: string
      - in: query
        name: Level
        description: The users permission level, which must be set to one of the following
          strings
        type: string
      - in: query
        name: StackId
        description: The stack ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Set
      - Permission