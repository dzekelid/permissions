swagger: "2.0"
x-collection-name: Google Cloud Identity Access Management
x-complete: 1
info:
  title: Google Identity and Access Management (IAM)
  description: manages-identity-and-access-control-for-google-cloud-platform-resources-including-the-creation-of-service-accounts-which-you-can-use-to-authenticate-to-google-and-make-api-calls-
  contact:
    name: Google
    url: https://google.com
  version: v1
host: iam.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/{resource}:testIamPermissions:
    post:
      summary: Tests Permissions
      description: |-
        Tests the specified permissions against the IAM access control policy
        for a ServiceAccount.
      operationId: iam.projects.serviceAccounts.testIamPermissions
      x-api-path-slug: v1resourcetestiampermissions-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resource
        description: 'REQUIRED: The resource for which the policy detail is being
          requested'
      responses:
        200:
          description: OK
      tags:
      - Permission