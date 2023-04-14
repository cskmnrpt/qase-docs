# Test Case

### Created Test Case

Payload example:

```json
{
  "event_name": "case.created",
  "timestamp": 1650530190,
  "payload": {
    "id": 1610,
    "title": "Example test case",
    "description": "Description test case",
    "preconditions": "something",
    "postconditions": "something",
    "priority": {
      "id": 2,
      "title": "Medium",
      "icon": "genderless",
      "color": "medium"
    },
    "severity": {
      "id": 4,
      "title": "Normal",
      "icon": "genderless",
      "color": "normal"
    },
    "behavior": {
      "id": 2,
      "title": "Positive"
    },
    "type": {
      "id": 8,
      "title": "Functional"
    },
    "automation": {
      "id": 1,
      "title": "To be automated"
    },
    "status": {
      "id": 0,
      "title": "Actual"
    },
    "suite_id": 12,
    "milestone_id": null,
    "steps": [
      {
        "position": 1,
        "action": "simple action",
        "expected_result": "expected result",
        "data": "input data",
        "attachments": [],
        "shared": false
      }
    ],
    "attachments": [],
    "custom_fields": [
      {
        "id": 174,
        "title": "Test Number",
        "type": "number",
        "value": "1"
      }
    ]
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

{% hint style="info" %}
This event is being sent when a new test case is created.
{% endhint %}

#### Event name

`case.created`

#### Payload fields

| Parameter      | Type    | Description                              |
| -------------- | ------- | ---------------------------------------- |
| id             | integer | Test case title                          |
| title          | string  | Test case title                          |
| description    | string  | Test case description                    |
| preconditions  | string  | Test case preconditions                  |
| postconditions | string  | Test case postconditions                 |
| severity       | object  | An object of test case severity          |
| priority       | object  | An object of test case priority          |
| type           | object  | An object of test case type              |
| status         | object  | An object of test case status            |
| automation     | object  | An object of test case automation status |
| behavior       | object  | An object of test case behavior          |
| suite\_id      | integer | Suite ID (nullable)                      |
| milestone\_id  | integer | Milestone\_id (nullable)                 |
| steps          | array   | An array of test steps objects.          |
| attachments    | array   | An array of attachments ids.             |
| custom\_fields | array   | An array of custom fields objects.       |

**Step object**

| Parameter        | Type    | Description                                                           |
| ---------------- | ------- | --------------------------------------------------------------------- |
| position         | integer | Step position                                                         |
| action           | string  | Required field (if shared\_step\_id is not provided). Can't be empty. |
| expected\_result | string  |                                                                       |
| shared           | boolean | Actual status step                                                    |
| attachments      | array   | An array of attachments IDs.                                          |

**Custom field object**

| Parameter | Type    | Description                                                                               |
| --------- | ------- | ----------------------------------------------------------------------------------------- |
| id        | integer | Custom field ID                                                                           |
| title     | string  | Custom field title                                                                        |
| value     | string  | Available only for selectbox fields. An object with selectbox values.                     |
| type      | string  | Custom field type. Available values: `number`, `string`, `text`, `selectbox`, `checkbox`. |

### Cloned Test Case

Payload example:

```json
{
  "event_name": "case.cloned",
  "timestamp": 1650530878,
  "payload": {
    "id": 1611,
    "from_id": 1610
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

{% hint style="info" %}
This event is being sent when a test case is cloned.
{% endhint %}

#### Event name

`case.cloned`

#### Payload fields

| Parameter | Type    | Description             |
| --------- | ------- | ----------------------- |
| id        | integer | Test case ID (clone)    |
| from\_id  | integer | Test case ID (original) |

### Updated Test Case

Payload example:

JSON

```json
{
  "event_name": "case.updated",
  "timestamp": 1650530630,
  "payload": {
    "id": 1610
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

> #### 📘
>
> This event is being sent when a test case is updated. It returns only ID of test case and notifies that fields were updated.

#### Event name

`case.updated`

#### Payload fields

| Parameter | Type    | Description  |
| --------- | ------- | ------------ |
| id        | integer | Test case ID |

### Deleted Test Case

Payload example:

```json
{
  "event_name": "case.deleted",
  "timestamp": 1650530938,
  "payload": {
    "id": 1611
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

{% hint style="info" %}
This event is being sent when a test case is deleted.
{% endhint %}

#### Event name

`case.deleted`

#### Payload fields

| Parameter | Type    | Description  |
| --------- | ------- | ------------ |
| id        | integer | Test case ID |

\
