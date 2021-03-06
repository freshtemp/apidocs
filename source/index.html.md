---
title: API Reference

language_tabs:
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the FreshTemp API! You can use our API to access FreshTemp API endpoints, which can get information on various sensors, task results, and other information in our database.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

# Authentication

> To authorize, use this code:

```ruby
require 'freshtemp'

api = FreshTemp::APIClient.authorize!('hjkh76g65dds37nbvxa')
```

```python
import freshtemp

api = freshtemp.authorize('hjkh76g65dds37nbvxa')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: hjkh76g65dds37nbvxa"
```

```javascript
const freshtemp = require('freshtemp');

let api = freshtemp.authorize('hjkh76g65dds37nbvxa');
```

> Make sure to replace `hjkh76g65dds37nbvxa` with your API key.

FreshTemp uses API keys to allow access to the API. You can register a new FreshTemp API key at our [developer portal](http://app.freshtemp.com).

FreshTemp expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: hjkh76g65dds37nbvxa`

<aside class="notice">
You must replace <code>hjkh76g65dds37nbvxa</code> with your personal API key.
</aside>

# Users

## The user object


```json
[
  {
    "id": "usr_87df9sa7fclkjaf",
    "object" : "user",
    "api_version": "v1",
    "username": "",
    "email": "",
    "locations": {
      "loc_fdkj8asldkj",
      "loc_fdkj8asldkj",
    }
  }
]
```

The user object

<table><thead>
<tr>
<th style="color: #939da3;text-transform: uppercase;">Attributes</th>
<th></th>
</tr>
</thead><tbody>
<tr>
<td style="width:180px; text-align: right">id<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>Unique identifier for the object</td>
</tr>
<tr>
<td style="width:180px; text-align: right">object<div style="color: #939da3;padding: 4px 0 0;">string, value is "user"</div></td>
<td>String representing the object’s type.</td>
</tr>
</tbody></table>

## Create a user

Not currently supported

## Retrieve a user

Not currently supported

## Update a user

Not currently supported

## Delete a user

Not currently supported

## List All Users

Not currently supported

# Locations

## The location object


```json
[
  {
    "id": "loc_87df9sa7fclkjaf",
    "object" : "location",
    "api_version": "v1",
    "name": "Restaurant #123",
    "address" : "1 Pike Place, Seattle, WA",
    "created" : "2017-01-01 01:23:49 UTC",
    "timezone": "EDT",
  }
]
```

The location object

<table><thead>
<tr>
<th style="color: #939da3;text-transform: uppercase;">Attributes</th>
<th></th>
</tr>
</thead><tbody>
<tr>
<td style="width:180px; text-align: right">id<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>Unique identifier for the object</td>
</tr>
<tr>
<td style="width:180px; text-align: right">object<div style="color: #939da3;padding: 4px 0 0;">string, value is "location"</div></td>
<td>String representing the object’s type.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">api_version<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The FreshTemp API version used to render data.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">address<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The address of the location.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">created<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The datetime when the location was created.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">timezone<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The timezone at the location.</td>
</tr>
</tbody></table>

## Create a location

Not currently supported

## Retrieve a location

Not currently supported

## Update a location

Not currently supported

## Delete a location

Not currently supported

## List All Locations

Not currently supported

# Sensors

## The sensor object

```json
[
  {
    "id": "sen_87df9sa7fclkjaf",
    "object" : "sensor",
    "api_version": "v1",
    "mac_address": "00:41:23:23:af:42",
    "created" : "2017-01-03 08:32:32 UTC",
    "adc_reading" : "302",
    "temperature" : "43.34",
    "last_updated" : " 2017-03-04 23:32:23 UTC",
    "transmit_interval" : "210",
  }
]
```

The sensor object

<table><thead>
<tr>
<th style="color: #939da3;text-transform: uppercase;">Attributes</th>
<th></th>
</tr>
</thead><tbody>
<tr>
<td style="width:180px; text-align: right">id<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>Unique identifier for the object</td>
</tr>
<tr>
<td style="width:180px; text-align: right">object<div style="color: #939da3;padding: 4px 0 0;">string, value is "location"</div></td>
<td>String representing the object’s type.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">api_version<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The FreshTemp API version used to render data.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">mac_address<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The unique mac address of the sensor.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">created<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The datetime when the sensor was created.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">adc_reading<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The ADC value returned from the last measurement reading.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">temperature<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The last measured temperature of the sensor.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">last_updated<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The datetime when the last measurement was recorded.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">transmit_interval<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The frequency at which the sensor records and transmits data (in seconds).</td>
</tr>
</tbody></table>

# Checklists

## Get All Checklists

# Corrective Action Group

## Get All Corrective Action Group

# Corrective Action

## Get All Corrective Actions

# Task Results

## Get All Task Results

# Randomizer Group

## Get All Randomizer Groups

# Randomizer Item

## Get All Task Randomizer Items

# Tasks

## The task object


```json
[
  {
    "id": "tsk_87df9sa7fclkjaf",
    "object" : "task",
    "api_version": "v1",
    "title": "Pest check",
    "subtitle": "Is there any evidence of pest activity?",
    "corrective_action_group": "cag_32usjf87zuqodld",
    "not_available_group": "nag_19us47fodld",
    "randomizer_group": "rng_53uald7hkal42",
  }
]
```

The task object

<table><thead>
<tr>
<th style="color: #939da3;text-transform: uppercase;">Attributes</th>
<th></th>
</tr>
</thead><tbody>
<tr>
<td style="width:180px; text-align: right">id<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>Unique identifier for the object</td>
</tr>
<tr>
<td style="width:180px; text-align: right">object<div style="color: #939da3;padding: 4px 0 0;">string, value is "task"</div></td>
<td>String representing the object’s type.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">api_version<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The FreshTemp API version used to render data.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">title<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The title of the task.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">subtitle<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The subtitle of the task.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">corrective_action_group<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The corrective action group used if a violation occurs.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">not_available_group<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The corrective action group used if not available action is taken.</td>
</tr>
<tr>
<td style="width:180px; text-align: right">randomizer_group<div style="color: #939da3;padding: 4px 0 0;">string</div></td>
<td>The randomizer group used if task requires item randomization.</td>
</tr>
</tbody></table>

## Get All Tasks

```ruby
require 'freshtemp'

ft = FreshTemp::APIClient.authorize!('hjkh76g65dds37nbvxa')
ft.tasks.get('loc_8RUs1PpoUuNXyw')
```

```python
import freshtemp

api = freshtemp.authorize('hjkh76g65dds37nbvxa')
api.tasks.get('loc_8RUs1PpoUuNXyw')
```

```shell
curl "https://api.freshtemp.com/v1/tasks/loc_8RUs1PpoUuNXyw"
  -H "Authorization: hjkh76g65dds37nbvxa"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "tsk_87df9sa7Clkjaf",
    "object" : "task",
    "api_version": "v1",
    "title": "Pest check",
    "subtitle": "Is there any evidence of pest activity?",
    "corrective_action_group": "cag_32usjf87zuqodld",
    "not_available_group": "nag_19us47fodld",
    "randomizer_group": "rng_53uald7hkal42",
  },
  {
    "id": "tsk_6DBkbiJBdBn4Zm",
    "location" : 2,
    "type": "temp-probe",
    "title": "Walk in Cooler",
    "subtitle": "32°F to 41°F",
    "corrective_action_group": "cag_99Afjnak48afkl",
    "not_available_group": "nag_19us47fodld",
    "randomizer_group": "rng_53uald7hkal42",
  }
]
```

This endpoint retrieves all tasks.

<table><thead>
<tr>
<th style="color: #939da3;text-transform: uppercase;">Arguments</th>
<th></th>
</tr>
</thead><tbody>
<tr>
<td style="width:180px; text-align: right">location_id<div style="color: #ffae54;text-transform: uppercase;padding: 4px 0 0;">required</div></td>
<td>The location ID where the tasks are to be retrieved</td>
</tr>
</tbody></table>

### HTTPS Request

`GET https://api.freshtemp.com/v1/tasks/loc_8RUs1PpoUuNXyw`

<aside class="success">
Remember — Every request is an authenticated!
</aside>


<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://api.freshtemp.com/v1/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the parameter to retrieve

