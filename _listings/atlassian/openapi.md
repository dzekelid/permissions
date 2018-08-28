swagger: "2.0"
x-collection-name: Atlassian
x-complete: 1
info:
  title: Stride API
  description: this-service-provides-public-api-for-the-stride-
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/filter/{id}/permission:
    get:
      summary: Get share permissions
      description: Returns the share permissions for a filter. A filter can be shared
        with groups, projects, all logged-in users, or the public. Sharing with all
        logged-in users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getSharePermissions_get
      x-api-path-slug: api2filteridpermission-get
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Share
      - Permissions
    post:
      summary: Add share permission
      description: "Add a share permissions to a filter. If you add a global share
        permission (i.e., all logged-in users or the public) it will overwrite all
        share permissions for the filter.  \nBe aware that this method uses different
        objects for updating share permissions compared to [Update filter](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-id-put).
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Share
        dashboards and filters_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
        and the calling user must own the filter."
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.addSharePermission_post
      x-api-path-slug: api2filteridpermission-post
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Share
      - Permission
  /api/2/mypermissions:
    get:
      summary: Get my permissions
      description: |-
        Checks whether the current user has the given permissions. You can optionally provide a specific context to get permissions for (`projectKey` OR `projectId` OR `issueKey` OR `issueId`)

        If there is no context provided, then the project related permissions will return true if the user has that permission in ANY project.

        If a project context is provided, project related permissions will return true if the user has the permissions in the specified project. For permissions that are determined using issue data (e.g Current Assignee), true will be returned if the user meets the permission criteria in ANY issue in that project.

        If an issue context is provided, it will return whether or not the user has each permission in that specific issue.

        The above means that for issue-level permissions (EDIT_ISSUE for example), hasPermission may be true when no context is provided, or when a project context is provided, **but** may be false for any given (or all) issues. This would occur (for example) if Reporters were given the EDIT_ISSUE permission. This is because any user could be a reporter, except in the context of a concrete issue, where the reporter is known.

        Global permissions work in the same way regardless of the scope.
      operationId: com.atlassian.jira.rest.v2.permission.PermissionsResource.getMyPermissions_get
      x-api-path-slug: api2mypermissions-get
      parameters:
      - in: query
        name: issueId
        description: Id of the issue to scope returned permissions for
      - in: query
        name: issueKey
        description: Key of the issue to scope returned permissions for
      - in: query
        name: permissions
        description: A comma separated list of permission keys to check
      - in: query
        name: projectId
        description: Id of project to scope returned permissions for
      - in: query
        name: projectKey
        description: Key of project to scope returned permissions for
      responses:
        200:
          description: OK
      tags:
      - My
      - Permissions
  /api/2/permissions:
    get:
      summary: Get all permissions
      description: Returns all permissions that are present in the Jira instance -
        Global, Project and the global ones added by plugins
      operationId: com.atlassian.jira.rest.v2.permission.PermissionsResource.getAllPermissions_get
      x-api-path-slug: api2permissions-get
      responses:
        200:
          description: OK
      tags:
      - Permissions
  /api/2/user/permission/search:
    get:
      summary: Find users with permissions
      description: |-
        Returns a list of users who fulfill both of these criteria:

        *   their user attributes match a search string.
        *   they have a set of permissions for a project or issue.

        If no search string is provided, a list of all users with the permissions is returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   Get users for any project, _Administer Jira_ [global permission](href=).
        *   Get users for a project, _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg) for the project.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.findUsersWithAllPermissions_get
      x-api-path-slug: api2userpermissionsearch-get
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: issueKey
        description: The issue key for the issue
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: permissions
        description: A comma-separated list of permissions
      - in: query
        name: projectKey
        description: The project key for the project (case sensitive)
      - in: query
        name: query
        description: A search input that is matched against appropriate user attributes
          to find relevant users
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      - in: query
        name: username
        description: The search string
      responses:
        200:
          description: OK
      tags:
      - Find
      - Users
      - Permissions
  /api/2/filter/{id}/permission/{permissionId}:
    get:
      summary: Get share permission
      description: Returns a share permission for a filter. A filter can be shared
        with groups, projects, all logged-in users, or the public. Sharing with all
        logged-in users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getSharePermission_get
      x-api-path-slug: api2filteridpermissionpermissionid-get
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      - in: path
        name: permissionId
        description: The ID of the share permission
      responses:
        200:
          description: OK
      tags:
      - Share
      - Permission
    delete:
      summary: Delete share permission
      description: Deletes a share permission from a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
        and the calling user must own the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.deleteSharePermission_delete
      x-api-path-slug: api2filteridpermissionpermissionid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      - in: path
        name: permissionId
        description: The ID of the share permission
      responses:
        200:
          description: OK
      tags:
      - Share
      - Permission
  /api/2/permissionscheme:
    get:
      summary: Get all permission schemes
      description: |-
        Returns all permission schemes.

        ### About permission schemes and grants

        A permission scheme is a collection of permission grants. A permission grant consists of a `holder` and a `permission`.

        #### Holder

        The `holder` object contains information about the user or group being granted the permission. For example, the _Administer projects_ permission is granted to a group named _Teams in space administrators_. In this case, the type is `"type": "group"`, and the parameter is the group name, `"parameter": "Teams in space administrators"`. The `holder` object is defined by the following properties:

        *   `type` Identifies the user or group (see the list of types below).
        *   `parameter` The value of this property depends on the `type`. For example, if the `type` is a group, then you need to specify the group name.

        The following `types` are available. The expected values for the `parameter` are given in parenthesis (some `types` may not have a `parameter`):

        *   `anyone` Grant for anonymous users.
        *   `applicationRole` Grant for users with access to the specified application (application name). See [Manage application access](https://confluence.atlassian.com/cloud/manage-application-access-744721629.html) for more information.
        *   `assignee` Grant for the user currently assigned to an issue.
        *   `group` Grant for the specified group (group name).
        *   `groupCustomField` Grant for a user in the group selected in the specified custom field (custom field ID).
        *   `projectLead` Grant for a project lead.
        *   `projectRole` Grant for the specified project role (project role ID).
        *   `reporter` Grant for the user who reported the issue.
        *   `sd.customer.portal.only` Jira Service Desk only. Grants customers permission to access the customer portal but not Jira. See [Customizing Jira Service Desk permissions](https://confluence.atlassian.com/x/24dKLg) for more information.
        *   `user` Grant for the specified user (user ID).
        *   `userCustomField` Grant for a user selected in the specified custom field (custom field ID).

        #### Permissions

        The [built-in Jira permissions](https://confluence.atlassian.com/x/yodKLg) are listed below. Apps can also define custom permissions. See the [project permission](https://developer.atlassian.com/cloud/jira/platform/modules/project-permission/) and [global permission](https://developer.atlassian.com/cloud/jira/platform/modules/global-permission/) module documentation for more information.

        **Project permissions**

        *   `ADMINISTER_PROJECTS`
        *   `BROWSE_PROJECTS`
        *   `MANAGE_SPRINTS_PERMISSION` (Jira Software only)
        *   `SERVICEDESK_AGENT` (Jira Service Desk only)
        *   `VIEW_DEV_TOOLS` (Jira Software only)
        *   `VIEW_READONLY_WORKFLOW`

        **Issue permissions**

        *   `ASSIGNABLE_USER`
        *   `ASSIGN_ISSUES`
        *   `CLOSE_ISSUES`
        *   `CREATE_ISSUES`
        *   `DELETE_ISSUES`
        *   `EDIT_ISSUES`
        *   `LINK_ISSUES`
        *   `MODIFY_REPORTER`
        *   `MOVE_ISSUES`
        *   `RESOLVE_ISSUES`
        *   `SCHEDULE_ISSUES`
        *   `SET_ISSUE_SECURITY`
        *   `TRANSITION_ISSUES`

        **Voters and watchers permissions**

        *   `MANAGE_WATCHERS`
        *   `VIEW_VOTERS_AND_WATCHERS`

        **Comments permissions**

        *   `ADD_COMMENTS`
        *   `DELETE_ALL_COMMENTS`
        *   `DELETE_OWN_COMMENTS`
        *   `EDIT_ALL_COMMENTS`
        *   `EDIT_OWN_COMMENTS`

        **Attachments permissions**

        *   `CREATE_ATTACHMENTS`
        *   `DELETE_ALL_ATTACHMENTS`
        *   `DELETE_OWN_ATTACHMENTS`

        **Time tracking permissions**

        *   `DELETE_ALL_WORKLOGS`
        *   `DELETE_OWN_WORKLOGS`
        *   `EDIT_ALL_WORKLOGS`
        *   `EDIT_OWN_WORKLOGS`
        *   `WORK_ON_ISSUES`

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getAllPermissionSchemes_g
      x-api-path-slug: api2permissionscheme-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Schemes
    post:
      summary: Create permission scheme
      description: Creates a new permission scheme. You can create a permission scheme
        with or without defining a set of permission grants. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.createPermissionScheme_po
      x-api-path-slug: api2permissionscheme-post
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
  /api/2/permissionscheme/{schemeId}:
    get:
      summary: Get permission scheme
      description: Returns a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionScheme_get
      x-api-path-slug: api2permissionschemeschemeid-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: schemeId
        description: The ID of the permission scheme to return (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
    put:
      summary: Update permission scheme
      description: |-
        Updates a permission scheme. Below are some important things to note when using this resource:

        *   If a permissions list is present in the request, then it will be set in the permission scheme, overwriting _all existing_ grants.
        *   If you want to update only the name and description, then do not send a permissions list in the request.
        *   Sending an empty list will remove all permission grants from the permission scheme.

        If you want to add or delete a single permission grant instead of updating the whole list, see [Create permission grant](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-post) or [Delete permission scheme entity](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-permissionId-delete). See [About permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes) for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.updatePermissionScheme_pu
      x-api-path-slug: api2permissionschemeschemeid-put
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: schemeId
        description: The ID of the permission scheme to update (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
    delete:
      summary: Delete permission scheme
      description: Deletes a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.deletePermissionScheme_de
      x-api-path-slug: api2permissionschemeschemeid-delete
      parameters:
      - in: path
        name: schemeId
        description: The ID of the permission scheme being deleted (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
  /api/2/permissionscheme/{schemeId}/permission:
    get:
      summary: Get permission scheme grants
      description: Returns all permission grants for a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionSchemeGrants
      x-api-path-slug: api2permissionschemeschemeidpermission-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: schemeId
        description: The ID of the permission scheme (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
      - Grants
    post:
      summary: Create permission grant
      description: Creates a new permission grant in the given permission scheme.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
        Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.createPermissionGrant_pos
      x-api-path-slug: api2permissionschemeschemeidpermission-post
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: schemeId
        description: The ID of the permission scheme in which to create a new permission
          grant
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Grant
  /api/2/permissionscheme/{schemeId}/permission/{permissionId}:
    get:
      summary: Get permission scheme grant
      description: Returns a permission grant. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionSchemeGrant_
      x-api-path-slug: api2permissionschemeschemeidpermissionpermissionid-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: permissionId
        description: The ID of the permission grant (e
      - in: path
        name: schemeId
        description: The ID of the permission scheme (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
      - Grant
    delete:
      summary: Delete permission scheme entity
      description: Deletes a permission grant from a permission scheme. See [About
        permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes)
        for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.deletePermissionSchemeEnt
      x-api-path-slug: api2permissionschemeschemeidpermissionpermissionid-delete
      parameters:
      - in: path
        name: permissionId
        description: The ID of the permission grant to delete (e
      - in: path
        name: schemeId
        description: The ID of the permission scheme to delete the permission grant
          from (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
      - Entity
  /api/2/project/{projectKeyOrId}/permissionscheme:
    get:
      summary: Get assigned permission scheme
      description: |-
        Gets the [permission scheme](https://confluence.atlassian.com/x/yodKLg) associated with the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)
      operationId: com.atlassian.jira.rest.v2.permission.ProjectPermissionSchemeResource.getAssignedPermissionScheme_ge
      x-api-path-slug: api2projectprojectkeyoridpermissionscheme-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Assigned
      - Permission
      - Scheme
    put:
      summary: Assign permission scheme
      description: |-
        Associates a permission scheme with a particular project. See [Managing project permissions](https://confluence.atlassian.com/x/yodKLg) for more information about permission schemes.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
      operationId: com.atlassian.jira.rest.v2.permission.ProjectPermissionSchemeResource.assignPermissionScheme_put
      x-api-path-slug: api2projectprojectkeyoridpermissionscheme-put
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Permission
      - Scheme
  /api/2/user/viewissue/search:
    get:
      summary: Find users with browse permission
      description: |-
        Returns a list of users who fulfill both of these criteria:

        *   their user attributes match a search string.
        *   they have permission to browse issues.

        Use this resource to find users who can browse:

        *   an issue, by providing the `issueKey`.
        *   any issue in a project, by providing the `projectKey`.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.findUsersWithBrowsePermission_get
      x-api-path-slug: api2userviewissuesearch-get
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: issueKey
        description: The issue key for the issue
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: projectKey
        description: The project key for the project (case sensitive)
      - in: query
        name: query
        description: A search input that is matched against appropriate user attributes
          to find relevant users
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      - in: query
        name: username
        description: The search string
      responses:
        200:
          description: OK
      tags:
      - Find
      - Users
      - Browse
      - Permission
  /api/2/attachment/meta:
    get:
      summary: Get global attachment settings
      description: "Returns the global attachment settings, that is, whether attachments
        are enabled and the maximum attachment size allowed.  \n  \nNote that there
        are also [project permissions](https://confluence.atlassian.com/x/yodKLg)
        that restrict whether users can create and delete attachments or not.  \n
        \ \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        None."
      operationId: com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.getAttachmentMeta_get
      x-api-path-slug: api2attachmentmeta-get
      responses:
        200:
          description: OK
      tags:
      - Global
      - Attachment
      - Settings
  /api/2/attachment/{id}:
    get:
      summary: Get attachment metadata
      description: "Returns the metadata for an attachment. Note that the attachment
        itself is not returned.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        issue that the attachment belongs to."
      operationId: com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.getAttachment_get
      x-api-path-slug: api2attachmentid-get
      parameters:
      - in: path
        name: id
        description: The ID of the attachment
      responses:
        200:
          description: OK
      tags:
      - Attachment
      - Metadata
    delete:
      summary: Delete attachment
      description: "Deletes an attachment from an issue.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Any of the following permissions in the project that the issue
        is in:\n\n*   _Delete own attachments_ [project permission](https://confluence.atlassian.com/x/yodKLg)
        to delete an attachment created by the calling user.\n*   _Delete all attachments_
        [project permission](https://confluence.atlassian.com/x/yodKLg) to delete
        an attachment created by any user."
      operationId: com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.removeAttachment_delete
      x-api-path-slug: api2attachmentid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the attachment
      responses:
        200:
          description: OK
      tags:
      - Attachment
  /api/2/attachment/{id}/expand/human:
    get:
      summary: Get all metadata for an expanded attachment
      description: "Returns the metadata for the contents of an attachment, if it
        is an archive, and metadata for the attachment itself. For example, if the
        attachment is a ZIP archive, then information about the files in the archive
        is returned and metadata for the ZIP archive. Currently, only the ZIP archive
        format is supported.  \n  \nUse this method to retrieve data that is presented
        in the UI, as this method returns the metadata for the attachment itself,
        such as the attachment's ID and name. Otherwise, use [Get contents metadata
        for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-raw-get),
        which only returns the metadata for the attachment's contents.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        issue that the attachment belongs to."
      operationId: com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.expandAttachmentForHumans_get
      x-api-path-slug: api2attachmentidexpandhuman-get
      parameters:
      - in: path
        name: id
        description: The ID of the attachment
      responses:
        200:
          description: OK
      tags:
      - Metadataan
      - Expanded
      - Attachment
  /api/2/attachment/{id}/expand/raw:
    get:
      summary: Get contents metadata for an expanded attachment
      description: "Returns the metadata for the contents of an attachment, if it
        is an archive. For example, if the attachment is a ZIP archive, then information
        about the files in the archive is returned. Currently, only the ZIP archive
        format is supported.  \n  \nUse this method if you are processing the data
        without presenting it in the UI, as this method only returns the metadata
        for the contents of the attachment. Otherwise, to retrieve data to present
        in the UI, use [Get all metadata for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-human-get)
        which also returns the metadata for the attachment itself, such as the attachment's
        ID and name.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        issue that the attachment belongs to."
      operationId: com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.expandAttachmentForMachines_get
      x-api-path-slug: api2attachmentidexpandraw-get
      parameters:
      - in: path
        name: id
        description: The ID of the attachment
      responses:
        200:
          description: OK
      tags:
      - Contents
      - Metadataan
      - Expanded
      - Attachment
  /api/2/component:
    post:
      summary: Create component
      description: |-
        Creates a component. Use components to provide containers for issues within a project. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

        *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
        *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ComponentResource.createComponent_post
      x-api-path-slug: api2component-post
      parameters:
      - in: header
        name: force-account-id
      responses:
        200:
          description: OK
      tags:
      - Component
  /api/2/component/{id}:
    get:
      summary: Get component
      description: 'Returns a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required: _Browse projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).'
      operationId: com.atlassian.jira.rest.v2.issue.ComponentResource.getComponent_get
      x-api-path-slug: api2componentid-get
      parameters:
      - in: path
        name: id
        description: The ID of the component
      responses:
        200:
          description: OK
      tags:
      - Component
    put:
      summary: Update component
      description: |-
        Modifies a component. Any fields included in the request are overwritten. If `leadUserName` is an empty string ("") the component lead is removed. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

        *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
        *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ComponentResource.updateComponent_put
      x-api-path-slug: api2componentid-put
      parameters:
      - in: header
        name: force-account-id
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Component
    delete:
      summary: Delete component
      description: |-
        Deletes a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

        *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
        *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ComponentResource.deleteComponent_delete
      x-api-path-slug: api2componentid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the component
      - in: query
        name: moveIssuesTo
        description: The ID of the component to replace the deleted component
      responses:
        200:
          description: OK
      tags:
      - Component
  /api/2/component/{id}/relatedIssueCounts:
    get:
      summary: Get component issues count
      description: Returns the counts of issues assigned to the component. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira.
      operationId: com.atlassian.jira.rest.v2.issue.ComponentResource.getComponentRelatedIssues_get
      x-api-path-slug: api2componentidrelatedissuecounts-get
      parameters:
      - in: path
        name: id
        description: The ID of the component
      responses:
        200:
          description: OK
      tags:
      - Component
      - Issues
      - Count
  /api/2/configuration:
    get:
      summary: Get global settings
      description: "Returns the [global settings](https://confluence.atlassian.com/x/qYXKM)
        in Jira. These settings determine whether optional features (for example,
        sub-tasks, time tracking, and others) are enabled. If time tracking is enabled,
        this method also returns the time tracking configuration.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.ConfigurationResource.getConfiguration_get
      x-api-path-slug: api2configuration-get
      responses:
        200:
          description: OK
      tags:
      - Global
      - Settings
  /api/2/configuration/timetracking:
    get:
      summary: Get selected time tracking provider
      description: "Returns the time tracking provider that is currently selected.
        Note that if time tracking is disabled, then a successful but empty response
        is returned.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.getSelectedTimeTrackingImplementa
      x-api-path-slug: api2configurationtimetracking-get
      responses:
        200:
          description: OK
      tags:
      - Selected
      - Time
      - Tracking
      - Provider
    put:
      summary: Select time tracking provider
      description: "Selects a time tracking provider.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.selectTimeTrackingImplementation_
      x-api-path-slug: api2configurationtimetracking-put
      responses:
        200:
          description: OK
      tags:
      - Select
      - Time
      - Tracking
      - Provider
    delete:
      summary: Disable time tracking
      description: "Disables time tracking.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.disableTimeTracking_delete
      x-api-path-slug: api2configurationtimetracking-delete
      responses:
        200:
          description: OK
      tags:
      - Disable
      - Time
      - Tracking
  /api/2/configuration/timetracking/list:
    get:
      summary: Get all time tracking providers
      description: "Returns all time tracking providers. By default, Jira only has
        one time tracking provider: _JIRA provided time tracking_. However, you can
        install other time tracking providers via apps from the Atlassian Marketplace.
        For more information on time tracking providers, see the documentation for
        the [Time Tracking Provider](https://developer.atlassian.com/cloud/jira/platform/modules/time-tracking-provider/)
        module.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.getAvailableTimeTrackingImplement
      x-api-path-slug: api2configurationtimetrackinglist-get
      responses:
        200:
          description: OK
      tags:
      - Time
      - Tracking
      - Providers
  /api/2/configuration/timetracking/options:
    get:
      summary: Get time tracking settings
      description: "Returns the time tracking settings. This includes settings such
        as the time format, default time unit, and others. For more information, see
        [Configuring time tracking](https://confluence.atlassian.com/x/qoXKM).  \n
        \ \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.getSharedTimeTrackingConfiguratio
      x-api-path-slug: api2configurationtimetrackingoptions-get
      responses:
        200:
          description: OK
      tags:
      - Time
      - Tracking
      - Settings
    put:
      summary: Set time tracking settings
      description: "Sets the time tracking settings.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.setSharedTimeTrackingConfiguratio
      x-api-path-slug: api2configurationtimetrackingoptions-put
      responses:
        200:
          description: OK
      tags:
      - Set
      - Time
      - Tracking
      - Settings
  /api/2/customFieldOption/{id}:
    get:
      summary: Get custom field option
      description: "Returns a custom field option. For example, an option in a cascading
        select list.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** None."
      operationId: com.atlassian.jira.rest.v2.issue.customfield.CustomFieldOptionResource.getCustomFieldOption_get
      x-api-path-slug: api2customfieldoptionid-get
      parameters:
      - in: path
        name: id
        description: The ID of the custom field option
      responses:
        200:
          description: OK
      tags:
      - Custom
      - Field
      - Option
  /api/2/dashboard:
    get:
      summary: Get all dashboards
      description: "Returns a list of dashboards owned by or shared with the user.
        The list may be filtered to include only favorite or owned dashboards.  \n
        \ \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        Permission to access Jira."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardResource.getAllDashboards_get
      x-api-path-slug: api2dashboard-get
      parameters:
      - in: query
        name: filter
        description: The filter applied to the list of dashboards
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      responses:
        200:
          description: OK
      tags:
      - Dashboards
  /api/2/dashboard/{dashboardId}/items/{itemId}/properties:
    get:
      summary: Get dashboard item property keys
      description: "Returns the keys of all properties for a dashboard item.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira. However, to get the property keys the
        user must be the owner of the dashboard or be shared the dashboard. Note,
        users with the _Administer Jira_ [global permission](href=) are considered
        owners of the System dashboard. The System dashboard is considered to be shared
        with all other users."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.getDashboardItemPropertyKeys_get
      x-api-path-slug: api2dashboarddashboardiditemsitemidproperties-get
      parameters:
      - in: path
        name: dashboardId
        description: The ID of the dashboard
      - in: path
        name: itemId
        description: The ID of the dashboard item
      responses:
        200:
          description: OK
      tags:
      - Dashboard
      - Item
      - Property
      - Keys
  /api/2/dashboard/{dashboardId}/items/{itemId}/properties/{propertyKey}:
    get:
      summary: Get dashboard item property
      description: "Returns the key and value of a dashboard item property.  \n  \nA
        dashboard item enables an app to add user-specific information to a user dashboard.
        Dashboard items are exposed to users as gadgets that users can add to their
        dashboards. For more information on how users do this, see [Adding and customizing
        gadgets](https://confluence.atlassian.com/x/7AeiLQ).  \n  \nWhen an app creates
        a dashboard item it registers a callback to receive the dashboard item ID.
        The callback fires whenever the item is rendered or, where the item is configurable,
        the user edits the item. The app then uses this resource to store the item's
        content or configuration details. For more information on working with dashboard
        items, see [Building a dashboard item for a JIRA Connect add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/)
        and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/)
        documentation.  \n  \nThere is no resource to set or get dashboard items.
        \ \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        Permission to access Jira. However, to get a dashboard item property the user
        must be the owner of the dashboard or be shared the dashboard. Note, users
        with the _Administer Jira_ [global permission](href=) are considered owners
        of the System dashboard. The System dashboard is considered to be shared with
        all other users."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.getDashboardItemProperty_get
      x-api-path-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-get
      parameters:
      - in: path
        name: dashboardId
        description: The ID of the dashboard
      - in: path
        name: itemId
        description: The ID of the dashboard item
      - in: path
        name: propertyKey
        description: The key of the dashboard item property
      responses:
        200:
          description: OK
      tags:
      - Dashboard
      - Item
      - Property
    put:
      summary: Set dashboard item property
      description: "Sets the value of a dashboard item property. Use this resource
        in apps to store custom data against a dashboard item.  \n  \nA dashboard
        item enables an app to add user-specific information to a user dashboard.
        Dashboard items are exposed to users as gadgets that users can add to their
        dashboards. For more information on how users do this, see [Adding and customizing
        gadgets](https://confluence.atlassian.com/x/7AeiLQ).  \n  \nWhen an app creates
        a dashboard item it registers a callback to receive the dashboard item ID.
        The callback fires whenever the item is rendered or, where the item is configurable,
        the user edits the item. The app then uses this resource to store the item's
        content or configuration details. For more information on working with dashboard
        items, see [Building a dashboard item for a JIRA Connect add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/)
        and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/)
        documentation.  \n  \nThere is no resource to set or get dashboard items.
        \ \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        Permission to access Jira. However, to set a dashboard item property the user
        must be the owner of the dashboard. Note, users with the _Administer Jira_
        [global permission](href=) are considered owners of the System dashboard.
        \ \n  \nThe value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627),
        non-empty JSON blob. The maximum length is 32768 bytes."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.setDashboardItemProperty_put
      x-api-path-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-put
      parameters:
      - in: path
        name: dashboardId
        description: The ID of the dashboard
      - in: path
        name: itemId
        description: The ID of the dashboard item
      - in: path
        name: propertyKey
        description: The key of the dashboard item property
      responses:
        200:
          description: OK
      tags:
      - Set
      - Dashboard
      - Item
      - Property
    delete:
      summary: Delete dashboard item property
      description: "Deletes a dashboard item property.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira. However, to delete a dashboard item
        property the user must be the owner of the dashboard. Note, users with the
        _Administer Jira_ [global permission](href=) are considered owners of the
        System dashboard."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.deleteDashboardItemProperty_delet
      x-api-path-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-delete
      parameters:
      - in: path
        name: dashboardId
        description: The ID of the dashboard
      - in: path
        name: itemId
        description: The ID of the dashboard item
      - in: path
        name: propertyKey
        description: The key of the dashboard item property
      responses:
        200:
          description: OK
      tags:
      - Dashboard
      - Item
      - Property
  /api/2/dashboard/{id}:
    get:
      summary: Get dashboard
      description: "Returns a dashboard.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira. However, to get a dashboard, the dashboard
        must be shared with the user or the user must own it. Note, users with the
        _Administer Jira_ [global permission](href=) are considered owners of the
        System dashboard. The System dashboard is considered to be shared with all
        other users."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardResource.getDashboard_get
      x-api-path-slug: api2dashboardid-get
      parameters:
      - in: path
        name: id
        description: The ID of the dashboard
      responses:
        200:
          description: OK
      tags:
      - Dashboard
  /api/2/field:
    get:
      summary: Get fields
      description: |-
        Returns all issue fields in Jira, both system and custom fields.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the following rules apply:

        *   Fields that cannot be added to the issue navigator are always returned.
        *   Fields that cannot be placed on an issue screen are always returned.
        *   Fields that depend on global Jira settings are only returned if the setting is enabled. That is, timetracking fields, subtasks, votes, and watches.
        *   For all other fields, this method only returns the fields that the current user has permission to see (that is, the field can be used in at least one project that the user can see).
      operationId: com.atlassian.jira.rest.v2.issue.FieldResource.getFields_get
      x-api-path-slug: api2field-get
      responses:
        200:
          description: OK
      tags:
      - Fields
    post:
      summary: Create custom field
      description: |-
        Creates a custom field.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.issue.FieldResource.createCustomField_post
      x-api-path-slug: api2field-post
      responses:
        200:
          description: OK
      tags:
      - Custom
      - Field
  /api/2/field/{fieldKey}/option:
    get:
      summary: Get all issue field options
      description: |-
        Returns all options defined for a select list issue field. A select list issue field is a type of [issue field](https://developer.atlassian.com/cloud/jira/platform/modules/issue-field/) that allows a user to select an value from a list of options.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getAllIssueFieldOptions_get
      x-api-path-slug: api2fieldfieldkeyoption-get
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: startAt
        description: The starting index of the returned objects
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Field
      - Options
    post:
      summary: Create issue field option
      description: |-
        Creates an option for a select list issue field.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.createIssueFieldOption_post
      x-api-path-slug: api2fieldfieldkeyoption-post
      parameters:
      - in: path
        name: fieldKey
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Field
      - Option
  /api/2/field/{fieldKey}/option/suggestions/edit:
    get:
      summary: Get selectable issue field options
      description: |-
        Returns options defined for a select list issue field that can be viewed and selected by the currently logged in user.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getSelectableIssueFieldOptions_get
      x-api-path-slug: api2fieldfieldkeyoptionsuggestionsedit-get
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: projectId
        description: Filters the results to options that are only available in the
          specified project
      - in: query
        name: startAt
        description: The starting index of the returned objects
      responses:
        200:
          description: OK
      tags:
      - Selectable
      - Issue
      - Field
      - Options
  /api/2/field/{fieldKey}/option/suggestions/search:
    get:
      summary: Get visible issue field options
      description: |-
        Returns options defined for a select list issue field that can be viewed by the currently logged in user.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getVisibleIssueFieldOptions_get
      x-api-path-slug: api2fieldfieldkeyoptionsuggestionssearch-get
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: projectId
        description: Filters the results to options that are only available in the
          specified project
      - in: query
        name: startAt
        description: The starting index of the returned objects
      responses:
        200:
          description: OK
      tags:
      - Visible
      - Issue
      - Field
      - Options
  /api/2/field/{fieldKey}/option/{optionId}:
    get:
      summary: Get issue field option
      description: |-
        Returns an option from a select list issue field.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getIssueFieldOption_get
      x-api-path-slug: api2fieldfieldkeyoptionoptionid-get
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: path
        name: optionId
        description: The ID of the option to be returned
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Field
      - Option
    put:
      summary: Update issue field option
      description: |-
        Updates an option for a select list issue field. If the option does not exist, a new option is created.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.updateIssueFieldOption_put
      x-api-path-slug: api2fieldfieldkeyoptionoptionid-put
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: path
        name: optionId
        description: The ID of the option to be updated
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Field
      - Option
    delete:
      summary: Delete issue field option
      description: |-
        Deletes an option from a select list issue field.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.deleteIssueFieldOption_delete
      x-api-path-slug: api2fieldfieldkeyoptionoptionid-delete
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: path
        name: optionId
        description: The ID of the option to be deleted
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Field
      - Option
  /api/2/field/{fieldKey}/option/{optionId}/issue:
    delete:
      summary: Replace issue field option
      description: |-
        Deselects a select list issue field option in all issues that it has been selected in. A different option can be selected to replace the deselected option. The update can also be limited to a smaller set of issues by using a JQL query.

        This is an [asynchronous method](#async). The response object will contain a link to the long-running task. For example, _https://your-domain.atlassian.net/rest/api/2/task/10127_.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.replaceIssueFieldOption_delete
      x-api-path-slug: api2fieldfieldkeyoptionoptionidissue-delete
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: query
        name: jql
        description: A JQL query that specifies the issues to be updated
      - in: path
        name: optionId
        description: The ID of the option to be deselected
      - in: query
        name: replaceWith
        description: The ID of the option that will replace the currently selected
          option
      responses:
        200:
          description: OK
      tags:
      - Replace
      - Issue
      - Field
      - Option
  /api/2/filter:
    get:
      summary: Get filters
      description: |-
        Returns all filters. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned:

        *   Filters owned by the user.
        *   Filters shared with a group that the user is a member of.
        *   Filters shared with a private project that the user can browse.
        *   Filters shared with a public project, even if the user is anonymous.
        *   Filters shared with the public, even if the user is anonymous.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getFilters_get
      x-api-path-slug: api2filter-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      responses:
        200:
          description: OK
      tags:
      - Filters
    post:
      summary: Create filter
      description: Creates a new filter. The new filter is not shared and not selected
        as a favorite. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.createFilter_post
      x-api-path-slug: api2filter-post
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      responses:
        200:
          description: OK
      tags:
      - Filter
  /api/2/filter/defaultShareScope:
    get:
      summary: Get default share scope
      description: Returns the default sharing settings for new filters and dashboards
        for a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getDefaultShareScope_get
      x-api-path-slug: api2filterdefaultsharescope-get
      responses:
        200:
          description: OK
      tags:
      - Default
      - Share
      - Scope
    put:
      summary: Set default share scope
      description: Sets the default sharing for new filters and dashboards for a user.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
        to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.setDefaultShareScope_put
      x-api-path-slug: api2filterdefaultsharescope-put
      responses:
        200:
          description: OK
      tags:
      - Set
      - Default
      - Share
      - Scope
  /api/2/filter/favourite:
    get:
      summary: Get favourite filters
      description: Returns the favorite filters of the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getFavouriteFilters_get
      x-api-path-slug: api2filterfavourite-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      responses:
        200:
          description: OK
      tags:
      - Favourite
      - Filters
  /api/2/filter/my:
    get:
      summary: Get my filters
      description: Returns the filters owned by the calling user. If `includeFavourites`
        is `true`, the user's favorite filters are also returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getMyFilters_get
      x-api-path-slug: api2filtermy-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: includeFavourites
        description: Include the users favorite filters in the response
      responses:
        200:
          description: OK
      tags:
      - My
      - Filters
  /api/2/filter/search:
    get:
      summary: Search for filters
      description: |-
        Search for filters. This method is similar to [Get filters](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-get) except that you can refine the results to include filters that have specific attributes. For example, filters with a particular name. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned (if no search parameters are set):

        *   Filters owned by the user.
        *   Filters shared with a group that the user is a member of.
        *   Filters shared with a private project that the user can browse.
        *   Filters shared with a public project, even if the user is anonymous.
        *   Filters shared with the public, even if the user is anonymous.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getFiltersPaginated_get
      x-api-path-slug: api2filtersearch-get
      parameters:
      - in: query
        name: accountId
        description: Returns filters with an owner that exactly matches `accountId`
          of the owner
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: filterName
        description: Returns filters with a name that partially matches `filterName`
      - in: header
        name: force-account-id
      - in: query
        name: groupname
        description: Returns filters that are shared with a group that has a name
          that exactly matches `groupname`
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: orderBy
        description: '[Orders](https://developer'
      - in: query
        name: owner
        description: Returns filters with an owner that exactly matches `owner`
      - in: query
        name: projectId
        description: Returns filters that are shared with a project that has an ID
          that exactly matches `projectId`
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      responses:
        200:
          description: OK
      tags:
      - Searchfilters
  /api/2/filter/{id}:
    get:
      summary: Get filter
      description: Returns a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission view the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getFilter_get
      x-api-path-slug: api2filterid-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the filter to return
      responses:
        200:
          description: OK
      tags:
      - Filter
    put:
      summary: Update filter
      description: |-
        Updates an existing filter. Use this method to update a filter's name, description, JQL, or sharing. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can update:

        *   Private filters (i.e., not shared) can only be updated by the creator of the filter.
        *   Shared filters can only be updated by the creator of the filter or a Jira administrator.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.updateFilter_put
      x-api-path-slug: api2filterid-put
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the filter to update
      responses:
        200:
          description: OK
      tags:
      - Filter
    delete:
      summary: Delete filter
      description: |-
        Delete a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can delete:

        *   Private filters (i.e., not shared) can only be deleted by the creator of the filter.
        *   Shared filters can only be deleted by the creator of the filter or a Jira administrator.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.deleteFilter_delete
      x-api-path-slug: api2filterid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the filter to delete
      responses:
        200:
          description: OK
      tags:
      - Filter
  /api/2/filter/{id}/columns:
    get:
      summary: Get columns
      description: Returns the columns configured for a filter. The column configuration
        is used when the filter's results are viewed in _List View_ with the _Columns_
        set to _Filter_. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getColumns_get
      x-api-path-slug: api2filteridcolumns-get
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Columns
    put:
      summary: Set columns
      description: Sets the columns for a filter. Only navigable fields can be set
        as columns. Use [Get fields](https://developer.atlassian.com/cloud/jira/platform/rest#api-api-2-field-get)
        to get the list fields in Jira. A navigable field has `navigable` set to `true`.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
        to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
        and permission to view the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.setColumns_put
      x-api-path-slug: api2filteridcolumns-put
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Set
      - Columns
    delete:
      summary: Reset columns
      description: Reset the user's column configuration for the filter to the default.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
        to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
        and permission to view the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.resetColumns_delete
      x-api-path-slug: api2filteridcolumns-delete
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Reset
      - Columns
  /api/2/filter/{id}/favourite:
    put:
      summary: Add filter as favorite
      description: Add a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
        and permission to view the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.setFavouriteForFilter_put
      x-api-path-slug: api2filteridfavourite-put
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Filter
      - As
      - Favorite
    delete:
      summary: Remove filter as favorite
      description: Removes a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
        and permission to view the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.deleteFavouriteForFilter_delete
      x-api-path-slug: api2filteridfavourite-delete
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Filter
      - As
      - Favorite
  /api/2/group:
    get:
      summary: Get group
      description: |-
        This resource is deprecated, use [`group/member`](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-group-member-get).

        Returns all users in a group.

        **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.getGroup_get
      x-api-path-slug: api2group-get
      parameters:
      - in: query
        name: expand
        description: List of fields to expand
      - in: query
        name: groupname
        description: The name of the group
      responses:
        200:
          description: OK
      tags:
      - Group
    post:
      summary: Create group
      description: |-
        Creates a group.

        **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.createGroup_post
      x-api-path-slug: api2group-post
      responses:
        200:
          description: OK
      tags:
      - Group
    delete:
      summary: Remove group
      description: |-
        Deletes a group.

        **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.removeGroup_delete
      x-api-path-slug: api2group-delete
      parameters:
      - in: query
        name: groupname
        description: The name of the group
      - in: query
        name: swapGroup
        description: The group to transfer restrictions to
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Group
  /api/2/group/member:
    get:
      summary: Get users from group
      description: |-
        Returns all users in a group. Users are ordered by username.

        **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.getUsersFromGroup_get
      x-api-path-slug: api2groupmember-get
      parameters:
      - in: query
        name: groupname
        description: The name of the group
      - in: query
        name: includeInactiveUsers
        description: Include inactive users
      - in: query
        name: maxResults
        description: The maximum number of users to return per page
      - in: query
        name: startAt
        description: The index of the first user to return
      responses:
        200:
          description: OK
      tags:
      - Users
      - From
      - Group
  /api/2/group/user:
    post:
      summary: Add user to group
      description: |-
        Adds a user to a group.

        **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.addUserToGroup_post
      x-api-path-slug: api2groupuser-post
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: groupname
        description: The name of the group
      responses:
        200:
          description: OK
      tags:
      - User
      - To
      - Group
    delete:
      summary: Remove user from group
      description: Removes a user from a group. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
        _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.removeUserFromGroup_delete
      x-api-path-slug: api2groupuser-delete
      parameters:
      - in: query
        name: accountid
        description: The account id of the user to remove
      - in: header
        name: force-account-id
      - in: query
        name: groupname
        description: The name of the group
      - in: query
        name: username
        description: The username of the user to remove
      responses:
        200:
          description: OK
      tags:
      - Remove
      - User
      - From
      - Group
  /api/2/issuetype:
    get:
      summary: Get all issue types for user
      description: Returns all issue types. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira, however, only issue types that are
        visible to the user are returned.
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.getIssueAllTypes_get
      x-api-path-slug: api2issuetype-get
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Typesuser
    post:
      summary: Create issue type
      description: Creates an issue type and adds it to the default issue type scheme.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
        Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.createIssueType_post
      x-api-path-slug: api2issuetype-post
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
  /api/2/issuetype/{id}:
    get:
      summary: Get issue type
      description: |-
        Returns an issue type. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:

        *   _Administer Jira_ [global permission](href=) to get the details of any issue type.
        *   _Browse projects_ project permission to get the details of any issue type associated with the projects the user has permission to browse.
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.getIssueType_get
      x-api-path-slug: api2issuetypeid-get
      parameters:
      - in: path
        name: id
        description: The ID of the issue type
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
    put:
      summary: Update issue type
      description: Updates the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.updateIssueType_put
      x-api-path-slug: api2issuetypeid-put
      parameters:
      - in: path
        name: id
        description: The ID of the issue type
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
    delete:
      summary: Delete issue type
      description: Deletes the issue type. If the issue type is in use, all uses are
        updated with the alternative issue type (`alternativeIssueTypeId`). A list
        of alternative issue types can be obtained from the [Get alternative issue
        types](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-alternatives-get)
        resource. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        _Administer Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.deleteIssueType_delete
      x-api-path-slug: api2issuetypeid-delete
      parameters:
      - in: query
        name: alternativeIssueTypeId
        description: The ID of the replacement issue type
      - in: path
        name: id
        description: The ID of the issue type
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
  /api/2/issuetype/{id}/alternatives:
    get:
      summary: Get alternative issue types
      description: Returns a list of issue types that can be used to replace the issue
        type. The alternative issue types are those assigned to the same workflow
        scheme, field configuration scheme, and screen scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira.
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.getAlternativeIssueTypes_get
      x-api-path-slug: api2issuetypeidalternatives-get
      parameters:
      - in: path
        name: id
        description: The ID of the issue type
      responses:
        200:
          description: OK
      tags:
      - Alternative
      - Issue
      - Types
  /api/2/issuetype/{id}/avatar2:
    post:
      summary: Create issue type avatar
      description: |-
        Creates an avatar for the issue type. Specify the avatar's local file location as binary data in the body of the request. Also, include the following headers:

        *   `X-Atlassian-Token: no-check`
        *   `Content-Type: image/_image type_` Valid image types are JPEG, GIF, or PNG.

        For example: `curl --request POST \ --user email@example.com: \ --header 'X-Atlassian-Token: no-check' \ --header 'Content-Type: image/< image_type>' \ --data-binary "" \ --url 'https://your-domain.atlassian.net/rest/api/2/issuetype/{issueTypeId}'This` The avatar is cropped to a square. If no crop parameters are specified, the square originates at the top left of the image. The length of the square's sides is set to the smaller of the height or width of the image. The cropped image is then used to create avatars of 16x16, 24x24, 32x32, and 48x48 in size. After creating the avatar, use [Update issue type](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-put) to set it as the issue type's active avatar. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.createIssueTypeAvatar_post
      x-api-path-slug: api2issuetypeidavatar2-post
      parameters:
      - in: path
        name: id
        description: The ID of the issue type
      - in: query
        name: size
        description: The length of each side of the crop region
      - in: query
        name: x
        description: The X coordinate of the top-left corner of the crop region
      - in: query
        name: "y"
        description: The Y coordinate of the top-left corner of the crop region
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
      - Avatar
  /api/2/issuetype/{issueTypeId}/properties:
    get:
      summary: Get issue type property keys
      description: |-
        Returns all the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys of the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   _Administer Jira_ [global permission](href=) to get the property keys of any issue type.
        *   _Browse projects_ project permission to get the property keys of any issue types associated with the projects the user has permission to browse.
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.getIssueTypePropertyKeys_get
      x-api-path-slug: api2issuetypeissuetypeidproperties-get
      parameters:
      - in: path
        name: issueTypeId
        description: The ID of the issue type
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
      - Property
      - Keys
  /api/2/issuetype/{issueTypeId}/properties/{propertyKey}:
    get:
      summary: Get issue type property
      description: |-
        Returns the key and value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:

        *   _Administer Jira_ [global permission](href=) to get the details of any issue type.
        *   _Browse projects_ project permission to get the details of any issue types associated with the projects the user has permission to browse.
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.getIssueTypeProperty_get
      x-api-path-slug: api2issuetypeissuetypeidpropertiespropertykey-get
      parameters:
      - in: path
        name: issueTypeId
        description: The ID of the issue type
      - in: path
        name: propertyKey
        description: The key of the property
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
      - Property
    put:
      summary: Set issue type property
      description: Creates or updates the value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).
        Use this resource to store and update data against an issue type. The value
        of the request body must be a [valid](http://tools.ietf.org/html/rfc4627),
        non-empty JSON blob. The maximum length of the property value is 32768 bytes.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
        Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.setIssueTypeProperty_put
      x-api-path-slug: api2issuetypeissuetypeidpropertiespropertykey-put
      parameters:
      - in: path
        name: issueTypeId
        description: The ID of the issue type
      - in: path
        name: propertyKey
        description: The key of the issue type property
      responses:
        200:
          description: OK
      tags:
      - Set
      - Issue
      - Type
      - Property
    delete:
      summary: Delete issue type property
      description: Deletes the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
        Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.deleteIssueTypeProperty_delete
      x-api-path-slug: api2issuetypeissuetypeidpropertiespropertykey-delete
      parameters:
      - in: path
        name: issueTypeId
        description: The ID of the issue type
      - in: path
        name: propertyKey
        description: The key of the property
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
      - Property
  /api/2/notificationscheme:
    get:
      summary: Get notification schemes paginated
      description: |-
        Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) list of [notification schemes](https://confluence.atlassian.com/x/8YdKLg) in order by display name.

        ### About notification schemes

        A notification scheme is a list of events and recipients who will receive notifications for those events. The list is contained within the `notificationSchemeEvents` object and contains pairs of `events` and `notifications`:

        *   `event` Identifies the type of event. The events can be [Jira system events](https://confluence.atlassian.com/x/8YdKLg#Creatinganotificationscheme-eventsEvents) or [custom events](https://confluence.atlassian.com/x/AIlKLg).
        *   `notifications` Identifies the [recipients](https://confluence.atlassian.com/x/8YdKLg#Creatinganotificationscheme-recipientsRecipients) of notifications for each event. Recipients can be any of the following types:

        *   `CurrentAssignee`
        *   `Reporter`
        *   `CurrentUser`
        *   `ProjectLead`
        *   `ComponentLead`
        *   `User` (the `parameter` is the user key)
        *   `Group` (the `parameter` is the group name)
        *   `ProjectRole` (the `parameter` is the project role ID)
        *   `EmailAddress`
        *   `AllWatchers`
        *   `UserCustomField` (the `parameter` is the ID of the custom field)
        *   `GroupCustomField`(the `parameter` is the ID of the custom field)

        _Note that you should allow for events without recipients to appear in responses._

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the requesting user must have permission to administer at least one project associated with a notification scheme for it to be returned.
      operationId: com.atlassian.jira.rest.v2.notification.NotificationSchemeResource.getNotificationSchemes_get
      x-api-path-slug: api2notificationscheme-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      responses:
        200:
          description: OK
      tags:
      - Notification
      - Schemes
      - Paginated
  /api/2/notificationscheme/{id}:
    get:
      summary: Get notification scheme
      description: |-
        Returns a [notification scheme](https://confluence.atlassian.com/x/8YdKLg), including the list of events and the recipients who will receive notifications for those events.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the requesting user must have permission to administer at least one project associated with the requested notification scheme.
      operationId: com.atlassian.jira.rest.v2.notification.NotificationSchemeResource.getNotificationScheme_get
      x-api-path-slug: api2notificationschemeid-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the notification scheme
      responses:
        200:
          description: OK
      tags:
      - Notification
      - Scheme
  /api/2/project:
    get:
      summary: Get all projects
      description: |-
        Returns all projects visible to the currently logged in user. For projects to be visible, the authenticated user must be granted either _Browse projects_ or _Administer projects_ permissions. If no user is logged in, it returns all projects that are visible for anonymous users.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getAllProjects_get
      x-api-path-slug: api2project-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: recent
        description: Returns the most recently accessed projects for the current user
      responses:
        200:
          description: OK
      tags:
      - Projects
    post:
      summary: Create project
      description: |-
        Creates a new project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.createProject_post
      x-api-path-slug: api2project-post
      parameters:
      - in: header
        name: force-account-id
      responses:
        200:
          description: OK
      tags:
      - Project
  /api/2/project/type:
    get:
      summary: Get all project types
      description: |-
        Returns all [project types](https://confluence.atlassian.com/x/Var1Nw), whether or not the instance has a valid license for each type.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.project.type.ProjectTypeResource.getAllProjectTypes_get
      x-api-path-slug: api2projecttype-get
      responses:
        200:
          description: OK
      tags:
      - Project
      - Types
  /api/2/project/type/{projectTypeKey}:
    get:
      summary: Get project type by key
      description: |-
        Returns a [project type](https://confluence.atlassian.com/x/Var1Nw).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.project.type.ProjectTypeResource.getProjectTypeByKey_get
      x-api-path-slug: api2projecttypeprojecttypekey-get
      parameters:
      - in: path
        name: projectTypeKey
        description: The key of the project type
      responses:
        200:
          description: OK
      tags:
      - Project
      - Type
      - By
      - Key
  /api/2/project/type/{projectTypeKey}/accessible:
    get:
      summary: Get accessible project type by key
      description: |-
        Returns a [project type](https://confluence.atlassian.com/x/Var1Nw) if it is accessible to the logged in user.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.project.type.ProjectTypeResource.getAccessibleProjectTypeByKey_get
      x-api-path-slug: api2projecttypeprojecttypekeyaccessible-get
      parameters:
      - in: path
        name: projectTypeKey
        description: The key of the project type
      responses:
        200:
          description: OK
      tags:
      - Accessible
      - Project
      - Type
      - By
      - Key
  /api/2/project/{projectIdOrKey}:
    get:
      summary: Get project
      description: |-
        Returns the [project details](https://confluence.atlassian.com/x/ahLpNw) for the specified project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getProject_get
      x-api-path-slug: api2projectprojectidorkey-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
    put:
      summary: Update project
      description: |-
        Updates the [project details](https://confluence.atlassian.com/x/ahLpNw) of an existing project.

        All parameters are optional in the body of the request.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.updateProject_put
      x-api-path-slug: api2projectprojectidorkey-put
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: header
        name: force-account-id
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
    delete:
      summary: Delete project
      description: |-
        Deletes an existing project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.deleteProject_delete
      x-api-path-slug: api2projectprojectidorkey-delete
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
  /api/2/project/{projectIdOrKey}/component:
    get:
      summary: Get project components paginated
      description: |-
        Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all components existing in a single project. See the [Get project components](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-components-get) resource if you want to get a full list of versions without pagination.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectComponentsPaginated_get
      x-api-path-slug: api2projectprojectidorkeycomponent-get
      parameters:
      - in: query
        name: maxResults
        description: The maximum number of components to return per page
      - in: query
        name: orderBy
        description: '[Order](https://developer'
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: query
        name: query
        description: Filter the results using a literal string
      - in: query
        name: startAt
        description: The starting index of the returned list of components
      responses:
        200:
          description: OK
      tags:
      - Project
      - Components
      - Paginated
  /api/2/project/{projectIdOrKey}/components:
    get:
      summary: Get project components
      description: |-
        Returns all components existing in a single project. See the [Get project components paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-component-get) resource if you want to get a full list of components with pagination.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectComponents_get
      x-api-path-slug: api2projectprojectidorkeycomponents-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Components
  /api/2/project/{projectIdOrKey}/properties:
    get:
      summary: Get project property keys
      description: |-
        Returns all [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys for the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.getProjectPropertyKeys_get
      x-api-path-slug: api2projectprojectidorkeyproperties-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Property
      - Keys
  /api/2/project/{projectIdOrKey}/properties/{propertyKey}:
    get:
      summary: Get project property
      description: |-
        Returns the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.getProjectProperty_get
      x-api-path-slug: api2projectprojectidorkeypropertiespropertykey-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: path
        name: propertyKey
        description: The project property key
      responses:
        200:
          description: OK
      tags:
      - Project
      - Property
    put:
      summary: Set project property
      description: |-
        Sets the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). You can use project properties to store custom data against the project.

        The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 bytes.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.setProjectProperty_put
      x-api-path-slug: api2projectprojectidorkeypropertiespropertykey-put
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: path
        name: propertyKey
        description: The key of the project property
      responses:
        200:
          description: OK
      tags:
      - Set
      - Project
      - Property
    delete:
      summary: Delete project property
      description: |-
        Removes the [property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) from the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.deleteProjectProperty_delete
      x-api-path-slug: api2projectprojectidorkeypropertiespropertykey-delete
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: path
        name: propertyKey
        description: The project property key
      responses:
        200:
          description: OK
      tags:
      - Project
      - Property
  /api/2/project/{projectIdOrKey}/role:
    get:
      summary: Get project roles for project
      description: |-
        Returns a list of [project roles](https://confluence.atlassian.com/x/3odKLg) for the project.

        Note that all project roles are shared with all projects in Jira Cloud. See the [Get all project roles](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-get) resource for more information.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.getProjectRoles_get
      x-api-path-slug: api2projectprojectidorkeyrole-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Rolesproject
  /api/2/project/{projectIdOrKey}/role/{id}:
    get:
      summary: Get project role for project
      description: |-
        Returns the project role's details and actors associated with the project. The list of actors is sorted by display name.

        If you would like to check to see whether a user belongs to a role based on their group memberships, use the [Get user](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-user-get) resource with the `groups` expand parameter selected. Then check whether the user keys and groups match with the actors returned for the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.getProjectRole_get
      x-api-path-slug: api2projectprojectidorkeyroleid-get
      parameters:
      - in: path
        name: id
        description: The ID of the project role
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Roleproject
    post:
      summary: Add actors to project role
      description: |-
        Adds additional actors to a project role for the project.

        If you want to replace all actors for the project, then use [Set actors for project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-put).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.addActorUsers_post
      x-api-path-slug: api2projectprojectidorkeyroleid-post
      parameters:
      - in: header
        name: force-account-id
      - in: path
        name: id
        description: The ID of the project role
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Actors
      - To
      - Project
      - Role
    put:
      summary: Set actors for project role
      description: |-
        Associates actors with the project role for the project, replacing all existing actors.

        If you want to add actors to the project without overwriting the existing list, then use [Add actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-post).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.setActors_put
      x-api-path-slug: api2projectprojectidorkeyroleid-put
      parameters:
      - in: header
        name: force-account-id
      - in: path
        name: id
        description: The ID of the project role
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Set
      - Actorsproject
      - Role
    delete:
      summary: Delete actors from project role
      description: |-
        Deletes actors from a project role for the project.

        If you want to remove default actors from the project role, see the [Delete default actors from project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-delete) resource.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.deleteActor_delete
      x-api-path-slug: api2projectprojectidorkeyroleid-delete
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: group
        description: The name of the group to remove from the project role
      - in: path
        name: id
        description: The ID of the project role
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: query
        name: user
        description: The user account ID of the user to remove from the project role
      responses:
        200:
          description: OK
      tags:
      - Actors
      - From
      - Project
      - Role
  /api/2/project/{projectIdOrKey}/statuses:
    get:
      summary: Get all statuses
      description: |-
        Returns the valid statuses for a project. The statuses are grouped by issue type, as each project has a set of valid issue types and each issue type has a set of valid statuses.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getAllStatuses_get
      x-api-path-slug: api2projectprojectidorkeystatuses-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Statuses
  /api/2/project/{projectIdOrKey}/type/{newProjectTypeKey}:
    put:
      summary: Update project type
      description: |-
        Updates the [project type](https://confluence.atlassian.com/x/GwiiLQ).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.updateProjectType_put
      x-api-path-slug: api2projectprojectidorkeytypenewprojecttypekey-put
      parameters:
      - in: path
        name: newProjectTypeKey
        description: The key of the new project type
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Type
  /api/2/project/{projectIdOrKey}/version:
    get:
      summary: Get project versions paginated
      description: |-
        Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all versions existing in a single project. See the [Get project versions](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-versions-get) resource if you want to get a full list of versions without pagination.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectVersionsPaginated_get
      x-api-path-slug: api2projectprojectidorkeyversion-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: maxResults
        description: The maximum number of versions to return per page
      - in: query
        name: orderBy
        description: '[Order](https://developer'
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: query
        name: query
        description: Filter the results using a literal string
      - in: query
        name: startAt
        description: The starting index of the returned list of versions (page offset)
      - in: query
        name: status
        description: A comma separated string used to filter the results by version
          status
      responses:
        200:
          description: OK
      tags:
      - Project
      - Versions
      - Paginated
  /api/2/project/{projectIdOrKey}/versions:
    get:
      summary: Get project versions
      description: |-
        Returns all versions existing in a single project. The response is not paginated. Use [Get project versions paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-version-get) if you want to get the versions in a project with pagination.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectVersions_get
      x-api-path-slug: api2projectprojectidorkeyversions-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Versions
  /api/2/project/{projectKeyOrId}/issuesecuritylevelscheme:
    get:
      summary: Get project issue security scheme
      description: |-
        Returns the [issue security scheme](https://confluence.atlassian.com/x/J4lKLg) associated with the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or the _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectIssueSecurityLevelSchemeResource.getIssueSecurityScheme_get
      x-api-path-slug: api2projectprojectkeyoridissuesecuritylevelscheme-get
      parameters:
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Issue
      - Security
      - Scheme
  /api/2/project/{projectKeyOrId}/notificationscheme:
    get:
      summary: Get project notification scheme
      description: |-
        Gets a [notification scheme](https://confluence.atlassian.com/x/8YdKLg) associated with the project. See the [Get notification scheme](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-notificationscheme-id-get) resource for more information about notification schemes.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.notification.ProjectNotificationSchemeResource.getNotificationScheme_get
      x-api-path-slug: api2projectprojectkeyoridnotificationscheme-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Notification
      - Scheme
  /api/2/project/{projectKeyOrId}/securitylevel:
    get:
      summary: Get project issue security levels
      description: |-
        Returns all [issue security](https://confluence.atlassian.com/x/J4lKLg) levels for the project that the currently authenticated user has access to. If the user does not have permission to see an issue security level, then that level is not returned. If the user lacks the _Set Issue Security_ permission, then an empty list is returned.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Set Issue Security_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.securitylevel.ProjectSecurityLevelResource.getSecurityLevelsForProject_ge
      x-api-path-slug: api2projectprojectkeyoridsecuritylevel-get
      parameters:
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Issue
      - Security
      - Levels
  /api/2/role:
    get:
      summary: Get all project roles
      description: |-
        Gets a list of all project roles, complete with project role details and default actors.

        ### About project roles

        [Project roles](https://confluence.atlassian.com/x/3odKLg) are a flexible way to to associate users and groups with projects. In Jira Cloud, the list of project roles is shared globally with all projects, but each project can have a different set of actors associated with it (unlike groups, which have the same membership throughout all Jira applications).

        Project roles can be used in [permission schemes](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-get), [email notification schemes](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-notificationscheme-get), [issue security levels](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuesecurityschemes-get), [comment visibility](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-comment-list-post), and workflow conditions.

        #### Members and actors

        In the Jira REST API, a member of a project role is called an _actor_. An _actor_ is a group or user associated with a project role.

        Actors may be set as [default members](https://confluence.atlassian.com/x/3odKLg#Managingprojectroles-Specifying'defaultmembers'foraprojectrole) of the project role or set at the project level:

        *   Default actors: Users and groups that are assigned to the project role for all newly created projects. The default actors can be removed at the project level later if desired.
        *   Actors: Users and groups that are associated with a project role for a particular project, which may differ from the default actors. This allows you to assign a particular user to different roles in different projects.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.getAllProjectRoles_get
      x-api-path-slug: api2role-get
      responses:
        200:
          description: OK
      tags:
      - Project
      - Roles
    post:
      summary: Create project role
      description: |-
        Creates a new project role with no [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get). You can use the [Add default actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-post) the project method to add default actors to the project role after creating it.

        _Note that although a new project role is available to all projects upon creation, any default actors that are associated with the project role are not added to projects that existed prior to the role being created._<

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.createProjectRole_post
      x-api-path-slug: api2role-post
      responses:
        200:
          description: OK
      tags:
      - Project
      - Role
  /api/2/role/{id}:
    get:
      summary: Get project role by ID
      description: |-
        Gets the project role details and the default actors associated with the role. The list of default actors is sorted by display name.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.getProjectRoleById_get
      x-api-path-slug: api2roleid-get
      parameters:
      - in: path
        name: id
        description: The ID of the project role
      responses:
        200:
          description: OK
      tags:
      - Project
      - Role
      - By
      - ID
    post:
      summary: Partial update project role
      description: |-
        Update either the project role's name or its description.

        You cannot update both the name and description at the same time using this method. If you send a request with both a name and a description, then only the name will be updated, regardless of the order of appearance in the body of the request.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.partialUpdateProjectRole_post
      x-api-path-slug: api2roleid-post
      parameters:
      - in: path
        name: id
        description: The ID of the project role
      responses:
        200:
          description: OK
      tags:
      - Partial
      - Update
      - Project
      - Role
    put:
      summary: Fully update project role
      description: |-
        Update the project role's name and description. You must include both a name and a description in the request.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.fullyUpdateProjectRole_put
      x-api-path-slug: api2roleid-put
      parameters:
      - in: path
        name: id
        description: The ID of the project role
      responses:
        200:
          description: OK
      tags:
      - Fully
      - Update
      - Project
      - Role
    delete:
      summary: Delete project role
      description: |-
        Deletes a project role. You must specify a replacement project role if you wish to delete a project role that is in use.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.deleteProjectRole_delete
      x-api-path-slug: api2roleid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the project role to delete
      - in: query
        name: swap
        description: The ID of the project role that will replace the one being deleted
      responses:
        200:
          description: OK
      tags:
      - Project
      - Role
  /api/2/role/{id}/actors:
    get:
      summary: Get default actors for project role
      description: |-
        Returns the [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) for the project role.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.getProjectRoleActorsForRole_get
      x-api-path-slug: api2roleidactors-get
      parameters:
      - in: path
        name: id
        description: The ID of the project role
      responses:
        200:
          description: OK
      tags:
      - Default
      - Actorsproject
      - Role
    post:
      summary: Add default actors to project role
      description: |-
        Adds [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) to the given role. You may add either groups or users, but you cannot add groups and users in the same request.

        Changing a project role's default actors does not affect project role members for projects already created.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.addProjectRoleActorsToRole_post
      x-api-path-slug: api2roleidactors-post
      parameters:
      - in: header
        name: force-account-id
      - in: path
        name: id
        description: The ID of the project role
      responses:
        200:
          description: OK
      tags:
      - Default
      - Actors
      - To
      - Project
      - Role
    delete:
      summary: Delete default actors from project role
      description: |-
        Removes [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) from the project role. You may remove either a group or user, but you cannot remove a group and a user in the same request.

        Changing a project role's default actors does not affect project role members for projects already created.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.deleteProjectRoleActorsFromRole_delete
      x-api-path-slug: api2roleidactors-delete
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: group
        description: The group name of the group to be removed as a default actor
      - in: path
        name: id
        description: The ID of the project role
      - in: query
        name: user
        description: The user account ID of the user to remove as a default actor
      responses:
        200:
          description: OK
      tags:
      - Default
      - Actors
      - From
      - Project
      - Role
  /api/2/search:
    get:
      summary: Search for issues using JQL (GET)
      description: |-
        Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.

        If the JQL query expression is too large to be encoded as a query parameter, use the [POST](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-post) version of this resource.
      operationId: com.atlassian.jira.rest.v2.search.SearchResource.searchForIssuesUsingJql_get
      x-api-path-slug: api2search-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: fields
        description: A comma-separated list of fields to return for each issue, use
          it to retrieve a subset of fields
      - in: query
        name: fieldsByKeys
        description: Reference fields by their key (rather than ID)
      - in: query
        name: jql
        description: A [JQL](https://confluence
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: properties
        description: A comma-separated list of up to 5 issue properties to include
          in the results
      - in: query
        name: startAt
        description: The index of the first item to return in the page of results
          (page offset)
      - in: query
        name: validateQuery
        description: Determines how to validate the JQL query and treat the validation
          results
      responses:
        200:
          description: OK
      tags:
      - Searchissues
      - Using
      - JQL
      - (GET)
    post:
      summary: Search for issues using JQL (POST)
      description: |-
        Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.

        There is a [GET](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-get) version of this resource that can be used for smaller JQL query expressions.
      operationId: com.atlassian.jira.rest.v2.search.SearchResource.searchForIssuesUsingJql_post
      x-api-path-slug: api2search-post
      responses:
        200:
          description: OK
      tags:
      - Searchissues
      - Using
      - JQL
      - (POST)
  /api/2/user:
    get:
      summary: Get user
      description: Returns a user. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
        None.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.getUser_get
      x-api-path-slug: api2user-get
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: header
        name: force-account-id
      - in: query
        name: key
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
    post:
      summary: Create user
      description: 'Creates a user. This resource is retained for legacy compatibility.
        As soon as a more suitable alternative is available this resource will be
        deprecated. The option is provided to set or generate a password for the user.
        When using the option to generate a password, by omitting `password` from
        the request, include `"notification": "true"` to ensure the user is sent an
        email advising them that their account has been created. This email includes
        a link for the user to set their password. If the notification isn''t sent
        for a generated password, the user will need to be sent a reset password request
        from Jira. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        _Administer Jira_ [global permission](href=)'
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.createUser_post
      x-api-path-slug: api2user-post
      responses:
        200:
          description: OK
      tags:
      - User
    delete:
      summary: Delete user
      description: Deletes a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Site administration (i.e., member of the site-admin [group](https://confluence.atlassian.com/display/Cloud/Manage+groups)).
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.removeUser_delete
      x-api-path-slug: api2user-delete
      parameters:
      - in: query
        name: accountId
        description: the account ID
      - in: header
        name: force-account-id
      - in: query
        name: key
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
  /api/2/user/assignable/multiProjectSearch:
    get:
      summary: Find users assignable to projects
      description: |-
        Returns a list of users who fulfill both of these criteria:

        *   their user attributes match a string.
        *   they can be assigned issues in one or more projects.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.findBulkAssignableUsers_get
      x-api-path-slug: api2userassignablemultiprojectsearch-get
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: projectKeys
        description: A comma-separated list of project keys (case sensitive)
      - in: query
        name: query
        description: A search input that is matched against appropriate user attributes
          to find relevant users
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      - in: query
        name: username
        description: The search string
      responses:
        200:
          description: OK
      tags:
      - Find
      - Users
      - Assignable
      - To
      - Projects
  /api/2/user/assignable/search:
    get:
      summary: Find users assignable to issues
      description: |-
        Returns a list of users that can be assigned to an issue. Use this method to find the list of users who can be assigned to:

        *   a new issue, by providing the `projectKeyOrId`.
        *   an updated issue, by providing the `issueKey`.
        *   to an issue during a transition (workflow action), by providing the `issueKey` and the transition id in `actionDescriptorId`. You can obtain the IDs of an issue's valid transitions using the `transitions` option in the `expand` parameter of [Get issue](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issue-issueIdOrKey-get).

        In all these cases, you can pass a username to determine if a user can be assigned to an issue. The user is returned in the response if they can be assigned to the issue or issue transition. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.findAssignableUsers_get
      x-api-path-slug: api2userassignablesearch-get
      parameters:
      - in: query
        name: actionDescriptorId
        description: The ID of the transition
      - in: header
        name: force-account-id
      - in: query
        name: issueKey
        description: The key of the issue
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: project
        description: The project ID or project key (case sensitive)
      - in: query
        name: query
        description: A search input that is matched against appropriate user attributes
          to find relevant users
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - Find
      - Users
      - Assignable
      - To
      - Issues
  /api/2/user/bulk:
    get:
      summary: Bulk get users
      description: Returns details of users specified in a list of usernames or keys.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
        Jira_ [global permission](href=). Users with permission to access Jira can
        call this method, but empty search results are returned.
      operationId: com.atlassian.jira.rest.v2.user.UserBulkResource.bulkGetUsers_get
      x-api-path-slug: api2userbulk-get
      parameters:
      - in: query
        name: key
        description: Comma-separated list of user keys
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      - in: query
        name: username
        description: Comma-separated list of usernames
      responses:
        200:
          description: OK
      tags:
      - Bulk
      - Get
      - Users
  /api/2/user/columns:
    get:
      summary: Get user default columns
      description: |-
        Returns the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed in the request, the calling user's details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To get the column details for any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLgl).
        *   To get the calling user's column details: None
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.getUserDefaultColumns_get
      x-api-path-slug: api2usercolumns-get
      parameters:
      - in: query
        name: accountId
        description: the account ID
      - in: header
        name: force-account-id
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
      - Default
      - Columns
    put:
      summary: Set user default columns
      description: |-
        Sets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed, the calling user's default columns are set. If no column details are sent, then all default columns are removed. The parameters for this resource are expressed as HTML form data. For example, in curl: `curl -X PUT -d username= -d columns=summary -d columns=description ` **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
        *   To set the calling user's columns: None
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.setUserColumns_put
      x-api-path-slug: api2usercolumns-put
      parameters:
      - in: query
        name: accountId
        description: the account ID
      - in: header
        name: force-account-id
      responses:
        200:
          description: OK
      tags:
      - Set
      - User
      - Default
      - Columns
    delete:
      summary: Reset user default columns
      description: |-
        Resets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user to the system default. If a username is not passed, the calling user's default columns are reset. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
        *   To set the calling user's columns: None
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.resetUserColumns_delete
      x-api-path-slug: api2usercolumns-delete
      parameters:
      - in: query
        name: accountId
        description: the account ID
      - in: header
        name: force-account-id
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - Reset
      - User
      - Default
      - Columns
  /api/2/user/groups:
    get:
      summary: Get user groups
      description: Returns the groups to which a user belongs. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
        _Browse users and groups_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.getUserGroups_get
      x-api-path-slug: api2usergroups-get
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user
      - in: header
        name: force-account-id
      - in: query
        name: key
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
      - Groups
  /api/2/user/picker:
    get:
      summary: Find users for picker
      description: Returns a list of users whose attributes match the query term.
        The returned object includes the `html` field where the matched query term
        is highlighted with the HTML strong tag. A list of usernames can be provided
        to exclude users from the results. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Browse users and groups_ [global permission](href=). Users with
        permission to access Jira can call this method, but will only get search results
        for an exact name match.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.findUsersForPicker_get
      x-api-path-slug: api2userpicker-get
      parameters:
      - in: query
        name: exclude
        description: A comma-separated list of usernames to exclude from the search
          results
      - in: query
        name: excludeAccountIds
        description: A comma-separated list of user accountIds to exclude from the
          search results
      - in: header
        name: force-account-id
      - in: query
        name: maxResults
        description: The maximum number of items to return
      - in: query
        name: query
        description: A search input that is matched against appropriate user attributes
          to find relevant users
      - in: query
        name: showAvatar
        description: Include the URI to the users avatar
      responses:
        200:
          description: OK
      tags:
      - Find
      - Userspicker
  /api/2/user/properties:
    get:
      summary: Get user property keys
      description: |-
        Returns all property keys on a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To access the property keys on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
        *   To access the calling user's property keys: None

        Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
      operationId: com.atlassian.jira.rest.v2.userproperty.UserPropertyResource.getUserPropertyKeys_get
      x-api-path-slug: api2userproperties-get
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user
      - in: header
        name: force-account-id
      - in: query
        name: userKey
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
      - Property
      - Keys
  /api/2/user/properties/{propertyKey}:
    get:
      summary: Get user property
      description: |-
        Returns the value of a user's property. If no property key is provided [Get user property keys](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-user-properties-get) is called. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To get a property from any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
        *   To get a property from the calling user's record: None

        Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
      operationId: com.atlassian.jira.rest.v2.userproperty.UserPropertyResource.getUserProperty_get
      x-api-path-slug: api2userpropertiespropertykey-get
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user
      - in: header
        name: force-account-id
      - in: path
        name: propertyKey
        description: The key of the users property
      - in: query
        name: userKey
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
      - Property
    put:
      summary: Set user property
      description: |-
        Sets the value of a user's property. Use this resource to store custom data against a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To set a property on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
        *   To set a property on the calling user's record: None

        Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
      operationId: com.atlassian.jira.rest.v2.userproperty.UserPropertyResource.setUserProperty_put
      x-api-path-slug: api2userpropertiespropertykey-put
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user
      - in: header
        name: force-account-id
      - in: path
        name: propertyKey
        description: The key of the users property
      - in: query
        name: userKey
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - Set
      - User
      - Property
    delete:
      summary: Delete user property
      description: |-
        Deletes a property from a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To delete a property from any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
        *   To delete a property from the calling user's record: None

        Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
      operationId: com.atlassian.jira.rest.v2.userproperty.UserPropertyResource.deleteUserProperty_delete
      x-api-path-slug: api2userpropertiespropertykey-delete
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user
      - in: header
        name: force-account-id
      - in: path
        name: propertyKey
        description: The key of the users property
      - in: query
        name: userKey
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
      - Property
  /api/2/user/search:
    get:
      summary: Find users
      description: Returns a list of users that match the search string and property.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse
        users and groups_ [global permission](href=). Users with permission to access
        Jira can call this method, but empty search results are returned.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.findUsers_get
      x-api-path-slug: api2usersearch-get
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: includeActive
        description: Include active users
      - in: query
        name: includeInactive
        description: Include inactive users
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: property
        description: A query string used to search properties
      - in: query
        name: query
        description: A search input that is matched against appropriate user attributes
          to find relevant users
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      - in: query
        name: username
        description: A query string used to search username, display name, and email
          address
      responses:
        200:
          description: OK
      tags:
      - Find
      - Users
  /api/2/user/search/query:
    get:
      summary: Find users by query
      description: |-
        Finds users using a structured query and returns user details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). The available queries statements are:

        `is assignee of PROJ` Returns the users that are assignees of at least one issue in project _PROJ_.*   `is assignee of (PROJ-1, PROJ-2)` Returns users that are assignees on the issues _PROJ-1_ or _PROJ-2_.
        *   `is reporter of (PROJ-1, PROJ-2)` Returns users that are reporters on the issues _PROJ-1_ or _PROJ-2_.
        *   `is watcher of (PROJ-1, PROJ-2)` Returns users that are watchers on the issues _PROJ-1_ or _PROJ-2_.
        *   `is voter of (PROJ-1, PROJ-2)` Returns users that are voters on the issues _PROJ-1_ or _PROJ-2_.
        *   `is commenter of (PROJ-1, PROJ-2)` Returns users that have posted a comment on the issues _PROJ-1_ or _PROJ-2_.
        *   `is transitioner of (PROJ-1, PROJ-2)` Returns users that have performed a transition on issues _PROJ-1_ or _PROJ-2_.
        *   `[propertyKey].entity.property.path is "property value"` Returns users with the entity property value.

        The list of issues can be extended as needed, as in _(PROJ-1, PROJ-2, ... PROJ-n)_. Statements can be combined using the `AND` and `OR` operators to form more complex queries, for example:

        `is assignee of PROJ AND [propertyKey].entity.property.path is "property value"`
      operationId: com.atlassian.jira.rest.v2.search.UserSearchResource.findUsersByQuery_get
      x-api-path-slug: api2usersearchquery-get
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: includeInactive
        description: Include inactive users in the results
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: query
        description: The search query
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      responses:
        200:
          description: OK
      tags:
      - Find
      - Users
      - By
      - Query
  /api/2/user/search/query/key:
    get:
      summary: Find user keys by query
      description: |-
        Finds users using a structured query and returns a list of user keys. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). The available query statements are:

        *   `is assignee of PROJ` Returns the users that are assignees of at least one issue in project _PROJ_.
        *   `is assignee of (PROJ-1, PROJ-2)` Returns users that are assignees on the issues _PROJ-1_ or _PROJ-2_.
        *   `is reporter of (PROJ-1, PROJ-2)` Returns users that are reporters on the issues _PROJ-1_ or _PROJ-2_.
        *   `is watcher of (PROJ-1, PROJ-2)` Returns users that are watchers on the issues _PROJ-1_ or _PROJ-2_.
        *   `is voter of (PROJ-1, PROJ-2)` Returns users that are voters on the issues _PROJ-1_ or _PROJ-2_.
        *   `is commenter of (PROJ-1, PROJ-2)` Returns users that have posted a comment on the issues _PROJ-1_ or _PROJ-2_.
        *   `is transitioner of (PROJ-1, PROJ-2)` Returns users that have performed a transition on issues _PROJ-1_ or _PROJ-2_.
        *   `[propertyKey].entity.property.path is "property value"` Returns users with the entity property value.

        The list of issues can be extended as needed, as in _(PROJ-1, PROJ-2, ... PROJ-n)_. Statements can be combined using the `AND` and `OR` operators to form more complex queries, for example:

        `is assignee of PROJ AND [propertyKey].entity.property.path is "property value"`
      operationId: com.atlassian.jira.rest.v2.search.UserSearchResource.findUserKeysByQuery_get
      x-api-path-slug: api2usersearchquerykey-get
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: includeInactive
        description: Include inactive users in the results
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: query
        description: The search query
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      responses:
        200:
          description: OK
      tags:
      - Find
      - User
      - Keys
      - By
      - Query
  /api/2/version:
    post:
      summary: Create version
      description: Creates a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
        or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.createVersion_post
      x-api-path-slug: api2version-post
      responses:
        200:
          description: OK
      tags:
      - Version
  /api/2/version/{id}:
    get:
      summary: Get version
      description: 'Returns a project version. [Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required: _Browse projects_ project permission'
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.getVersion_get
      x-api-path-slug: api2versionid-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the version
      responses:
        200:
          description: OK
      tags:
      - Version
    put:
      summary: Update version
      description: Modifies a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
        or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.updateVersion_put
      x-api-path-slug: api2versionid-put
      parameters:
      - in: path
        name: id
        description: The ID of the version
      responses:
        200:
          description: OK
      tags:
      - Version
    delete:
      summary: Delete version
      description: Deletes a project version. Deprecated, use [Delete and replace
        version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post)
        that supports swapping version values in custom fields, in addition to the
        swapping for `fixVersion` and `affectedVersion` provided in this resource.
        Alternative versions can be provided to update issues that use the deleted
        version in `fixVersion` or `affectedVersion`. If alternatives are not provided,
        occurrences of `fixVersion` and `affectedVersion` that contain the deleted
        version are cleared. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
        or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.deleteVersion_delete
      x-api-path-slug: api2versionid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the version
      - in: query
        name: moveAffectedIssuesTo
        description: The ID of the version to update `affectedVersion` to when the
          field contains the deleted version
      - in: query
        name: moveFixIssuesTo
        description: The ID of the version to update `fixVersion` to when the field
          contains the deleted version
      responses:
        200:
          description: OK
      tags:
      - Version
  /api/2/version/{id}/mergeto/{moveIssuesTo}:
    put:
      summary: Merge versions
      description: Merges two project versions. The merge is completed by deleting
        the version specified in `id` and replacing any occurrences of its ID in `fixVersion`
        with the version ID specified in `moveIssuesTo`. Consider using [Delete and
        replace version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post)
        instead. This resource supports swapping version values in `fixVersion`, `affectedVersion`,
        and custom fields. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
        or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.mergeVersions_put
      x-api-path-slug: api2versionidmergetomoveissuesto-put
      parameters:
      - in: path
        name: id
        description: The ID of the version to delete
      - in: path
        name: moveIssuesTo
        description: The ID of the version to merge into
      responses:
        200:
          description: OK
      tags:
      - Merge
      - Versions
  /api/2/version/{id}/move:
    post:
      summary: Move version
      description: Modifies the version's sequence within the project, which affects
        the display order of the versions in Jira. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
        or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.moveVersion_post
      x-api-path-slug: api2versionidmove-post
      parameters:
      - in: path
        name: id
        description: The ID of the version to be moved
      responses:
        200:
          description: OK
      tags:
      - Move
      - Version
  /api/2/version/{id}/relatedIssueCounts:
    get:
      summary: Get version's related issues count
      description: |-
        Returns the following counts for a version:

        *   Number of issues where the `fixVersion` is set to the version.
        *   Number of issues where the `affectedVersion` is set to the version.
        *   Number of issues where a version custom field is set to the version.

        [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: _Browse projects_ project permission
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.getVersionRelatedIssues_get
      x-api-path-slug: api2versionidrelatedissuecounts-get
      parameters:
      - in: path
        name: id
        description: The ID of the version
      responses:
        200:
          description: OK
      tags:
      - Versions
      - Related
      - Issues
      - Count
  /api/2/version/{id}/removeAndSwap:
    post:
      summary: Delete and replace version
      description: Deletes a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
        or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
        Alternative versions can be provided to update issues that use the deleted
        version in `fixVersion`, `affectedVersion`, or any version picker custom fields.
        If alternatives are not provided, occurrences of `fixVersion`, `affectedVersion`,
        and any version picker custom field, that contain the deleted version, are
        cleared. Any replacement version must be in the same project as the version
        being deleted and cannot be the version being deleted.
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.deleteAndReplaceVersion_post
      x-api-path-slug: api2versionidremoveandswap-post
      parameters:
      - in: path
        name: id
        description: The ID of the version
      responses:
        200:
          description: OK
      tags:
      - Replace
      - Version
  /api/2/version/{id}/unresolvedIssueCount:
    get:
      summary: Get version's unresolved issues count
      description: 'Returns counts of the issues and unresolved issues for the project
        version. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:
        _Browse projects_ project permission'
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.getVersionUnresolvedIssues_get
      x-api-path-slug: api2versionidunresolvedissuecount-get
      parameters:
      - in: path
        name: id
        description: The ID of the version
      responses:
        200:
          description: OK
      tags:
      - Versions
      - Unresolved
      - Issues
      - Count
  /api/2/workflow:
    get:
      summary: Get all workflows
      description: |-
        Returns all workflows in Jira or a single workflow.

        If the `workflowName` parameter is specified, a workflow will be returned as an object (not in an array). Otherwise, an array of workflow objects will be returned.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.WorkflowsResource.getAllWorkflows_get
      x-api-path-slug: api2workflow-get
      parameters:
      - in: query
        name: workflowName
        description: The name of the workflow to be returned
      responses:
        200:
          description: OK
      tags:
      - Workflows
  /api/2/workflow/transitions/{transitionId}/properties:
    get:
      summary: Get workflow transition properties
      description: |-
        Returns the properties on a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.WorkflowTransitionResource.getWorkflowTransitionProperties_get
      x-api-path-slug: api2workflowtransitionstransitionidproperties-get
      parameters:
      - in: query
        name: includeReservedKeys
        description: Some properties with keys that have the _jira
      - in: query
        name: key
        description: The key of the property being returned, also known as the name
          of the property
      - in: path
        name: transitionId
        description: The ID of the transition
      - in: query
        name: workflowMode
        description: The workflow status
      - in: query
        name: workflowName
        description: The name of the workflow that the transition belongs to
      responses:
        200:
          description: OK
      tags:
      - Workflow
      - Transition
      - Properties
    post:
      summary: Create workflow transition property
      description: |-
        Adds a property to a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.WorkflowTransitionResource.createWorkflowTransitionProperty_post
      x-api-path-slug: api2workflowtransitionstransitionidproperties-post
      parameters:
      - in: query
        name: key
        description: The key of the property being added, also known as the name of
          the property
      - in: path
        name: transitionId
        description: The ID of the transition
      - in: query
        name: workflowMode
        description: The workflow status
      - in: query
        name: workflowName
        description: The name of the workflow that the transition belongs to
      responses:
        200:
          description: OK
      tags:
      - Workflow
      - Transition
      - Property
    put:
      summary: Update workflow transition property
      description: |-
        Updates a workflow transition by changing the property value. Trying to update a property that does not exist results in a new property being added to the transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.WorkflowTransitionResource.updateWorkflowTransitionProperty_put
      x-api-path-slug: api2workflowtransitionstransitionidproperties-put
      parameters:
      - in: query
        name: key
        description: The key of the property being updated, also known as the name
          of the property
      - in: path
        name: transitionId
        description: The ID of the transition
      - in: query
        name: workflowMode
        description: The workflow status
      - in: query
        name: workflowName
        description: The name of the workflow that the transition belongs to
      responses:
        200:
          description: OK
      tags:
      - Workflow
      - Transition
      - Property
    delete:
      summary: Delete workflow transition property
      description: |-
        Deletes a property from a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.WorkflowTransitionResource.deleteWorkflowTransitionProperty_delete
      x-api-path-slug: api2workflowtransitionstransitionidproperties-delete
      parameters:
      - in: query
        name: key
        description: The name of the transition property to delete, also known as
          the name of the property
      - in: path
        name: transitionId
        description: The ID of the transition
      - in: query
        name: workflowMode
        description: The workflow status
      - in: query
        name: workflowName
        description: The name of the workflow that the transition belongs to
      responses:
        200:
          description: OK
      tags:
      - Workflow
      - Transition
      - Property
  /api/2/worklog/deleted:
    get:
      summary: Get IDs of deleted worklogs
      description: "Returns a list of IDs and delete timestamps for worklogs deleted
        after a date and time.  \n  \nThis resource is paginated, with a limit of
        1000 worklogs per page. Each page lists worklogs from oldest to youngest.
        If the number of items in the date range exceeds 1000, `until` indicates the
        timestamp of the youngest item on the page. Also, `nextPage` provides the
        URL for the next page of worklogs. The `lastPage` parameter is set to true
        on the last page of worklogs.  \n  \nThis resource does not return worklogs
        deleted during the minute preceding the request.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira."
      operationId: com.atlassian.jira.rest.v2.issue.worklog.WorklogResource.getIdsOfWorklogsDeletedSince_get
      x-api-path-slug: api2worklogdeleted-get
      parameters:
      - in: query
        name: since
        description: The date and time, in UNIX timestamp format, after which deleted
          worklogs are returned
      responses:
        200:
          description: OK
      tags:
      - IDs
      - Of
      - Deleted
      - Worklogs
  /api/2/worklog/list:
    post:
      summary: Get worklogs
      description: "Returns worklog details for a list of worklog IDs.  \n  \nWorklogs
        can be set as viewable by:\n\n*   all users\n*   members of a project role
        or group\n\nFor a worklog to be returned, it must be set as _Viewable by All
        Users_ or the calling user must be a member of the project role or group with
        permission to view the worklog.  \n  \nThe returned list of worklogs is limited
        to 1000 items. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira."
      operationId: com.atlassian.jira.rest.v2.issue.worklog.WorklogResource.getWorklogsForIds_post
      x-api-path-slug: api2workloglist-post
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      responses:
        200:
          description: OK
      tags:
      - Worklogs
  /api/2/worklog/updated:
    get:
      summary: Get IDs of updated worklogs
      description: "Returns a list of IDs and update timestamps for worklogs updated
        after a date and time.  \n  \nThis resource is paginated, with a limit of
        1000 worklogs per page. Each page lists worklogs from oldest to youngest.
        If the number of items in the date range exceeds 1000, `until` indicates the
        timestamp of the youngest item on the page. Also, `nextPage` provides the
        URL for the next page of worklogs. The `lastPage` parameter is set to true
        on the last page of worklogs.  \n  \nThis resource does not return worklogs
        updated during the minute preceding the request.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira."
      operationId: com.atlassian.jira.rest.v2.issue.worklog.WorklogResource.getIdsOfWorklogsModifiedSince_get
      x-api-path-slug: api2worklogupdated-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: since
        description: The date and time, in UNIX timestamp format, after which updated
          worklogs are returned
      responses:
        200:
          description: OK
      tags:
      - IDs
      - Of
      - Updated
      - Worklogs