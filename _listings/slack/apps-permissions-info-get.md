---
swagger: "2.0"
info:
  title: Slack
  description: One way to interact with the Slack platform is its HTTP RPC-based Web
    API, a collection of methods requiring OAuth 2.0-based user, bot, or workspace
    tokens blessed with related OAuth scopes.
  version: 1.0.3
host: slack.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /apps.permissions.info:
    get:
      summary: App Permissions
      description: Returns list of permissions this app has on a team
      operationId: apps_permissions_info
      parameters:
      - in: query
        name: token
        description: Authentication token
      responses:
        200:
          description: OK
      tags:
      - messaging
      - permissions
definitions:
  objs_im:
    properties:
      is_org_shared:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      is_user_deleted:
        description: This is a default description.
        type: post
      priority:
        description: This is a default description.
        type: post
      is_im:
        description: This is a default description.
        type: post
  objs_paging:
    properties:
      count:
        description: This is a default description.
        type: post
      total:
        description: This is a default description.
        type: post
      page:
        description: This is a default description.
        type: post
      pages:
        description: This is a default description.
        type: post
  objs_file:
    properties:
      image_exif_rotation:
        description: This is a default description.
        type: post
      filetype:
        description: This is a default description.
        type: post
      channels:
        description: This is a default description.
        type: post
      display_as_bot:
        description: This is a default description.
        type: post
      thumb_64:
        description: This is a default description.
        type: post
      size:
        description: This is a default description.
        type: post
      original_h:
        description: This is a default description.
        type: post
      thumb_360_w:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
      url_private:
        description: This is a default description.
        type: post
  objs_user_profile:
    properties:
      last_name:
        description: This is a default description.
        type: post
      status_emoji:
        description: This is a default description.
        type: post
      display_name_normalized:
        description: This is a default description.
        type: post
      image_32:
        description: This is a default description.
        type: post
      skype:
        description: This is a default description.
        type: post
      image_72:
        description: This is a default description.
        type: post
      image_192:
        description: This is a default description.
        type: post
      first_name:
        description: This is a default description.
        type: post
      display_name:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  objs_team_profile_field:
    properties:
      hint:
        description: This is a default description.
        type: post
      ordering:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
      possible_values:
        description: This is a default description.
        type: post
      label:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      is_hidden:
        description: This is a default description.
        type: post
      field_name:
        description: This is a default description.
        type: post
      options:
        description: This is a default description.
        type: post
  objs_comment:
    properties:
      comment:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      timestamp:
        description: This is a default description.
        type: post
      is_intro:
        description: This is a default description.
        type: post
      user:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
  objs_channel:
    properties:
      is_general:
        description: This is a default description.
        type: post
      name_normalized:
        description: This is a default description.
        type: post
      is_member:
        description: This is a default description.
        type: post
      is_archived:
        description: This is a default description.
        type: post
      topic:
        description: This is a default description.
        type: post
      unread_count_display:
        description: This is a default description.
        type: post
      is_org_shared:
        description: This is a default description.
        type: post
      is_channel:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      priority:
        description: This is a default description.
        type: post
  objs_group:
    properties:
      is_pending_ext_shared:
        description: This is a default description.
        type: post
      name_normalized:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      is_moved:
        description: This is a default description.
        type: post
      is_mpim:
        description: This is a default description.
        type: post
      is_archived:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      is_group:
        description: This is a default description.
        type: post
      topic:
        description: This is a default description.
        type: post
      unread_count:
        description: This is a default description.
        type: post
  objs_user_profile_short:
    properties:
      first_name:
        description: This is a default description.
        type: post
      display_name:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      real_name:
        description: This is a default description.
        type: post
      avatar_hash:
        description: This is a default description.
        type: post
      is_ultra_restricted:
        description: This is a default description.
        type: post
      is_restricted:
        description: This is a default description.
        type: post
      image_72:
        description: This is a default description.
        type: post
  objs_team:
    properties:
      domain:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      email_domain:
        description: This is a default description.
        type: post
      has_compliance_export:
        description: This is a default description.
        type: post
      icon:
        description: This is a default description.
        type: post
  objs_message:
    properties:
      attachments:
        description: This is a default description.
        type: post
      text:
        description: This is a default description.
        type: post
      topic:
        description: This is a default description.
        type: post
      reply_count:
        description: This is a default description.
        type: post
      replies:
        description: This is a default description.
        type: post
      subscribed:
        description: This is a default description.
        type: post
      icons:
        description: This is a default description.
        type: post
      purpose:
        description: This is a default description.
        type: post
      subtype:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
x-collection-name: Slack
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