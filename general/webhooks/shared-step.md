# Shared step

### Created Shared Step

Payload example:

```json
{
  "event_name": "shared_step.created",
  "timestamp": 1650577292,
  "payload": {
    "hash": "678ec0e6bf8ddeadfc241016f876923542a4761a",
    "title": "fff",
    "steps": [
      {
        "hash": "40bf38b525073257aad38a51c5f5734f8b0f30b8",
        "action": "action",
        "expected_result": "expected",
        "data": "data",
        "attachments": []
      }
    ]
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

> #### 📘
>
> This event is being sent when a new shared step is created.

#### Event name

`shared_step.created`

#### Payload fields

| Parameter | Type   | Description       |
| --------- | ------ | ----------------- |
| hash      | string | Shared step hash  |
| steps     | array  | An array of steps |
| data      | string | Shared step data  |

### Deleted Shared Step

Payload example:

```json
{
  "event_name": "shared_step.deleted",
  "timestamp": 1650540719,
  "payload": {
    "hash": "2563d587b856810934dea4185ce31b9b0dbf352c"
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

> #### 📘
>
> This event is being sent when a shared\_step is deleted.

#### Event name

`shared_step.deleted`

#### Payload fields

| Parameter | Type   | Description      |
| --------- | ------ | ---------------- |
| hash      | string | Shared step hash |

### Updated Shared Step

Payload example:

```json
{
  "event_name": "shared_step.updated",
  "timestamp": 1650540693,
  "payload": {
    "hash": "2563d597b756810934dea4185ce31b2b0dbf377c"
  },
  "team_member_id": 40,
  "project_code": "ID"
}
```

> #### 📘
>
> This event is being sent when a shared step is updated.

#### Event name

`shared_step.updated`

#### Payload fields

| Parameter | Type   | Description      |
| --------- | ------ | ---------------- |
| id        | string | Shared step hash |

\
