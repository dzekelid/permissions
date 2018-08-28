swagger: "2.0"
x-collection-name: Dropbox
x-complete: 1
info:
  title: Dropbox Notify Appendix API v1
  description: the-dropbox-notify--is-a-part-of-dropbox-core-ap-with-a-separate-endpoint-for-notification-call-
  termsOfService: https://www.dropbox.com/developers/reference/tos
  contact:
    name: Dropbox
    url: https://www.dropbox.com/developers
  version: 1.0.0
host: api-notify.dropbox.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /members/set_permissions:
    post:
      summary: Set Member Permissions
      description: Set member permissions.
      operationId: postMembersSetPermissions
      x-api-path-slug: membersset-permissions-post
      parameters:
      - in: query
        name: external_id
        description: optional external ID
      - in: query
        name: member_id
        description: optional member ID
      - in: query
        name: new_is_admin
        description: optional change the admin status of the member
      responses:
        200:
          description: OK
      tags:
      - Set
      - Member
      - Permissions