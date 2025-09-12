# Community
(*community*)

## Overview

### Available Operations

* [listMembers](#listmembers) - List members
* [appsApiRestV0MemberGetMember](#appsapirestv0membergetmember) - Get member
* [appsApiRestV0OrganizationListOrganization](#appsapirestv0organizationlistorganization) - List organizations
* [appsApiRestV0OrganizationGetOrganization](#appsapirestv0organizationgetorganization) - Get organization

## listMembers

Retrieve a paginated list of OWASP community members.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_members" method="get" path="/api/v0/members/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
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
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
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

**Promise\<[models.PagedMemberSchema](../../models/pagedmemberschema.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## appsApiRestV0MemberGetMember

Retrieve member details.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="apps_api_rest_v0_member_get_member" method="get" path="/api/v0/members/{member_id}" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const result = await nest.community.appsApiRestV0MemberGetMember({
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
import { communityAppsApiRestV0MemberGetMember } from "owasp-nest/funcs/communityAppsApiRestV0MemberGetMember.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const res = await communityAppsApiRestV0MemberGetMember(nest, {
    memberId: "OWASP",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityAppsApiRestV0MemberGetMember failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.AppsApiRestV0MemberGetMemberRequest](../../models/operations/appsapirestv0membergetmemberrequest.md)                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MemberSchema](../../models/memberschema.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.MemberErrorResponse | 404                        | application/json           |
| errors.NestApiError        | 4XX, 5XX                   | \*/\*                      |

## appsApiRestV0OrganizationListOrganization

Retrieve a paginated list of GitHub organizations.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="apps_api_rest_v0_organization_list_organization" method="get" path="/api/v0/organizations/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const result = await nest.community.appsApiRestV0OrganizationListOrganization({
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
import { communityAppsApiRestV0OrganizationListOrganization } from "owasp-nest/funcs/communityAppsApiRestV0OrganizationListOrganization.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const res = await communityAppsApiRestV0OrganizationListOrganization(nest, {
    location: "United States of America",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityAppsApiRestV0OrganizationListOrganization failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.AppsApiRestV0OrganizationListOrganizationRequest](../../models/operations/appsapirestv0organizationlistorganizationrequest.md)                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedOrganizationSchema](../../models/pagedorganizationschema.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## appsApiRestV0OrganizationGetOrganization

Retrieve project details.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="apps_api_rest_v0_organization_get_organization" method="get" path="/api/v0/organizations/{organization_id}" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const result = await nest.community.appsApiRestV0OrganizationGetOrganization({
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
import { communityAppsApiRestV0OrganizationGetOrganization } from "owasp-nest/funcs/communityAppsApiRestV0OrganizationGetOrganization.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKeyHeader: process.env["NEST_API_KEY_HEADER"] ?? "",
});

async function run() {
  const res = await communityAppsApiRestV0OrganizationGetOrganization(nest, {
    organizationId: "OWASP",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityAppsApiRestV0OrganizationGetOrganization failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.AppsApiRestV0OrganizationGetOrganizationRequest](../../models/operations/appsapirestv0organizationgetorganizationrequest.md)                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.OrganizationSchema](../../models/organizationschema.md)\>**

### Errors

| Error Type                       | Status Code                      | Content Type                     |
| -------------------------------- | -------------------------------- | -------------------------------- |
| errors.OrganizationErrorResponse | 404                              | application/json                 |
| errors.NestApiError              | 4XX, 5XX                         | \*/\*                            |