# Community

## Overview

### Available Operations

* [listMembers](#listmembers) - List members
* [getMember](#getmember) - Get member
* [listOrganizations](#listorganizations) - List organizations
* [getOrganization](#getorganization) - Get organization
* [listSnapshots](#listsnapshots) - List snapshots
* [getSnapshot](#getsnapshot) - Get snapshot
* [listSnapshotChapters](#listsnapshotchapters) - List new chapters in snapshot
* [listSnapshotIssues](#listsnapshotissues) - List new issues in snapshot
* [listSnapshotMembers](#listsnapshotmembers) - List new members in snapshot
* [listSnapshotProjects](#listsnapshotprojects) - List new projects in snapshot
* [listSnapshotReleases](#listsnapshotreleases) - List new releases in snapshot

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

## listSnapshots

Retrieve a paginated list of OWASP snapshots.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_snapshots" method="get" path="/api/v0/snapshots/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.community.listSnapshots({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { communityListSnapshots } from "owasp-nest/funcs/communityListSnapshots.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await communityListSnapshots(nest, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityListSnapshots failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListSnapshotsRequest](../../models/operations/listsnapshotsrequest.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedSnapshot](../../models/pagedsnapshot.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## getSnapshot

Retrieve snapshot details.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_snapshot" method="get" path="/api/v0/snapshots/{snapshot_id}" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.community.getSnapshot({
    snapshotId: "2025-02",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { communityGetSnapshot } from "owasp-nest/funcs/communityGetSnapshot.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await communityGetSnapshot(nest, {
    snapshotId: "2025-02",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityGetSnapshot failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetSnapshotRequest](../../models/operations/getsnapshotrequest.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SnapshotDetail](../../models/snapshotdetail.md)\>**

### Errors

| Error Type           | Status Code          | Content Type         |
| -------------------- | -------------------- | -------------------- |
| errors.SnapshotError | 404                  | application/json     |
| errors.NestApiError  | 4XX, 5XX             | \*/\*                |

## listSnapshotChapters

Retrieve a paginated list of new chapters in a snapshot.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_snapshot_chapters" method="get" path="/api/v0/snapshots/{snapshot_id}/chapters/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.community.listSnapshotChapters({
    snapshotId: "2025-02",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { communityListSnapshotChapters } from "owasp-nest/funcs/communityListSnapshotChapters.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await communityListSnapshotChapters(nest, {
    snapshotId: "2025-02",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityListSnapshotChapters failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListSnapshotChaptersRequest](../../models/operations/listsnapshotchaptersrequest.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedChapter](../../models/pagedchapter.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## listSnapshotIssues

Retrieve a paginated list of new issues in a snapshot.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_snapshot_issues" method="get" path="/api/v0/snapshots/{snapshot_id}/issues/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.community.listSnapshotIssues({
    snapshotId: "2025-02",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { communityListSnapshotIssues } from "owasp-nest/funcs/communityListSnapshotIssues.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await communityListSnapshotIssues(nest, {
    snapshotId: "2025-02",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityListSnapshotIssues failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListSnapshotIssuesRequest](../../models/operations/listsnapshotissuesrequest.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedSnapshotIssue](../../models/pagedsnapshotissue.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## listSnapshotMembers

Retrieve a paginated list of new members in a snapshot.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_snapshot_members" method="get" path="/api/v0/snapshots/{snapshot_id}/members/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.community.listSnapshotMembers({
    snapshotId: "2025-02",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { communityListSnapshotMembers } from "owasp-nest/funcs/communityListSnapshotMembers.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await communityListSnapshotMembers(nest, {
    snapshotId: "2025-02",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityListSnapshotMembers failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListSnapshotMembersRequest](../../models/operations/listsnapshotmembersrequest.md)                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedMember](../../models/pagedmember.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## listSnapshotProjects

Retrieve a paginated list of new projects in a snapshot.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_snapshot_projects" method="get" path="/api/v0/snapshots/{snapshot_id}/projects/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.community.listSnapshotProjects({
    snapshotId: "2025-02",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { communityListSnapshotProjects } from "owasp-nest/funcs/communityListSnapshotProjects.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await communityListSnapshotProjects(nest, {
    snapshotId: "2025-02",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityListSnapshotProjects failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListSnapshotProjectsRequest](../../models/operations/listsnapshotprojectsrequest.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedProject](../../models/pagedproject.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |

## listSnapshotReleases

Retrieve a paginated list of new releases in a snapshot.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_snapshot_releases" method="get" path="/api/v0/snapshots/{snapshot_id}/releases/" -->
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.community.listSnapshotReleases({
    snapshotId: "2025-02",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { NestCore } from "owasp-nest/core.js";
import { communityListSnapshotReleases } from "owasp-nest/funcs/communityListSnapshotReleases.js";

// Use `NestCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const nest = new NestCore({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const res = await communityListSnapshotReleases(nest, {
    snapshotId: "2025-02",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("communityListSnapshotReleases failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListSnapshotReleasesRequest](../../models/operations/listsnapshotreleasesrequest.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PagedSnapshotRelease](../../models/pagedsnapshotrelease.md)\>**

### Errors

| Error Type          | Status Code         | Content Type        |
| ------------------- | ------------------- | ------------------- |
| errors.NestApiError | 4XX, 5XX            | \*/\*               |