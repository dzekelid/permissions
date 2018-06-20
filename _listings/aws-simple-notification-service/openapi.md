---
swagger: "2.0"
x-collection-name: AWS Simple Notification Service
x-complete: 1
info:
  title: AWS Simple Notification Service API
  version: 1.0.0
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
      description: Adds a statement to a topic's access control policy, granting access
        for the specified AWS accounts to the specified actions.
      operationId: addPermission
      x-api-path-slug: actionaddpermission-get
      parameters:
      - in: query
        name: ActionName.member.N
        description: The action you want to allow for the specified principal(s)
        type: string
      - in: query
        name: AWSAccountId.member.N
        description: The AWS account IDs of the users (principals) who will be given
          access to the specified actions
        type: string
      - in: query
        name: Label
        description: A unique identifier for the new policy statement
        type: string
      - in: query
        name: TopicArn
        description: The ARN of the topic whose access control policy you wish to
          modify
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions
  /?Action=RemovePermission:
    get:
      summary: Remove Permission
      description: Removes a statement from a topic's access control policy.
      operationId: removePermission
      x-api-path-slug: actionremovepermission-get
      parameters:
      - in: query
        name: Label
        description: The unique label of the statement you want to remove
        type: string
      - in: query
        name: TopicArn
        description: The ARN of the topic whose access control policy you wish to
          modify
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions
---