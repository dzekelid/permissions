---
name: Apigee
x-slug: apigee
description: Apigee Edge is a platform for developing and managing API proxies. Think
  of a proxy as an abstraction layer that fronts for your backend service APIs and
  provides value-added features like security, rate limiting, quotas, analytics, and
  more. The primary consumers of Edge API proxies are app developers who want to use
  your backend services.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
x-kinRank: "8"
x-alexaRank: "0"
tags: Permissions
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/apis.md
specificationVersion: "0.14"
apis:
- name: Apigee Edge Get Organizations Name Userroles Role Name Permissions
  x-api-slug: apigee-edge
  description: Gets a list of permissions associated with the specified resource for
    a single resource.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///organizations/{org_name}/userroles/{role_name}/permissions
  tags: Organizations,Userroles,Role,Permissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/organizationsorg-nameuserrolesrole-namepermissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/organizationsorg-nameuserrolesrole-namepermissions-get-openapi.md
- name: Apigee Edge Post Organizations Name Userroles Role Name Permissions
  x-api-slug: apigee-edge
  description: Associates permissions for a resource with a user role.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///organizations/{org_name}/userroles/{role_name}/permissions
  tags: Organizations,Userroles,Role,Permissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/organizationsorg-nameuserrolesrole-namepermissions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/organizationsorg-nameuserrolesrole-namepermissions-post-openapi.md
- name: Apigee Edge Get Organizations Name Userroles Role Name Permissions Get
  x-api-slug: apigee-edge
  description: Checks the particular userrole permission of a resource at organization
    level.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///organizations/{org_name}/userroles/{role_name}/permissions/get
  tags: Organizations,Userroles,Role,Permissions,Get
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/organizationsorg-nameuserrolesrole-namepermissionsget-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/organizationsorg-nameuserrolesrole-namepermissionsget-get-openapi.md
- name: Apigee Edge Delete Organizations Name Userroles Role Name Permissions Get
  x-api-slug: apigee-edge
  description: Deletes particular userrole permission at organization level.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///organizations/{org_name}/userroles/{role_name}/permissions/get
  tags: Organizations,Userroles,Role,Permissions,Get
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/organizationsorg-nameuserrolesrole-namepermissionsget-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/organizationsorg-nameuserrolesrole-namepermissionsget-delete-openapi.md
- name: Apigee Edge Post Organizations Name Userroles Role Name Resourcepermissions
  x-api-slug: apigee-edge
  description: Adds multiple resource permissions for resource at organization level.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///organizations/{org_name}/userroles/{role_name}/resourcepermissions
  tags: Organizations,Userroles,Role,Resourcepermissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/organizationsorg-nameuserrolesrole-nameresourcepermissions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/organizationsorg-nameuserrolesrole-nameresourcepermissions-post-openapi.md
- name: Apigee Edge Get Userroles Role Name Permissions
  x-api-slug: apigee-edge
  description: Gets permission for a specific resource at global level.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///userroles/{role_name}/permissions
  tags: Userroles,Role,Permissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/userrolesrole-namepermissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/userrolesrole-namepermissions-get-openapi.md
- name: Apigee Edge Post Userroles Role Name Permissions
  x-api-slug: apigee-edge
  description: Adds permissions for resource at global level.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///userroles/{role_name}/permissions
  tags: Userroles,Role,Permissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/userrolesrole-namepermissions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/userrolesrole-namepermissions-post-openapi.md
- name: Apigee Edge Get Userroles Role Name Permissions Get
  x-api-slug: apigee-edge
  description: Checks particular userrole permission for a resource at global level.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///userroles/{role_name}/permissions/get
  tags: Userroles,Role,Permissions,Get
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/userrolesrole-namepermissionsget-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/userrolesrole-namepermissionsget-get-openapi.md
- name: Apigee Edge Delete Userroles Role Name Permissions Get
  x-api-slug: apigee-edge
  description: Deletes particular userrole permission for a resource at global level
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///userroles/{role_name}/permissions/get
  tags: Userroles,Role,Permissions,Get
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/userrolesrole-namepermissionsget-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/userrolesrole-namepermissionsget-delete-openapi.md
- name: Apigee Edge Post Userroles Role Name Resourcepermissions
  x-api-slug: apigee-edge
  description: Adds multiple resource permissions for resource at global level.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///userroles/{role_name}/resourcepermissions
  tags: Userroles,Role,Resourcepermissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/userrolesrole-nameresourcepermissions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/userrolesrole-nameresourcepermissions-post-openapi.md
- name: Apigee Edge Get Users User Name Permissions
  x-api-slug: apigee-edge
  description: Gets permissions for a user at global level
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///users/{user_name}/permissions
  tags: Users,User,Permissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/usersuser-namepermissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/usersuser-namepermissions-get-openapi.md
- name: Apigee Edge Get Users User Email Permissions Get
  x-api-slug: apigee-edge
  description: Checks user has particular permission for a resource at global level
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1///users/{user_email}permissions/get
  tags: Users,User,Emailpermissions,Get
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/usersuser-emailpermissionsget-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/usersuser-emailpermissionsget-get-openapi.md
- name: Apigee Edge
  x-api-slug: apigee-edge
  description: Apigee Edge is a platform for developing and managing API proxies.
    Think of a proxy as an abstraction layer that fronts for your backend service
    APIs and provides value-added features like security, rate limiting, quotas, analytics,
    and more. The primary consumers of Edge API proxies are app developers who want
    to use your backend services.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/apigee-edge.png
  humanURL: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
  baseURL: https://api.enterprise.apigee.com//v1/
  tags: Permissions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/apigee/openapi.md
x-common:
- type: x-website
  url: https://docs.apigee.com/api-platform/get-started/what-apigee-edge
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---