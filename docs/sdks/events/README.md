# Events
(*events*)

## Overview

### Available Operations

* [appsApiRestV0EventListEvents](#appsapirestv0eventlistevents) - List events

## appsApiRestV0EventListEvents

Retrieve a paginated list of OWASP events.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="apps_api_rest_v0_event_list_events" method="get" path="/api/v0/events/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const result = await nest.events.appsApiRestV0EventListEvents({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { eventsAppsApiRestV0EventListEvents } from "owasp-nest/funcs/eventsAppsApiRestV0EventListEvents.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const res = await eventsAppsApiRestV0EventListEvents(nest, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("eventsAppsApiRestV0EventListEvents failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.AppsApiRestV0EventListEventsRequest](../../models/operations/appsapirestv0eventlisteventsrequest.md)                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedEventSchema](../../models/pagedeventschema.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |