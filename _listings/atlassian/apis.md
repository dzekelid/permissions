---
name: Atlassian
x-slug: atlassian
description: Millions of users globally rely on Atlassian products every day for improving
  software development, project management, collaboration, and code quality.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
x-kinRank: "8"
x-alexaRank: "1656"
tags: Permissions
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/apis.md
specificationVersion: "0.14"
apis:
- name: Jira Cloud REST API - Get share permissions
  x-api-slug: api2filteridpermission-get
  description: Returns the share permissions for a filter. A filter can be shared
    with groups, projects, all logged-in users, or the public. Sharing with all logged-in
    users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-get-openapi.md
- name: Jira Cloud REST API - Get my permissions
  x-api-slug: api2mypermissions-get
  description: |-
    Checks whether the current user has the given permissions. You can optionally provide a specific context to get permissions for (`projectKey` OR `projectId` OR `issueKey` OR `issueId`)

    If there is no context provided, then the project related permissions will return true if the user has that permission in ANY project.

    If a project context is provided, project related permissions will return true if the user has the permissions in the specified project. For permissions that are determined using issue data (e.g Current Assignee), true will be returned if the user meets the permission criteria in ANY issue in that project.

    If an issue context is provided, it will return whether or not the user has each permission in that specific issue.

    The above means that for issue-level permissions (EDIT_ISSUE for example), hasPermission may be true when no context is provided, or when a project context is provided, **but** may be false for any given (or all) issues. This would occur (for example) if Reporters were given the EDIT_ISSUE permission. This is because any user could be a reporter, except in the context of a concrete issue, where the reporter is known.

    Global permissions work in the same way regardless of the scope.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2mypermissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2mypermissions-get-openapi.md
- name: Jira Cloud REST API - Get all permissions
  x-api-slug: api2permissions-get
  description: Returns all permissions that are present in the Jira instance - Global,
    Project and the global ones added by plugins
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissions-get-openapi.md
- name: Jira Cloud REST API - Find users with permissions
  x-api-slug: api2userpermissionsearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have a set of permissions for a project or issue.

    If no search string is provided, a list of all users with the permissions is returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   Get users for any project, _Administer Jira_ [global permission](href=).
    *   Get users for a project, _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg) for the project.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpermissionsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpermissionsearch-get-openapi.md
- name: Jira Cloud REST API - Add share permission
  x-api-slug: api2filteridpermission-post
  description: "Add a share permissions to a filter. If you add a global share permission
    (i.e., all logged-in users or the public) it will overwrite all share permissions
    for the filter.  \nBe aware that this method uses different objects for updating
    share permissions compared to [Update filter](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-id-put).
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Share
    dashboards and filters_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    and the calling user must own the filter."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-post-openapi.md
- name: Jira Cloud REST API - Get share permission
  x-api-slug: api2filteridpermissionpermissionid-get
  description: Returns a share permission for a filter. A filter can be shared with
    groups, projects, all logged-in users, or the public. Sharing with all logged-in
    users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-get-openapi.md
- name: Jira Cloud REST API - Delete share permission
  x-api-slug: api2filteridpermissionpermissionid-delete
  description: Deletes a share permission from a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and the calling user must own the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-delete-openapi.md
- name: Jira Cloud REST API - Get all permission schemes
  x-api-slug: api2permissionscheme-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-get-openapi.md
- name: Jira Cloud REST API - Create permission scheme
  x-api-slug: api2permissionscheme-post
  description: Creates a new permission scheme. You can create a permission scheme
    with or without defining a set of permission grants. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-post-openapi.md
- name: Jira Cloud REST API - Get permission scheme
  x-api-slug: api2permissionschemeschemeid-get
  description: Returns a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-get-openapi.md
- name: Jira Cloud REST API - Update permission scheme
  x-api-slug: api2permissionschemeschemeid-put
  description: |-
    Updates a permission scheme. Below are some important things to note when using this resource:

    *   If a permissions list is present in the request, then it will be set in the permission scheme, overwriting _all existing_ grants.
    *   If you want to update only the name and description, then do not send a permissions list in the request.
    *   Sending an empty list will remove all permission grants from the permission scheme.

    If you want to add or delete a single permission grant instead of updating the whole list, see [Create permission grant](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-post) or [Delete permission scheme entity](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-permissionId-delete). See [About permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes) for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-put-openapi.md
- name: Jira Cloud REST API - Delete permission scheme
  x-api-slug: api2permissionschemeschemeid-delete
  description: Deletes a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-delete-openapi.md
- name: Jira Cloud REST API - Get permission scheme grants
  x-api-slug: api2permissionschemeschemeidpermission-get
  description: Returns all permission grants for a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-get-openapi.md
- name: Jira Cloud REST API - Create permission grant
  x-api-slug: api2permissionschemeschemeidpermission-post
  description: Creates a new permission grant in the given permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-post-openapi.md
- name: Jira Cloud REST API - Get permission scheme grant
  x-api-slug: api2permissionschemeschemeidpermissionpermissionid-get
  description: Returns a permission grant. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-get-openapi.md
- name: Jira Cloud REST API - Delete permission scheme entity
  x-api-slug: api2permissionschemeschemeidpermissionpermissionid-delete
  description: Deletes a permission grant from a permission scheme. See [About permission
    schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes)
    for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-delete-openapi.md
