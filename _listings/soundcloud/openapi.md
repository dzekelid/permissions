---
swagger: "2.0"
x-collection-name: SoundCloud
x-complete: 1
info:
  title: Sound Cloud
  description: access-host-upload-and-comment-on-audio-
  version: 1.0.0
host: api.soundcloud.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tracks/{track_id}/permissions.json:
    get:
      summary: Get Tracks Track Permissions
      description: Returns all users with permission for a track by track id
      operationId: getTracksTrackPermissions.json
      x-api-path-slug: trackstrack-idpermissions-json-get
      parameters:
      - in: query
        name: consumer_key
      responses:
        200:
          description: OK
      tags:
      - Tracks
      - Track
      - Permissions
    put:
      summary: Put Tracks Track Permissions
      description: Updates the list of permitted users for a track by track id
      operationId: putTracksTrackPermissions.json
      x-api-path-slug: trackstrack-idpermissions-json-put
      responses:
        200:
          description: OK
      tags:
      - Tracks
      - Track
      - Permissions
  /tracks/{track_id}/permissions.{format}:
    get:
      summary: Get Tracks Track Permissions. Format
      description: Returns all users with permission for a track by track id
      operationId: getTracksTrackPermissions.Format
      x-api-path-slug: trackstrack-idpermissions-format-get
      parameters:
      - in: query
        name: consumer_key
        description: Access, host, upload, and comment on audio
      - in: path
        name: track_id
        description: Access, host, upload, and comment on audio
      responses:
        200:
          description: OK
      tags:
      - Tracks
      - Track
      - Permissions
      - ""
      - Format
    put:
      summary: Put Tracks Track Permissions. Format
      description: Updates the list of permitted users for a track by track id
      operationId: putTracksTrackPermissions.Format
      x-api-path-slug: trackstrack-idpermissions-format-put
      parameters:
      - in: path
        name: track_id
        description: Access, host, upload, and comment on audio
      responses:
        200:
          description: OK
      tags:
      - Tracks
      - Track
      - Permissions
      - ""
      - Format
---