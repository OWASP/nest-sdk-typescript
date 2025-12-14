# Milestones

## Overview

### Available Operations

* [listMilestones](#listmilestones) - List milestones
* [getMilestone](#getmilestone) - Get milestone

## listMilestones

Retrieve a paginated list of GitHub milestones.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_milestones" method="get" path="/api/v0/milestones/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.milestones.listMilestones({
    organization: "OWASP",
    repository: "Nest",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { milestonesListMilestones } from "owasp-nest/funcs/milestonesListMilestones.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await milestonesListMilestones(nest, {
    organization: "OWASP",
    repository: "Nest",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("milestonesListMilestones failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListMilestonesRequest](../../models/operations/listmilestonesrequest.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedMilestone](../../models/pagedmilestone.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## getMilestone

Retrieve a specific GitHub milestone by organization, repository, and milestone number.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_milestone" method="get" path="/api/v0/milestones/{organization_id}/{repository_id}/{milestone_id}" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.milestones.getMilestone({
    organizationId: "OWASP",
    repositoryId: "Nest",
    milestoneId: 1,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { milestonesGetMilestone } from "owasp-nest/funcs/milestonesGetMilestone.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await milestonesGetMilestone(nest, {
    organizationId: "OWASP",
    repositoryId: "Nest",
    milestoneId: 1,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("milestonesGetMilestone failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetMilestoneRequest](../../models/operations/getmilestonerequest.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MilestoneDetail](../../models/milestonedetail.md)\>**

### Errors

| Error Type            | Status Code           | Content Type          |
| --------------------- | --------------------- | --------------------- |
| errors.MilestoneError | 404                   | application/json      |
| errors.NestApiError   | 4XX, 5XX              | \*/\*                 |