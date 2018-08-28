swagger: "2.0"
x-collection-name: Trello
x-complete: 1
info:
  title: Trello
  description: this-document-describes-the-rest-api-of-trello-as-published-by-trello-com---a-hrefhttpstrello-comdocsindex-html-target-blankofficial-documentationa--a-hrefhttpstrello-comdocsapi-target-blankthe-html-pages-that-were-scraped-in-order-to-generate-this-specification-a
  termsOfService: https://trello.com/legal
  contact:
    name: Trello
    url: https://trello.com/home
  version: "1.0"
host: trello.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /boards/{idBoard}/prefs/permissionLevel:
    put:
      summary: Put Boards Preferences Permissionlevel
      description: Put boards preferences permissionlevel.
      operationId: updateBoardsPrefsPermissionLevelByIdBoard
      x-api-path-slug: boardsidboardprefspermissionlevel-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Permission Level to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Preferences
      - Permissionlevel
  /organizations/{idOrg}/prefs/permissionLevel:
    put:
      summary: Put Organizations Preferences Permissionlevel
      description: Put organizations preferences permissionlevel.
      operationId: updateOrganizationsPrefsPermissionLevelByIdOrg
      x-api-path-slug: organizationsidorgprefspermissionlevel-put
      parameters:
      - in: body
        name: body
        description: Attributes of Prefs Permission Level to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Preferences
      - Permissionlevel