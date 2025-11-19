# ListSnapshotProjectsRequest

## Example Usage

```typescript
import { ListSnapshotProjectsRequest } from "owasp-nest/models/operations";

let value: ListSnapshotProjectsRequest = {
  snapshotId: "2025-02",
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        | Example                                                                                            |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `snapshotId`                                                                                       | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                | 2025-02                                                                                            |
| `ordering`                                                                                         | [operations.ListSnapshotProjectsOrdering](../../models/operations/listsnapshotprojectsordering.md) | :heavy_minus_sign:                                                                                 | Ordering field                                                                                     |                                                                                                    |
| `page`                                                                                             | *number*                                                                                           | :heavy_minus_sign:                                                                                 | Page number                                                                                        |                                                                                                    |
| `pageSize`                                                                                         | *number*                                                                                           | :heavy_minus_sign:                                                                                 | Number of items per page                                                                           |                                                                                                    |