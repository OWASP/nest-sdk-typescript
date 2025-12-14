# Events

## Overview

### Available Operations

* [listEvents](#listevents) - List events
* [getEvent](#getevent) - Get event

## listEvents

Retrieve a paginated list of OWASP events.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_events" method="get" path="/api/v0/events/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.events.listEvents({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { eventsListEvents } from "owasp-nest/funcs/eventsListEvents.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await eventsListEvents(nest, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("eventsListEvents failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListEventsRequest](../../models/operations/listeventsrequest.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedEvent](../../models/pagedevent.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## getEvent

Retrieve an event details.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_event" method="get" path="/api/v0/events/{event_id}" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.events.getEvent({
    eventId: "owasp-global-appsec-usa-2025-washington-dc",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { eventsGetEvent } from "owasp-nest/funcs/eventsGetEvent.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await eventsGetEvent(nest, {
    eventId: "owasp-global-appsec-usa-2025-washington-dc",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("eventsGetEvent failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetEventRequest](../../models/operations/geteventrequest.md)                                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.EventDetail](../../models/eventdetail.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.EventError   | 404                 | application/json    |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |