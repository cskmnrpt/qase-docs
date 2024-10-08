# Test run

### Started Test Run

Payload example:

```json
{
  "event_name": "run.started",
  "timestamp": 1650540069,
  "payload": {
    "id": 1,
    "title": "Test run 2022/04/21",
    "description": null,
     "plan": {
      "id": 3,
      "title": "d"
    },
    "cases_count": 14,
    "environment": null
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

> #### 📘
>
> This event is being sent when a new test run is started.

#### Event name

`run.started`

#### Payload fields

| Parameter    | Type    | Description                 |
| ------------ | ------- | --------------------------- |
| id           | integer | Test run ID                 |
| title        | string  | Test run title              |
| description  | string  | Test run description        |
| plan         | object  | Test plan ID and title.     |
| cases\_count | integer | Amount of test cases in run |
| environment  | string  | Environment slug. Nullable. |

### Completed Test Run

Payload example:

```json
{
  "event_name": "run.completed",
  "timestamp": 1650540194,
  "payload": {
    "id": 2,
    "cases": 14,
    "passed": 0,
    "failed": 0,
    "blocked": 0,
    "duration": 0
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

> #### 📘
>
> This event is being sent when a test run is successfully completed.

#### Event name

`run.completed`

#### Payload fields

| Parameter | Type    | Description                       |
| --------- | ------- | --------------------------------- |
| id        | integer | Test run ID                       |
| cases     | integer | Amount of test cases in a run     |
| passed    | integer | Amount of passed cases            |
| failed    | integer | Amount of failed cases            |
| blocked   | integer | Amount of blocked cases           |
| duration  | integer | Test run duration in milliseconds |

### Aborted Test Run

Payload example:

```json
{
  "event_name": "run.aborted",
  "timestamp": 1650540148,
  "payload": {
    "id": 1,
    "cases": 14,
    "passed": 0,
    "untested": 14,
    "failed": 0,
    "blocked": 0,
    "skipped": 0,
    "duration": 0
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

> #### 📘
>
> This event is being sent when a test run is aborted.

#### Event name

`run.aborted`

#### Payload fields

| Parameter | Type    | Description                       |
| --------- | ------- | --------------------------------- |
| id        | integer | Test run ID                       |
| cases     | integer | Amount of test cases in a run     |
| passed    | integer | Amount of passed cases            |
| skiped    | integer | Amount of skiped cases            |
| failed    | integer | Amount of failed cases            |
| untested  | integer | Amount of untested cases          |
| blocked   | integer | Amount of blocked cases           |
| duration  | integer | Test run duration in milliseconds |

### Deleted Test Run

Payload example:

```json
{
  "event_name": "run.deleted",
  "timestamp": 1650540289,
  "payload": {
    "id": 1
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

> #### 📘
>
> This event is being sent when a test run is deleted.

#### Event name

`run.deleted`

#### Payload fields

| Parameter | Type    | Description |
| --------- | ------- | ----------- |
| id        | integer | Test run ID |

### Report visibility changed Test Run

Payload example:

```json
{
  "event_name": "run.report_changed",
  "timestamp": 1650540222,
  "payload": {
    "id": 2,
    "visible": true
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

> #### 📘
>
> This event is being sent when a public report visibility has been changed.

#### Event name

`run.report_changed`

#### Payload fields

| Parameter | Type    | Description                                |
| --------- | ------- | ------------------------------------------ |
| id        | integer | Test run ID                                |
| visible   | boolean | Shows if public report is available or not |

### Updated Test Run

Payload example:

```json
{
  "event_name": "run.updated",
  "timestamp": 1650540114,
  "payload": {
    "id": 1,
    "cases_added": 14
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

> #### 📘
>
> This event is being sent when a test plan is updated and new test cases were added.

#### Event name

`run.updated`

#### Payload fields

| Parameter    | Type    | Description                 |
| ------------ | ------- | --------------------------- |
| id           | integer | Test run ID                 |
| cases\_count | integer | Amount of test cases in run |

