---
name: AWS Simple Queue Service
description: Amazon Simple Queue Service (SQS) is a fast, reliable, scalable, fully
  managed message queuing service. Amazon SQS makes it simple and cost-effective to
  decouple the components of a cloud application. You can use Amazon SQS to transmit
  any volume of data, without losing messages or requiring other services to be always
  available. Amazon SQS includesnbsp;standard queuesnbsp;with high throughput and
  at-least-once processing, andnbsp;FIFO queuesnbsp;that provide FIFO (first-in, first-out)
  delivery and exactly-once processing. nbsp;nWith Amazon SQS, you can offload the
  administrative burden of operating and scaling a highly available messaging cluster,
  while paying a low price for only what you use.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Application-Services_AmazonSQS.png
x-kinRank: "10"
x-alexaRank: ""
tags:
- Stack Network
- Orchestration
- Jobs
- Amazon Web Services
created: "2018-03-23"
modified: "2018-03-23"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/aws-simple-queue-service/apis.yaml
specificationVersion: "0.14"
apis:
- name: AWS Simple Queue Service API
  description: Amazon Simple Queue Service (SQS) is a fast, reliable, scalable, fully
    managed message queuing service
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Application-Services_AmazonSQS.png
  humanURL: ""
  baseURL: :///
  tags: Permissions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/aws-simple-queue-service/action-removepermission-get.md
- name: AWS Simple Queue Service API Remove Permission
  description: Revokes any permissions in the queue policy that matches the specified
    Label parameter.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Application-Services_AmazonSQS.png
  humanURL: https://aws.amazon.com/sqs/
  baseURL: http:://{host}//
  tags: Permissions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/permissions/master/_listings/aws-simple-queue-service/action-removepermission-get.md
x-common:
- type: x-change-log
  url: http://aws.amazon.com/releasenotes/Amazon-SQ
- type: x-command-line-interface
  url: http://docs.aws.amazon.com/cli/latest/reference/sqs/index.html
- type: x-console
  url: https://console.aws.amazon.com/sqs/
- type: x-documentation
  url: http://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/
- type: x-faq
  url: https://aws.amazon.com/sqs/faqs/
- type: x-forum
  url: https://forums.aws.amazon.com/forum.jspa?forumID=12
- type: x-getting-started
  url: https://aws.amazon.com/sqs/getting-started/
- type: x-pricing
  url: https://aws.amazon.com/sqs/pricing/
- type: x-website
  url: https://aws.amazon.com/sqs/
- type: x-change-log
  url: http://aws.amazon.com/releasenotes/Amazon-SQ
- type: x-command-line-interface
  url: http://docs.aws.amazon.com/cli/latest/reference/sqs/index.html
- type: x-console
  url: https://console.aws.amazon.com/sqs/
- type: x-documentation
  url: http://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/
- type: x-faq
  url: https://aws.amazon.com/sqs/faqs/
- type: x-forum
  url: https://forums.aws.amazon.com/forum.jspa?forumID=12
- type: x-getting-started
  url: https://aws.amazon.com/sqs/getting-started/
- type: x-pricing
  url: https://aws.amazon.com/sqs/pricing/
- type: x-website
  url: https://aws.amazon.com/sqs/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---