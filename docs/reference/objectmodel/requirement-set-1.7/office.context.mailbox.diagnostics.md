---
title: Office.context.mailbox.diagnostics - requirement set 1.7
description: ''
ms.date: 11/05/2019
localization_priority: Normal
---

# diagnostics

### [Office](Office.md)[.context](Office.context.md)[.mailbox](Office.context.mailbox.md).diagnostics

Provides diagnostic information to an Outlook add-in.

##### Requirements

|Requirement| Value|
|---|---|
|[Minimum mailbox requirement set version](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| 1.0|
|[Minimum permission level](/outlook/add-ins/understanding-outlook-add-in-permissions)| ReadItem|
|[Applicable Outlook mode](/outlook/add-ins/#extension-points)| Compose or Read|

##### Members and methods

| Member | Type |
|--------|------|
| [hostName](#hostname-string) | Member |
| [hostVersion](#hostversion-string) | Member |
| [OWAView](#owaview-string) | Member |

### Members

#### hostName: String

Gets a string that represents the name of the host application.

A string that can be one of the following values: `Outlook`, `OutlookWebApp`, `OutlookIOS`, or `OutlookAndroid`.

> [!NOTE]
> The `Outlook` value is returned for Outlook on desktop clients (i.e., Windows and Mac).

##### Type

*   String

##### Requirements

|Requirement| Value|
|---|---|
|[Minimum mailbox requirement set version](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| 1.0|
|[Minimum permission level](/outlook/add-ins/understanding-outlook-add-in-permissions)| ReadItem|
|[Applicable Outlook mode](/outlook/add-ins/#extension-points)| Compose or Read|

<br>

---
---

#### hostVersion: String

Gets a string that represents the version of either the host application or the Exchange Server (e.g., "15.0.468.0").

If the mail add-in is running on an Outlook desktop or mobile client, the `hostVersion` property returns the version of the host application, Outlook. In Outlook on the web, the property returns the version of the Exchange Server.

##### Type

*   String

##### Requirements

|Requirement| Value|
|---|---|
|[Minimum mailbox requirement set version](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| 1.0|
|[Minimum permission level](/outlook/add-ins/understanding-outlook-add-in-permissions)| ReadItem|
|[Applicable Outlook mode](/outlook/add-ins/#extension-points)| Compose or Read|

<br>

---
---

#### OWAView: String

Gets a string that represents the current view of Outlook on the web.

The returned string can be one of the following values: `OneColumn`, `TwoColumns`, or `ThreeColumns`.

If the host application is not Outlook on the web, then accessing this property results in `undefined`.

Outlook on the web has three views that correspond to the width of the screen and the window, and the number of columns that can be displayed:

*   `OneColumn`, which is displayed when the screen is narrow. Outlook on the web uses this single-column layout on the entire screen of a smartphone.
*   `TwoColumns`, which is displayed when the screen is wider. Outlook on the web uses this view on most tablets.
*   `ThreeColumns`, which is displayed when the screen is wide. For example, Outlook on the web uses this view in a full screen window on a desktop computer.

##### Type

*   String

##### Requirements

|Requirement| Value|
|---|---|
|[Minimum mailbox requirement set version](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| 1.0|
|[Minimum permission level](/outlook/add-ins/understanding-outlook-add-in-permissions)| ReadItem|
|[Applicable Outlook mode](/outlook/add-ins/#extension-points)| Compose or Read|
