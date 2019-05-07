# ![LOGO](logo.png) Postmark **flow**ground Connector

## Description

A generated **flow**ground connector for the Postmark API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/postmarkapp.com/server/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:43:45+03:00

## API Description

Postmark makes sending and receiving email
incredibly easy.


## Authorization

This API does not require authorization.

## Actions

### Get bounces

*Tags:* `Bounces API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `count` - _required_ - Number of bounces to return per request. Max 500.
* `offset` - _required_ - Number of bounces to skip.
* `type` - _optional_ - Filter by type of bounce
    Possible values: HardBounce, Transient, Unsubscribe, Subscribe, AutoResponder, AddressChange, DnsError, SpamNotification, OpenRelayTest, Unknown, SoftBounce, VirusNotification, MailFrontier Matador., BadEmailAddress, SpamComplaint, ManuallyDeactivated, Unconfirmed, Blocked, SMTPApiError, InboundError, DMARCPolicy, TemplateRenderingFailed.
* `inactive` - _optional_ - Filter by emails that were deactivated by Postmark due to the bounce. Set to true or false. If this isn't specified it will return both active and inactive.
* `emailFilter` - _optional_ - Filter by email address
* `messageID` - _optional_ - Filter by messageID
* `tag` - _optional_ - Filter by tag
* `todate` - _optional_ - Filter messages up to the date specified. e.g. `2014-02-01`
* `fromdate` - _optional_ - Filter messages starting from the date specified. e.g. `2014-02-01`

### Get bounced tags

*Tags:* `Bounces API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Get a single bounce

*Tags:* `Bounces API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `bounceid` - _required_ - The ID of the bounce to retrieve.

### Activate a bounce

*Tags:* `Bounces API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `bounceid` - _required_ - The ID of the Bounce to activate.

### Get bounce dump

*Tags:* `Bounces API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `bounceid` - _required_ - The ID for the bounce dump to retrieve.

### Get delivery stats

*Tags:* `Bounces API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Send a single email

*Tags:* `Sending API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Send a batch of emails

*Tags:* `Sending API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Send a batch of email using templates.

*Tags:* `Sending API` `Templates API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Send an email using a Template

*Tags:* `Sending API` `Templates API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Inbound message search

*Tags:* `Messages API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `count` - _required_ - Number of messages to return per request. Max 500.
* `offset` - _required_ - Number of messages to skip
* `recipient` - _optional_ - Filter by the user who was receiving the email
* `fromemail` - _optional_ - Filter by the sender email address
* `subject` - _optional_ - Filter by email subject
* `mailboxhash` - _optional_ - Filter by mailboxhash
* `tag` - _optional_ - Filter by tag
* `status` - _optional_ - Filter by status (`blocked`, `processed`, `queued`, `failed`, `scheduled`)
    Possible values: blocked, processed, queued, failed, scheduled.
* `todate` - _optional_ - Filter messages up to the date specified. e.g. `2014-02-01`
* `fromdate` - _optional_ - Filter messages starting from the date specified. e.g. `2014-02-01`

### Bypass rules for a blocked inbound message

*Tags:* `Messages API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `messageid` - _required_ - The ID of the message which should bypass inbound rules.

### Inbound message details

*Tags:* `Messages API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `messageid` - _required_ - The ID of the message for which to details will be retrieved.

### Retry a failed inbound message for processing

*Tags:* `Messages API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `messageid` - _required_ - The ID of the inbound message on which we should retry processing.

### Outbound message search

*Tags:* `Messages API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `count` - _required_ - Number of messages to return per request. Max 500.
* `offset` - _required_ - Number of messages to skip
* `recipient` - _optional_ - Filter by the user who was receiving the email
* `fromemail` - _optional_ - Filter by the sender email address
* `tag` - _optional_ - Filter by tag
* `status` - _optional_ - Filter by status (`queued` or `sent`)
    Possible values: queued, sent.
* `todate` - _optional_ - Filter messages up to the date specified. e.g. `2014-02-01`
* `fromdate` - _optional_ - Filter messages starting from the date specified. e.g. `2014-02-01`

### Clicks for a all messages

*Tags:* `Messages API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `count` - _required_ - Number of message clicks to return per request. Max 500.
* `offset` - _required_ - Number of messages to skip
* `recipient` - _optional_ - Filter by To, Cc, Bcc
* `tag` - _optional_ - Filter by tag
* `client_name` - _optional_ - Filter by client name, i.e. Outlook, Gmail
* `client_company` - _optional_ - Filter by company, i.e. Microsoft, Apple, Google
* `client_family` - _optional_ - Filter by client family, i.e. OS X, Chrome
* `os_name` - _optional_ - Filter by full OS name and specific version, i.e. OS X 10.9 Mavericks, Windows 7
* `os_family` - _optional_ - Filter by kind of OS used without specific version, i.e. OS X, Windows
* `os_company` - _optional_ - Filter by company which produced the OS, i.e. Apple Computer, Inc., Microsoft Corporation
* `platform` - _optional_ - Filter by platform, i.e. webmail, desktop, mobile
* `country` - _optional_ - Filter by country messages were opened in, i.e. Denmark, Russia
* `region` - _optional_ - Filter by full name of region messages were opened in, i.e. Moscow, New York
* `city` - _optional_ - Filter by full name of region messages were opened in, i.e. Moscow, New York

