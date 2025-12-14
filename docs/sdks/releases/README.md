# Releases

## Overview

### Available Operations

* [listReleases](#listreleases) - List releases
* [getRelease](#getrelease) - Get release

## listReleases

Retrieve a paginated list of GitHub releases.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_releases" method="get" path="/api/v0/releases/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.releases.listReleases({
    organization: "OWASP",
    repository: "Nest",
    tagName: "0.2.10",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { releasesListReleases } from "owasp-nest/funcs/releasesListReleases.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await releasesListReleases(nest, {
    organization: "OWASP",
    repository: "Nest",
    tagName: "0.2.10",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("releasesListReleases failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListReleasesRequest](../../models/operations/listreleasesrequest.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedRelease](../../models/pagedrelease.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## getRelease

Retrieve a specific GitHub release by organization, repository, and tag name.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_release" method="get" path="/api/v0/releases/{organization_id}/{repository_id}/{release_id}" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.releases.getRelease({
    organizationId: "OWASP",
    repositoryId: "Nest",
    releaseId: "0.2.10",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { releasesGetRelease } from "owasp-nest/funcs/releasesGetRelease.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await releasesGetRelease(nest, {
    organizationId: "OWASP",
    repositoryId: "Nest",
    releaseId: "0.2.10",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("releasesGetRelease failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetReleaseRequest](../../models/operations/getreleaserequest.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.ReleaseDetail](../../models/releasedetail.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.ReleaseError | 404                 | application/json    |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |