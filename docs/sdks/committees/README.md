# Committees
(*committees*)

## Overview

### Available Operations

* [listCommittees](#listcommittees) - List committees
* [appsApiRestV0CommitteeGetChapter](#appsapirestv0committeegetchapter) - Get committee

## listCommittees

Retrieve a paginated list of OWASP committees.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_committees" method="get" path="/api/v0/committees/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const result = await nest.committees.listCommittees({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { committeesListCommittees } from "owasp-nest/funcs/committeesListCommittees.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const res = await committeesListCommittees(nest, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("committeesListCommittees failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListCommitteesRequest](../../models/operations/listcommitteesrequest.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedCommitteeSchema](../../models/pagedcommitteeschema.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## appsApiRestV0CommitteeGetChapter

Retrieve committee details.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="apps_api_rest_v0_committee_get_chapter" method="get" path="/api/v0/committees/{committee_id}" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const result = await nest.committees.appsApiRestV0CommitteeGetChapter({
    committeeId: "project",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { committeesAppsApiRestV0CommitteeGetChapter } from "owasp-nest/funcs/committeesAppsApiRestV0CommitteeGetChapter.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const res = await committeesAppsApiRestV0CommitteeGetChapter(nest, {
    committeeId: "project",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("committeesAppsApiRestV0CommitteeGetChapter failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.AppsApiRestV0CommitteeGetChapterRequest](../../models/operations/appsapirestv0committeegetchapterrequest.md)                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CommitteeSchema](../../models/committeeschema.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.CommitteeErrorResponse | 404                           | application/json              |
| errors.NestApiError           | 4XX, 5XX                      | \*/\*                         |