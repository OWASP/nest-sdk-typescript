# ListRepositoriesRequest

## Example Usage

```typescript
import { ListRepositoriesRequest } from "owasp-nest/models/operations";

let value: ListRepositoriesRequest = {
  organizationId: "OWASP",
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                | Example                                                                                    |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `organizationId`                                                                           | *string*                                                                                   | :heavy_minus_sign:                                                                         | Organization that repositories belong to                                                   | OWASP                                                                                      |
| `ordering`                                                                                 | [operations.ListRepositoriesOrdering](../../models/operations/listrepositoriesordering.md) | :heavy_minus_sign:                                                                         | Ordering field                                                                             |                                                                                            |
| `page`                                                                                     | *number*                                                                                   | :heavy_minus_sign:                                                                         | Page number                                                                                |                                                                                            |
| `pageSize`                                                                                 | *number*                                                                                   | :heavy_minus_sign:                                                                         | Number of items per page                                                                   |                                                                                            |