# ListSnapshotIssuesRequest

## Example Usage

```typescript
import { ListSnapshotIssuesRequest } from "owasp-nest/models/operations";

let value: ListSnapshotIssuesRequest = {
  snapshotId: "2025-02",
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    | Example                                                                                        |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `snapshotId`                                                                                   | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            | 2025-02                                                                                        |
| `ordering`                                                                                     | [operations.ListSnapshotIssuesOrdering](../../models/operations/listsnapshotissuesordering.md) | :heavy_minus_sign:                                                                             | Ordering field                                                                                 |                                                                                                |
| `page`                                                                                         | *number*                                                                                       | :heavy_minus_sign:                                                                             | Page number                                                                                    |                                                                                                |
| `pageSize`                                                                                     | *number*                                                                                       | :heavy_minus_sign:                                                                             | Number of items per page                                                                       |                                                                                                |