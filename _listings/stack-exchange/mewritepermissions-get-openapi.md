---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 0
info:
  title: Stack Exchange My Write Permissions
  description: "Returns the write permissions a user has via the api, given an access
    token.\n \nThe Stack Exchange API gives users the ability to create, edit, and
    delete certain types. This method returns whether the passed user is capable of
    performing those actions at all, as well as how many times a day they can.\n \nThis
    method does not consider the user's current quota (ie. if they've already exhausted
    it for today) nor any additional restrictions on write access, such as editing
    deleted comments.\n \nThis method returns a list of write_permissions."
  version: "2.0"
host: api.stackexchange.com
basePath: /2.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /me/write-permissions:
    get:
      summary: My Write Permissions
      description: "Returns the write permissions a user has via the api, given an
        access token.\n \nThe Stack Exchange API gives users the ability to create,
        edit, and delete certain types. This method returns whether the passed user
        is capable of performing those actions at all, as well as how many times a
        day they can.\n \nThis method does not consider the user's current quota (ie.
        if they've already exhausted it for today) nor any additional restrictions
        on write access, such as editing deleted comments.\n \nThis method returns
        a list of write_permissions."
      operationId: returns-the-write-permissions-a-user-has-via-the-api-given-an-access-token-the-stack-exchange-api-gi
      x-api-path-slug: mewritepermissions-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Write Permissions
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