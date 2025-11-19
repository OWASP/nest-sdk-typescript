# PagedSnapshotRelease

## Example Usage

```typescript
import { PagedSnapshotRelease } from "owasp-nest/models";

let value: PagedSnapshotRelease = {
  currentPage: 22983,
  hasNext: true,
  hasPrevious: false,
  items: [],
  totalCount: 885303,
  totalPages: 235026,
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `currentPage`                                            | *number*                                                 | :heavy_check_mark:                                       | Current page number                                      |
| `hasNext`                                                | *boolean*                                                | :heavy_check_mark:                                       | Whether there is a next page                             |
| `hasPrevious`                                            | *boolean*                                                | :heavy_check_mark:                                       | Whether there is a previous page                         |
| `items`                                                  | [models.SnapshotRelease](../models/snapshotrelease.md)[] | :heavy_check_mark:                                       | N/A                                                      |
| `totalCount`                                             | *number*                                                 | :heavy_check_mark:                                       | Total number of items                                    |
| `totalPages`                                             | *number*                                                 | :heavy_check_mark:                                       | Total number of pages                                    |