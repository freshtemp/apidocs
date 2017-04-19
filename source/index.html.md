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

FreshTemp uses API keys to allow access to the API. You can register a new FreshTemp API key at our [developer portal](http://app.freshtemp.com/developer).

FreshTemp expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: hjkh76g65dds37nbvxa`

<aside class="notice">
You must replace <code>hjkh76g65dds37nbvxa</code> with your personal API key.
</aside>

# Users

## Get All Users

# Locations

## Get All Locations

# Equipment

## Get All Equipment

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

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
location | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — Every request is an authenticated!
</aside>

## Get a Specific Kitten

```ruby
require 'freshtemp'

api = freshtemp::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import freshtemp

api = freshtemp.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const freshtemp = require('freshtemp');

let api = freshtemp.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://api.freshtemp.com/v1/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

