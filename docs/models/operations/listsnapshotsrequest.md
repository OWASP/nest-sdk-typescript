# ListSnapshotsRequest

## Example Usage

```typescript
import { ListSnapshotsRequest } from "owasp-nest/models/operations";

let value: ListSnapshotsRequest = {};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ordering`                                                                           | [operations.ListSnapshotsOrdering](../../models/operations/listsnapshotsordering.md) | :heavy_minus_sign:                                                                   | Ordering field                                                                       |
| `page`                                                                               | *number*                                                                             | :heavy_minus_sign:                                                                   | Page number                                                                          |
| `pageSize`                                                                           | *number*                                                                             | :heavy_minus_sign:                                                                   | Number of items per page                                                             |