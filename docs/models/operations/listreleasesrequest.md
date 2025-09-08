# ListReleasesRequest

## Example Usage

```typescript
import { ListReleasesRequest } from "owasp-nest/models/operations";

let value: ListReleasesRequest = {
  tagName: "v1.0.0",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        | Example                                                                            |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `tagName`                                                                          | *string*                                                                           | :heavy_minus_sign:                                                                 | Tag name of the release                                                            | v1.0.0                                                                             |
| `ordering`                                                                         | [operations.ListReleasesOrdering](../../models/operations/listreleasesordering.md) | :heavy_minus_sign:                                                                 | Ordering field                                                                     |                                                                                    |
| `page`                                                                             | *number*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |                                                                                    |
| `pageSize`                                                                         | *number*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |                                                                                    |