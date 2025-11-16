# ListSnapshotMembersRequest

## Example Usage

```typescript
import { ListSnapshotMembersRequest } from "owasp-nest/models/operations";

let value: ListSnapshotMembersRequest = {
  snapshotId: "2025-02",
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      | Example                                                                                          |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `snapshotId`                                                                                     | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              | 2025-02                                                                                          |
| `ordering`                                                                                       | [operations.ListSnapshotMembersOrdering](../../models/operations/listsnapshotmembersordering.md) | :heavy_minus_sign:                                                                               | Ordering field                                                                                   |                                                                                                  |
| `page`                                                                                           | *number*                                                                                         | :heavy_minus_sign:                                                                               | Page number                                                                                      |                                                                                                  |
| `pageSize`                                                                                       | *number*                                                                                         | :heavy_minus_sign:                                                                               | Number of items per page                                                                         |                                                                                                  |