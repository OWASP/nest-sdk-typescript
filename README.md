# owasp-nest

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *owasp-nest* API.

<div align="left">
    <a href="https://www.speakeasy.com/?utm_source=owasp-nest&utm_campaign=typescript"><img src="https://www.speakeasy.com/assets/badges/built-by-speakeasy.svg" /></a>
    <a href="https://opensource.org/licenses/MIT">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" style="width: 100px; height: 28px;" />
    </a>
</div>

<!-- Start Summary [summary] -->
## Summary

OWASP Nest: Open Worldwide Application Security Project API
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [owasp-nest](#owasp-nest)
  * [SDK Installation](#sdk-installation)
  * [Requirements](#requirements)
  * [SDK Example Usage](#sdk-example-usage)
  * [Authentication](#authentication)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Standalone functions](#standalone-functions)
  * [Retries](#retries)
  * [Error Handling](#error-handling)
  * [Server Selection](#server-selection)
  * [Custom HTTP Client](#custom-http-client)
  * [Debugging](#debugging)
* [Development](#development)
  * [Maturity](#maturity)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

The SDK can be installed with either [npm](https://www.npmjs.com/), [pnpm](https://pnpm.io/), [bun](https://bun.sh/) or [yarn](https://classic.yarnpkg.com/en/) package managers.

### NPM

```bash
npm add owasp-nest
```

### PNPM

```bash
pnpm add owasp-nest
```

### Bun

```bash
bun add owasp-nest
```

### Yarn

```bash
yarn add owasp-nest zod

# Note that Yarn does not install peer dependencies automatically. You will need
# to install zod as shown above.
```

> [!NOTE]
> This package is published with CommonJS and ES Modules (ESM) support.
<!-- End SDK Installation [installation] -->

<!-- Start Requirements [requirements] -->
## Requirements

For supported JavaScript runtimes, please consult [RUNTIMES.md](RUNTIMES.md).
<!-- End Requirements [requirements] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.chapters.listChapters({
    country: "India",
    region: "Asia",
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->

<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name     | Type   | Scheme  | Environment Variable |
| -------- | ------ | ------- | -------------------- |
| `apiKey` | apiKey | API key | `NEST_API_KEY`       |

To authenticate with the API the `apiKey` parameter must be set when initializing the SDK client instance. For example:
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.chapters.listChapters({
    country: "India",
    region: "Asia",
  });

  console.log(result);
}

run();

```
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [chapters](docs/sdks/chapters/README.md)

* [listChapters](docs/sdks/chapters/README.md#listchapters) - List chapters
* [getChapter](docs/sdks/chapters/README.md#getchapter) - Get chapter

### [committees](docs/sdks/committees/README.md)

* [listCommittees](docs/sdks/committees/README.md#listcommittees) - List committees
* [getCommittee](docs/sdks/committees/README.md#getcommittee) - Get committee

### [community](docs/sdks/community/README.md)

* [listMembers](docs/sdks/community/README.md#listmembers) - List members
* [getMember](docs/sdks/community/README.md#getmember) - Get member
* [listOrganizations](docs/sdks/community/README.md#listorganizations) - List organizations
* [getOrganization](docs/sdks/community/README.md#getorganization) - Get organization

### [events](docs/sdks/events/README.md)

* [listEvents](docs/sdks/events/README.md#listevents) - List events

### [issues](docs/sdks/issues/README.md)

* [listIssues](docs/sdks/issues/README.md#listissues) - List issues


### [projects](docs/sdks/projects/README.md)

* [listProjects](docs/sdks/projects/README.md#listprojects) - List projects
* [getProject](docs/sdks/projects/README.md#getproject) - Get project

### [releases](docs/sdks/releases/README.md)

* [listReleases](docs/sdks/releases/README.md#listreleases) - List releases

### [repositories](docs/sdks/repositories/README.md)

* [listRepositories](docs/sdks/repositories/README.md#listrepositories) - List repositories

### [sponsors](docs/sdks/sponsors/README.md)

* [listSponsors](docs/sdks/sponsors/README.md#listsponsors) - List sponsors
* [getSponsor](docs/sdks/sponsors/README.md#getsponsor) - Get sponsor

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Standalone functions [standalone-funcs] -->
## Standalone functions

All the methods listed above are available as standalone functions. These
functions are ideal for use in applications running in the browser, serverless
runtimes or other environments where application bundle size is a primary
concern. When using a bundler to build your application, all unused
functionality will be either excluded from the final bundle or tree-shaken away.

To read more about standalone functions, check [FUNCTIONS.md](./FUNCTIONS.md).

<details>

<summary>Available standalone functions</summary>

- [`chaptersGetChapter`](docs/sdks/chapters/README.md#getchapter) - Get chapter
- [`chaptersListChapters`](docs/sdks/chapters/README.md#listchapters) - List chapters
- [`committeesGetCommittee`](docs/sdks/committees/README.md#getcommittee) - Get committee
- [`committeesListCommittees`](docs/sdks/committees/README.md#listcommittees) - List committees
- [`communityGetMember`](docs/sdks/community/README.md#getmember) - Get member
- [`communityGetOrganization`](docs/sdks/community/README.md#getorganization) - Get organization
- [`communityListMembers`](docs/sdks/community/README.md#listmembers) - List members
- [`communityListOrganizations`](docs/sdks/community/README.md#listorganizations) - List organizations
- [`eventsListEvents`](docs/sdks/events/README.md#listevents) - List events
- [`issuesListIssues`](docs/sdks/issues/README.md#listissues) - List issues
- [`projectsGetProject`](docs/sdks/projects/README.md#getproject) - Get project
- [`projectsListProjects`](docs/sdks/projects/README.md#listprojects) - List projects
- [`releasesListReleases`](docs/sdks/releases/README.md#listreleases) - List releases
- [`repositoriesListRepositories`](docs/sdks/repositories/README.md#listrepositories) - List repositories
- [`sponsorsGetSponsor`](docs/sdks/sponsors/README.md#getsponsor) - Get sponsor
- [`sponsorsListSponsors`](docs/sdks/sponsors/README.md#listsponsors) - List sponsors

</details>
<!-- End Standalone functions [standalone-funcs] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.chapters.listChapters({
    country: "India",
    region: "Asia",
  }, {
    retries: {
      strategy: "backoff",
      backoff: {
        initialInterval: 1,
        maxInterval: 50,
        exponent: 1.1,
        maxElapsedTime: 100,
      },
      retryConnectionErrors: false,
    },
  });

  console.log(result);
}

run();

```

If you'd like to override the default retry strategy for all operations that support retries, you can provide a retryConfig at SDK initialization:
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  retryConfig: {
    strategy: "backoff",
    backoff: {
      initialInterval: 1,
      maxInterval: 50,
      exponent: 1.1,
      maxElapsedTime: 100,
    },
    retryConnectionErrors: false,
  },
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.chapters.listChapters({
    country: "India",
    region: "Asia",
  });

  console.log(result);
}

run();

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`NestError`](./src/models/errors/nesterror.ts) is the base class for all HTTP error responses. It has the following properties:

| Property            | Type       | Description                                                                             |
| ------------------- | ---------- | --------------------------------------------------------------------------------------- |
| `error.message`     | `string`   | Error message                                                                           |
| `error.statusCode`  | `number`   | HTTP response status code eg `404`                                                      |
| `error.headers`     | `Headers`  | HTTP response headers                                                                   |
| `error.body`        | `string`   | HTTP body. Can be empty string if no body is returned.                                  |
| `error.rawResponse` | `Response` | Raw HTTP response                                                                       |
| `error.data$`       |            | Optional. Some errors may contain structured data. [See Error Classes](#error-classes). |

### Example
```typescript
import { Nest } from "owasp-nest";
import * as errors from "owasp-nest/models/errors";

const nest = new Nest({
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  try {
    const result = await nest.chapters.getChapter({
      chapterId: "London",
    });

    console.log(result);
  } catch (error) {
    // The base class for HTTP error responses
    if (error instanceof errors.NestError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);

      // Depending on the method different errors may be thrown
      if (error instanceof errors.ChapterErrorResponse) {
        console.log(error.data$.message); // string
      }
    }
  }
}

run();

```

### Error Classes
**Primary error:**
* [`NestError`](./src/models/errors/nesterror.ts): The base class for HTTP error responses.

<details><summary>Less common errors (12)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/httpclienterrors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/httpclienterrors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/httpclienterrors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/httpclienterrors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/httpclienterrors.ts): Unrecognised or unexpected error.


**Inherit from [`NestError`](./src/models/errors/nesterror.ts)**:
* [`ChapterErrorResponse`](./src/models/errors/chaptererrorresponse.ts): Chapter error response schema. Status code `404`. Applicable to 1 of 16 methods.*
* [`CommitteeErrorResponse`](./src/models/errors/committeeerrorresponse.ts): Committee error response schema. Status code `404`. Applicable to 1 of 16 methods.*
* [`MemberErrorResponse`](./src/models/errors/membererrorresponse.ts): Member error response schema. Status code `404`. Applicable to 1 of 16 methods.*
* [`OrganizationErrorResponse`](./src/models/errors/organizationerrorresponse.ts): Organization error response schema. Status code `404`. Applicable to 1 of 16 methods.*
* [`ProjectErrorResponse`](./src/models/errors/projecterrorresponse.ts): Project error response schema. Status code `404`. Applicable to 1 of 16 methods.*
* [`SponsorErrorResponse`](./src/models/errors/sponsorerrorresponse.ts): Sponsor error response schema. Status code `404`. Applicable to 1 of 16 methods.*
* [`ResponseValidationError`](./src/models/errors/responsevalidationerror.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>

\* Check [the method documentation](#available-resources-and-operations) to see if the error is applicable.
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Override Server URL Per-Client

The default server can be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { Nest } from "owasp-nest";

const nest = new Nest({
  serverURL: "https://nest.owasp.dev",
  apiKey: process.env["NEST_API_KEY"] ?? "",
});

async function run() {
  const result = await nest.chapters.listChapters({
    country: "India",
    region: "Asia",
  });

  console.log(result);
}

run();

```
<!-- End Server Selection [server] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The TypeScript SDK makes API calls using an `HTTPClient` that wraps the native
[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API). This
client is a thin wrapper around `fetch` and provides the ability to attach hooks
around the request lifecycle that can be used to modify the request or handle
errors and response.

The `HTTPClient` constructor takes an optional `fetcher` argument that can be
used to integrate a third-party HTTP client or when writing tests to mock out
the HTTP client and feed in fixtures.

The following example shows how to use the `"beforeRequest"` hook to to add a
custom header and a timeout to requests and how to use the `"requestError"` hook
to log errors:

```typescript
import { Nest } from "owasp-nest";
import { HTTPClient } from "owasp-nest/lib/http";

const httpClient = new HTTPClient({
  // fetcher takes a function that has the same signature as native `fetch`.
  fetcher: (request) => {
    return fetch(request);
  }
});

httpClient.addHook("beforeRequest", (request) => {
  const nextRequest = new Request(request, {
    signal: request.signal || AbortSignal.timeout(5000)
  });

  nextRequest.headers.set("x-custom-header", "custom value");

  return nextRequest;
});

httpClient.addHook("requestError", (error, request) => {
  console.group("Request Error");
  console.log("Reason:", `${error}`);
  console.log("Endpoint:", `${request.method} ${request.url}`);
  console.groupEnd();
});

const sdk = new Nest({ httpClient });
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass a logger that matches `console`'s interface as an SDK option.

> [!WARNING]
> Beware that debug logging will reveal secrets, like API tokens in headers, in log messages printed to a console or files. It's recommended to use this feature only during local development and not in production.

```typescript
import { Nest } from "owasp-nest";

const sdk = new Nest({ debugLogger: console });
```

You can also enable a default debug logger by setting an environment variable `NEST_DEBUG` to true.
<!-- End Debugging [debug] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation.
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release.

### SDK Created by [Speakeasy](https://www.speakeasy.com/?utm_source=owasp-nest&utm_campaign=typescript)
