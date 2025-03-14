---
title: Outlook add-in API requirement set 1.8
description: ''
ms.date: 10/31/2019
localization_priority: Priority
---

# Outlook add-in API requirement set 1.8

The Outlook add-in API subset of the JavaScript API for Office includes objects, methods, properties and events that you can use in an Outlook add-in.

## What's new in 1.8?

Requirement set 1.8 includes all of the features of [Requirement set 1.7](../requirement-set-1.7/outlook-requirement-set-1.7.md). It added the following features.

- Added new APIs for attachments, categories, delegate access, enhanced location, internet headers, and block on send features.
- Added optional `options` parameter to Event.completed.
- Added support for AttachmentsChanged and EnhancedLocationsChanged events.

### Change log

- Added [AttachmentContent](/javascript/api/outlook/office.attachmentcontent?view=outlook-js-1.8): Adds a new object that represents the content of an attachment.
- Added [Categories](/javascript/api/outlook/office.categories?view=outlook-js-1.8): Adds a new object that represents an item's categories.
- Added [CategoryDetails](/javascript/api/outlook/office.categorydetails?view=outlook-js-1.8): Adds a new object that represents a category's details (its name and associated color).
- Added [EnhancedLocation](/javascript/api/outlook/office.enhancedlocation?view=outlook-js-1.8): Adds a new object that represents the set of locations on an appointment.
- Added [InternetHeaders](/javascript/api/outlook/office.internetheaders?view=outlook-js-1.8): Adds a new object that represents the custom internet headers of a message item. Compose mode only.
- Added [LocationDetails](/javascript/api/outlook/office.locationdetails?view=outlook-js-1.8): Adds a new object that represents a location. Read only.
- Added [LocationIdentifier](/javascript/api/outlook/office.locationidentifier?view=outlook-js-1.8): Adds a new object that represents the id of a location.
- Added [MasterCategories](/javascript/api/outlook/office.mastercategories?view=outlook-js-1.8): Adds a new object that represents the categories master list on a mailbox.
- Added [SharedProperties](/javascript/api/outlook/office.sharedproperties?view=outlook-js-1.8): Adds a new object that represents the properties of an appointment or message item in a shared folder, calendar, or mailbox.
- Added [SupportsSharedFolders manifest element](../../manifest/supportssharedfolders.md): Adds a child element to the [DesktopFormFactor](../../manifest/desktopformfactor.md) manifest element. It defines whether the add-in is available in delegate scenarios.
- Added [Office.context.mailbox.masterCategories](/javascript/api/outlook/office.mailbox?view=outlook-js-1.8#mastercategories): Adds a new property that represents the categories master list on a mailbox.
- Added [Office.context.mailbox.item.categories](/javascript/api/outlook/office.item?view=outlook-js-1.8#categories): Adds a new property that represents the set of categories on an item.
- Added [Office.context.mailbox.item.addFileAttachmentFromBase64Async](office.context.mailbox.item.md#addfileattachmentfrombase64asyncbase64file-attachmentname-options-callback): Adds a new method that allows you to attach a file represented as a base64 encoded string to a message or appointment.
- Added [Office.context.mailbox.item.enhancedLocation](office.context.mailbox.item.md#enhancedlocation-enhancedlocation): Adds a new property that represents the set of locations on an appointment.
- Added [Office.context.mailbox.item.getAllInternetHeadersAsync](/javascript/api/outlook/office.messageread?view=outlook-js-1.8#getallinternetheadersasync-options--callback-): Adds a new method that gets all the internet headers for a message item. Read mode only.
- Added [Office.context.mailbox.item.getAttachmentContentAsync](office.context.mailbox.item.md#getattachmentcontentasyncattachmentid-options-callback--attachmentcontent): Adds a new method to get the content of a specific attachment.
- Added [Office.context.mailbox.item.getAttachmentsAsync](office.context.mailbox.item.md#getattachmentsasyncoptions-callback--arrayattachmentdetails): Adds a new method that gets an item's attachments in compose mode.
- Added [Office.context.mailbox.item.getItemIdAsync](office.context.mailbox.item.md#getitemidasyncoptions-callback): Adds a new method that gets the ID of a saved appointment or message item.
- Added [Office.context.mailbox.item.getSharedPropertiesAsync](office.context.mailbox.item.md#getsharedpropertiesasyncoptions-callback): Adds a new method that gets an object which represents the sharedProperties of an appointment or message item.
- Added [Office.context.mailbox.item.internetHeaders](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.8#internetheaders): Adds a new property that represents the custom internet headers on a message item. Compose mode only.
- Modified [Event.completed](/javascript/api/office/office.addincommands.event#completed-options-): Adds a new optional parameter `options`, which is a dictionary with one valid value `allowEvent`. This value is used to cancel execution of an event.
- Added [Office.MailboxEnums.AttachmentContentFormat](/javascript/api/outlook/office.mailboxenums.attachmentcontentformat?view=outlook-js-1.8): Adds a new enum that specifies the formatting that applies to an attachment's content.
- Added [Office.MailboxEnums.AttachmentStatus](/javascript/api/outlook/office.mailboxenums.attachmentstatus?view=outlook-js-1.8): Adds a new enum that specifies whether an attachment was added to or removed from an item.
- Added [Office.MailboxEnums.CategoryColor](/javascript/api/outlook/office.mailboxenums.categorycolor?view=outlook-js-1.8): Adds a new enum that specifies the colors available to be associated with categories.
- Added [Office.MailboxEnums.DelegatePermissions](/javascript/api/outlook/office.mailboxenums.delegatepermissions?view=outlook-js-1.8): Adds a new bit flag enum that specifies the delegate permissions.
- Added [Office.MailboxEnums.LocationType](/javascript/api/outlook/office.mailboxenums.locationtype?view=outlook-js-1.8): Adds a new enum that specifies an appointment location's type.
- Modified [Office.EventType](/javascript/api/office/office.eventtype): Adds support for `AttachmentsChanged` and `EnhancedLocationsChanged` events.

## See also

- [Outlook add-ins](/outlook/add-ins/)
- [Outlook add-in code samples](https://developer.microsoft.com/outlook/gallery/?filterBy=Outlook,Samples,Add-ins)
- [Get started](/outlook/add-ins/quick-start)
- [Requirement sets and supported clients](../../requirement-sets/outlook-api-requirement-sets.md)
