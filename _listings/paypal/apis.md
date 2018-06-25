---
name: PayPal
x-slug: paypal
description: PayPal is the faster, safer way to send money, make an online payment,
  receive money or set up a merchant account.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
x-kinRank: "10"
x-alexaRank: "71"
tags: Permissions
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/paypal/apis.md
specificationVersion: "0.14"
apis:
- name: Paypal Cancel Permissions
  x-api-slug: paypal
  description: Use the CancelPermissions API operation to cancel access to a set of
    permissions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com////Permissions/CancelPermissions
  tags: Payments,Permissions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/paypal/permissionscancelpermissions-post-openapi.md
- name: Paypal Get Permissions
  x-api-slug: paypal
  description: Use the GetPermissons API operation to obtain the permissions associated
    with an access token.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com////Permissions/GetPermissions
  tags: Payments,Permissions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/paypal/permissionsgetpermissions-post-openapi.md
- name: Paypal Request Permissions
  x-api-slug: paypal
  description: "Use the RequestPermissions API operation to request permissions to
    execute API operations on a PayPal account holder\u2019s behalf."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com////Permissions/RequestPermissions
  tags: Payments,Permissions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/paypal/permissionsrequestpermissions-post-openapi.md
- name: Paypal
  x-api-slug: paypal
  description: PayPal is the faster, safer way to send money, make an online payment,
    receive money or set up a merchant account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com//
  tags: Permissions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/paypal/openapi.md
x-common:
- type: x-base-url
  url: https://api.paypal.com
- type: x-crunchbase
  url: https://crunchbase.com/organization/paypal
- type: x-crunchbase
  url: http://www.crunchbase.com/company/paypal
- type: x-developer
  url: https://developer.paypal.com/
- type: x-faq
  url: https://developer.paypal.com/docs/faq/
- type: x-getting-started
  url: https://developer.paypal.com/docs/
- type: x-github
  url: https://github.com/paypal
- type: x-playground
  url: https://devtools-paypal.com/hateoas/index.html
- type: x-privacy
  url: https://www.paypal.com/us/cgi-bin/webscr?cmd=p/gen/ua/policy_privacy-outside
- type: x-release-notes
  url: https://developer.paypal.com/docs/release-notes/
- type: x-terms-of-service
  url: https://cms.paypal.com/us/cgi-bin/?cmd=_render-content&content_ID=ua/Legal_Hub_full
- type: x-twitter
  url: https://twitter.com/paypal
- type: x-website
  url: https://paypal.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---