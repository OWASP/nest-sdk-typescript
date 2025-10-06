# Community
(*community*)

## Overview

### Available Operations

* [listMembers](#listmembers) - List members
* [getMember](#getmember) - Get member
* [listOrganizations](#listorganizations) - List organizations
* [getOrganization](#getorganization) - Get organization

## listMembers

Retrieve a paginated list of OWASP community members.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_members" method="get" path="/api/v0/members/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.community.listMembers({
    location: "India",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { communityListMembers } from "owasp-nest/funcs/communityListMembers.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await communityListMembers(nest, {
    location: "India",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityListMembers failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListMembersRequest](../../models/operations/listmembersrequest.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedMember](../../models/pagedmember.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## getMember

Retrieve member details.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_member" method="get" path="/api/v0/members/{member_id}" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.community.getMember({
    memberId: "OWASP",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { communityGetMember } from "owasp-nest/funcs/communityGetMember.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await communityGetMember(nest, {
    memberId: "OWASP",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityGetMember failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetMemberRequest](../../models/operations/getmemberrequest.md)                                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MemberDetail](../../models/memberdetail.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.MemberError  | 404                 | application/json    |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## listOrganizations

Retrieve a paginated list of GitHub organizations.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_organizations" method="get" path="/api/v0/organizations/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.community.listOrganizations({
    location: "United States of America",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { communityListOrganizations } from "owasp-nest/funcs/communityListOrganizations.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await communityListOrganizations(nest, {
    location: "United States of America",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityListOrganizations failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListOrganizationsRequest](../../models/operations/listorganizationsrequest.md)                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedOrganization](../../models/pagedorganization.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## getOrganization

Retrieve project details.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_organization" method="get" path="/api/v0/organizations/{organization_id}" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.community.getOrganization({
    organizationId: "OWASP",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { communityGetOrganization } from "owasp-nest/funcs/communityGetOrganization.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await communityGetOrganization(nest, {
    organizationId: "OWASP",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityGetOrganization failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetOrganizationRequest](../../models/operations/getorganizationrequest.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.OrganizationDetail](../../models/organizationdetail.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.OrganizationError | 404                      | application/json         |
| errors.NestApiError      | 4XX, 5XX                 | \*/\*                    |