### Retrieve Message Clicks

*Tags:* `Messages API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `messageid` - _required_ - The ID of the Outbound Message for which click statistics should be retrieved.
* `count` - _required_ - Number of message clicks to return per request. Max 500.
* `offset` - _required_ - Number of messages to skip.

### Opens for all messages

*Tags:* `Messages API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `count` - _required_ - Number of message opens to return per request. Max 500.
* `offset` - _required_ - Number of messages to skip
* `recipient` - _optional_ - Filter by To, Cc, Bcc
* `tag` - _optional_ - Filter by tag
* `client_name` - _optional_ - Filter by client name, i.e. Outlook, Gmail
* `client_company` - _optional_ - Filter by company, i.e. Microsoft, Apple, Google
* `client_family` - _optional_ - Filter by client family, i.e. OS X, Chrome
* `os_name` - _optional_ - Filter by full OS name and specific version, i.e. OS X 10.9 Mavericks, Windows 7
* `os_family` - _optional_ - Filter by kind of OS used without specific version, i.e. OS X, Windows
* `os_company` - _optional_ - Filter by company which produced the OS, i.e. Apple Computer, Inc., Microsoft Corporation
* `platform` - _optional_ - Filter by platform, i.e. webmail, desktop, mobile
* `country` - _optional_ - Filter by country messages were opened in, i.e. Denmark, Russia
* `region` - _optional_ - Filter by full name of region messages were opened in, i.e. Moscow, New York
* `city` - _optional_ - Filter by full name of region messages were opened in, i.e. Moscow, New York

### Retrieve Message Opens

*Tags:* `Messages API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `messageid` - _required_ - The ID of the Outbound Message for which open statistics should be retrieved.
* `count` - _required_ - Number of message opens to return per request. Max 500.
* `offset` - _required_ - Number of messages to skip.

### Outbound message details

*Tags:* `Messages API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `messageid` - _required_ - The ID of the message for which to retrieve details.

### Outbound message dump

*Tags:* `Messages API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `messageid` - _required_ - The ID of the message for which to retrieve a dump.

### Get Server Configuration

*Tags:* `Server Configuration API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Edit Server Configuration

*Tags:* `Server Configuration API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Get outbound overview

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats up to the date specified. e.g. `2014-02-01`

### Get bounce counts

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats up to the date specified. e.g. `2014-02-01`

### Get click counts

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats up to the date specified. e.g. `2014-02-01`

### Get browser usage by family

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats up to the date specified. e.g. `2014-02-01`

### Get clicks by body location

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats up to the date specified. e.g. `2014-02-01`

### Get browser plaform usage

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats up to the date specified. e.g. `2014-02-01`

### Get email open counts

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats up to the date specified. e.g. `2014-02-01`

### Get email client usage

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats up to the date specified. e.g. `2014-02-01`

### Get email platform usage

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats up to the date specified. e.g. `2014-02-01`

### Get sent counts

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats up to the date specified. e.g. `2014-02-01`

### Get spam complaints

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats up to the date specified. e.g. `2014-02-01`

### Get tracked email counts

*Tags:* `Stats API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `tag` - _optional_ - Filter by tag
* `fromdate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`
* `todate` - _optional_ - Filter stats starting from the date specified. e.g. `2014-01-01`

### Get the Templates associated with this Server

*Tags:* `Templates API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `Count` - _required_ - The number of Templates to return
* `Offset` - _required_ - The number of Templates to "skip" before returning results.

### Create a Template

*Tags:* `Templates API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Test Template Content

*Tags:* `Templates API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Delete a Template

*Tags:* `Templates API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `templateIdOrAlias` - _required_ - The 'TemplateID' or 'Alias' value for the Template you wish to delete.

### Get a Template

*Tags:* `Templates API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `templateIdOrAlias` - _required_ - The 'TemplateID' or 'Alias' value for the Template you wish to retrieve.

### Update a Template

*Tags:* `Templates API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `templateIdOrAlias` - _required_ - The 'TemplateID' or 'Alias' value for the Template you wish to update.

### List inbound rule triggers

*Tags:* `Inbound Rules API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `count` - _required_ - Number of records to return per request.
* `offset` - _required_ - Number of records to skip.

### Create an inbound rule trigger

*Tags:* `Inbound Rules API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Delete a single trigger

*Tags:* `Inbound Rules API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `triggerid` - _required_ - The ID of the Inbound Rule that should be deleted.

### Search triggers

*Tags:* `Tag Triggers API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `count` - _required_ - Number of records to return per request.
* `offset` - _required_ - Number of records to skip.
* `match_name` - _optional_ - Filter by delivery tag

### Create a trigger for a tag

*Tags:* `Tag Triggers API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.

### Delete a single trigger

*Tags:* `Tag Triggers API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `triggerid` - _required_ - The ID for the Tag Trigger that should be deleted.

### Get a single trigger

*Tags:* `Tag Triggers API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `triggerid` - _required_ - The ID for the Tag Trigger for which data should be retrieved.

### Edit a single trigger

*Tags:* `Tag Triggers API`

#### Input Parameters
* `X-Postmark-Server-Token` - _required_ - The token associated with the Server on which this request will operate.
* `triggerid` - _required_ - The ID of the Tag Trigger that should be modified by this request.

## License

**flow**ground :- Telekom iPaaS / postmarkapp-com-server-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
