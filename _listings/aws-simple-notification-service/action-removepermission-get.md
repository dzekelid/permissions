---
swagger: "2.0"
info:
  title: AWS Simple Notification Service API Remove Permission
  version: 1.0.0
  description: Removes a statement from a topic's access control policy.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=RemovePermission:
    get:
      summary: ' Remove Permission '
      description: Removes a statement from a topic's access control policy
      operationId: removePermission
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
      - permissions
definitions: []
x-collection-name: AWS Simple Notification Service
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