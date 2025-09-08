# Repositories
(*repositories*)

## Overview

### Available Operations

* [listRepositories](#listrepositories) - List repositories

## listRepositories

Retrieve a paginated list of GitHub repositories.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_repositories" method="get" path="/api/v1/repositories/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKeyAuth: process.env["NEST_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await nest.repositories.listRepositories({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { repositoriesListRepositories } from "owasp-nest/funcs/repositoriesListRepositories.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKeyAuth: process.env["NEST_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await repositoriesListRepositories(nest, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("repositoriesListRepositories failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListRepositoriesRequest](../../models/operations/listrepositoriesrequest.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedRepositorySchema](../../models/pagedrepositoryschema.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |