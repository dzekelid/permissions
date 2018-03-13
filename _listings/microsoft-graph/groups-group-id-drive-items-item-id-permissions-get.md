---
swagger: "2.0"
info:
  title: Microsoft Graph API
  description: 'Microsoft Graph exposes multiple APIs from Office 365 and other Microsoft
    cloud services through a single endpoint: https://graph.microsoft.com. Microsoft
    Graph simplifies queries that would otherwise be more complex.'
  version: 1.0.0
host: graph.microsoft.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /groups/{group-id}/drive/items/{item-id}/permissions:
    get:
      summary: List Permissions On A Drive Item
      description: List permissions on a DriveItem List the effective permissions
        of on a DriveItem
      operationId: ListPermissionsOnADriveItem
      parameters:
      - in: path
        name: group-id
        type: string
      - in: header
        name: if-none-match
        description: If this request header is included and the etag provided matches
          the current etag on the item, an HTTP 304 Not Modified response is returned
        type: string
      - in: path
        name: item-id
        type: string
      responses:
        200:
          description: Successful Response
          schema:
            type: array
            items:
              $ref: '#/definitions/Permission'
      tags:
      - list
      - permissions
      - ondrive
      - item
definitions:
  alternativeSecurityId:
    properties:
      identityProvider:
        description: This is a default description.
        type: String
      key:
        description: This is a default description.
        type: Binary
      type:
        description: This is a default description.
        type: Int32
  assignedLicense:
    properties:
      disabledPlans:
        description: A collection of the unique identifiers for plans that have been
          disabled.
        type: Guid collection
      skuId:
        description: The unique identifier for the SKU.
        type: Guid
  assignedPlan:
    properties:
      assignedDateTime:
        description: 'The date and time at which the plan was assigned; for example:
          2013-01-02T19:32:30Z. The Timestamp type represents date and time information
          using ISO 8601 format and is always in UTC time. For example, midnight UTC
          on Jan 1, 2014 would look like this: 2014-01-01T00:00:00Z'
        type: DateTimeOffset
      capabilityStatus:
        description: "For example, \u201CEnabled\u201D."
        type: String
      service:
        description: "The name of the service; for example, \u201CExchange\u201D."
        type: String
      servicePlanId:
        description: A GUID that identifies the service plan.
        type: Guid
  attachment:
    properties:
      Get attachment:
        description: Read the properties and relationships of an attachment, attached
          to an event, message, or post.
        type: attachment
      Add attachment to an event:
        description: Add a file, item, or link attachment to an event.
        type: attachment
      Add attachment to a message:
        description: Add a file, item, or link attachment to a message.
        type: attachment
      Add attachment to a post:
        description: Add a file, item, or link attachment to a post.
        type: attachment
      List attachments of an event:
        description: Get a list of attachments for an event.
        type: attachment collection
      List attachments of a message:
        description: Get a list of attachments for a message.
        type: attachment collection
      List attachments of a post:
        description: Get a list of attachments for a post.
        type: attachment collection
      Delete:
        description: Delete an attachment on an event, message, or post.
        type: None
  attendee:
    properties:
      status:
        description: The attendees response (none, accepted, declined, etc.) for the
          event and date-time that the response was sent.
        type: ResponseStatus
      type:
        description: 'The attendee type: Required, Optional, Resource.'
        type: String
      emailAddress:
        description: Includes the name and SMTP address of the attendee.
        type: emailAddress
  attendeeAvailability:
    properties:
      attendee:
        description: The type of attendee - whether its a person or a resource, and
          whether required or optional if its a person.
        type: AttendeeBase
      availability:
        description: 'The availability status of the attendee. Possible values are:
          free, tentative, busy, oof, workingElsewhere, unknown.'
        type: String
  attendeeBase:
    properties:
      type:
        description: 'The type of attendee. Possible values are: required, optional,
          resource. Currently if the attendee is a person, findMeetingTimes always
          considers the person is of the Required type.'
        type: String
      emailAddress:
        description: Includes the name and SMTP address of the attendee.
        type: emailAddress
  Audio:
    properties:
      album:
        description: The title of the album for this audio file.
        type: string
      albumArtist:
        description: The artist named on the album for the audio file.
        type: string
      artist:
        description: The performing artist for the audio file.
        type: string
      bitrate:
        description: Bitrate expressed in kbps.
        type: string
      composers:
        description: The name of the composer of the audio file.
        type: string
      copyright:
        description: Copyright information for the audio file.
        type: string
      disc:
        description: The number of the disc this audio file came from.
        type: number
      discCount:
        description: The total number of discs in this album.
        type: number
      duration:
        description: Duration of the audio file, expressed in milliseconds
        type: number
      genre:
        description: The genre of this audio file.
        type: string
  automaticRepliesSetting:
    properties:
      externalAudience:
        description: 'The set of audience external to the signed-in users organization
          who will receive the ExternalReplyMessage, if Status is AlwaysEnabled or
          Scheduled. Possible values are: none, contactsOnly, all.'
        type: String
      externalReplyMessage:
        description: The automatic reply to send to the specified external audience,
          if Status is AlwaysEnabled or Scheduled.
        type: string
      internalReplyMessage:
        description: The automatic reply to send to the audience internal to the signed-in
          users organization, if Status is AlwaysEnabled or Scheduled.
        type: string
      scheduledEndDateTime:
        description: The date and time that automatic replies are set to end, if Status
          is set to Scheduled.
        type: dateTimeTimeZone
      scheduledStartDateTime:
        description: The date and time that automatic replies are set to begin, if
          Status is set to Scheduled.
        type: dateTimeTimeZone
      status:
        description: 'Configurations status for automatic replies. Possible values
          are: disabled, alwaysEnabled, scheduled.'
        type: String
  calendar:
    properties:
      List calendars:
        description: Get all the users calendars, or the calendars in the default
          or other specific calendar group.
        type: calendar collection
      Create calendar:
        description: Create a new calendar in the default calendar group or specified
          calendar group.
        type: calendar
      Get calendar:
        description: Read properties and relationships of calendar object.
        type: calendar
      Update:
        description: Update calendar object.
        type: calendar
      Delete:
        description: Delete calendar object.
        type: None
      List calendarView:
        description: Get the occurrences, exceptions, and single instances of events
          in a calendar view defined by a time range, from the users primary calendar
          (../me/calendarview) or from a specified calendar.
        type: Event collection
      List events:
        description: Retrieve a list of events in a calendar.  The list contains single
          instance meetings and series masters.
        type: Event collection
      Create Event:
        description: Create a new Event in the default or specified calendar.
        type: Event
      Create single-value extended property:
        description: Create one or more single-value extended properties in a new
          or existing calendar.
        type: calendar
      Get calendar with single-value extended property:
        description: Get calendars that contain a single-value extended property by
          using $expand or $filter.
        type: calendar
  calendarGroup:
    properties:
      List calendar groups:
        description: Get the users calendar groups.
        type: Calendar collection
      Create calendar group:
        description: Create a new calendar group.
        type: Calendar
      Get calendar group:
        description: Read properties and relationships of a calendar group object.
        type: calendarGroup
      Update:
        description: Update calendarGroup object.
        type: calendarGroup
      Delete:
        description: Delete calendarGroup object.
        type: None
      List calendars:
        description: List calendars in a calendar group.
        type: Calendar collection
      Create Calendar:
        description: Create a new Calendar in a calendar group.
        type: Calendar
  Chart:
    properties:
      Get Chart:
        description: Read properties and relationships of chart object.
        type: Chart
      Create ChartSeries:
        description: Create a new ChartSeries by posting to the series collection.
        type: ChartSeries
      List series:
        description: Get a ChartSeries object collection.
        type: ChartSeries collection
      Update:
        description: Update Chart object.
        type: Chart
      Image:
        description: Renders the chart as a base64-encoded image by scaling the chart
          to fit the specified dimensions.
        type: Image base64 encoded string
      Delete:
        description: Deletes the chart object.
        type: None
      Setdata:
        description: Resets the source data for the chart.
        type: None
      Setposition:
        description: Positions the chart relative to cells on the worksheet.
        type: None
      List:
        description: Get chart object collection.
        type: Chart collection
      Itemat:
        description: Gets a chart based on its position in the collection.
        type: Chart
  ChartAreaFormat:
    properties:
      fill:
        description: Represents the fill format of an object, which includes background
          formatting information. Read-only.
        type: ChartFill
      font:
        description: Represents the font attributes (font name, font size, color,
          etc.) for the current object. Read-only.
        type: ChartFont
  ChartAxes:
    properties:
      categoryAxis:
        description: Represents the category axis in a chart. Read-only.
        type: ChartAxis
      seriesAxis:
        description: Represents the series axis of a 3-dimensional chart. Read-only.
        type: ChartAxis
      valueAxis:
        description: Represents the value axis in an axis. Read-only.
        type: ChartAxis
  ChartAxis:
    properties:
      Get ChartAxis:
        description: Read properties and relationships of chartAxis object.
        type: ChartAxis
      Update:
        description: Update ChartAxis object.
        type: ChartAxis
  ChartAxisFormat:
    properties:
      font:
        description: Represents the font attributes (font name, font size, color,
          etc.) for a chart axis element. Read-only.
        type: ChartFont
      line:
        description: Represents chart line formatting. Read-only.
        type: ChartLineFormat
  ChartAxisTitle:
    properties:
      Get ChartAxisTitle:
        description: Read properties and relationships of chartAxisTitle object.
        type: ChartAxisTitle
      Update:
        description: Update ChartAxisTitle object.
        type: ChartAxisTitle
  ChartAxisTitleFormat:
    properties:
      font:
        description: Represents the font attributes, such as font name, font size,
          color, etc. of chart axis title object. Read-only.
        type: ChartFont
  ChartDataLabelFormat:
    properties:
      fill:
        description: Represents the fill format of the current chart data label. Read-only.
        type: ChartFill
      font:
        description: Represents the font attributes (font name, font size, color,
          etc.) for a chart data label. Read-only.
        type: ChartFont
  ChartDataLabels:
    properties:
      Get ChartDataLabels:
        description: Read properties and relationships of chartDataLabels object.
        type: ChartDataLabels
      Update:
        description: Update ChartDataLabels object.
        type: ChartDataLabels
  ChartFill:
    properties:
      Clear:
        description: Clear the fill color of a chart element.
        type: None
      Setsolidcolor:
        description: Sets the fill formatting of a chart element to a uniform color.
        type: None
  ChartFont:
    properties:
      Get ChartFont:
        description: Read properties and relationships of chartFont object.
        type: ChartFont
      Update:
        description: Update ChartFont object.
        type: ChartFont
  ChartGridlines:
    properties:
      Get ChartGridlines:
        description: Read properties and relationships of chartGridlines object.
        type: ChartGridlines
      Update:
        description: Update ChartGridlines object.
        type: ChartGridlines
  ChartGridlinesFormat:
    properties:
      line:
        description: Represents chart line formatting. Read-only.
        type: ChartLineFormat
  ChartLegend:
    properties:
      Get ChartLegend:
        description: Read properties and relationships of chartLegend object.
        type: ChartLegend
      Update:
        description: Update ChartLegend object.
        type: ChartLegend
  ChartLegendFormat:
    properties:
      fill:
        description: Represents the fill format of an object, which includes background
          formating information. Read-only.
        type: ChartFill
      font:
        description: Represents the font attributes such as font name, font size,
          color, etc. of a chart legend. Read-only.
        type: ChartFont
  ChartLineFormat:
    properties:
      Get ChartLineFormat:
        description: Read properties and relationships of chartLineFormat object.
        type: ChartLineFormat
      Update:
        description: Update ChartLineFormat object.
        type: ChartLineFormat
      Clear:
        description: Clear the line format of a chart element.
        type: None
  ChartPoint:
    properties:
      Get ChartPoint:
        description: Read properties and relationships of chartPoint object.
        type: ChartPoint
      List:
        description: Get chartPoint object collection.
        type: ChartPoint collection
      Itemat:
        description: Retrieve a point based on its position within the series.
        type: ChartPoint
  ChartPointFormat:
    properties:
      fill:
        description: Represents the fill format of a chart, which includes background
          formating information. Read-only.
        type: ChartFill
  ChartSeries:
    properties:
      Get ChartSeries:
        description: Read properties and relationships of chartSeries object.
        type: ChartSeries
      Create ChartPoints:
        description: Create a new ChartPoints by posting to the points collection.
        type: ChartPoints
      List points:
        description: Get a ChartPoints object collection.
        type: ChartPoints collection
      Update:
        description: Update ChartSeries object.
        type: ChartSeries
      List:
        description: Get chartSeries object collection.
        type: ChartSeries collection
      Itemat:
        description: Retrieves a series based on its position in the collection
        type: ChartSeries
  ChartSeriesFormat:
    properties:
      fill:
        description: Represents the fill format of a chart series, which includes
          background formating information. Read-only.
        type: ChartFill
      line:
        description: Represents line formatting. Read-only.
        type: ChartLineFormat
  ChartTitle:
    properties:
      Get ChartTitle:
        description: Read properties and relationships of chartTitle object.
        type: ChartTitle
      Update:
        description: Update ChartTitle object.
        type: ChartTitle
  ChartTitleFormat:
    properties:
      fill:
        description: Represents the fill format of an object, which includes background
          formatting information. Read-only.
        type: ChartFill
      font:
        description: Represents the font attributes (font name, font size, color,
          etc.) for the current object. Read-only.
        type: ChartFont
  chunkedUploadSessionDescriptor:
    properties:
      name:
        description: This is a default description.
        type: String
  contact:
    properties:
      Get contact:
        description: Read properties and relationships of contact object.
        type: contact
      Create:
        description: Add a contact to the root Contacts folder or to the contacts
          endpoint of another contact folder.
        type: contact
      Update:
        description: Update contact object.
        type: contact
      Delete:
        description: Delete contact object.
        type: None
      Create open extension:
        description: Create an open extension and add custom properties in a new or
          existing instance of a resource.
        type: openTypeExtension
      Get open extension:
        description: Get an open extension object or objects identified by name or
          fully qualified name.
        type: openTypeExtension collection
      Create single-value extended property:
        description: Create one or more single-value extended properties in a new
          or existing contact.
        type: contact
      Get contact with single-value extended property:
        description: Get contacts that contain a single-value extended property by
          using $expand or $filter.
        type: contact
      Create multi-value extended property:
        description: Create one or more multi-value extended properties in a new or
          existing contact.
        type: contact
      Get contact with multi-value extended property:
        description: Get a contact that contains a multi-value extended property by
          using $expand.
        type: contact
  contactFolder:
    properties:
      Get contactFolder:
        description: Get a contact folder by using the contact folder ID.
        type: contactFolder
      Update:
        description: Update contactFolder object.
        type: contactFolder
      Delete:
        description: Delete contactFolder object.
        type: None
      List childFolders:
        description: Get a collection of child folders under the specified contact
          folder.
        type: ContactFolder collection
      Create child contactFolder:
        description: Create a new contactFolder as a child of a specified folder.
        type: ContactFolder
      List contacts in folder:
        description: Get a contact collection from the default Contacts folder of
          the signed-in user (.../me/contacts), or from the specified contact folder.
        type: Contact collection
      Create contact in folder:
        description: Add a contact to the root Contacts folder or to the contacts
          endpoint of another contact folder.
        type: Contact
      Create single-value extended property:
        description: Create one or more single-value extended properties in a new
          or existing contactFolder.
        type: contactFolder
      Get contactFolder with single-value extended property:
        description: Get contactFolders that contain a single-value extended property
          by using $expand or $filter.
        type: contactFolder
      Create multi-value extended property:
        description: Create one or more multi-value extended properties in a new or
          existing contactFolder.
        type: contactFolder
  conversation:
    properties:
      List conversations:
        description: Get the list of conversations in this group.
        type: conversation collection
      Create:
        description: Create a new conversation by including a thread and a post.
        type: conversation
      Get conversation:
        description: Read properties and relationships of conversation object.
        type: conversation
      Delete:
        description: Delete conversation object.
        type: None
      List conversation threads:
        description: Get all the threads in a group conversation.
        type: conversationThread collection
      Create conversation thread:
        description: Create a thread in the specified conversation.
        type: conversationThread collection
  conversationThread:
    properties:
      List threads:
        description: Get all the threads of a group.
        type: conversationThread collection
      Create thread:
        description: Start a new conversation by first creating a thread. A new conversation,
          conversation thread, and post are created in the group.
        type: conversationThread
      Get conversationThread:
        description: Get a specific thread that belongs to a group.
        type: conversationThread
      Update:
        description: Update conversationThread object.
        type: conversationThread
      Delete:
        description: Delete conversationThread object.
        type: None
      Reply:
        description: Reply to this thread by creating a new Post entity.
        type: None
      List Posts:
        description: Get the posts of the specified thread.
        type: post collection
  dateTimeTimeZone:
    properties:
      DateTime:
        description: A single point of time in a combined date and time representation
          (&lt;date&gt;T&lt;time&gt;).
        type: String
      TimeZone:
        description: One of the following time zone names.
        type: String
  Deleted:
    properties:
      state:
        description: Represents the state of the deleted item.
        type: String
  device:
    properties:
      Create device:
        description: Create a new registered device in the directory.
        type: device
      Get device:
        description: Read properties and relationships of a device object.
        type: device
      List devices:
        description: Retrieve a list of devices registered in the directory.
        type: device collection
      Update device:
        description: Update the properties of a device object.
        type: device
      Delete device:
        description: Delete a device object.
        type: None
      Create registeredOwner:
        description: Add a user as a new owner of the device by posting to the registeredOwners
          navigation property.
        type: directoryObject
      List registeredOwners:
        description: Get the users that are registered owners of the device from the
          registeredOwners navigation property.
        type: directoryObject collection
      Create registeredUser:
        description: Add a registered user for the device by posting to the registeredUsers
          navigation property.
        type: directoryObject
      List registeredUsers:
        description: Get the registered users of the device from the registeredUsers
          navigation property.
        type: directoryObject collection
  directoryObject:
    properties:
      Get directoryObject:
        description: Read the properties  of a directory object.
        type: directoryObject
      Delete directoryObject:
        description: Delete a directory object.
        type: None
      checkMemberGroups:
        description: Check for membership in a list of groups. The check is transitive.
        type: String collection
      getMemberGroups:
        description: Return all the groups that the user, group, or directory object
          is a member of. The check is transitive.
        type: String collection
      getMemberObjects:
        description: Return all of the groups and directory roles that the user, group,
          or directory object is a member of. The check is transitive.
        type: String collection
  directoryRole:
    properties:
      Get directoryRole:
        description: Read properties and relationships of directoryRole object.
        type: directoryRole
      Create member:
        description: Add a user to the directory role by posting to the members navigation
          property.
        type: directoryObject
      List members:
        description: Get the users that are members of the directory role from the
          members navigation property.
        type: directoryObject collection
      Activate directoryRole:
        description: Activate a directory role.
        type: directoryRole
  directoryRoleTemplate:
    properties:
      Get directoryRoleTemplate:
        description: Read properties and relationships of directoryRoleTemplate object.
        type: directoryRoleTemplate
      List directoryRoleTemplate:
        description: Retrieve a list of directoryRoleTemplate objects.
        type: directoryRoleTemplate collection
  Drive:
    properties:
      id:
        description: The unique identifier of the drive. Read-only.
        type: String
      driveType:
        description: Describes the type of drive represented by this resource. OneDrive
          personal drives will return personal. OneDrive for Business will return
          business. SharePoint document libraries will return documentLibrary. Read-only.
        type: String
      owner:
        description: Optional. The user account that owns the drive.
        type: identitySet
      quota:
        description: Optional. Information about the drives storage space quota.
        type: quota
  DriveItem:
    properties:
      audio:
        description: Audio metadata, if the item is an audio file. Read-only.
        type: audio
      content:
        description: The content stream, if the item represents a file.
        type: Stream
      createdBy:
        description: Identity of the user, device, and application which created the
          item. Read-only.
        type: identitySet
      createdDateTime:
        description: Date and time of item creation. Read-only.
        type: DateTimeOffset
      cTag:
        description: An eTag for the content of the item. This eTag is not changed
          if only the metadata is changed. Note This property is not returned if the
          item is a folder. Read-only.
        type: String
      deleted:
        description: Information about the deleted state of the item. Read-only.
        type: deleted
      eTag:
        description: eTag for the entire item (metadata + content). Read-only.
        type: String
      file:
        description: File metadata, if the item is a file. Read-only.
        type: file
      fileSystemInfo:
        description: File system information on client. Read-write.
        type: fileSystemInfo
      folder:
        description: Folder metadata, if the item is a folder. Read-only.
        type: folder
  DriveRecipient:
    properties:
      email:
        description: The email address for the recipient, if the recipient has an
          associated email address.
        type: String
      alias:
        description: The alias of the domain object, for cases where an email address
          is unavailable (e.g. security groups).
        type: String
      objectId:
        description: The unique identifier for the recipient in the directory.
        type: String
  emailAddress:
    properties:
      address:
        description: The email address of the person or entity.
        type: String
      name:
        description: The display name of the person or entity.
        type: String
  entity:
    properties:
      Get entity:
        description: Read properties and relationships of entity object.
        type: entity
      Delete:
        description: Delete entity object.
        type: None
  event:
    properties:
      List events:
        description: Retrieve a list of event objects in the users mailbox. The list
          contains single instance meetings and series masters.
        type: event collection
      Create event:
        description: Create a new event by posting to the instances collection.
        type: event
      Get event:
        description: Read properties and relationships of event object.
        type: event
      Update:
        description: Update event object.
        type: event
      Delete:
        description: Delete event object.
        type: None
      accept:
        description: Accept the specified event.
        type: None
      tentativelyAccept:
        description: Tentatively accept the specified event.
        type: None
      decline:
        description: Decline invitation to the specified event.
        type: None
      dismissReminder:
        description: Dismiss the reminder for the specified event.
        type: None
      snoozeReminder:
        description: Snooze the reminder for the specified event.
        type: None
  eventMessage:
    properties:
      Get eventMessage:
        description: Read properties and relationships of eventMessage object.
        type: eventMessage
      Update:
        description: Update eventMessage object.
        type: eventMessage
      Delete:
        description: Delete eventMessage object.
        type: None
      copy:
        description: Copy a message to a folder.
        type: Message
      createForward:
        description: Create a draft of the Forward message. You can then update or
          send the draft.
        type: Message
      createReply:
        description: Create a draft of the Reply message. You can then update or send
          the draft.
        type: Message
      createReplyAll:
        description: Create a draft of the Reply All message. You can then update
          or send the draft.
        type: Message
      forward:
        description: Forward a message. The message is then saved in the Sent Items
          folder.
        type: None
      move:
        description: Move a message to a folder. This creates a new copy of the message
          in the destination folder.
        type: Message
      reply:
        description: Reply to the sender of a message. The message is then saved in
          the Sent Items folder.
        type: None
  Working with Excel in Microsoft Graph:
    properties: []
  Outlook extended properties overview:
    properties:
      '"{type} {guid} Name {name}"':
        description: Identifies a property by the namespace (the GUID) it belongs
          to, and a name.
        type: '"String {8ECCC264-6880-4EBE-992F-8888D2EEAA1D'
      '"{type} {guid} Id {id}"':
        description: Identifies a property by the namespace (the GUID) it belongs
          to, and an identifier.
        type: '"Integer {8ECCC264-6880-4EBE-992F-8888D2EEAA1'
  extension:
    properties:
      id:
        description: Read-only.
        type: String
  File:
    properties:
      hashes:
        description: Hashes of the files binary content, if available. Read-only.
        type: HashesType
      mimeType:
        description: The MIME type for the file. This is determined by logic on the
          server and might not be the value provided when the file was uploaded. Read-only.
        type: string
  fileAttachment:
    properties:
      Get:
        description: Read properties and relationships of fileAttachment object.
        type: fileAttachment
      Delete:
        description: Delete fileAttachment object.
        type: None
  FileSystemInfo:
    properties:
      createdDateTime:
        description: The UTC date and time the file was created on a client.
        type: DateTimeOffset
      lastModifiedDateTime:
        description: The UTC date and time the file was last modified on a client.
        type: DateTimeOffset
  Filter:
    properties:
      Apply:
        description: Apply the given filter criteria on the given column.
        type: None
      Clear:
        description: Clear the filter on the given column.
        type: None
  FilterCriteria:
    properties: []
  FilterDatetime:
    properties:
      date:
        description: The date in ISO8601 format used to filter data.
        type: string
      specificity:
        description: 'How specific the date should be used to keep data. For example,
          if the date is 2005-04-02 and the specifity is set to month, the filter
          operation will keep all rows with a date in the month of april 2009. Possible
          values are: Year, Monday, Day, Hour, Minute, Second.'
        type: string
  Folder:
    properties:
      childCount:
        description: Number of children contained immediately within this container.
        type: Int64
  FormatProtection:
    properties:
      Get FormatProtection:
        description: Read properties and relationships of formatProtection object.
        type: FormatProtection
      Update:
        description: Update FormatProtection object.
        type: FormatProtection
  GeoCoordinates:
    properties:
      altitude:
        description: Optional. The altitude (height), in feet,  above sea level for
          the item. Read-only.
        type: Double
      latitude:
        description: Optional. The latitude, in decimal, for the item. Read-only.
        type: Double
      longitude:
        description: Optional. The longitude, in decimal, for the item. Read-only.
        type: Double
  group:
    properties:
      Create group:
        description: Create a new group. It can be an Office 365 group, dynamic group
          or security group.
        type: group
      Get group:
        description: Read properties of a group object.
        type: group
      List groups:
        description: List group objects and their properties.
        type: group collection
      Update group:
        description: Update the properties of a group object.
        type: group
      Delete group:
        description: Delete group object.
        type: None
      Add member:
        description: Add a user or group to this group by posting to the members navigation
          property (supported for security groups and mail-enabled security groups
          only).
        type: None
      List members:
        description: Get the users and groups that are direct members of this group
          from the members navigation property.
        type: directoryObject collection
      Remove member:
        description: Remove a member from an Office 365 group, a security group or
          a mail-enabled security group through the members navigation property. You
          can remove users or other groups.
        type: None
      List memberOf:
        description: Get the groups that this group is a direct member of, from the
          memberOf navigation property.
        type: directoryObject collection
      Add owner:
        description: Add a new owner for the group by posting to the owners navigation
          property (supported for security groups and mail-enabled security groups
          only).
        type: '[None'
  Hashes:
    properties:
      sha1Hash:
        description: SHA1 hash for the contents of the file (if available). Read-only.
        type: String
      crc32Hash:
        description: The CRC32 value of the file (if available). Read-only.
        type: String
      quickXorHash:
        description: A proprietary hash of the file that can be used to determine
          if the contents of the file have changed (if available). Read-only.
        type: String
  Icon:
    properties:
      Get Icon:
        description: Read properties and relationships of icon object.
        type: Icon
      Update:
        description: Update Icon object.
        type: Icon
  Identity:
    properties:
      displayName:
        description: The identitys display name. Note that this may not always be
          available or up to date. For example, if a user changes their display name,
          the API may show the new value in a future response, but the items associated
          with the user wont show up as having changed when using find changes
        type: String
      id:
        description: Unique identifier for the identity.
        type: String
  IdentitySet:
    properties:
      application:
        description: Optional. The application associated with this action.
        type: Identity
      device:
        description: Optional. The device associated with this action.
        type: Identity
      user:
        description: Optional. The user associated with this action.
        type: Identity
  Image:
    properties:
      height:
        description: Optional. Height of the image, in pixels. Read-only.
        type: Int32
      width:
        description: Optional. Width of the image, in pixels. Read-only.
        type: Int32
  inferenceClassification:
    properties:
      Create inferenceClassificationOverride:
        description: Create an override for a sender identified by an SMTP address.
          Future messages from that SMTP address will be consistently classified as
          specified in the override.
        type: inferenceClassificationOverride
      List overrides:
        description: Get the overrides that a user has set up to always classify messages
          from certain senders in specific ways.
        type: inferenceClassificationOverride collection
  inferenceClassificationOverride:
    properties:
      Update:
        description: Change the ClassifyAs field of an override as specified.
        type: inferenceClassificationOverride
      Delete:
        description: Delete an override specified by its ID.
        type: None
  invitation manager:
    properties:
      Create invitation:
        description: Write properties and relationships of invitation object.
        type: invitation
  Configuring the invitation message:
    properties:
      ccRecipients:
        description: Additional recipients the invitation message should be sent to.
          Currently only 1 additional recipient is supported.
        type: Recipient
      customizedMessageBody:
        description: Customized message body you want to send if you dont want the
          default message.
        type: String
      messageLanguage:
        description: The language you want to send the default message in. If the
          customizedMessageBody is specified, this property is ignored, and the message
          is sent using the customizedMessageBody. The language format should be in
          ISO 639. The default is en-US.
        type: String
  itemAttachment:
    properties:
      Get:
        description: Read properties and relationships of itemAttachment object.
        type: itemAttachment
      Delete:
        description: Delete itemAttachment object.
        type: None
  itemBody:
    properties:
      content:
        description: The content of the item.
        type: String
      contentType:
        description: The type of the content. Possible values are Text and HTML.
        type: String
  ItemReference:
    properties:
      driveId:
        description: Unique identifier of the OneDrive instance that contains the
          item. Read-only.
        type: String
      id:
        description: Unique identifier of the item in the drive. Read-only.
        type: String
      path:
        description: Path that can be used to navigate to the item. Read-only.
        type: String
  licenseUnitsDetail:
    properties:
      enabled:
        description: This is a default description.
        type: Int32
      suspended:
        description: This is a default description.
        type: Int32
      warning:
        description: This is a default description.
        type: Int32
  localeInfo:
    properties:
      locale:
        description: A locale representation for the user, which includes the users
          preferred language and country/region. For example, en-us. The language
          component follows 2-letter codes as defined in ISO 639-1, and the country
          component follows 2-letter codes as defined in ISO 3166-1 alpha-2.
        type: string
      displayName:
        description: A name representing the users locale in natural language, for
          example, English (United States).
        type: string
  Location:
    properties:
      address:
        description: The street address of the location.
        type: physicalAddress
      displayName:
        description: The name associated with the location.
        type: String
      locationEmailAddress:
        description: Optional email address of the location.
        type: String
  locationConstraint:
    properties:
      isRequired:
        description: The client requests the service to include in the response a
          meeting location for the meeting. If this is true and all the resources
          are busy, findMeetingTimes will not return any meeting time suggestions.
          If this is false and all the resources are busy, findMeetingTimes would
          still look for meeting times without locations.
        type: Boolean
      locations:
        description: Constraint information for one or more locations that the client
          requests for the meeting.
        type: locationConstraintItem collection
      suggestLocation:
        description: The client requests the service to suggest one or more meeting
          locations.
        type: Boolean
  locationConstraintItem:
    properties:
      address:
        description: The street address of the location.
        type: physicalAddress
      displayName:
        description: The name associated with the location.
        type: String
      locationEmailAddress:
        description: Optional email address of the location.
        type: String
      resolveAvailability:
        description: If set to true and the specified resource is busy, findMeetingTimes
          looks for another resource that is free. If set to false and the specified
          resource is busy, findMeetingTimes returns the resource best ranked in the
          users cache without checking if its free. Default is true.
        type: Boolean
  mailboxSettings:
    properties:
      automaticRepliesSetting:
        description: Configuration settings to automatically notify the sender of
          an incoming email with a message from the signed-in user.
        type: automaticRepliesSetting
      language:
        description: The locale information for the user, including the preferred
          language and country/region.
        type: localeInfo
      timeZone:
        description: The default time zone for the users mailbox.
        type: string
  mailFolder:
    properties:
      Get mailFolder:
        description: Read properties and relationships of mailFolder object.
        type: mailFolder
      Create MailFolder:
        description: Create a new mailFolder under the current one by posting to the
          childFolders collection.
        type: MailFolder
      List childFolders:
        description: Get the folder collection under the specified folder. You can
          use the .../me/MailFolders shortcut to get the top-level folder collection
          and navigate to another folder.
        type: MailFolder collection
      Create Message:
        description: Create a new message in the current mailFolder by posting to
          the messages collection.
        type: Message
      List messages:
        description: Get all the messages in the signed-in users mailbox, or those
          messages in a specified folder in the mailbox.
        type: Message collection
      Update:
        description: Update the specified mailFolder object.
        type: mailFolder
      Delete:
        description: Delete the specified mailFolder object.
        type: None
      copy:
        description: Copy a mailFolder and its contents to another mailFolder.
        type: MailFolder
      move:
        description: Move a mailFolder and its contents to another mailFolder.
        type: MailFolder
      Create single-value extended property:
        description: Create one or more single-value extended properties in a new
          or existing mailFolder.
        type: mailFolder
  Manage Focused Inbox:
    properties: []
  meetingTimeSuggestion:
    properties:
      attendeeAvailability:
        description: An array that shows the availability status of each attendee
          for this meeting suggestion.
        type: attendeeAvailability collection
      confidence:
        description: A percentage that represents the likelhood of all the attendees
          attending.
        type: Double
      locations:
        description: An array that specifies the name and geographic location of each
          meeting location for this meeting suggestion.
        type: location collection
      meetingTimeSlot:
        description: A time period suggested for the meeting.
        type: timeSlot
      organizerAvailability:
        description: 'Availability of the meeting organizer for this meeting suggestion.
          Possible values are: free, tentative, busy, oof, workingElsewhere, unknown.'
        type: String
      suggestionReason:
        description: Reason for suggesting the meeting time.
        type: String
  meetingTimeSuggestionsResult:
    properties:
      attendeesUnavailable:
        description: This is a default description.
        type: 'All of the attendees'' availability is known, '
      attendeesUnavailableOrUnknown:
        description: This is a default description.
        type: Some or all of the attendees have unknown ava
      locationsUnavailable:
        description: This is a default description.
        type: The isRequired property of the locationConstr
      organizerUnavailable:
        description: This is a default description.
        type: The isOrganizerOptional parameter is false an
      unknown:
        description: This is a default description.
        type: The reason for not returning any meeting sugg
  message:
    properties:
      List messages:
        description: Get all the messages in the signed-in users mailbox (including
          the Deleted Items and Clutter folders).
        type: message collection
      Create message:
        description: Create a draft of a new message.
        type: message
      Get message:
        description: Read properties and relationships of message object.
        type: message
      Update:
        description: Update message object.
        type: message
      Delete:
        description: Delete message object.
        type: None
      copy:
        description: Copy a message to a folder.
        type: Message
      createForward:
        description: Create a draft of the Forward message. You can then update or
          send the draft.
        type: Message
      createReply:
        description: Create a draft of the Reply message. You can then update or send
          the draft.
        type: Message
      createReplyAll:
        description: Create a draft of the Reply All message. You can then update
          or send the draft.
        type: Message
      forward:
        description: Forward a message. The message is then saved in the Sent Items
          folder.
        type: None
  multiValueLegacyExtendedProperty:
    properties:
      Post:
        description: Create a multiValueLegacyExtendedProperty in a new or existing
          instance of a supported resource.
        type: 'A supported resource instance: message, mailF'
      Get:
        description: Get a resource instance with an extended property using $expand.
        type: A supported resource instance (message, mailF
  NamedItem:
    properties:
      Add:
        description: Adds a new name to the collection of the given scope.
        type: NamedItem
      AddFormulaLocal:
        description: Adds a new name to the collection of the given scope using the
          users locale for the formula.
        type: NamedItem
      Get NamedItem:
        description: Read properties and relationships of namedItem object.
        type: NamedItem
      Update:
        description: Update NamedItem object.
        type: NamedItem
      Range:
        description: Returns the range object that is associated with the name. Throws
          an exception if the named items type is not a range.
        type: Range
      List:
        description: Get namedItem object collection.
        type: NamedItem collection
  Working with files in Microsoft Graph:
    properties: []
  openTypeExtension (open extensions):
    properties: []
  organization:
    properties:
      Get organization:
        description: Read properties and relationships of organization object.
        type: organization
      Update:
        description: Update organization object. (Only the marketingNotificationMails
          and technicalNotificationMails properties can be updated.)
        type: organization
  outlookItem:
    properties:
      categories:
        description: This is a default description.
        type: String collection
      changeKey:
        description: This is a default description.
        type: String
      createdDateTime:
        description: 'The Timestamp type represents date and time information using
          ISO 8601 format and is always in UTC time. For example, midnight UTC on
          Jan 1, 2014 would look like this: 2014-01-01T00:00:00Z'
        type: DateTimeOffset
      id:
        description: Read-only.
        type: String
      lastModifiedDateTime:
        description: 'The Timestamp type represents date and time information using
          ISO 8601 format and is always in UTC time. For example, midnight UTC on
          Jan 1, 2014 would look like this: 2014-01-01T00:00:00Z'
        type: DateTimeOffset
  Package:
    properties:
      type:
        description: An string indicating the type of package. While oneNote is the
          only currently defined value, you should expect other package types to be
          returned and handle them accordingly.
        type: string
  passwordProfile:
    properties:
      forceChangePasswordNextSignIn:
        description: true if the user must change her password on the next login;
          otherwise false.
        type: Boolean
      password:
        description: "The password for the user. This property is required when a
          user is created. It can be updated, but the user will be required to change
          the password on the next login. The password must satisfy minimum requirements
          as specified by the user\u2019s passwordPolicies property. By default, a
          strong password is required."
        type: String
  patternedRecurrence:
    properties:
      pattern:
        description: The frequency of an event.
        type: RecurrencePattern
      range:
        description: The duration of an event.
        type: RecurrenceRange
  Permission:
    properties:
      id:
        description: The unique identifier of the permission among all permissions
          on the item. Read-only.
        type: String
      grantedTo:
        description: For user type permissions, the details of the users &amp; applications
          for this permission. Read-only.
        type: IdentitySet
      invitation:
        description: Details of any associated sharing invitation for this permission.
          Read-only.
        type: SharingInvitation
      inheritedFrom:
        description: Provides a reference to the ancestor of the current permission,
          if it is inherited from an ancestor. Read-only.
        type: ItemReference
      link:
        description: Provides the link details of the current permission, if it is
          a link type permissions. Read-only.
        type: SharingLink
      role:
        description: The type of permission, e.g. read. See below for the full list
          of roles. Read-only.
        type: Collection of String
      shareId:
        description: A unique token for this permission. Read-only.
        type: String
  Photo:
    properties:
      takenDateTime:
        description: Represents the date and time the photo was taken. Read-only.
        type: DateTimeOffset
      cameraMake:
        description: Camera manufacturer. Read-only.
        type: String
      cameraModel:
        description: Camera model. Read-only.
        type: String
      fNumber:
        description: The F-stop value from the camera. Read-only.
        type: Double
      exposureDenominator:
        description: The denominator for the exposure time fraction from the camera.
          Read-only.
        type: Int32
      exposureNumerator:
        description: The numerator for the exposure time fraction from the camera.
          Read-only.
        type: Int32
      focalLength:
        description: The focal length from the camera. Read-only.
        type: Double
      iso:
        description: The ISO value from the camera. Read-only.
        type: Int32
  physicalAddress:
    properties:
      city:
        description: The city.
        type: String
      countryOrRegion:
        description: The country or region. Its a free-format string value, for example,
          United States.
        type: String
      postalCode:
        description: The postal code.
        type: String
      state:
        description: The state.
        type: String
      street:
        description: The street.
        type: String
  post:
    properties:
      List posts:
        description: Get the posts of the specified thread.
        type: post
      Get post:
        description: Get the properties and relationships of a post in a specified
          thread.
        type: post
      Reply:
        description: Reply to a post and add a new post to the specified thread in
          a group conversation.
        type: None
      Forward:
        description: Forward a post to a recipient.
        type: None
      Attachments:
        description: This is a default description.
        type: string
      List attachments:
        description: Get all attachments on a post.
        type: attachment collection
      Add attachment:
        description: Add an attachment to a post.
        type: attachment
      Open extensions:
        description: This is a default description.
        type: string
      Create open extension:
        description: Create an open extension and add custom properties in a new or
          existing instance of a resource.
        type: openTypeExtension
      Get open extension:
        description: Get an open extension object or objects identified by name or
          fully qualified name.
        type: openTypeExtension collection
  profilePhoto:
    properties:
      Get profilePhoto:
        description: Get the specified profilePhoto or its metadata (profilePhoto
          properties).
        type: profilePhoto
      Update:
        description: Assign a photo to the specified user, group, or contact. The
          photo should be in binary. It replaces the existing photo, if any.
        type: profilePhoto
  provisionedPlan:
    properties:
      capabilityStatus:
        description: "For example, \u201CEnabled\u201D."
        type: String
      provisioningStatus:
        description: "For example, \u201CSuccess\u201D."
        type: String
      service:
        description: "The name of the service; for example, \u201CAccessControlS2S\u201D"
        type: String
  Quota:
    properties:
      total:
        description: Total allowed storage space, in bytes. Read-only.
        type: Int64
      used:
        description: Total space used, in bytes. Read-only.
        type: Int64
      remaining:
        description: Total space remaining before reaching the quota limit, in bytes.
          Read-only.
        type: Int64
      deleted:
        description: Total space consumed by files in the recycle bin, in bytes. Read-only.
        type: Int64
      state:
        description: Enumeration value that indicates the state of the storage space.
          Read-only.
        type: string
  Range:
    properties:
      Get Range:
        description: Read properties and relationships of range object.
        type: Range
      Update:
        description: Update Range object.
        type: Range
      Boundingrect:
        description: Gets the smallest range object that encompasses the given ranges.
          For example, the GetBoundingRect of B2:C5 and D10:E15 is B2:E16.
        type: Range
      Cell:
        description: Gets the range object containing the single cell based on row
          and column numbers. The cell can be outside the bounds of its parent range,
          so long as its stays within the worksheet grid. The returned cell is located
          relative to the top left cell of the range.
        type: Range
      Column:
        description: Gets a column contained in the range.
        type: Range
      Columnsafter:
        description: Gets a certain number of columns to the right of the given range.
        type: workbookRangeView
      Columnsbefore:
        description: Gets a certain number of columns to the left of the given range.
        type: workbookRangeView
      Entirecolumn:
        description: Gets an object that represents the entire column of the range.
        type: Range
      Entirerow:
        description: Gets an object that represents the entire row of the range.
        type: Range
      Intersection:
        description: Gets the range object that represents the rectangular intersection
          of the given ranges.
        type: Range
  RangeBorder:
    properties:
      Get RangeBorder:
        description: Read properties and relationships of rangeBorder object.
        type: RangeBorder
      Update:
        description: Update RangeBorder object.
        type: RangeBorder
      List:
        description: Get rangeBorder object collection.
        type: RangeBorder collection
      Itemat:
        description: Gets a border object using its index
        type: RangeBorder
  RangeFill:
    properties:
      Get RangeFill:
        description: Read properties and relationships of rangeFill object.
        type: RangeFill
      Update:
        description: Update RangeFill object.
        type: RangeFill
      Clear:
        description: Resets the range background.
        type: None
  RangeFont:
    properties:
      Get RangeFont:
        description: Read properties and relationships of rangeFont object.
        type: RangeFont
      Update:
        description: Update RangeFont object.
        type: RangeFont
  RangeFormat:
    properties:
      Get RangeFormat:
        description: Read properties and relationships of rangeFormat object.
        type: RangeFormat
      Create RangeBorder:
        description: Create a new RangeBorder by posting to the borders collection.
        type: RangeBorder
      List borders:
        description: Get a RangeBorder object collection.
        type: RangeBorder collection
      Update:
        description: Update RangeFormat object.
        type: RangeFormat
      Autofitcolumns:
        description: Changes the width of the columns of the current range to achieve
          the best fit, based on the current data in the columns.
        type: None
      Autofitrows:
        description: Changes the height of the rows of the current range to achieve
          the best fit, based on the current data in the columns.
        type: None
  RangeSort:
    properties:
      Apply:
        description: Perform a sort operation.
        type: None
  recipient:
    properties:
      emailAddress:
        description: The recipients email address.
        type: EmailAddress
  recurrencePattern:
    properties:
      dayOfMonth:
        description: The day of the month that the event occurs on.
        type: Int32
      daysOfWeek:
        description: 'A collection of the days of the week that the event occurs on.
          Possible values are: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday,
          Saturday.'
        type: String collection
      firstDayOfWeek:
        description: 'The day of the week  on which the recurrence starts. Possible
          values are: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday.'
        type: String
      index:
        description: 'The index of the week in which the recurrence occurs.: First,
          Second, Third, Fourth, Last.'
        type: String
      interval:
        description: The number of units of a given recurrence type between occurrences.
        type: Int32
      month:
        description: The month that the event occurs on.  This is a number from 1
          to 12.
        type: Int32
      type:
        description: 'The recurrence pattern type: Daily, Weekly, AbsoluteMonthly,
          RelativeMonthly, AbsoluteYearly, RelativeYearly.'
        type: String
  recurrenceRange:
    properties:
      endDate:
        description: The end date of the series.
        type: Date
      numberOfOccurrences:
        description: How many times to repeat the event.
        type: Int32
      recurrenceTimeZone:
        description: Time zone for the startDate and endDate properties.
        type: String
      startDate:
        description: The start date of the series.
        type: Date
      type:
        description: 'The recurrence range: EndDate = 0, NoEnd = 1, Numbered = 2.
          Possible values are: EndDate, NoEnd, Numbered.'
        type: String
  referenceAttachment:
    properties:
      Get:
        description: Read properties and relationships of referenceAttachment object.
        type: referenceAttachment
      Delete:
        description: Delete referenceAttachment object.
        type: None
  reminder:
    properties:
      changeKey:
        description: Identifies the version of the reminder. Every time the reminder
          is changed, changeKey changes as well. This allows Exchange to apply changes
          to the correct version of the object.
        type: String
      eventEndTime:
        description: The date, time and time zone that the event ends.
        type: DateTimeTimeZone
      eventId:
        description: The unique ID of the event. Read only.
        type: String
      eventLocation:
        description: The location of the event.
        type: Location
      eventStartTime:
        description: The date, time, and time zone that the event starts.
        type: DateTimeTimeZone
      eventSubject:
        description: The text of the events subject line.
        type: String
      eventWebLink:
        description: The URL to open the event in Outlook on the web.The event will
          open in the browser if you are logged in to your mailbox via Outlook on
          the web. You will be prompted to login if you are not already logged in
          with the browser.This URL can be accessed from within an iFrame.
        type: String
      reminderFireTime:
        description: The date, time, and time zone that the reminder is set to occur.
        type: DateTimeTimeZone
  RemoteItem:
    properties:
      createdBy:
        description: Identity of the user, device, and application which created the
          item. Read-only.
        type: IdentitySet
      createdDateTime:
        description: Date and time of item creation. Read-only.
        type: Timestamp
      file:
        description: Indicates that the remote item is a file. Read-only.
        type: File
      fileSystemInfo:
        description: Information about the remote item from the local file system.
          Read-only.
        type: FileSystemInfo
      folder:
        description: Indicates that the remote item is a folder. Read-only.
        type: Folder
      id:
        description: Unique identifier for the remote item in its drive. Read-only.
        type: String
      lastModifiedBy:
        description: Identity of the user, device, and application which last modified
          the item. Read-only.
        type: IdentitySet
      lastModifiedDateTime:
        description: Date and time the item was last modified. Read-only.
        type: Timestamp
      name:
        description: Optional. Filename of the remote item. Read-only.
        type: String
      package:
        description: If present, indicates that this item is a package instead of
          a folder or file. Packages are treated like files in some contexts and folders
          in others. Read-only.
        type: Package
  responseStatus:
    properties:
      response:
        description: 'The response type: None = 0, Organizer = 1, TentativelyAccepted
          = 2, Accepted = 3, Declined = 4, NotResponded = 5. Possible values are:
          None, Organizer, TentativelyAccepted, Accepted, Declined, NotResponded.'
        type: String
      time:
        description: 'The date and time that the response was returned. It uses ISO
          8601 format and is always in UTC time. For example, midnight UTC on Jan
          1, 2014 would look like this: 2014-01-01T00:00:00Z'
        type: DateTimeOffset
  SearchResult:
    properties:
      onClickTelemetryUrl:
        description: A callback URL that can be used to record telemetry information.
          The application should issue a GET on this URL if the user interacts with
          this item to improve the quality of results.
        type: String
  Service root:
    properties:
      Create device:
        description: Create a new device by posting to the devices collection.
        type: device
      List device:
        description: Get device object collection.
        type: device collection
      Activate directoryRole:
        description: Activate a directory role.
        type: directoryRole
      List directoryRole:
        description: Get directoryRole object collection.
        type: directoryRole collection
      List directoryRoleTemplate:
        description: Get directoryRoleTemplate object collection.
        type: directoryRoleTemplate collection
      List drive:
        description: Get drive object collection.
        type: drive collection
      Get drive:
        description: Get drive object properties.
        type: drive
      Create group:
        description: Create a new group by posting to the groups collection.
        type: group
      List group:
        description: Get group object collection.
        type: group collection
      List organization:
        description: Get organization object collection.
        type: organization collection
  servicePlanInfo:
    properties:
      servicePlanId:
        description: The unique identifier of the service plan.
        type: Guid
      servicePlanName:
        description: The name of the service plan.
        type: String
      provisioningStatus:
        description: The provisioning status of the service plan.
        type: String
      appliesTo:
        description: This is a default description.
        type: String
  Shared:
    properties:
      owner:
        description: The identity of the owner of the shared item. Read-only.
        type: IdentitySet
      scope:
        description: 'Indicates the scope of how the item is shared: anonymous, organization,
          or users. Read-only.'
        type: String
  SharedDriveItem:
    properties:
      id:
        description: The unique identifier for the share being accessed.
        type: String
      name:
        description: The display name of the shared item.
        type: String
      owner:
        description: Information about the owner of the shared item being referenced.
        type: IdentitySet
      items:
        description: A collection of shared DriveItem resources. This collection cannot
          be enumerated, but items can be accessed by their unique ID.
        type: Collection(DriveItem)
      root:
        description: The top level shared DriveItem. If a single file is shared, this
          item is the file. If a folder is shared, this item will be the folder. You
          can use the items facets to determine which case applies.
        type: DriveItem
  SharePointIds:
    properties:
      listId:
        description: The unique identifier for the items list in SharePoint.
        type: string
      listItemId:
        description: An integer identifier for the item within the containing list.
        type: string
      listItemUniqueId:
        description: The unique identifier for the item within OneDrive for Busienss
          or a SharePoint site.
        type: string
      siteId:
        description: The unique identifier for the items site collection.
        type: string
      webId:
        description: The unique identifier for the items site.
        type: string
  SharingInvitation:
    properties:
      email:
        description: The email address provided for the recipient of the sharing invitation.
          Read-only.
        type: String
      invitedBy:
        description: Provides information about who sent the invitation that created
          this permission, if that information is available. Read-only.
        type: identitySet
      signInRequired:
        description: If true the recipient of the invitation needs to sign in in order
          to access the shared item. Read-only.
        type: Boolean
  SharingLink:
    properties:
      application:
        description: The app the link is associated with.
        type: identity
      type:
        description: The type of the link created.
        type: String
      scope:
        description: The scope of the link represented by this permission. Value anonymous
          indicates the link is usable by anyone, organization indicates the link
          is only usable for users signed into the same tenant.
        type: String
      webUrl:
        description: A URL that opens the item in the browser on the OneDrive website.
        type: String
  singleValueLegacyExtendedProperty:
    properties:
      Post:
        description: Create a singleValueLegacyExtendedProperty in a new or existing
          instance of a supported resource.
        type: 'A supported resource instance: message, mailF'
      Get:
        description: Get a resource instance with an extended property using $expand
          or $filter.
        type: One or a collection of supported resource ins
  SortField:
    properties:
      ascending:
        description: Represents whether the sorting is done in an ascending fashion.
        type: boolean
      color:
        description: Represents the color that is the target of the condition if the
          sorting is on font or cell color.
        type: string
      dataOption:
        description: 'Represents additional sorting options for this field. Possible
          values are: Normal, TextAsNumber.'
        type: string
      key:
        description: Represents the column (or row, depending on the sort orientation)
          that the condition is on. Represented as an offset from the first column
          (or row).
        type: int
      sortOn:
        description: 'Represents the type of sorting of this condition. Possible values
          are: Value, CellColor, FontColor, Icon.'
        type: string
  SpecialFolder:
    properties:
      name:
        description: The unique identifier for this item in the /drive/special collection
        type: string
  subscribedSku:
    properties:
      Get subscribedSku:
        description: Read properties of the subscribedSku object.
        type: subscribedSku
  Subscription Resource Type:
    properties:
      changeType:
        description: 'Indicates the type of change in the subscribed resource that
          will raise a notification. The supported values are: created, updated, deleted.
          Multiple values can be combined using a comma-separated list.'
        type: string
      notificationUrl:
        description: The URL of the endpoint that will receive the notifications.
          This URL has to make use of the HTTPS protocol.
        type: string
      resource:
        description: Specifies the resource that will be monitored for changes. Do
          not include the base URL (https://graph.microsoft.com/v1.0/).
        type: string
      expirationDateTime:
        description: Specifies the date and time when the webhook subscription expires.
          The time is in UTC, and can be an amount of time from subscription creation
          that varies for the resource subscribed to.  See the table below for maximum
          values.
        type: dateTime
      clientState:
        description: Specifies the value of the clientState property sent by the service
          in each notification. The maximum length is 128 characters. The client can
          check that the notification came from the service by comparing the value
          of the clientState property sent with the subscription with the value of
          the clientState property received with each notification.
        type: string
      id:
        description: Unique identifier for the subscription. Read-only.
        type: string
  Table:
    properties:
      Get Table:
        description: Read properties and relationships of table object.
        type: Table
      Create TableColumn:
        description: Create a new TableColumn by posting to the columns collection.
        type: TableColumn
      List columns:
        description: Get a TableColumn object collection.
        type: TableColumn collection
      Create TableRow:
        description: Create a new TableRow by posting to the rows collection.
        type: TableRow
      List rows:
        description: Get a TableRow object collection.
        type: TableRow collection
      Update:
        description: Update Table object.
        type: Table
      Databodyrange:
        description: Gets the range object associated with the data body of the table.
        type: Range
      Headerrowrange:
        description: Gets the range object associated with header row of the table.
        type: Range
      Range:
        description: Gets the range object associated with the entire table.
        type: Range
      Totalrowrange:
        description: Gets the range object associated with totals row of the table.
        type: Range
  TableColumn:
    properties:
      Get TableColumn:
        description: Read properties and relationships of tableColumn object.
        type: TableColumn
      Update:
        description: Update TableColumn object.
        type: TableColumn
      Databodyrange:
        description: Gets the range object associated with the data body of the column.
        type: Range
      Headerrowrange:
        description: Gets the range object associated with the header row of the column.
        type: Range
      Range:
        description: Gets the range object associated with the entire column.
        type: Range
      Totalrowrange:
        description: Gets the range object associated with the totals row of the column.
        type: Range
      Delete:
        description: Deletes the column from the table.
        type: None
      List:
        description: Get tableColumn object collection.
        type: TableColumn collection
      Itemat:
        description: Gets a column based on its position in the collection.
        type: TableColumn
      Add:
        description: Adds a new column to the table.
        type: TableColumn
  TableRow:
    properties:
      Get TableRow:
        description: Read properties and relationships of tableRow object.
        type: TableRow
      Update:
        description: Update TableRow object.
        type: TableRow
      Range:
        description: Returns the range object associated with the entire row.
        type: Range
      Delete:
        description: Deletes the row from the table.
        type: None
      List:
        description: Get tableRow object collection.
        type: TableRow collection
      Itemat:
        description: Gets a row based on its position in the collection.
        type: TableRow
      Add:
        description: Adds a new row to the table.
        type: TableRow
  TableSort:
    properties:
      Get TableSort:
        description: Read properties and relationships of tableSort object.
        type: TableSort
      Apply:
        description: Perform a sort operation.
        type: None
      Clear:
        description: Clears the sorting that is currently on the table. While this
          doesnt modify the tables ordering, it clears the state of the header buttons.
        type: None
      Reapply:
        description: Reapplies the current sorting parameters to the table.
        type: None
  thumbnail:
    properties:
      height:
        description: The height of the thumbnail, in pixels.
        type: Int32
      url:
        description: The URL used to fetch the thumbnail content.
        type: String
      width:
        description: The width of the thumbnail, in pixels.
        type: Int32
  ThumbnailSet:
    properties:
      id:
        description: The id within the item. Read-only.
        type: String
      large:
        description: A 1920x1920 scaled thumbnail.
        type: Thumbnail
      medium:
        description: A 176x176 scaled thumbnail.
        type: Thumbnail
      small:
        description: A 48x48 cropped thumbnail.
        type: Thumbnail
      source:
        description: A custom thumbnail image or the original image used to generate
          other thumbnails.
        type: Thumbnail
  timeConstraint:
    properties:
      activityDomain:
        description: 'The nature of the activity, optional. Possible values are: work,
          personal, unrestricted, or unknown.'
        type: String
      timeslots:
        description: An array of time periods.
        type: timeSlot collection
  timeSlot:
    properties:
      end:
        description: The time a period begins.
        type: dateTimeTimeZone
      start:
        description: The time the period ends.
        type: dateTimeTimeZone
  UploadSession:
    properties:
      expirationDateTime:
        description: The date and time in UTC that the upload session will expire.
          The complete file must be uploaded before this expiration time is reached.
        type: DateTimeOffset
      nextExpectedRanges:
        description: A collection of byte ranges that the server is missing for the
          file. These ranges are zero indexed and of the format start-end (e.g. 0-26
          to indicate the first 27 bytes of the file).
        type: String collection
      uploadUrl:
        description: The URL endpoint that accepts PUT requests for byte ranges of
          the file.
        type: String
  user:
    properties:
      Get user:
        description: Read properties and relationships of user object.
        type: user
      Update user:
        description: Update user object.
        type: user
      Delete user:
        description: Delete user object.
        type: None
      List messages:
        description: Get all the messages in the signed-in users mailbox.
        type: Message collection
      Create Message:
        description: Create a new Message by posting to the messages collection.
        type: Message
      List mailFolders:
        description: Get the mail folder collection under the root folder of the signed-in
          user.
        type: MailFolder collection
      Create mailFolder:
        description: Create a new MailFolder by posting to the mailFolders collection.
        type: MailFolder
      sendMail:
        description: Send the message specified in the request body.
        type: None
      List events:
        description: Get a list of event objects in the users mailbox. The list contains
          single instance meetings and series masters.
        type: Event collection
      Create event:
        description: Create a new Event by posting to the events collection.
        type: Event
  Working with users in Microsoft Graph:
    properties: []
  verifiedDomain:
    properties:
      capabilities:
        description: "For example, \u201CEmail\u201D, \u201COfficeCommunicationsOnline\u201D."
        type: String
      isDefault:
        description: true if this is the default domain associated with the tenant;
          otherwise, false.
        type: Boolean
      isInitial:
        description: true if this is the initial domain associated with the tenant;
          otherwise, false
        type: Boolean
      name:
        description: "The domain name; for example, \u201Ccontoso.onmicrosoft.com\u201D"
        type: String
      type:
        description: "For example, \u201CManaged\u201D."
        type: String
  Video:
    properties:
      bitrate:
        description: Bit rate of the video in bits per second.
        type: Int32
      duration:
        description: Duration of the file in milliseconds.
        type: Int64
      height:
        description: Height of the video, in pixels.
        type: Int32
      width:
        description: Width of the video, in pixels.
        type: Int32
  Working with Webhooks in Microsoft Graph:
    properties: []
  Workbook:
    properties:
      names:
        description: Represents a collection of workbook scoped named items (named
          ranges and constants). Read-only.
        type: NamedItem collection
      tables:
        description: Represents a collection of tables associated with the workbook.
          Read-only.
        type: Table collection
      worksheets:
        description: Represents a collection of worksheets associated with the workbook.
          Read-only.
        type: Worksheet collection
  pivotTable:
    properties:
      Get workbookPivotTable:
        description: Read properties and relationships of workbookPivotTable object.
        type: workbookPivotTable
      Refresh:
        description: Refreshes the PivotTable.
        type: None
      Refreshall:
        description: Refresh all tables within given worksheet. Note that this action
          is available only on the pivot table collection.
        type: None
  rangeView:
    properties:
      List rows:
        description: Get a workbookRangeView object collection.
        type: workbookRangeView collection
      Itemat:
        description: Get a range view item based in index.
        type: workbookRangeView
      Range:
        description: Return the range object associated with the range view
        type: workbookRange
  Worksheet:
    properties:
      Get Worksheet:
        description: Read properties and relationships of worksheet object.
        type: Worksheet
      Create Chart:
        description: Create a new Chart by posting to the charts collection.
        type: Chart
      List names:
        description: Get named item collection associated with the worksheet.
        type: NamedItem collection
      List charts:
        description: Get a Chart object collection.
        type: Chart collection
      Create Table:
        description: Create a new Table by posting to the tables collection.
        type: Table
      List tables:
        description: Get a Table object collection.
        type: Table collection
      Update:
        description: Update Worksheet object.
        type: Worksheet
      Cell:
        description: Gets the range object containing the single cell based on row
          and column numbers. The cell can be outside the bounds of its parent range,
          so long as its stays within the worksheet grid.
        type: Range
      Range:
        description: Gets the range object specified by the address or name.
        type: Range
      Usedrange:
        description: The used range is the smallest range that encompasses any cells
          that have a value or formatting assigned to them. If the worksheet is blank,
          this function will return the top left cell.
        type: Range
  WorksheetProtection:
    properties:
      Get WorksheetProtection:
        description: Read properties and relationships of worksheetProtection object.
        type: WorksheetProtection
      Protect:
        description: Protect a worksheet. It throws if the worksheet has been protected.
        type: None
      Unprotect:
        description: Unprotect a worksheet
        type: None
  WorksheetProtectionOptions:
    properties:
      allowAutoFilter:
        description: Represents the worksheet protection option of allowing using
          auto filter feature.
        type: boolean
      allowDeleteColumns:
        description: Represents the worksheet protection option of allowing deleting
          columns.
        type: boolean
      allowDeleteRows:
        description: Represents the worksheet protection option of allowing deleting
          rows.
        type: boolean
      allowFormatCells:
        description: Represents the worksheet protection option of allowing formatting
          cells.
        type: boolean
      allowFormatColumns:
        description: Represents the worksheet protection option of allowing formatting
          columns.
        type: boolean
      allowFormatRows:
        description: Represents the worksheet protection option of allowing formatting
          rows.
        type: boolean
      allowInsertColumns:
        description: Represents the worksheet protection option of allowing inserting
          columns.
        type: boolean
      allowInsertHyperlinks:
        description: Represents the worksheet protection option of allowing inserting
          hyperlinks.
        type: boolean
      allowInsertRows:
        description: Represents the worksheet protection option of allowing inserting
          rows.
        type: boolean
      allowPivotTables:
        description: Represents the worksheet protection option of allowing using
          pivot table feature.
        type: boolean
x-collection-name: Microsoft Graph
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