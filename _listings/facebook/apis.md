---
name: Facebook
x-slug: facebook
description: Create an account or log into Facebook. Connect with friends, family
  and other people you know. Share photos and videos, send messages and get updates.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/196-facebook.jpg
x-kinRank: "9"
x-alexaRank: "3"
tags: Permissions
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/facebook/apis.md
specificationVersion: "0.14"
apis:
- name: Facebook Get User Permissions
  x-api-slug: facebook
  description: The permissions that user has granted the application.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/196-facebook.jpg
  humanURL: http:///business
  baseURL: https://graph.facebook.com////{user}/permissions
  tags: User,Permissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/facebook/userpermissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/facebook/userpermissions-get-openapi.md
- name: Facebook Delete User Permissions
  x-api-slug: facebook
  description: De-authorizes an application or revokes a specific extended permissions
    on behalf of a user
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/196-facebook.jpg
  humanURL: http:///business
  baseURL: https://graph.facebook.com////{user}/permissions
  tags: User,Permissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/facebook/userpermissions-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/facebook/userpermissions-delete-openapi.md
- name: Facebook
  x-api-slug: facebook
  description: Create an account or log into Facebook. Connect with friends, family
    and other people you know. Share photos and videos, send messages and get updates.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/196-facebook.jpg
  humanURL: http:///business
  baseURL: https://graph.facebook.com//
  tags: Permissions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/facebook/openapi.md
x-common:
- type: x-android-sdk
  url: https://developers.facebook.com/docs/android/share
- type: x-apigee-console
  url: https://api.apigee.com/v1/consoles/facebook/apidescription?format=internal&ver=1386216190000
- type: x-application-gallery
  url: https://developers.facebook.com/docs/showcase/
- type: x-base
  url: https://graph.facebook.com
- type: x-best-practices
  url: https://developers.facebook.com/docs/sharing/best-practices
- type: x-blog
  url: http://blog.facebook.com
- type: x-blog-rss
  url: https://www.facebook.com/business/news/rss/
- type: x-crunchbase
  url: http://www.crunchbase.com/company/facebook
- type: x-crunchbase
  url: https://crunchbase.com/organization/facebook
- type: x-developer
  url: https://developers.facebook.com/
- type: x-forum
  url: https://www.facebook.com/groups/fbdevelopers
- type: x-github
  url: https://github.com/facebook
- type: x-ios-sdk
  url: https://developers.facebook.com/docs/ios/share
- type: x-issues
  url: https://developers.facebook.com/status/issues/
- type: x-javascript-library
  url: https://developers.facebook.com/docs/reference/javascript/
- type: x-partners
  url: https://facebookmarketingpartners.com/
- type: x-php-sdk
  url: https://developers.facebook.com/docs/reference/php/
- type: x-plugins
  url: https://developers.facebook.com/docs/plugins/
- type: x-privacy
  url: https://www.facebook.com/settings?tab=privacy
- type: x-road-map
  url: https://developers.facebook.com/docs/apps/migrations
- type: x-status
  url: https://developers.facebook.com/status/
- type: x-terms-of-service
  url: https://www.facebook.com/terms
- type: x-terms-of-service
  url: https://developers.facebook.com/policy
- type: x-transparency-report
  url: https://www.facebook.com/about/government_requests
- type: x-twitter
  url: https://twitter.com/facebook
- type: x-website
  url: http:///business
- type: x-website
  url: http://facebook.com
- type: x-website
  url: https://facebook.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---