# ListReleasesRequest

## Example Usage

```typescript
import { ListReleasesRequest } from "owasp-nest/models/operations";

let value: ListReleasesRequest = {
  organization: "OWASP",
  repository: "Nest",
  tagName: "0.2.10",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        | Example                                                                            |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `organization`                                                                     | *string*                                                                           | :heavy_minus_sign:                                                                 | Organization that releases belong to (filtered by repository owner)                | OWASP                                                                              |
| `repository`                                                                       | *string*                                                                           | :heavy_minus_sign:                                                                 | Repository that releases belong to                                                 | Nest                                                                               |
| `tagName`                                                                          | *string*                                                                           | :heavy_minus_sign:                                                                 | Tag name of the release                                                            | 0.2.10                                                                             |
| `ordering`                                                                         | [operations.ListReleasesOrdering](../../models/operations/listreleasesordering.md) | :heavy_minus_sign:                                                                 | Ordering field                                                                     |                                                                                    |
| `page`                                                                             | *number*                                                                           | :heavy_minus_sign:                                                                 | Page number                                                                        |                                                                                    |
| `pageSize`                                                                         | *number*                                                                           | :heavy_minus_sign:                                                                 | Number of items per page                                                           |                                                                                    |