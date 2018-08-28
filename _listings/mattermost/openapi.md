swagger: "2.0"
x-collection-name: Mattermost
x-complete: 1
info:
  title: Mattermost
  version: 1.0.0
host: your-mattermost-url.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /analytics/old:
    get:
      summary: Get analytics
      description: |-
        Get some analytics data about the system. This endpoint uses the old format, the `/analytics` route is reserved for the new format when it gets implemented.

        The returned JSON changes based on the `name` query parameter but is always key/value pairs.

        __Minimum server version__: 4.0

        ##### Permissions
        Must have `manage_system` permission.
      operationId: get-some-analytics-data-about-the-system-this-endpoint-uses-the-old-format-the-analytics-route-is-re
      x-api-path-slug: analyticsold-get
      parameters:
      - in: query
        name: name
        description: Possible values are standard, post_counts_day, user_counts_with_posts_day
          or extra_counts
      - in: query
        name: team_id
        description: The team ID to filter the data by
      responses:
        200:
          description: OK
      tags:
      - Analytics