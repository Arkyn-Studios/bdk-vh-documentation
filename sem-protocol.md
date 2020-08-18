# VH App

**prefix:** `dk/bane/vhapp`

## Application events
---
**topic:** `prefix + /application-events`

example payloads:
```json
{
    "eventType": "USER_LOGIN_INITIATED",
    "user": "xmtn@bane.dk"
}
```

```json
{
    "eventType": "USER_LOGIN_COMPLETED",
    "user": "xmtn@bane.dk"
}
```

```json
{
    "eventType": "USER_LOGIN_TIMEOUT",
    "user": "xmtn@bane.dk"
}
```

```json
{
    "eventType": "USER_DATABASE_INITIALIZING",
    "user": "xmtn@bane.dk"
}
```

```json
{
    "eventType": "USER_DATABASE_READY",
    "user": "xmtn@bane.dk"
}
```

```json
{
    "eventType": "USER_DATABASE_FAILED",
    "user": "xmtn@bane.dk",
    "error": 
}
```

## Orders:
---
**topic:** `prefix + /orders`

example payload:
```json
{
    "orderNo": "1000023132",
    "eventType": "ORDER_UPDATED",
    "details": "https://some-service-somewhere/orders/1000023132"
}
```

```json
{
    "orderNo": "1000023132",
    "eventType": "CHANGE_ORDER",
    "changes": {
        "addStatus": "TEKO",
        "addPerson": "XMTN",
        "removePerson": "JHBL",
        ...
    }
}
```

## Notifications:
---
**topic:** `prefix + /notifications`

example payload:
```json
{
    "notificationNo": "10201000201",
    "eventType": "NOTIFICATION_UPDATED",
    "details": "https://some-service-somewhere/notifications/1000023132"
}
```

```json
{
    "orderNo": "10201000201",
    "eventType": "CHANGE_NOTIFICATION",
    "changes": {
        "addPerson": "XMTN",
        "addFunctionalLocation": "01110",
        "addEquipment": "123123131313"
        ...
    }
}
```

## Technical Structure:
---
**topic:** `prefix + /technical-structure`

```json
{
    "type": "BRANCH_UPDATED",
    "functionalLocation": "01110",
    "details": "https://some-service-somewhere/functional-location/01110"
}
```

```json
{
    "type": "BRANCH_DELETED",
    "functionalLocation": "01110",
    "details": "https://some-service-somewhere/functional-location/01110"
}
```

# Time
---

**prefix:** `dk/bane/time`

Time:
- Entries
- Reporting Trees / Contexts / Etc.