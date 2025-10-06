# ListCommitteesRequest

## Example Usage

```typescript
import { ListCommitteesRequest } from "owasp-nest/models/operations";

let value: ListCommitteesRequest = {};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `ordering`                                                                             | [operations.ListCommitteesOrdering](../../models/operations/listcommitteesordering.md) | :heavy_minus_sign:                                                                     | Ordering field                                                                         |
| `page`                                                                                 | *number*                                                                               | :heavy_minus_sign:                                                                     | Page number                                                                            |
| `pageSize`                                                                             | *number*                                                                               | :heavy_minus_sign:                                                                     | Number of items per page                                                               |