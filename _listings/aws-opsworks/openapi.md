---
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
---