- name: Jira Cloud REST API - Get assigned permission scheme
  x-api-slug: api2projectprojectkeyoridpermissionscheme-get
  description: |-
    Gets the [permission scheme](https://confluence.atlassian.com/x/yodKLg) associated with the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-get-openapi.md
- name: Jira Cloud REST API - Assign permission scheme
  x-api-slug: api2projectprojectkeyoridpermissionscheme-put
  description: |-
    Associates a permission scheme with a particular project. See [Managing project permissions](https://confluence.atlassian.com/x/yodKLg) for more information about permission schemes.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-put-openapi.md
- name: Jira Cloud REST API - Find users with browse permission
  x-api-slug: api2userviewissuesearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have permission to browse issues.

    Use this resource to find users who can browse:

    *   an issue, by providing the `issueKey`.
    *   any issue in a project, by providing the `projectKey`.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-openapi.md
- name: Jira Cloud REST API - Get global attachment settings
  x-api-slug: api2attachmentmeta-get
  description: "Returns the global attachment settings, that is, whether attachments
    are enabled and the maximum attachment size allowed.  \n  \nNote that there are
    also [project permissions](https://confluence.atlassian.com/x/yodKLg) that restrict
    whether users can create and delete attachments or not.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentmeta-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentmeta-get-openapi.md
- name: Jira Cloud REST API - Get attachment metadata
  x-api-slug: api2attachmentid-get
  description: "Returns the metadata for an attachment. Note that the attachment itself
    is not returned.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the issue
    that the attachment belongs to."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentid-get-openapi.md
- name: Jira Cloud REST API - Delete attachment
  x-api-slug: api2attachmentid-delete
  description: "Deletes an attachment from an issue.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Any of the following permissions in the project that the issue is
    in:\n\n*   _Delete own attachments_ [project permission](https://confluence.atlassian.com/x/yodKLg)
    to delete an attachment created by the calling user.\n*   _Delete all attachments_
    [project permission](https://confluence.atlassian.com/x/yodKLg) to delete an attachment
    created by any user."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentid-delete-openapi.md
- name: Jira Cloud REST API - Get all metadata for an expanded attachment
  x-api-slug: api2attachmentidexpandhuman-get
  description: "Returns the metadata for the contents of an attachment, if it is an
    archive, and metadata for the attachment itself. For example, if the attachment
    is a ZIP archive, then information about the files in the archive is returned
    and metadata for the ZIP archive. Currently, only the ZIP archive format is supported.
    \ \n  \nUse this method to retrieve data that is presented in the UI, as this
    method returns the metadata for the attachment itself, such as the attachment's
    ID and name. Otherwise, use [Get contents metadata for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-raw-get),
    which only returns the metadata for the attachment's contents.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the issue
    that the attachment belongs to."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentidexpandhuman-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentidexpandhuman-get-openapi.md
- name: Jira Cloud REST API - Get contents metadata for an expanded attachment
  x-api-slug: api2attachmentidexpandraw-get
  description: "Returns the metadata for the contents of an attachment, if it is an
    archive. For example, if the attachment is a ZIP archive, then information about
    the files in the archive is returned. Currently, only the ZIP archive format is
    supported.  \n  \nUse this method if you are processing the data without presenting
    it in the UI, as this method only returns the metadata for the contents of the
    attachment. Otherwise, to retrieve data to present in the UI, use [Get all metadata
    for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-human-get)
    which also returns the metadata for the attachment itself, such as the attachment's
    ID and name.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the issue
    that the attachment belongs to."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentidexpandraw-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentidexpandraw-get-openapi.md
- name: Jira Cloud REST API - Create component
  x-api-slug: api2component-post
  description: |-
    Creates a component. Use components to provide containers for issues within a project. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

    *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
    *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2component-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2component-post-openapi.md
- name: Jira Cloud REST API - Get component
  x-api-slug: api2componentid-get
  description: 'Returns a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required: _Browse projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-get-openapi.md
- name: Jira Cloud REST API - Update component
  x-api-slug: api2componentid-put
  description: |-
    Modifies a component. Any fields included in the request are overwritten. If `leadUserName` is an empty string ("") the component lead is removed. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

    *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
    *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-put-openapi.md
- name: Jira Cloud REST API - Delete component
  x-api-slug: api2componentid-delete
  description: |-
    Deletes a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

    *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
    *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-delete-openapi.md
- name: Jira Cloud REST API - Get component issues count
  x-api-slug: api2componentidrelatedissuecounts-get
  description: Returns the counts of issues assigned to the component. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentidrelatedissuecounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentidrelatedissuecounts-get-openapi.md
- name: Jira Cloud REST API - Get global settings
  x-api-slug: api2configuration-get
  description: "Returns the [global settings](https://confluence.atlassian.com/x/qYXKM)
    in Jira. These settings determine whether optional features (for example, sub-tasks,
    time tracking, and others) are enabled. If time tracking is enabled, this method
    also returns the time tracking configuration.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configuration-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configuration-get-openapi.md
- name: Jira Cloud REST API - Get selected time tracking provider
  x-api-slug: api2configurationtimetracking-get
  description: "Returns the time tracking provider that is currently selected. Note
    that if time tracking is disabled, then a successful but empty response is returned.
    \ \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-get-openapi.md
- name: Jira Cloud REST API - Select time tracking provider
  x-api-slug: api2configurationtimetracking-put
  description: "Selects a time tracking provider.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-put-openapi.md
- name: Jira Cloud REST API - Disable time tracking
  x-api-slug: api2configurationtimetracking-delete
  description: "Disables time tracking.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-delete-openapi.md
- name: Jira Cloud REST API - Get all time tracking providers
  x-api-slug: api2configurationtimetrackinglist-get
  description: "Returns all time tracking providers. By default, Jira only has one
    time tracking provider: _JIRA provided time tracking_. However, you can install
    other time tracking providers via apps from the Atlassian Marketplace. For more
    information on time tracking providers, see the documentation for the [Time Tracking
    Provider](https://developer.atlassian.com/cloud/jira/platform/modules/time-tracking-provider/)
    module.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackinglist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackinglist-get-openapi.md
- name: Jira Cloud REST API - Get time tracking settings
  x-api-slug: api2configurationtimetrackingoptions-get
  description: "Returns the time tracking settings. This includes settings such as
    the time format, default time unit, and others. For more information, see [Configuring
    time tracking](https://confluence.atlassian.com/x/qoXKM).  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackingoptions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackingoptions-get-openapi.md
- name: Jira Cloud REST API - Set time tracking settings
  x-api-slug: api2configurationtimetrackingoptions-put
  description: "Sets the time tracking settings.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackingoptions-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackingoptions-put-openapi.md
- name: Jira Cloud REST API - Get custom field option
  x-api-slug: api2customfieldoptionid-get
  description: "Returns a custom field option. For example, an option in a cascading
    select list.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** None."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2customfieldoptionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2customfieldoptionid-get-openapi.md
- name: Jira Cloud REST API - Get all dashboards
  x-api-slug: api2dashboard-get
  description: "Returns a list of dashboards owned by or shared with the user. The
    list may be filtered to include only favorite or owned dashboards.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboard-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboard-get-openapi.md
- name: Jira Cloud REST API - Get dashboard item property keys
  x-api-slug: api2dashboarddashboardiditemsitemidproperties-get
  description: "Returns the keys of all properties for a dashboard item.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira. However, to get the property keys the user
    must be the owner of the dashboard or be shared the dashboard. Note, users with
    the _Administer Jira_ [global permission](href=) are considered owners of the
    System dashboard. The System dashboard is considered to be shared with all other
    users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidproperties-get-openapi.md
- name: Jira Cloud REST API - Get dashboard item property
  x-api-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-get
  description: "Returns the key and value of a dashboard item property.  \n  \nA dashboard
    item enables an app to add user-specific information to a user dashboard. Dashboard
    items are exposed to users as gadgets that users can add to their dashboards.
    For more information on how users do this, see [Adding and customizing gadgets](https://confluence.atlassian.com/x/7AeiLQ).
    \ \n  \nWhen an app creates a dashboard item it registers a callback to receive
    the dashboard item ID. The callback fires whenever the item is rendered or, where
    the item is configurable, the user edits the item. The app then uses this resource
    to store the item's content or configuration details. For more information on
    working with dashboard items, see [Building a dashboard item for a JIRA Connect
    add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/)
    and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/)
    documentation.  \n  \nThere is no resource to set or get dashboard items.  \n
    \ \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to access Jira. However, to get a dashboard item property the user must be the
    owner of the dashboard or be shared the dashboard. Note, users with the _Administer
    Jira_ [global permission](href=) are considered owners of the System dashboard.
    The System dashboard is considered to be shared with all other users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set dashboard item property
  x-api-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-put
  description: "Sets the value of a dashboard item property. Use this resource in
    apps to store custom data against a dashboard item.  \n  \nA dashboard item enables
    an app to add user-specific information to a user dashboard. Dashboard items are
    exposed to users as gadgets that users can add to their dashboards. For more information
    on how users do this, see [Adding and customizing gadgets](https://confluence.atlassian.com/x/7AeiLQ).
    \ \n  \nWhen an app creates a dashboard item it registers a callback to receive
    the dashboard item ID. The callback fires whenever the item is rendered or, where
    the item is configurable, the user edits the item. The app then uses this resource
    to store the item's content or configuration details. For more information on
    working with dashboard items, see [Building a dashboard item for a JIRA Connect
    add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/)
    and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/)
    documentation.  \n  \nThere is no resource to set or get dashboard items.  \n
    \ \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to access Jira. However, to set a dashboard item property the user must be the
    owner of the dashboard. Note, users with the _Administer Jira_ [global permission](href=)
    are considered owners of the System dashboard.  \n  \nThe value of the request
    body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob.
    The maximum length is 32768 bytes."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete dashboard item property
  x-api-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-delete
  description: "Deletes a dashboard item property.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira. However, to delete a dashboard item property
    the user must be the owner of the dashboard. Note, users with the _Administer
    Jira_ [global permission](href=) are considered owners of the System dashboard."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Get dashboard
  x-api-slug: api2dashboardid-get
  description: "Returns a dashboard.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira. However, to get a dashboard, the dashboard
    must be shared with the user or the user must own it. Note, users with the _Administer
    Jira_ [global permission](href=) are considered owners of the System dashboard.
    The System dashboard is considered to be shared with all other users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboardid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboardid-get-openapi.md
- name: Jira Cloud REST API - Get fields
  x-api-slug: api2field-get
  description: |-
    Returns all issue fields in Jira, both system and custom fields.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the following rules apply:

    *   Fields that cannot be added to the issue navigator are always returned.
    *   Fields that cannot be placed on an issue screen are always returned.
    *   Fields that depend on global Jira settings are only returned if the setting is enabled. That is, timetracking fields, subtasks, votes, and watches.
    *   For all other fields, this method only returns the fields that the current user has permission to see (that is, the field can be used in at least one project that the user can see).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2field-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2field-get-openapi.md
- name: Jira Cloud REST API - Create custom field
  x-api-slug: api2field-post
  description: |-
    Creates a custom field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2field-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2field-post-openapi.md
- name: Jira Cloud REST API - Get all issue field options
  x-api-slug: api2fieldfieldkeyoption-get
  description: |-
    Returns all options defined for a select list issue field. A select list issue field is a type of [issue field](https://developer.atlassian.com/cloud/jira/platform/modules/issue-field/) that allows a user to select an value from a list of options.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoption-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoption-get-openapi.md
- name: Jira Cloud REST API - Create issue field option
  x-api-slug: api2fieldfieldkeyoption-post
  description: |-
    Creates an option for a select list issue field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoption-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoption-post-openapi.md
- name: Jira Cloud REST API - Get selectable issue field options
  x-api-slug: api2fieldfieldkeyoptionsuggestionsedit-get
  description: |-
    Returns options defined for a select list issue field that can be viewed and selected by the currently logged in user.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionsedit-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionsedit-get-openapi.md
- name: Jira Cloud REST API - Get visible issue field options
  x-api-slug: api2fieldfieldkeyoptionsuggestionssearch-get
  description: |-
    Returns options defined for a select list issue field that can be viewed by the currently logged in user.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionssearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionssearch-get-openapi.md
- name: Jira Cloud REST API - Get issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionid-get
  description: |-
    Returns an option from a select list issue field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-get-openapi.md
- name: Jira Cloud REST API - Update issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionid-put
  description: |-
    Updates an option for a select list issue field. If the option does not exist, a new option is created.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-put-openapi.md
- name: Jira Cloud REST API - Delete issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionid-delete
  description: |-
    Deletes an option from a select list issue field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-delete-openapi.md
- name: Jira Cloud REST API - Replace issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionidissue-delete
  description: |-
    Deselects a select list issue field option in all issues that it has been selected in. A different option can be selected to replace the deselected option. The update can also be limited to a smaller set of issues by using a JQL query.

    This is an [asynchronous method](#async). The response object will contain a link to the long-running task. For example, _https://your-domain.atlassian.net/rest/api/2/task/10127_.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionidissue-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionidissue-delete-openapi.md
- name: Jira Cloud REST API - Get filters
  x-api-slug: api2filter-get
  description: |-
    Returns all filters. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned:

    *   Filters owned by the user.
    *   Filters shared with a group that the user is a member of.
    *   Filters shared with a private project that the user can browse.
    *   Filters shared with a public project, even if the user is anonymous.
    *   Filters shared with the public, even if the user is anonymous.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filter-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filter-get-openapi.md
- name: Jira Cloud REST API - Create filter
  x-api-slug: api2filter-post
  description: Creates a new filter. The new filter is not shared and not selected
    as a favorite. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filter-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filter-post-openapi.md
- name: Jira Cloud REST API - Get default share scope
  x-api-slug: api2filterdefaultsharescope-get
  description: Returns the default sharing settings for new filters and dashboards
    for a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterdefaultsharescope-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterdefaultsharescope-get-openapi.md
- name: Jira Cloud REST API - Set default share scope
  x-api-slug: api2filterdefaultsharescope-put
  description: Sets the default sharing for new filters and dashboards for a user.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterdefaultsharescope-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterdefaultsharescope-put-openapi.md
- name: Jira Cloud REST API - Get favourite filters
  x-api-slug: api2filterfavourite-get
  description: Returns the favorite filters of the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterfavourite-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterfavourite-get-openapi.md
- name: Jira Cloud REST API - Get my filters
  x-api-slug: api2filtermy-get
  description: Returns the filters owned by the calling user. If `includeFavourites`
    is `true`, the user's favorite filters are also returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filtermy-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filtermy-get-openapi.md
- name: Jira Cloud REST API - Search for filters
  x-api-slug: api2filtersearch-get
  description: |-
    Search for filters. This method is similar to [Get filters](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-get) except that you can refine the results to include filters that have specific attributes. For example, filters with a particular name. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned (if no search parameters are set):

    *   Filters owned by the user.
    *   Filters shared with a group that the user is a member of.
    *   Filters shared with a private project that the user can browse.
    *   Filters shared with a public project, even if the user is anonymous.
    *   Filters shared with the public, even if the user is anonymous.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filtersearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filtersearch-get-openapi.md
- name: Jira Cloud REST API - Get filter
  x-api-slug: api2filterid-get
  description: Returns a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-get-openapi.md
- name: Jira Cloud REST API - Update filter
  x-api-slug: api2filterid-put
  description: |-
    Updates an existing filter. Use this method to update a filter's name, description, JQL, or sharing. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can update:

    *   Private filters (i.e., not shared) can only be updated by the creator of the filter.
    *   Shared filters can only be updated by the creator of the filter or a Jira administrator.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-put-openapi.md
- name: Jira Cloud REST API - Delete filter
  x-api-slug: api2filterid-delete
  description: |-
    Delete a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can delete:

    *   Private filters (i.e., not shared) can only be deleted by the creator of the filter.
    *   Shared filters can only be deleted by the creator of the filter or a Jira administrator.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-delete-openapi.md
- name: Jira Cloud REST API - Get columns
  x-api-slug: api2filteridcolumns-get
  description: Returns the columns configured for a filter. The column configuration
    is used when the filter's results are viewed in _List View_ with the _Columns_
    set to _Filter_. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    None, however the calling user must have permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-get-openapi.md
- name: Jira Cloud REST API - Set columns
  x-api-slug: api2filteridcolumns-put
  description: Sets the columns for a filter. Only navigable fields can be set as
    columns. Use [Get fields](https://developer.atlassian.com/cloud/jira/platform/rest#api-api-2-field-get)
    to get the list fields in Jira. A navigable field has `navigable` set to `true`.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-put-openapi.md
- name: Jira Cloud REST API - Reset columns
  x-api-slug: api2filteridcolumns-delete
  description: Reset the user's column configuration for the filter to the default.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-delete-openapi.md
- name: Jira Cloud REST API - Add filter as favorite
  x-api-slug: api2filteridfavourite-put
  description: Add a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridfavourite-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridfavourite-put-openapi.md
- name: Jira Cloud REST API - Remove filter as favorite
  x-api-slug: api2filteridfavourite-delete
  description: Removes a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridfavourite-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridfavourite-delete-openapi.md
- name: Jira Cloud REST API - Get group
  x-api-slug: api2group-get
  description: |-
    This resource is deprecated, use [`group/member`](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-group-member-get).

    Returns all users in a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-get-openapi.md
- name: Jira Cloud REST API - Create group
  x-api-slug: api2group-post
  description: |-
    Creates a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-post-openapi.md
- name: Jira Cloud REST API - Remove group
  x-api-slug: api2group-delete
  description: |-
    Deletes a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-delete-openapi.md
- name: Jira Cloud REST API - Get users from group
  x-api-slug: api2groupmember-get
  description: |-
    Returns all users in a group. Users are ordered by username.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupmember-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupmember-get-openapi.md
- name: Jira Cloud REST API - Add user to group
  x-api-slug: api2groupuser-post
  description: |-
    Adds a user to a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupuser-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupuser-post-openapi.md
- name: Jira Cloud REST API - Remove user from group
  x-api-slug: api2groupuser-delete
  description: Removes a user from a group. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
    _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupuser-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupuser-delete-openapi.md
- name: Jira Cloud REST API - Get all issue types for user
  x-api-slug: api2issuetype-get
  description: Returns all issue types. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira, however, only issue types that are visible
    to the user are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetype-get-openapi.md
- name: Jira Cloud REST API - Create issue type
  x-api-slug: api2issuetype-post
  description: Creates an issue type and adds it to the default issue type scheme.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
    Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetype-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetype-post-openapi.md
- name: Jira Cloud REST API - Get issue type
  x-api-slug: api2issuetypeid-get
  description: |-
    Returns an issue type. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:

    *   _Administer Jira_ [global permission](href=) to get the details of any issue type.
    *   _Browse projects_ project permission to get the details of any issue type associated with the projects the user has permission to browse.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-get-openapi.md
- name: Jira Cloud REST API - Update issue type
  x-api-slug: api2issuetypeid-put
  description: Updates the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-put-openapi.md
- name: Jira Cloud REST API - Delete issue type
  x-api-slug: api2issuetypeid-delete
  description: Deletes the issue type. If the issue type is in use, all uses are updated
    with the alternative issue type (`alternativeIssueTypeId`). A list of alternative
    issue types can be obtained from the [Get alternative issue types](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-alternatives-get)
    resource. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-delete-openapi.md
- name: Jira Cloud REST API - Get alternative issue types
  x-api-slug: api2issuetypeidalternatives-get
  description: Returns a list of issue types that can be used to replace the issue
    type. The alternative issue types are those assigned to the same workflow scheme,
    field configuration scheme, and screen scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeidalternatives-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeidalternatives-get-openapi.md
- name: Jira Cloud REST API - Create issue type avatar
  x-api-slug: api2issuetypeidavatar2-post
  description: |-
    Creates an avatar for the issue type. Specify the avatar's local file location as binary data in the body of the request. Also, include the following headers:

    *   `X-Atlassian-Token: no-check`
    *   `Content-Type: image/_image type_` Valid image types are JPEG, GIF, or PNG.

    For example: `curl --request POST \ --user email@example.com: \ --header 'X-Atlassian-Token: no-check' \ --header 'Content-Type: image/< image_type>' \ --data-binary "" \ --url 'https://your-domain.atlassian.net/rest/api/2/issuetype/{issueTypeId}'This` The avatar is cropped to a square. If no crop parameters are specified, the square originates at the top left of the image. The length of the square's sides is set to the smaller of the height or width of the image. The cropped image is then used to create avatars of 16x16, 24x24, 32x32, and 48x48 in size. After creating the avatar, use [Update issue type](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-put) to set it as the issue type's active avatar. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeidavatar2-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeidavatar2-post-openapi.md
- name: Jira Cloud REST API - Get issue type property keys
  x-api-slug: api2issuetypeissuetypeidproperties-get
  description: |-
    Returns all the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys of the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   _Administer Jira_ [global permission](href=) to get the property keys of any issue type.
    *   _Browse projects_ project permission to get the property keys of any issue types associated with the projects the user has permission to browse.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidproperties-get-openapi.md
- name: Jira Cloud REST API - Get issue type property
  x-api-slug: api2issuetypeissuetypeidpropertiespropertykey-get
  description: |-
    Returns the key and value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:

    *   _Administer Jira_ [global permission](href=) to get the details of any issue type.
    *   _Browse projects_ project permission to get the details of any issue types associated with the projects the user has permission to browse.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set issue type property
  x-api-slug: api2issuetypeissuetypeidpropertiespropertykey-put
  description: Creates or updates the value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).
    Use this resource to store and update data against an issue type. The value of
    the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty
    JSON blob. The maximum length of the property value is 32768 bytes. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete issue type property
  x-api-slug: api2issuetypeissuetypeidpropertiespropertykey-delete
  description: Deletes the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
    Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Get notification schemes paginated
  x-api-slug: api2notificationscheme-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2notificationscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2notificationscheme-get-openapi.md
- name: Jira Cloud REST API - Get notification scheme
  x-api-slug: api2notificationschemeid-get
  description: |-
    Returns a [notification scheme](https://confluence.atlassian.com/x/8YdKLg), including the list of events and the recipients who will receive notifications for those events.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the requesting user must have permission to administer at least one project associated with the requested notification scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2notificationschemeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2notificationschemeid-get-openapi.md
- name: Jira Cloud REST API - Get all projects
  x-api-slug: api2project-get
  description: |-
    Returns all projects visible to the currently logged in user. For projects to be visible, the authenticated user must be granted either _Browse projects_ or _Administer projects_ permissions. If no user is logged in, it returns all projects that are visible for anonymous users.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2project-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2project-get-openapi.md
- name: Jira Cloud REST API - Create project
  x-api-slug: api2project-post
  description: |-
    Creates a new project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2project-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2project-post-openapi.md
- name: Jira Cloud REST API - Get all project types
  x-api-slug: api2projecttype-get
  description: |-
    Returns all [project types](https://confluence.atlassian.com/x/Var1Nw), whether or not the instance has a valid license for each type.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttype-get-openapi.md
- name: Jira Cloud REST API - Get project type by key
  x-api-slug: api2projecttypeprojecttypekey-get
  description: |-
    Returns a [project type](https://confluence.atlassian.com/x/Var1Nw).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttypeprojecttypekey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttypeprojecttypekey-get-openapi.md
- name: Jira Cloud REST API - Get accessible project type by key
  x-api-slug: api2projecttypeprojecttypekeyaccessible-get
  description: |-
    Returns a [project type](https://confluence.atlassian.com/x/Var1Nw) if it is accessible to the logged in user.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttypeprojecttypekeyaccessible-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttypeprojecttypekeyaccessible-get-openapi.md
- name: Jira Cloud REST API - Get project
  x-api-slug: api2projectprojectidorkey-get
  description: |-
    Returns the [project details](https://confluence.atlassian.com/x/ahLpNw) for the specified project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-get-openapi.md
- name: Jira Cloud REST API - Update project
  x-api-slug: api2projectprojectidorkey-put
  description: |-
    Updates the [project details](https://confluence.atlassian.com/x/ahLpNw) of an existing project.

    All parameters are optional in the body of the request.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-put-openapi.md
- name: Jira Cloud REST API - Delete project
  x-api-slug: api2projectprojectidorkey-delete
  description: |-
    Deletes an existing project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-delete-openapi.md
- name: Jira Cloud REST API - Get project components paginated
  x-api-slug: api2projectprojectidorkeycomponent-get
  description: |-
    Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all components existing in a single project. See the [Get project components](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-components-get) resource if you want to get a full list of versions without pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeycomponent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeycomponent-get-openapi.md
- name: Jira Cloud REST API - Get project components
  x-api-slug: api2projectprojectidorkeycomponents-get
  description: |-
    Returns all components existing in a single project. See the [Get project components paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-component-get) resource if you want to get a full list of components with pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeycomponents-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeycomponents-get-openapi.md
- name: Jira Cloud REST API - Get project property keys
  x-api-slug: api2projectprojectidorkeyproperties-get
  description: |-
    Returns all [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys for the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyproperties-get-openapi.md
- name: Jira Cloud REST API - Get project property
  x-api-slug: api2projectprojectidorkeypropertiespropertykey-get
  description: |-
    Returns the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set project property
  x-api-slug: api2projectprojectidorkeypropertiespropertykey-put
  description: |-
    Sets the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). You can use project properties to store custom data against the project.

    The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 bytes.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete project property
  x-api-slug: api2projectprojectidorkeypropertiespropertykey-delete
  description: |-
    Removes the [property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) from the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Get project roles for project
  x-api-slug: api2projectprojectidorkeyrole-get
  description: |-
    Returns a list of [project roles](https://confluence.atlassian.com/x/3odKLg) for the project.

    Note that all project roles are shared with all projects in Jira Cloud. See the [Get all project roles](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-get) resource for more information.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyrole-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyrole-get-openapi.md
- name: Jira Cloud REST API - Get project role for project
  x-api-slug: api2projectprojectidorkeyroleid-get
  description: |-
    Returns the project role's details and actors associated with the project. The list of actors is sorted by display name.

    If you would like to check to see whether a user belongs to a role based on their group memberships, use the [Get user](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-user-get) resource with the `groups` expand parameter selected. Then check whether the user keys and groups match with the actors returned for the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-get-openapi.md
- name: Jira Cloud REST API - Add actors to project role
  x-api-slug: api2projectprojectidorkeyroleid-post
  description: |-
    Adds additional actors to a project role for the project.

    If you want to replace all actors for the project, then use [Set actors for project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-put).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-post-openapi.md
- name: Jira Cloud REST API - Set actors for project role
  x-api-slug: api2projectprojectidorkeyroleid-put
  description: |-
    Associates actors with the project role for the project, replacing all existing actors.

    If you want to add actors to the project without overwriting the existing list, then use [Add actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-post).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-put-openapi.md
- name: Jira Cloud REST API - Delete actors from project role
  x-api-slug: api2projectprojectidorkeyroleid-delete
  description: |-
    Deletes actors from a project role for the project.

    If you want to remove default actors from the project role, see the [Delete default actors from project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-delete) resource.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-delete-openapi.md
- name: Jira Cloud REST API - Get all statuses
  x-api-slug: api2projectprojectidorkeystatuses-get
  description: |-
    Returns the valid statuses for a project. The statuses are grouped by issue type, as each project has a set of valid issue types and each issue type has a set of valid statuses.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeystatuses-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeystatuses-get-openapi.md
- name: Jira Cloud REST API - Update project type
  x-api-slug: api2projectprojectidorkeytypenewprojecttypekey-put
  description: |-
    Updates the [project type](https://confluence.atlassian.com/x/GwiiLQ).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeytypenewprojecttypekey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeytypenewprojecttypekey-put-openapi.md
- name: Jira Cloud REST API - Get project versions paginated
  x-api-slug: api2projectprojectidorkeyversion-get
  description: |-
    Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all versions existing in a single project. See the [Get project versions](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-versions-get) resource if you want to get a full list of versions without pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyversion-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyversion-get-openapi.md
- name: Jira Cloud REST API - Get project versions
  x-api-slug: api2projectprojectidorkeyversions-get
  description: |-
    Returns all versions existing in a single project. The response is not paginated. Use [Get project versions paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-version-get) if you want to get the versions in a project with pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyversions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyversions-get-openapi.md
- name: Jira Cloud REST API - Get project issue security scheme
  x-api-slug: api2projectprojectkeyoridissuesecuritylevelscheme-get
  description: |-
    Returns the [issue security scheme](https://confluence.atlassian.com/x/J4lKLg) associated with the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or the _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridissuesecuritylevelscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridissuesecuritylevelscheme-get-openapi.md
- name: Jira Cloud REST API - Get project notification scheme
  x-api-slug: api2projectprojectkeyoridnotificationscheme-get
  description: |-
    Gets a [notification scheme](https://confluence.atlassian.com/x/8YdKLg) associated with the project. See the [Get notification scheme](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-notificationscheme-id-get) resource for more information about notification schemes.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridnotificationscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridnotificationscheme-get-openapi.md
- name: Jira Cloud REST API - Get project issue security levels
  x-api-slug: api2projectprojectkeyoridsecuritylevel-get
  description: |-
    Returns all [issue security](https://confluence.atlassian.com/x/J4lKLg) levels for the project that the currently authenticated user has access to. If the user does not have permission to see an issue security level, then that level is not returned. If the user lacks the _Set Issue Security_ permission, then an empty list is returned.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Set Issue Security_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridsecuritylevel-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridsecuritylevel-get-openapi.md
- name: Jira Cloud REST API - Get all project roles
  x-api-slug: api2role-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2role-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2role-get-openapi.md
- name: Jira Cloud REST API - Create project role
  x-api-slug: api2role-post
  description: |-
    Creates a new project role with no [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get). You can use the [Add default actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-post) the project method to add default actors to the project role after creating it.

    _Note that although a new project role is available to all projects upon creation, any default actors that are associated with the project role are not added to projects that existed prior to the role being created._<

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2role-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2role-post-openapi.md
- name: Jira Cloud REST API - Get project role by ID
  x-api-slug: api2roleid-get
  description: |-
    Gets the project role details and the default actors associated with the role. The list of default actors is sorted by display name.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-get-openapi.md
- name: Jira Cloud REST API - Partial update project role
  x-api-slug: api2roleid-post
  description: |-
    Update either the project role's name or its description.

    You cannot update both the name and description at the same time using this method. If you send a request with both a name and a description, then only the name will be updated, regardless of the order of appearance in the body of the request.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-post-openapi.md
- name: Jira Cloud REST API - Fully update project role
  x-api-slug: api2roleid-put
  description: |-
    Update the project role's name and description. You must include both a name and a description in the request.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-put-openapi.md
- name: Jira Cloud REST API - Delete project role
  x-api-slug: api2roleid-delete
  description: |-
    Deletes a project role. You must specify a replacement project role if you wish to delete a project role that is in use.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-delete-openapi.md
- name: Jira Cloud REST API - Get default actors for project role
  x-api-slug: api2roleidactors-get
  description: |-
    Returns the [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) for the project role.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-get-openapi.md
- name: Jira Cloud REST API - Add default actors to project role
  x-api-slug: api2roleidactors-post
  description: |-
    Adds [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) to the given role. You may add either groups or users, but you cannot add groups and users in the same request.

    Changing a project role's default actors does not affect project role members for projects already created.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-post-openapi.md
- name: Jira Cloud REST API - Delete default actors from project role
  x-api-slug: api2roleidactors-delete
  description: |-
    Removes [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) from the project role. You may remove either a group or user, but you cannot remove a group and a user in the same request.

    Changing a project role's default actors does not affect project role members for projects already created.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-delete-openapi.md
- name: Jira Cloud REST API - Search for issues using JQL (GET)
  x-api-slug: api2search-get
  description: |-
    Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.

    If the JQL query expression is too large to be encoded as a query parameter, use the [POST](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-post) version of this resource.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2search-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2search-get-openapi.md
- name: Jira Cloud REST API - Search for issues using JQL (POST)
  x-api-slug: api2search-post
  description: |-
    Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.

    There is a [GET](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-get) version of this resource that can be used for smaller JQL query expressions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2search-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2search-post-openapi.md
- name: Jira Cloud REST API - Get user
  x-api-slug: api2user-get
  description: Returns a user. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
    None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-get-openapi.md
- name: Jira Cloud REST API - Create user
  x-api-slug: api2user-post
  description: 'Creates a user. This resource is retained for legacy compatibility.
    As soon as a more suitable alternative is available this resource will be deprecated.
    The option is provided to set or generate a password for the user. When using
    the option to generate a password, by omitting `password` from the request, include
    `"notification": "true"` to ensure the user is sent an email advising them that
    their account has been created. This email includes a link for the user to set
    their password. If the notification isn''t sent for a generated password, the
    user will need to be sent a reset password request from Jira. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=)'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-post-openapi.md
- name: Jira Cloud REST API - Delete user
  x-api-slug: api2user-delete
  description: Deletes a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Site administration (i.e., member of the site-admin [group](https://confluence.atlassian.com/display/Cloud/Manage+groups)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-delete-openapi.md
- name: Jira Cloud REST API - Find users assignable to projects
  x-api-slug: api2userassignablemultiprojectsearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a string.
    *   they can be assigned issues in one or more projects.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userassignablemultiprojectsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userassignablemultiprojectsearch-get-openapi.md
- name: Jira Cloud REST API - Find users assignable to issues
  x-api-slug: api2userassignablesearch-get
  description: |-
    Returns a list of users that can be assigned to an issue. Use this method to find the list of users who can be assigned to:

    *   a new issue, by providing the `projectKeyOrId`.
    *   an updated issue, by providing the `issueKey`.
    *   to an issue during a transition (workflow action), by providing the `issueKey` and the transition id in `actionDescriptorId`. You can obtain the IDs of an issue's valid transitions using the `transitions` option in the `expand` parameter of [Get issue](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issue-issueIdOrKey-get).

    In all these cases, you can pass a username to determine if a user can be assigned to an issue. The user is returned in the response if they can be assigned to the issue or issue transition. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userassignablesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userassignablesearch-get-openapi.md
- name: Jira Cloud REST API - Bulk get users
  x-api-slug: api2userbulk-get
  description: Returns details of users specified in a list of usernames or keys.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
    Jira_ [global permission](href=). Users with permission to access Jira can call
    this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userbulk-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userbulk-get-openapi.md
- name: Jira Cloud REST API - Get user default columns
  x-api-slug: api2usercolumns-get
  description: |-
    Returns the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed in the request, the calling user's details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To get the column details for any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLgl).
    *   To get the calling user's column details: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-get-openapi.md
- name: Jira Cloud REST API - Set user default columns
  x-api-slug: api2usercolumns-put
  description: |-
    Sets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed, the calling user's default columns are set. If no column details are sent, then all default columns are removed. The parameters for this resource are expressed as HTML form data. For example, in curl: `curl -X PUT -d username= -d columns=summary -d columns=description ` **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To set the calling user's columns: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-put-openapi.md
- name: Jira Cloud REST API - Reset user default columns
  x-api-slug: api2usercolumns-delete
  description: |-
    Resets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user to the system default. If a username is not passed, the calling user's default columns are reset. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To set the calling user's columns: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-delete-openapi.md
- name: Jira Cloud REST API - Get user groups
  x-api-slug: api2usergroups-get
  description: Returns the groups to which a user belongs. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
    _Browse users and groups_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usergroups-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usergroups-get-openapi.md
- name: Jira Cloud REST API - Find users for picker
  x-api-slug: api2userpicker-get
  description: Returns a list of users whose attributes match the query term. The
    returned object includes the `html` field where the matched query term is highlighted
    with the HTML strong tag. A list of usernames can be provided to exclude users
    from the results. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    _Browse users and groups_ [global permission](href=). Users with permission to
    access Jira can call this method, but will only get search results for an exact
    name match.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpicker-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpicker-get-openapi.md
- name: Jira Cloud REST API - Get user property keys
  x-api-slug: api2userproperties-get
  description: |-
    Returns all property keys on a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To access the property keys on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To access the calling user's property keys: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userproperties-get-openapi.md
- name: Jira Cloud REST API - Get user property
  x-api-slug: api2userpropertiespropertykey-get
  description: |-
    Returns the value of a user's property. If no property key is provided [Get user property keys](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-user-properties-get) is called. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To get a property from any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To get a property from the calling user's record: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set user property
  x-api-slug: api2userpropertiespropertykey-put
  description: |-
    Sets the value of a user's property. Use this resource to store custom data against a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To set a property on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To set a property on the calling user's record: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete user property
  x-api-slug: api2userpropertiespropertykey-delete
  description: |-
    Deletes a property from a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To delete a property from any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To delete a property from the calling user's record: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Find users
  x-api-slug: api2usersearch-get
  description: Returns a list of users that match the search string and property.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse
    users and groups_ [global permission](href=). Users with permission to access
    Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearch-get-openapi.md
- name: Jira Cloud REST API - Find users by query
  x-api-slug: api2usersearchquery-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearchquery-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearchquery-get-openapi.md
- name: Jira Cloud REST API - Find user keys by query
  x-api-slug: api2usersearchquerykey-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearchquerykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearchquerykey-get-openapi.md
- name: Jira Cloud REST API - Create version
  x-api-slug: api2version-post
  description: Creates a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2version-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2version-post-openapi.md
- name: Jira Cloud REST API - Get version
  x-api-slug: api2versionid-get
  description: 'Returns a project version. [Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required: _Browse projects_ project permission'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-get-openapi.md
- name: Jira Cloud REST API - Update version
  x-api-slug: api2versionid-put
  description: Modifies a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-put-openapi.md
- name: Jira Cloud REST API - Delete version
  x-api-slug: api2versionid-delete
  description: Deletes a project version. Deprecated, use [Delete and replace version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post)
    that supports swapping version values in custom fields, in addition to the swapping
    for `fixVersion` and `affectedVersion` provided in this resource. Alternative
    versions can be provided to update issues that use the deleted version in `fixVersion`
    or `affectedVersion`. If alternatives are not provided, occurrences of `fixVersion`
    and `affectedVersion` that contain the deleted version are cleared. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-delete-openapi.md
- name: Jira Cloud REST API - Merge versions
  x-api-slug: api2versionidmergetomoveissuesto-put
  description: Merges two project versions. The merge is completed by deleting the
    version specified in `id` and replacing any occurrences of its ID in `fixVersion`
    with the version ID specified in `moveIssuesTo`. Consider using [Delete and replace
    version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post)
    instead. This resource supports swapping version values in `fixVersion`, `affectedVersion`,
    and custom fields. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidmergetomoveissuesto-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidmergetomoveissuesto-put-openapi.md
- name: Jira Cloud REST API - Move version
  x-api-slug: api2versionidmove-post
  description: Modifies the version's sequence within the project, which affects the
    display order of the versions in Jira. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidmove-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidmove-post-openapi.md
- name: Jira Cloud REST API - Get version's related issues count
  x-api-slug: api2versionidrelatedissuecounts-get
  description: |-
    Returns the following counts for a version:

    *   Number of issues where the `fixVersion` is set to the version.
    *   Number of issues where the `affectedVersion` is set to the version.
    *   Number of issues where a version custom field is set to the version.

    [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: _Browse projects_ project permission
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidrelatedissuecounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidrelatedissuecounts-get-openapi.md
- name: Jira Cloud REST API - Delete and replace version
  x-api-slug: api2versionidremoveandswap-post
  description: Deletes a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
    Alternative versions can be provided to update issues that use the deleted version
    in `fixVersion`, `affectedVersion`, or any version picker custom fields. If alternatives
    are not provided, occurrences of `fixVersion`, `affectedVersion`, and any version
    picker custom field, that contain the deleted version, are cleared. Any replacement
    version must be in the same project as the version being deleted and cannot be
    the version being deleted.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidremoveandswap-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidremoveandswap-post-openapi.md
- name: Jira Cloud REST API - Get version's unresolved issues count
  x-api-slug: api2versionidunresolvedissuecount-get
  description: 'Returns counts of the issues and unresolved issues for the project
    version. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: _Browse
    projects_ project permission'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidunresolvedissuecount-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidunresolvedissuecount-get-openapi.md
- name: Jira Cloud REST API - Get all workflows
  x-api-slug: api2workflow-get
  description: |-
    Returns all workflows in Jira or a single workflow.

    If the `workflowName` parameter is specified, a workflow will be returned as an object (not in an array). Otherwise, an array of workflow objects will be returned.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflow-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflow-get-openapi.md
- name: Jira Cloud REST API - Get workflow transition properties
  x-api-slug: api2workflowtransitionstransitionidproperties-get
  description: |-
    Returns the properties on a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-get-openapi.md
- name: Jira Cloud REST API - Create workflow transition property
  x-api-slug: api2workflowtransitionstransitionidproperties-post
  description: |-
    Adds a property to a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-post-openapi.md
- name: Jira Cloud REST API - Update workflow transition property
  x-api-slug: api2workflowtransitionstransitionidproperties-put
  description: |-
    Updates a workflow transition by changing the property value. Trying to update a property that does not exist results in a new property being added to the transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-put-openapi.md
- name: Jira Cloud REST API - Delete workflow transition property
  x-api-slug: api2workflowtransitionstransitionidproperties-delete
  description: |-
    Deletes a property from a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-delete-openapi.md
- name: Jira Cloud REST API - Get IDs of deleted worklogs
  x-api-slug: api2worklogdeleted-get
  description: "Returns a list of IDs and delete timestamps for worklogs deleted after
    a date and time.  \n  \nThis resource is paginated, with a limit of 1000 worklogs
    per page. Each page lists worklogs from oldest to youngest. If the number of items
    in the date range exceeds 1000, `until` indicates the timestamp of the youngest
    item on the page. Also, `nextPage` provides the URL for the next page of worklogs.
    The `lastPage` parameter is set to true on the last page of worklogs.  \n  \nThis
    resource does not return worklogs deleted during the minute preceding the request.
    \ \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2worklogdeleted-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2worklogdeleted-get-openapi.md
- name: Jira Cloud REST API - Get worklogs
  x-api-slug: api2workloglist-post
  description: "Returns worklog details for a list of worklog IDs.  \n  \nWorklogs
    can be set as viewable by:\n\n*   all users\n*   members of a project role or
    group\n\nFor a worklog to be returned, it must be set as _Viewable by All Users_
    or the calling user must be a member of the project role or group with permission
    to view the worklog.  \n  \nThe returned list of worklogs is limited to 1000 items.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workloglist-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workloglist-post-openapi.md
- name: Jira Cloud REST API - Get IDs of updated worklogs
  x-api-slug: api2worklogupdated-get
  description: "Returns a list of IDs and update timestamps for worklogs updated after
    a date and time.  \n  \nThis resource is paginated, with a limit of 1000 worklogs
    per page. Each page lists worklogs from oldest to youngest. If the number of items
    in the date range exceeds 1000, `until` indicates the timestamp of the youngest
    item on the page. Also, `nextPage` provides the URL for the next page of worklogs.
    The `lastPage` parameter is set to true on the last page of worklogs.  \n  \nThis
    resource does not return worklogs updated during the minute preceding the request.
    \ \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2worklogupdated-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2worklogupdated-get-openapi.md
- name: Jira Cloud REST API - Add share permission
  x-api-slug: api2filteridpermission-post
  description: "Add a share permissions to a filter. If you add a global share permission
    (i.e., all logged-in users or the public) it will overwrite all share permissions
    for the filter.  \nBe aware that this method uses different objects for updating
    share permissions compared to [Update filter](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-id-put).
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Share
    dashboards and filters_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    and the calling user must own the filter."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-post-openapi.md
- name: Jira Cloud REST API - Get share permission
  x-api-slug: api2filteridpermissionpermissionid-get
  description: Returns a share permission for a filter. A filter can be shared with
    groups, projects, all logged-in users, or the public. Sharing with all logged-in
    users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-get-openapi.md
- name: Jira Cloud REST API - Delete share permission
  x-api-slug: api2filteridpermissionpermissionid-delete
  description: Deletes a share permission from a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and the calling user must own the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-delete-openapi.md
- name: Jira Cloud REST API - Get all permission schemes
  x-api-slug: api2permissionscheme-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-get-openapi.md
- name: Jira Cloud REST API - Create permission scheme
  x-api-slug: api2permissionscheme-post
  description: Creates a new permission scheme. You can create a permission scheme
    with or without defining a set of permission grants. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-post-openapi.md
- name: Jira Cloud REST API - Get permission scheme
  x-api-slug: api2permissionschemeschemeid-get
  description: Returns a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-get-openapi.md
- name: Jira Cloud REST API - Update permission scheme
  x-api-slug: api2permissionschemeschemeid-put
  description: |-
    Updates a permission scheme. Below are some important things to note when using this resource:

    *   If a permissions list is present in the request, then it will be set in the permission scheme, overwriting _all existing_ grants.
    *   If you want to update only the name and description, then do not send a permissions list in the request.
    *   Sending an empty list will remove all permission grants from the permission scheme.

    If you want to add or delete a single permission grant instead of updating the whole list, see [Create permission grant](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-post) or [Delete permission scheme entity](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-permissionId-delete). See [About permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes) for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-put-openapi.md
- name: Jira Cloud REST API - Delete permission scheme
  x-api-slug: api2permissionschemeschemeid-delete
  description: Deletes a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-delete-openapi.md
- name: Jira Cloud REST API - Get permission scheme grants
  x-api-slug: api2permissionschemeschemeidpermission-get
  description: Returns all permission grants for a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-get-openapi.md
- name: Jira Cloud REST API - Create permission grant
  x-api-slug: api2permissionschemeschemeidpermission-post
  description: Creates a new permission grant in the given permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-post-openapi.md
- name: Jira Cloud REST API - Get permission scheme grant
  x-api-slug: api2permissionschemeschemeidpermissionpermissionid-get
  description: Returns a permission grant. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-get-openapi.md
- name: Jira Cloud REST API - Delete permission scheme entity
  x-api-slug: api2permissionschemeschemeidpermissionpermissionid-delete
  description: Deletes a permission grant from a permission scheme. See [About permission
    schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes)
    for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-delete-openapi.md
- name: Jira Cloud REST API - Get assigned permission scheme
  x-api-slug: api2projectprojectkeyoridpermissionscheme-get
  description: |-
    Gets the [permission scheme](https://confluence.atlassian.com/x/yodKLg) associated with the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-get-openapi.md
- name: Jira Cloud REST API - Assign permission scheme
  x-api-slug: api2projectprojectkeyoridpermissionscheme-put
  description: |-
    Associates a permission scheme with a particular project. See [Managing project permissions](https://confluence.atlassian.com/x/yodKLg) for more information about permission schemes.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-put-openapi.md
- name: Jira Cloud REST API - Find users with browse permission
  x-api-slug: api2userviewissuesearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have permission to browse issues.

    Use this resource to find users who can browse:

    *   an issue, by providing the `issueKey`.
    *   any issue in a project, by providing the `projectKey`.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-openapi.md
- name: Jira Cloud REST API - Get global attachment settings
  x-api-slug: api2attachmentmeta-get
  description: "Returns the global attachment settings, that is, whether attachments
    are enabled and the maximum attachment size allowed.  \n  \nNote that there are
    also [project permissions](https://confluence.atlassian.com/x/yodKLg) that restrict
    whether users can create and delete attachments or not.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentmeta-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentmeta-get-openapi.md
- name: Jira Cloud REST API - Get attachment metadata
  x-api-slug: api2attachmentid-get
  description: "Returns the metadata for an attachment. Note that the attachment itself
    is not returned.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the issue
    that the attachment belongs to."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentid-get-openapi.md
- name: Jira Cloud REST API - Delete attachment
  x-api-slug: api2attachmentid-delete
  description: "Deletes an attachment from an issue.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Any of the following permissions in the project that the issue is
    in:\n\n*   _Delete own attachments_ [project permission](https://confluence.atlassian.com/x/yodKLg)
    to delete an attachment created by the calling user.\n*   _Delete all attachments_
    [project permission](https://confluence.atlassian.com/x/yodKLg) to delete an attachment
    created by any user."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentid-delete-openapi.md
- name: Jira Cloud REST API - Get all metadata for an expanded attachment
  x-api-slug: api2attachmentidexpandhuman-get
  description: "Returns the metadata for the contents of an attachment, if it is an
    archive, and metadata for the attachment itself. For example, if the attachment
    is a ZIP archive, then information about the files in the archive is returned
    and metadata for the ZIP archive. Currently, only the ZIP archive format is supported.
    \ \n  \nUse this method to retrieve data that is presented in the UI, as this
    method returns the metadata for the attachment itself, such as the attachment's
    ID and name. Otherwise, use [Get contents metadata for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-raw-get),
    which only returns the metadata for the attachment's contents.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the issue
    that the attachment belongs to."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentidexpandhuman-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentidexpandhuman-get-openapi.md
- name: Jira Cloud REST API - Get contents metadata for an expanded attachment
  x-api-slug: api2attachmentidexpandraw-get
  description: "Returns the metadata for the contents of an attachment, if it is an
    archive. For example, if the attachment is a ZIP archive, then information about
    the files in the archive is returned. Currently, only the ZIP archive format is
    supported.  \n  \nUse this method if you are processing the data without presenting
    it in the UI, as this method only returns the metadata for the contents of the
    attachment. Otherwise, to retrieve data to present in the UI, use [Get all metadata
    for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-human-get)
    which also returns the metadata for the attachment itself, such as the attachment's
    ID and name.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the issue
    that the attachment belongs to."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentidexpandraw-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2attachmentidexpandraw-get-openapi.md
- name: Jira Cloud REST API - Create component
  x-api-slug: api2component-post
  description: |-
    Creates a component. Use components to provide containers for issues within a project. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

    *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
    *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2component-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2component-post-openapi.md
- name: Jira Cloud REST API - Get component
  x-api-slug: api2componentid-get
  description: 'Returns a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required: _Browse projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-get-openapi.md
- name: Jira Cloud REST API - Update component
  x-api-slug: api2componentid-put
  description: |-
    Modifies a component. Any fields included in the request are overwritten. If `leadUserName` is an empty string ("") the component lead is removed. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

    *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
    *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-put-openapi.md
- name: Jira Cloud REST API - Delete component
  x-api-slug: api2componentid-delete
  description: |-
    Deletes a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

    *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
    *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentid-delete-openapi.md
- name: Jira Cloud REST API - Get component issues count
  x-api-slug: api2componentidrelatedissuecounts-get
  description: Returns the counts of issues assigned to the component. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentidrelatedissuecounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2componentidrelatedissuecounts-get-openapi.md
- name: Jira Cloud REST API - Get global settings
  x-api-slug: api2configuration-get
  description: "Returns the [global settings](https://confluence.atlassian.com/x/qYXKM)
    in Jira. These settings determine whether optional features (for example, sub-tasks,
    time tracking, and others) are enabled. If time tracking is enabled, this method
    also returns the time tracking configuration.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configuration-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configuration-get-openapi.md
- name: Jira Cloud REST API - Get selected time tracking provider
  x-api-slug: api2configurationtimetracking-get
  description: "Returns the time tracking provider that is currently selected. Note
    that if time tracking is disabled, then a successful but empty response is returned.
    \ \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-get-openapi.md
- name: Jira Cloud REST API - Select time tracking provider
  x-api-slug: api2configurationtimetracking-put
  description: "Selects a time tracking provider.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-put-openapi.md
- name: Jira Cloud REST API - Disable time tracking
  x-api-slug: api2configurationtimetracking-delete
  description: "Disables time tracking.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetracking-delete-openapi.md
- name: Jira Cloud REST API - Get all time tracking providers
  x-api-slug: api2configurationtimetrackinglist-get
  description: "Returns all time tracking providers. By default, Jira only has one
    time tracking provider: _JIRA provided time tracking_. However, you can install
    other time tracking providers via apps from the Atlassian Marketplace. For more
    information on time tracking providers, see the documentation for the [Time Tracking
    Provider](https://developer.atlassian.com/cloud/jira/platform/modules/time-tracking-provider/)
    module.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackinglist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackinglist-get-openapi.md
- name: Jira Cloud REST API - Get time tracking settings
  x-api-slug: api2configurationtimetrackingoptions-get
  description: "Returns the time tracking settings. This includes settings such as
    the time format, default time unit, and others. For more information, see [Configuring
    time tracking](https://confluence.atlassian.com/x/qoXKM).  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackingoptions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackingoptions-get-openapi.md
- name: Jira Cloud REST API - Set time tracking settings
  x-api-slug: api2configurationtimetrackingoptions-put
  description: "Sets the time tracking settings.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackingoptions-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2configurationtimetrackingoptions-put-openapi.md
- name: Jira Cloud REST API - Get custom field option
  x-api-slug: api2customfieldoptionid-get
  description: "Returns a custom field option. For example, an option in a cascading
    select list.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** None."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2customfieldoptionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2customfieldoptionid-get-openapi.md
- name: Jira Cloud REST API - Get all dashboards
  x-api-slug: api2dashboard-get
  description: "Returns a list of dashboards owned by or shared with the user. The
    list may be filtered to include only favorite or owned dashboards.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboard-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboard-get-openapi.md
- name: Jira Cloud REST API - Get dashboard item property keys
  x-api-slug: api2dashboarddashboardiditemsitemidproperties-get
  description: "Returns the keys of all properties for a dashboard item.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira. However, to get the property keys the user
    must be the owner of the dashboard or be shared the dashboard. Note, users with
    the _Administer Jira_ [global permission](href=) are considered owners of the
    System dashboard. The System dashboard is considered to be shared with all other
    users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidproperties-get-openapi.md
- name: Jira Cloud REST API - Get dashboard item property
  x-api-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-get
  description: "Returns the key and value of a dashboard item property.  \n  \nA dashboard
    item enables an app to add user-specific information to a user dashboard. Dashboard
    items are exposed to users as gadgets that users can add to their dashboards.
    For more information on how users do this, see [Adding and customizing gadgets](https://confluence.atlassian.com/x/7AeiLQ).
    \ \n  \nWhen an app creates a dashboard item it registers a callback to receive
    the dashboard item ID. The callback fires whenever the item is rendered or, where
    the item is configurable, the user edits the item. The app then uses this resource
    to store the item's content or configuration details. For more information on
    working with dashboard items, see [Building a dashboard item for a JIRA Connect
    add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/)
    and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/)
    documentation.  \n  \nThere is no resource to set or get dashboard items.  \n
    \ \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to access Jira. However, to get a dashboard item property the user must be the
    owner of the dashboard or be shared the dashboard. Note, users with the _Administer
    Jira_ [global permission](href=) are considered owners of the System dashboard.
    The System dashboard is considered to be shared with all other users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set dashboard item property
  x-api-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-put
  description: "Sets the value of a dashboard item property. Use this resource in
    apps to store custom data against a dashboard item.  \n  \nA dashboard item enables
    an app to add user-specific information to a user dashboard. Dashboard items are
    exposed to users as gadgets that users can add to their dashboards. For more information
    on how users do this, see [Adding and customizing gadgets](https://confluence.atlassian.com/x/7AeiLQ).
    \ \n  \nWhen an app creates a dashboard item it registers a callback to receive
    the dashboard item ID. The callback fires whenever the item is rendered or, where
    the item is configurable, the user edits the item. The app then uses this resource
    to store the item's content or configuration details. For more information on
    working with dashboard items, see [Building a dashboard item for a JIRA Connect
    add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/)
    and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/)
    documentation.  \n  \nThere is no resource to set or get dashboard items.  \n
    \ \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to access Jira. However, to set a dashboard item property the user must be the
    owner of the dashboard. Note, users with the _Administer Jira_ [global permission](href=)
    are considered owners of the System dashboard.  \n  \nThe value of the request
    body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob.
    The maximum length is 32768 bytes."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete dashboard item property
  x-api-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-delete
  description: "Deletes a dashboard item property.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira. However, to delete a dashboard item property
    the user must be the owner of the dashboard. Note, users with the _Administer
    Jira_ [global permission](href=) are considered owners of the System dashboard."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Get dashboard
  x-api-slug: api2dashboardid-get
  description: "Returns a dashboard.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira. However, to get a dashboard, the dashboard
    must be shared with the user or the user must own it. Note, users with the _Administer
    Jira_ [global permission](href=) are considered owners of the System dashboard.
    The System dashboard is considered to be shared with all other users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboardid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2dashboardid-get-openapi.md
- name: Jira Cloud REST API - Get fields
  x-api-slug: api2field-get
  description: |-
    Returns all issue fields in Jira, both system and custom fields.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the following rules apply:

    *   Fields that cannot be added to the issue navigator are always returned.
    *   Fields that cannot be placed on an issue screen are always returned.
    *   Fields that depend on global Jira settings are only returned if the setting is enabled. That is, timetracking fields, subtasks, votes, and watches.
    *   For all other fields, this method only returns the fields that the current user has permission to see (that is, the field can be used in at least one project that the user can see).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2field-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2field-get-openapi.md
- name: Jira Cloud REST API - Create custom field
  x-api-slug: api2field-post
  description: |-
    Creates a custom field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2field-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2field-post-openapi.md
- name: Jira Cloud REST API - Get all issue field options
  x-api-slug: api2fieldfieldkeyoption-get
  description: |-
    Returns all options defined for a select list issue field. A select list issue field is a type of [issue field](https://developer.atlassian.com/cloud/jira/platform/modules/issue-field/) that allows a user to select an value from a list of options.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoption-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoption-get-openapi.md
- name: Jira Cloud REST API - Create issue field option
  x-api-slug: api2fieldfieldkeyoption-post
  description: |-
    Creates an option for a select list issue field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoption-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoption-post-openapi.md
- name: Jira Cloud REST API - Get selectable issue field options
  x-api-slug: api2fieldfieldkeyoptionsuggestionsedit-get
  description: |-
    Returns options defined for a select list issue field that can be viewed and selected by the currently logged in user.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionsedit-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionsedit-get-openapi.md
- name: Jira Cloud REST API - Get visible issue field options
  x-api-slug: api2fieldfieldkeyoptionsuggestionssearch-get
  description: |-
    Returns options defined for a select list issue field that can be viewed by the currently logged in user.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionssearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionssearch-get-openapi.md
- name: Jira Cloud REST API - Get issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionid-get
  description: |-
    Returns an option from a select list issue field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-get-openapi.md
- name: Jira Cloud REST API - Update issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionid-put
  description: |-
    Updates an option for a select list issue field. If the option does not exist, a new option is created.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-put-openapi.md
- name: Jira Cloud REST API - Delete issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionid-delete
  description: |-
    Deletes an option from a select list issue field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-delete-openapi.md
- name: Jira Cloud REST API - Replace issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionidissue-delete
  description: |-
    Deselects a select list issue field option in all issues that it has been selected in. A different option can be selected to replace the deselected option. The update can also be limited to a smaller set of issues by using a JQL query.

    This is an [asynchronous method](#async). The response object will contain a link to the long-running task. For example, _https://your-domain.atlassian.net/rest/api/2/task/10127_.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionidissue-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2fieldfieldkeyoptionoptionidissue-delete-openapi.md
- name: Jira Cloud REST API - Get filters
  x-api-slug: api2filter-get
  description: |-
    Returns all filters. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned:

    *   Filters owned by the user.
    *   Filters shared with a group that the user is a member of.
    *   Filters shared with a private project that the user can browse.
    *   Filters shared with a public project, even if the user is anonymous.
    *   Filters shared with the public, even if the user is anonymous.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filter-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filter-get-openapi.md
- name: Jira Cloud REST API - Create filter
  x-api-slug: api2filter-post
  description: Creates a new filter. The new filter is not shared and not selected
    as a favorite. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filter-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filter-post-openapi.md
- name: Jira Cloud REST API - Get default share scope
  x-api-slug: api2filterdefaultsharescope-get
  description: Returns the default sharing settings for new filters and dashboards
    for a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterdefaultsharescope-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterdefaultsharescope-get-openapi.md
- name: Jira Cloud REST API - Set default share scope
  x-api-slug: api2filterdefaultsharescope-put
  description: Sets the default sharing for new filters and dashboards for a user.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterdefaultsharescope-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterdefaultsharescope-put-openapi.md
- name: Jira Cloud REST API - Get favourite filters
  x-api-slug: api2filterfavourite-get
  description: Returns the favorite filters of the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterfavourite-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterfavourite-get-openapi.md
- name: Jira Cloud REST API - Get my filters
  x-api-slug: api2filtermy-get
  description: Returns the filters owned by the calling user. If `includeFavourites`
    is `true`, the user's favorite filters are also returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filtermy-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filtermy-get-openapi.md
- name: Jira Cloud REST API - Search for filters
  x-api-slug: api2filtersearch-get
  description: |-
    Search for filters. This method is similar to [Get filters](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-get) except that you can refine the results to include filters that have specific attributes. For example, filters with a particular name. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned (if no search parameters are set):

    *   Filters owned by the user.
    *   Filters shared with a group that the user is a member of.
    *   Filters shared with a private project that the user can browse.
    *   Filters shared with a public project, even if the user is anonymous.
    *   Filters shared with the public, even if the user is anonymous.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filtersearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filtersearch-get-openapi.md
- name: Jira Cloud REST API - Get filter
  x-api-slug: api2filterid-get
  description: Returns a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-get-openapi.md
- name: Jira Cloud REST API - Update filter
  x-api-slug: api2filterid-put
  description: |-
    Updates an existing filter. Use this method to update a filter's name, description, JQL, or sharing. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can update:

    *   Private filters (i.e., not shared) can only be updated by the creator of the filter.
    *   Shared filters can only be updated by the creator of the filter or a Jira administrator.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-put-openapi.md
- name: Jira Cloud REST API - Delete filter
  x-api-slug: api2filterid-delete
  description: |-
    Delete a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can delete:

    *   Private filters (i.e., not shared) can only be deleted by the creator of the filter.
    *   Shared filters can only be deleted by the creator of the filter or a Jira administrator.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filterid-delete-openapi.md
- name: Jira Cloud REST API - Get columns
  x-api-slug: api2filteridcolumns-get
  description: Returns the columns configured for a filter. The column configuration
    is used when the filter's results are viewed in _List View_ with the _Columns_
    set to _Filter_. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    None, however the calling user must have permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-get-openapi.md
- name: Jira Cloud REST API - Set columns
  x-api-slug: api2filteridcolumns-put
  description: Sets the columns for a filter. Only navigable fields can be set as
    columns. Use [Get fields](https://developer.atlassian.com/cloud/jira/platform/rest#api-api-2-field-get)
    to get the list fields in Jira. A navigable field has `navigable` set to `true`.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-put-openapi.md
- name: Jira Cloud REST API - Reset columns
  x-api-slug: api2filteridcolumns-delete
  description: Reset the user's column configuration for the filter to the default.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridcolumns-delete-openapi.md
- name: Jira Cloud REST API - Add filter as favorite
  x-api-slug: api2filteridfavourite-put
  description: Add a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridfavourite-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridfavourite-put-openapi.md
- name: Jira Cloud REST API - Remove filter as favorite
  x-api-slug: api2filteridfavourite-delete
  description: Removes a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridfavourite-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridfavourite-delete-openapi.md
- name: Jira Cloud REST API - Get share permissions
  x-api-slug: api2filteridpermission-get
  description: Returns the share permissions for a filter. A filter can be shared
    with groups, projects, all logged-in users, or the public. Sharing with all logged-in
    users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-get-openapi.md
- name: Jira Cloud REST API - Get group
  x-api-slug: api2group-get
  description: |-
    This resource is deprecated, use [`group/member`](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-group-member-get).

    Returns all users in a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-get-openapi.md
- name: Jira Cloud REST API - Create group
  x-api-slug: api2group-post
  description: |-
    Creates a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-post-openapi.md
- name: Jira Cloud REST API - Remove group
  x-api-slug: api2group-delete
  description: |-
    Deletes a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2group-delete-openapi.md
- name: Jira Cloud REST API - Get users from group
  x-api-slug: api2groupmember-get
  description: |-
    Returns all users in a group. Users are ordered by username.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupmember-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupmember-get-openapi.md
- name: Jira Cloud REST API - Add user to group
  x-api-slug: api2groupuser-post
  description: |-
    Adds a user to a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupuser-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupuser-post-openapi.md
- name: Jira Cloud REST API - Remove user from group
  x-api-slug: api2groupuser-delete
  description: Removes a user from a group. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
    _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupuser-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2groupuser-delete-openapi.md
- name: Jira Cloud REST API - Get all issue types for user
  x-api-slug: api2issuetype-get
  description: Returns all issue types. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira, however, only issue types that are visible
    to the user are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetype-get-openapi.md
- name: Jira Cloud REST API - Create issue type
  x-api-slug: api2issuetype-post
  description: Creates an issue type and adds it to the default issue type scheme.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
    Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetype-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetype-post-openapi.md
- name: Jira Cloud REST API - Get issue type
  x-api-slug: api2issuetypeid-get
  description: |-
    Returns an issue type. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:

    *   _Administer Jira_ [global permission](href=) to get the details of any issue type.
    *   _Browse projects_ project permission to get the details of any issue type associated with the projects the user has permission to browse.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-get-openapi.md
- name: Jira Cloud REST API - Update issue type
  x-api-slug: api2issuetypeid-put
  description: Updates the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-put-openapi.md
- name: Jira Cloud REST API - Delete issue type
  x-api-slug: api2issuetypeid-delete
  description: Deletes the issue type. If the issue type is in use, all uses are updated
    with the alternative issue type (`alternativeIssueTypeId`). A list of alternative
    issue types can be obtained from the [Get alternative issue types](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-alternatives-get)
    resource. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeid-delete-openapi.md
- name: Jira Cloud REST API - Get alternative issue types
  x-api-slug: api2issuetypeidalternatives-get
  description: Returns a list of issue types that can be used to replace the issue
    type. The alternative issue types are those assigned to the same workflow scheme,
    field configuration scheme, and screen scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeidalternatives-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeidalternatives-get-openapi.md
- name: Jira Cloud REST API - Create issue type avatar
  x-api-slug: api2issuetypeidavatar2-post
  description: |-
    Creates an avatar for the issue type. Specify the avatar's local file location as binary data in the body of the request. Also, include the following headers:

    *   `X-Atlassian-Token: no-check`
    *   `Content-Type: image/_image type_` Valid image types are JPEG, GIF, or PNG.

    For example: `curl --request POST \ --user email@example.com: \ --header 'X-Atlassian-Token: no-check' \ --header 'Content-Type: image/< image_type>' \ --data-binary "" \ --url 'https://your-domain.atlassian.net/rest/api/2/issuetype/{issueTypeId}'This` The avatar is cropped to a square. If no crop parameters are specified, the square originates at the top left of the image. The length of the square's sides is set to the smaller of the height or width of the image. The cropped image is then used to create avatars of 16x16, 24x24, 32x32, and 48x48 in size. After creating the avatar, use [Update issue type](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-put) to set it as the issue type's active avatar. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeidavatar2-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeidavatar2-post-openapi.md
- name: Jira Cloud REST API - Get issue type property keys
  x-api-slug: api2issuetypeissuetypeidproperties-get
  description: |-
    Returns all the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys of the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   _Administer Jira_ [global permission](href=) to get the property keys of any issue type.
    *   _Browse projects_ project permission to get the property keys of any issue types associated with the projects the user has permission to browse.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidproperties-get-openapi.md
- name: Jira Cloud REST API - Get issue type property
  x-api-slug: api2issuetypeissuetypeidpropertiespropertykey-get
  description: |-
    Returns the key and value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:

    *   _Administer Jira_ [global permission](href=) to get the details of any issue type.
    *   _Browse projects_ project permission to get the details of any issue types associated with the projects the user has permission to browse.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set issue type property
  x-api-slug: api2issuetypeissuetypeidpropertiespropertykey-put
  description: Creates or updates the value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).
    Use this resource to store and update data against an issue type. The value of
    the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty
    JSON blob. The maximum length of the property value is 32768 bytes. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete issue type property
  x-api-slug: api2issuetypeissuetypeidpropertiespropertykey-delete
  description: Deletes the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
    Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Get my permissions
  x-api-slug: api2mypermissions-get
  description: |-
    Checks whether the current user has the given permissions. You can optionally provide a specific context to get permissions for (`projectKey` OR `projectId` OR `issueKey` OR `issueId`)

    If there is no context provided, then the project related permissions will return true if the user has that permission in ANY project.

    If a project context is provided, project related permissions will return true if the user has the permissions in the specified project. For permissions that are determined using issue data (e.g Current Assignee), true will be returned if the user meets the permission criteria in ANY issue in that project.

    If an issue context is provided, it will return whether or not the user has each permission in that specific issue.

    The above means that for issue-level permissions (EDIT_ISSUE for example), hasPermission may be true when no context is provided, or when a project context is provided, **but** may be false for any given (or all) issues. This would occur (for example) if Reporters were given the EDIT_ISSUE permission. This is because any user could be a reporter, except in the context of a concrete issue, where the reporter is known.

    Global permissions work in the same way regardless of the scope.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2mypermissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2mypermissions-get-openapi.md
- name: Jira Cloud REST API - Get notification schemes paginated
  x-api-slug: api2notificationscheme-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2notificationscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2notificationscheme-get-openapi.md
- name: Jira Cloud REST API - Get notification scheme
  x-api-slug: api2notificationschemeid-get
  description: |-
    Returns a [notification scheme](https://confluence.atlassian.com/x/8YdKLg), including the list of events and the recipients who will receive notifications for those events.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the requesting user must have permission to administer at least one project associated with the requested notification scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2notificationschemeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2notificationschemeid-get-openapi.md
- name: Jira Cloud REST API - Get all projects
  x-api-slug: api2project-get
  description: |-
    Returns all projects visible to the currently logged in user. For projects to be visible, the authenticated user must be granted either _Browse projects_ or _Administer projects_ permissions. If no user is logged in, it returns all projects that are visible for anonymous users.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2project-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2project-get-openapi.md
- name: Jira Cloud REST API - Create project
  x-api-slug: api2project-post
  description: |-
    Creates a new project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2project-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2project-post-openapi.md
- name: Jira Cloud REST API - Get all project types
  x-api-slug: api2projecttype-get
  description: |-
    Returns all [project types](https://confluence.atlassian.com/x/Var1Nw), whether or not the instance has a valid license for each type.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttype-get-openapi.md
- name: Jira Cloud REST API - Get project type by key
  x-api-slug: api2projecttypeprojecttypekey-get
  description: |-
    Returns a [project type](https://confluence.atlassian.com/x/Var1Nw).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttypeprojecttypekey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttypeprojecttypekey-get-openapi.md
- name: Jira Cloud REST API - Get accessible project type by key
  x-api-slug: api2projecttypeprojecttypekeyaccessible-get
  description: |-
    Returns a [project type](https://confluence.atlassian.com/x/Var1Nw) if it is accessible to the logged in user.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttypeprojecttypekeyaccessible-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projecttypeprojecttypekeyaccessible-get-openapi.md
- name: Jira Cloud REST API - Get project
  x-api-slug: api2projectprojectidorkey-get
  description: |-
    Returns the [project details](https://confluence.atlassian.com/x/ahLpNw) for the specified project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-get-openapi.md
- name: Jira Cloud REST API - Update project
  x-api-slug: api2projectprojectidorkey-put
  description: |-
    Updates the [project details](https://confluence.atlassian.com/x/ahLpNw) of an existing project.

    All parameters are optional in the body of the request.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-put-openapi.md
- name: Jira Cloud REST API - Delete project
  x-api-slug: api2projectprojectidorkey-delete
  description: |-
    Deletes an existing project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkey-delete-openapi.md
- name: Jira Cloud REST API - Get project components paginated
  x-api-slug: api2projectprojectidorkeycomponent-get
  description: |-
    Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all components existing in a single project. See the [Get project components](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-components-get) resource if you want to get a full list of versions without pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeycomponent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeycomponent-get-openapi.md
- name: Jira Cloud REST API - Get project components
  x-api-slug: api2projectprojectidorkeycomponents-get
  description: |-
    Returns all components existing in a single project. See the [Get project components paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-component-get) resource if you want to get a full list of components with pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeycomponents-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeycomponents-get-openapi.md
- name: Jira Cloud REST API - Get project property keys
  x-api-slug: api2projectprojectidorkeyproperties-get
  description: |-
    Returns all [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys for the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyproperties-get-openapi.md
- name: Jira Cloud REST API - Get project property
  x-api-slug: api2projectprojectidorkeypropertiespropertykey-get
  description: |-
    Returns the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set project property
  x-api-slug: api2projectprojectidorkeypropertiespropertykey-put
  description: |-
    Sets the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). You can use project properties to store custom data against the project.

    The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 bytes.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete project property
  x-api-slug: api2projectprojectidorkeypropertiespropertykey-delete
  description: |-
    Removes the [property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) from the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Get project roles for project
  x-api-slug: api2projectprojectidorkeyrole-get
  description: |-
    Returns a list of [project roles](https://confluence.atlassian.com/x/3odKLg) for the project.

    Note that all project roles are shared with all projects in Jira Cloud. See the [Get all project roles](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-get) resource for more information.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyrole-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyrole-get-openapi.md
- name: Jira Cloud REST API - Get project role for project
  x-api-slug: api2projectprojectidorkeyroleid-get
  description: |-
    Returns the project role's details and actors associated with the project. The list of actors is sorted by display name.

    If you would like to check to see whether a user belongs to a role based on their group memberships, use the [Get user](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-user-get) resource with the `groups` expand parameter selected. Then check whether the user keys and groups match with the actors returned for the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-get-openapi.md
- name: Jira Cloud REST API - Add actors to project role
  x-api-slug: api2projectprojectidorkeyroleid-post
  description: |-
    Adds additional actors to a project role for the project.

    If you want to replace all actors for the project, then use [Set actors for project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-put).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-post-openapi.md
- name: Jira Cloud REST API - Set actors for project role
  x-api-slug: api2projectprojectidorkeyroleid-put
  description: |-
    Associates actors with the project role for the project, replacing all existing actors.

    If you want to add actors to the project without overwriting the existing list, then use [Add actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-post).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-put-openapi.md
- name: Jira Cloud REST API - Delete actors from project role
  x-api-slug: api2projectprojectidorkeyroleid-delete
  description: |-
    Deletes actors from a project role for the project.

    If you want to remove default actors from the project role, see the [Delete default actors from project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-delete) resource.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyroleid-delete-openapi.md
- name: Jira Cloud REST API - Get all statuses
  x-api-slug: api2projectprojectidorkeystatuses-get
  description: |-
    Returns the valid statuses for a project. The statuses are grouped by issue type, as each project has a set of valid issue types and each issue type has a set of valid statuses.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeystatuses-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeystatuses-get-openapi.md
- name: Jira Cloud REST API - Update project type
  x-api-slug: api2projectprojectidorkeytypenewprojecttypekey-put
  description: |-
    Updates the [project type](https://confluence.atlassian.com/x/GwiiLQ).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeytypenewprojecttypekey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeytypenewprojecttypekey-put-openapi.md
- name: Jira Cloud REST API - Get project versions paginated
  x-api-slug: api2projectprojectidorkeyversion-get
  description: |-
    Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all versions existing in a single project. See the [Get project versions](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-versions-get) resource if you want to get a full list of versions without pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyversion-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyversion-get-openapi.md
- name: Jira Cloud REST API - Get project versions
  x-api-slug: api2projectprojectidorkeyversions-get
  description: |-
    Returns all versions existing in a single project. The response is not paginated. Use [Get project versions paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-version-get) if you want to get the versions in a project with pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyversions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectidorkeyversions-get-openapi.md
- name: Jira Cloud REST API - Get project issue security scheme
  x-api-slug: api2projectprojectkeyoridissuesecuritylevelscheme-get
  description: |-
    Returns the [issue security scheme](https://confluence.atlassian.com/x/J4lKLg) associated with the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or the _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridissuesecuritylevelscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridissuesecuritylevelscheme-get-openapi.md
- name: Jira Cloud REST API - Get project notification scheme
  x-api-slug: api2projectprojectkeyoridnotificationscheme-get
  description: |-
    Gets a [notification scheme](https://confluence.atlassian.com/x/8YdKLg) associated with the project. See the [Get notification scheme](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-notificationscheme-id-get) resource for more information about notification schemes.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridnotificationscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridnotificationscheme-get-openapi.md
- name: Jira Cloud REST API - Get project issue security levels
  x-api-slug: api2projectprojectkeyoridsecuritylevel-get
  description: |-
    Returns all [issue security](https://confluence.atlassian.com/x/J4lKLg) levels for the project that the currently authenticated user has access to. If the user does not have permission to see an issue security level, then that level is not returned. If the user lacks the _Set Issue Security_ permission, then an empty list is returned.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Set Issue Security_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridsecuritylevel-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridsecuritylevel-get-openapi.md
- name: Jira Cloud REST API - Get all project roles
  x-api-slug: api2role-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2role-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2role-get-openapi.md
- name: Jira Cloud REST API - Create project role
  x-api-slug: api2role-post
  description: |-
    Creates a new project role with no [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get). You can use the [Add default actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-post) the project method to add default actors to the project role after creating it.

    _Note that although a new project role is available to all projects upon creation, any default actors that are associated with the project role are not added to projects that existed prior to the role being created._<

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2role-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2role-post-openapi.md
- name: Jira Cloud REST API - Get project role by ID
  x-api-slug: api2roleid-get
  description: |-
    Gets the project role details and the default actors associated with the role. The list of default actors is sorted by display name.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-get-openapi.md
- name: Jira Cloud REST API - Partial update project role
  x-api-slug: api2roleid-post
  description: |-
    Update either the project role's name or its description.

    You cannot update both the name and description at the same time using this method. If you send a request with both a name and a description, then only the name will be updated, regardless of the order of appearance in the body of the request.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-post-openapi.md
- name: Jira Cloud REST API - Fully update project role
  x-api-slug: api2roleid-put
  description: |-
    Update the project role's name and description. You must include both a name and a description in the request.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-put-openapi.md
- name: Jira Cloud REST API - Delete project role
  x-api-slug: api2roleid-delete
  description: |-
    Deletes a project role. You must specify a replacement project role if you wish to delete a project role that is in use.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleid-delete-openapi.md
- name: Jira Cloud REST API - Get default actors for project role
  x-api-slug: api2roleidactors-get
  description: |-
    Returns the [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) for the project role.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-get-openapi.md
- name: Jira Cloud REST API - Add default actors to project role
  x-api-slug: api2roleidactors-post
  description: |-
    Adds [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) to the given role. You may add either groups or users, but you cannot add groups and users in the same request.

    Changing a project role's default actors does not affect project role members for projects already created.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-post-openapi.md
- name: Jira Cloud REST API - Delete default actors from project role
  x-api-slug: api2roleidactors-delete
  description: |-
    Removes [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) from the project role. You may remove either a group or user, but you cannot remove a group and a user in the same request.

    Changing a project role's default actors does not affect project role members for projects already created.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2roleidactors-delete-openapi.md
- name: Jira Cloud REST API - Search for issues using JQL (GET)
  x-api-slug: api2search-get
  description: |-
    Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.

    If the JQL query expression is too large to be encoded as a query parameter, use the [POST](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-post) version of this resource.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2search-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2search-get-openapi.md
- name: Jira Cloud REST API - Search for issues using JQL (POST)
  x-api-slug: api2search-post
  description: |-
    Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.

    There is a [GET](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-get) version of this resource that can be used for smaller JQL query expressions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2search-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2search-post-openapi.md
- name: Jira Cloud REST API - Get user
  x-api-slug: api2user-get
  description: Returns a user. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
    None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-get-openapi.md
- name: Jira Cloud REST API - Create user
  x-api-slug: api2user-post
  description: 'Creates a user. This resource is retained for legacy compatibility.
    As soon as a more suitable alternative is available this resource will be deprecated.
    The option is provided to set or generate a password for the user. When using
    the option to generate a password, by omitting `password` from the request, include
    `"notification": "true"` to ensure the user is sent an email advising them that
    their account has been created. This email includes a link for the user to set
    their password. If the notification isn''t sent for a generated password, the
    user will need to be sent a reset password request from Jira. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=)'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-post-openapi.md
- name: Jira Cloud REST API - Delete user
  x-api-slug: api2user-delete
  description: Deletes a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Site administration (i.e., member of the site-admin [group](https://confluence.atlassian.com/display/Cloud/Manage+groups)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2user-delete-openapi.md
- name: Jira Cloud REST API - Find users assignable to projects
  x-api-slug: api2userassignablemultiprojectsearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a string.
    *   they can be assigned issues in one or more projects.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userassignablemultiprojectsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userassignablemultiprojectsearch-get-openapi.md
- name: Jira Cloud REST API - Find users assignable to issues
  x-api-slug: api2userassignablesearch-get
  description: |-
    Returns a list of users that can be assigned to an issue. Use this method to find the list of users who can be assigned to:

    *   a new issue, by providing the `projectKeyOrId`.
    *   an updated issue, by providing the `issueKey`.
    *   to an issue during a transition (workflow action), by providing the `issueKey` and the transition id in `actionDescriptorId`. You can obtain the IDs of an issue's valid transitions using the `transitions` option in the `expand` parameter of [Get issue](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issue-issueIdOrKey-get).

    In all these cases, you can pass a username to determine if a user can be assigned to an issue. The user is returned in the response if they can be assigned to the issue or issue transition. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userassignablesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userassignablesearch-get-openapi.md
- name: Jira Cloud REST API - Bulk get users
  x-api-slug: api2userbulk-get
  description: Returns details of users specified in a list of usernames or keys.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
    Jira_ [global permission](href=). Users with permission to access Jira can call
    this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userbulk-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userbulk-get-openapi.md
- name: Jira Cloud REST API - Get user default columns
  x-api-slug: api2usercolumns-get
  description: |-
    Returns the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed in the request, the calling user's details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To get the column details for any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLgl).
    *   To get the calling user's column details: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-get-openapi.md
- name: Jira Cloud REST API - Set user default columns
  x-api-slug: api2usercolumns-put
  description: |-
    Sets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed, the calling user's default columns are set. If no column details are sent, then all default columns are removed. The parameters for this resource are expressed as HTML form data. For example, in curl: `curl -X PUT -d username= -d columns=summary -d columns=description ` **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To set the calling user's columns: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-put-openapi.md
- name: Jira Cloud REST API - Reset user default columns
  x-api-slug: api2usercolumns-delete
  description: |-
    Resets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user to the system default. If a username is not passed, the calling user's default columns are reset. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To set the calling user's columns: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usercolumns-delete-openapi.md
- name: Jira Cloud REST API - Get user groups
  x-api-slug: api2usergroups-get
  description: Returns the groups to which a user belongs. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
    _Browse users and groups_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usergroups-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usergroups-get-openapi.md
- name: Jira Cloud REST API - Find users with permissions
  x-api-slug: api2userpermissionsearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have a set of permissions for a project or issue.

    If no search string is provided, a list of all users with the permissions is returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   Get users for any project, _Administer Jira_ [global permission](href=).
    *   Get users for a project, _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg) for the project.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpermissionsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpermissionsearch-get-openapi.md
- name: Jira Cloud REST API - Find users for picker
  x-api-slug: api2userpicker-get
  description: Returns a list of users whose attributes match the query term. The
    returned object includes the `html` field where the matched query term is highlighted
    with the HTML strong tag. A list of usernames can be provided to exclude users
    from the results. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    _Browse users and groups_ [global permission](href=). Users with permission to
    access Jira can call this method, but will only get search results for an exact
    name match.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpicker-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpicker-get-openapi.md
- name: Jira Cloud REST API - Get user property keys
  x-api-slug: api2userproperties-get
  description: |-
    Returns all property keys on a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To access the property keys on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To access the calling user's property keys: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userproperties-get-openapi.md
- name: Jira Cloud REST API - Get user property
  x-api-slug: api2userpropertiespropertykey-get
  description: |-
    Returns the value of a user's property. If no property key is provided [Get user property keys](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-user-properties-get) is called. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To get a property from any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To get a property from the calling user's record: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set user property
  x-api-slug: api2userpropertiespropertykey-put
  description: |-
    Sets the value of a user's property. Use this resource to store custom data against a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To set a property on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To set a property on the calling user's record: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete user property
  x-api-slug: api2userpropertiespropertykey-delete
  description: |-
    Deletes a property from a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To delete a property from any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To delete a property from the calling user's record: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userpropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Find users
  x-api-slug: api2usersearch-get
  description: Returns a list of users that match the search string and property.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse
    users and groups_ [global permission](href=). Users with permission to access
    Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearch-get-openapi.md
- name: Jira Cloud REST API - Find users by query
  x-api-slug: api2usersearchquery-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearchquery-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearchquery-get-openapi.md
- name: Jira Cloud REST API - Find user keys by query
  x-api-slug: api2usersearchquerykey-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearchquerykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2usersearchquerykey-get-openapi.md
- name: Jira Cloud REST API - Create version
  x-api-slug: api2version-post
  description: Creates a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2version-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2version-post-openapi.md
- name: Jira Cloud REST API - Get version
  x-api-slug: api2versionid-get
  description: 'Returns a project version. [Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required: _Browse projects_ project permission'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-get-openapi.md
- name: Jira Cloud REST API - Update version
  x-api-slug: api2versionid-put
  description: Modifies a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-put-openapi.md
- name: Jira Cloud REST API - Delete version
  x-api-slug: api2versionid-delete
  description: Deletes a project version. Deprecated, use [Delete and replace version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post)
    that supports swapping version values in custom fields, in addition to the swapping
    for `fixVersion` and `affectedVersion` provided in this resource. Alternative
    versions can be provided to update issues that use the deleted version in `fixVersion`
    or `affectedVersion`. If alternatives are not provided, occurrences of `fixVersion`
    and `affectedVersion` that contain the deleted version are cleared. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionid-delete-openapi.md
- name: Jira Cloud REST API - Merge versions
  x-api-slug: api2versionidmergetomoveissuesto-put
  description: Merges two project versions. The merge is completed by deleting the
    version specified in `id` and replacing any occurrences of its ID in `fixVersion`
    with the version ID specified in `moveIssuesTo`. Consider using [Delete and replace
    version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post)
    instead. This resource supports swapping version values in `fixVersion`, `affectedVersion`,
    and custom fields. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidmergetomoveissuesto-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidmergetomoveissuesto-put-openapi.md
- name: Jira Cloud REST API - Move version
  x-api-slug: api2versionidmove-post
  description: Modifies the version's sequence within the project, which affects the
    display order of the versions in Jira. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidmove-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidmove-post-openapi.md
- name: Jira Cloud REST API - Get version's related issues count
  x-api-slug: api2versionidrelatedissuecounts-get
  description: |-
    Returns the following counts for a version:

    *   Number of issues where the `fixVersion` is set to the version.
    *   Number of issues where the `affectedVersion` is set to the version.
    *   Number of issues where a version custom field is set to the version.

    [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: _Browse projects_ project permission
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidrelatedissuecounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidrelatedissuecounts-get-openapi.md
- name: Jira Cloud REST API - Delete and replace version
  x-api-slug: api2versionidremoveandswap-post
  description: Deletes a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
    Alternative versions can be provided to update issues that use the deleted version
    in `fixVersion`, `affectedVersion`, or any version picker custom fields. If alternatives
    are not provided, occurrences of `fixVersion`, `affectedVersion`, and any version
    picker custom field, that contain the deleted version, are cleared. Any replacement
    version must be in the same project as the version being deleted and cannot be
    the version being deleted.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidremoveandswap-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidremoveandswap-post-openapi.md
- name: Jira Cloud REST API - Get version's unresolved issues count
  x-api-slug: api2versionidunresolvedissuecount-get
  description: 'Returns counts of the issues and unresolved issues for the project
    version. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: _Browse
    projects_ project permission'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidunresolvedissuecount-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2versionidunresolvedissuecount-get-openapi.md
- name: Jira Cloud REST API - Get all workflows
  x-api-slug: api2workflow-get
  description: |-
    Returns all workflows in Jira or a single workflow.

    If the `workflowName` parameter is specified, a workflow will be returned as an object (not in an array). Otherwise, an array of workflow objects will be returned.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflow-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflow-get-openapi.md
- name: Jira Cloud REST API - Get workflow transition properties
  x-api-slug: api2workflowtransitionstransitionidproperties-get
  description: |-
    Returns the properties on a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-get-openapi.md
- name: Jira Cloud REST API - Create workflow transition property
  x-api-slug: api2workflowtransitionstransitionidproperties-post
  description: |-
    Adds a property to a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-post-openapi.md
- name: Jira Cloud REST API - Update workflow transition property
  x-api-slug: api2workflowtransitionstransitionidproperties-put
  description: |-
    Updates a workflow transition by changing the property value. Trying to update a property that does not exist results in a new property being added to the transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-put-openapi.md
- name: Jira Cloud REST API - Delete workflow transition property
  x-api-slug: api2workflowtransitionstransitionidproperties-delete
  description: |-
    Deletes a property from a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-delete-openapi.md
- name: Jira Cloud REST API - Get IDs of deleted worklogs
  x-api-slug: api2worklogdeleted-get
  description: "Returns a list of IDs and delete timestamps for worklogs deleted after
    a date and time.  \n  \nThis resource is paginated, with a limit of 1000 worklogs
    per page. Each page lists worklogs from oldest to youngest. If the number of items
    in the date range exceeds 1000, `until` indicates the timestamp of the youngest
    item on the page. Also, `nextPage` provides the URL for the next page of worklogs.
    The `lastPage` parameter is set to true on the last page of worklogs.  \n  \nThis
    resource does not return worklogs deleted during the minute preceding the request.
    \ \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2worklogdeleted-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2worklogdeleted-get-openapi.md
- name: Jira Cloud REST API - Get worklogs
  x-api-slug: api2workloglist-post
  description: "Returns worklog details for a list of worklog IDs.  \n  \nWorklogs
    can be set as viewable by:\n\n*   all users\n*   members of a project role or
    group\n\nFor a worklog to be returned, it must be set as _Viewable by All Users_
    or the calling user must be a member of the project role or group with permission
    to view the worklog.  \n  \nThe returned list of worklogs is limited to 1000 items.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workloglist-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2workloglist-post-openapi.md
- name: Jira Cloud REST API - Get IDs of updated worklogs
  x-api-slug: api2worklogupdated-get
  description: "Returns a list of IDs and update timestamps for worklogs updated after
    a date and time.  \n  \nThis resource is paginated, with a limit of 1000 worklogs
    per page. Each page lists worklogs from oldest to youngest. If the number of items
    in the date range exceeds 1000, `until` indicates the timestamp of the youngest
    item on the page. Also, `nextPage` provides the URL for the next page of worklogs.
    The `lastPage` parameter is set to true on the last page of worklogs.  \n  \nThis
    resource does not return worklogs updated during the minute preceding the request.
    \ \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2worklogupdated-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2worklogupdated-get-openapi.md
- name: Jira Cloud REST API - Find users with browse permission
  x-api-slug: api2userviewissuesearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have permission to browse issues.

    Use this resource to find users who can browse:

    *   an issue, by providing the `issueKey`.
    *   any issue in a project, by providing the `projectKey`.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-openapi.md
- name: Jira Cloud REST API - Find users with browse permission
  x-api-slug: api2userviewissuesearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have permission to browse issues.

    Use this resource to find users who can browse:

    *   an issue, by providing the `issueKey`.
    *   any issue in a project, by providing the `projectKey`.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-openapi.md
- name: Jira Cloud REST API - Find users with browse permission
  x-api-slug: api2userviewissuesearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have permission to browse issues.

    Use this resource to find users who can browse:

    *   an issue, by providing the `issueKey`.
    *   any issue in a project, by providing the `projectKey`.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-openapi.md
- name: Jira Cloud REST API - Find users with browse permission
  x-api-slug: api2userviewissuesearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have permission to browse issues.

    Use this resource to find users who can browse:

    *   an issue, by providing the `issueKey`.
    *   any issue in a project, by providing the `projectKey`.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-openapi.md
- name: Jira Cloud REST API - Find users with browse permission
  x-api-slug: api2userviewissuesearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have permission to browse issues.

    Use this resource to find users who can browse:

    *   an issue, by providing the `issueKey`.
    *   any issue in a project, by providing the `projectKey`.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-openapi.md
- name: Jira Cloud REST API - Find users with browse permission
  x-api-slug: api2userviewissuesearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have permission to browse issues.

    Use this resource to find users who can browse:

    *   an issue, by providing the `issueKey`.
    *   any issue in a project, by providing the `projectKey`.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2userviewissuesearch-get-openapi.md
- name: Jira Cloud REST API - Assign permission scheme
  x-api-slug: api2projectprojectkeyoridpermissionscheme-put
  description: |-
    Associates a permission scheme with a particular project. See [Managing project permissions](https://confluence.atlassian.com/x/yodKLg) for more information about permission schemes.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-put-openapi.md
- name: Jira Cloud REST API - Get assigned permission scheme
  x-api-slug: api2projectprojectkeyoridpermissionscheme-get
  description: |-
    Gets the [permission scheme](https://confluence.atlassian.com/x/yodKLg) associated with the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-get-openapi.md
- name: Jira Cloud REST API - Delete permission scheme entity
  x-api-slug: api2permissionschemeschemeidpermissionpermissionid-delete
  description: Deletes a permission grant from a permission scheme. See [About permission
    schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes)
    for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-delete-openapi.md
- name: Jira Cloud REST API - Delete permission scheme entity
  x-api-slug: api2permissionschemeschemeidpermissionpermissionid-delete
  description: Deletes a permission grant from a permission scheme. See [About permission
    schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes)
    for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-delete-openapi.md
- name: Jira Cloud REST API - Get permission scheme grant
  x-api-slug: api2permissionschemeschemeidpermissionpermissionid-get
  description: Returns a permission grant. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-get-openapi.md
- name: Jira Cloud REST API - Get permission scheme grant
  x-api-slug: api2permissionschemeschemeidpermissionpermissionid-get
  description: Returns a permission grant. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-get-openapi.md
- name: Jira Cloud REST API - Create permission grant
  x-api-slug: api2permissionschemeschemeidpermission-post
  description: Creates a new permission grant in the given permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-post-openapi.md
- name: Jira Cloud REST API - Get permission scheme grants
  x-api-slug: api2permissionschemeschemeidpermission-get
  description: Returns all permission grants for a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-get-openapi.md
- name: Jira Cloud REST API - Get permission scheme grants
  x-api-slug: api2permissionschemeschemeidpermission-get
  description: Returns all permission grants for a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeidpermission-get-openapi.md
- name: Jira Cloud REST API - Delete permission scheme
  x-api-slug: api2permissionschemeschemeid-delete
  description: Deletes a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-delete-openapi.md
- name: Jira Cloud REST API - Delete permission scheme
  x-api-slug: api2permissionschemeschemeid-delete
  description: Deletes a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-delete-openapi.md
- name: Jira Cloud REST API - Update permission scheme
  x-api-slug: api2permissionschemeschemeid-put
  description: |-
    Updates a permission scheme. Below are some important things to note when using this resource:

    *   If a permissions list is present in the request, then it will be set in the permission scheme, overwriting _all existing_ grants.
    *   If you want to update only the name and description, then do not send a permissions list in the request.
    *   Sending an empty list will remove all permission grants from the permission scheme.

    If you want to add or delete a single permission grant instead of updating the whole list, see [Create permission grant](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-post) or [Delete permission scheme entity](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-permissionId-delete). See [About permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes) for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-put-openapi.md
- name: Jira Cloud REST API - Update permission scheme
  x-api-slug: api2permissionschemeschemeid-put
  description: |-
    Updates a permission scheme. Below are some important things to note when using this resource:

    *   If a permissions list is present in the request, then it will be set in the permission scheme, overwriting _all existing_ grants.
    *   If you want to update only the name and description, then do not send a permissions list in the request.
    *   Sending an empty list will remove all permission grants from the permission scheme.

    If you want to add or delete a single permission grant instead of updating the whole list, see [Create permission grant](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-post) or [Delete permission scheme entity](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-permissionId-delete). See [About permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes) for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-put-openapi.md
- name: Jira Cloud REST API - Get permission scheme
  x-api-slug: api2permissionschemeschemeid-get
  description: Returns a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-get-openapi.md
- name: Jira Cloud REST API - Get permission scheme
  x-api-slug: api2permissionschemeschemeid-get
  description: Returns a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionschemeschemeid-get-openapi.md
- name: Jira Cloud REST API - Create permission scheme
  x-api-slug: api2permissionscheme-post
  description: Creates a new permission scheme. You can create a permission scheme
    with or without defining a set of permission grants. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-post-openapi.md
- name: Jira Cloud REST API - Create permission scheme
  x-api-slug: api2permissionscheme-post
  description: Creates a new permission scheme. You can create a permission scheme
    with or without defining a set of permission grants. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-post-openapi.md
- name: Jira Cloud REST API - Get all permission schemes
  x-api-slug: api2permissionscheme-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-get-openapi.md
- name: Jira Cloud REST API - Get all permission schemes
  x-api-slug: api2permissionscheme-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2permissionscheme-get-openapi.md
- name: Jira Cloud REST API - Delete share permission
  x-api-slug: api2filteridpermissionpermissionid-delete
  description: Deletes a share permission from a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and the calling user must own the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-delete-openapi.md
- name: Jira Cloud REST API - Delete share permission
  x-api-slug: api2filteridpermissionpermissionid-delete
  description: Deletes a share permission from a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and the calling user must own the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-delete-openapi.md
- name: Jira Cloud REST API - Get share permission
  x-api-slug: api2filteridpermissionpermissionid-get
  description: Returns a share permission for a filter. A filter can be shared with
    groups, projects, all logged-in users, or the public. Sharing with all logged-in
    users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-get-openapi.md
- name: Jira Cloud REST API - Get share permission
  x-api-slug: api2filteridpermissionpermissionid-get
  description: Returns a share permission for a filter. A filter can be shared with
    groups, projects, all logged-in users, or the public. Sharing with all logged-in
    users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermissionpermissionid-get-openapi.md
- name: Jira Cloud REST API - Add share permission
  x-api-slug: api2filteridpermission-post
  description: "Add a share permissions to a filter. If you add a global share permission
    (i.e., all logged-in users or the public) it will overwrite all share permissions
    for the filter.  \nBe aware that this method uses different objects for updating
    share permissions compared to [Update filter](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-id-put).
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Share
    dashboards and filters_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    and the calling user must own the filter."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-post-openapi.md
- name: Jira Cloud REST API - Add share permission
  x-api-slug: api2filteridpermission-post
  description: "Add a share permissions to a filter. If you add a global share permission
    (i.e., all logged-in users or the public) it will overwrite all share permissions
    for the filter.  \nBe aware that this method uses different objects for updating
    share permissions compared to [Update filter](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-id-put).
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Share
    dashboards and filters_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    and the calling user must own the filter."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/atlassian/api2filteridpermission-post-openapi.md
x-common:
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/platform/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/confluence/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/software/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/service-desk/swagger.v3.json
- type: x-website
  url: http://atlassian.com/
- type: x-website
  url: http://www.atlassian.com
- type: x-api-gallery
  url: http://att.dev.program.api.gallery.streamdata.io
- type: x-api-stack
  url: http://atlassian.stack.network
- type: x-blog
  url: http://blogs.atlassian.com/
- type: x-crunchbase
  url: https://crunchbase.com/organization/atlassian
- type: x-crunchbase
  url: http://www.crunchbase.com/company/atlassian
- type: x-email
  url: copyright@atlassian.com
- type: x-email
  url: trademarks@atlassian.com
- type: x-email
  url: sales@atlassian.com
- type: x-email
  url: ar_enterprise@atlassian.com
- type: x-email
  url: privacy@atlassian.com
- type: x-email
  url: eudatarep@atlassian.com
- type: x-email
  url: experts@atlassian.com
- type: x-email
  url: remittance@atlassian.com
- type: x-email
  url: ap@atlassian.com
- type: x-email
  url: procurement@atlassian.com
- type: x-github
  url: https://github.com/atlassian
- type: x-privacy-policy
  url: https://www.atlassian.com/legal/privacy-policy?_ga=2.188884514.868776184.1519225620-845241124.1519225620
- type: x-twitter
  url: https://twitter.com/atlassian
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---