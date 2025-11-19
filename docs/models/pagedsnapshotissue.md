# PagedSnapshotIssue

## Example Usage

```typescript
import { PagedSnapshotIssue } from "owasp-nest/models";

let value: PagedSnapshotIssue = {
  currentPage: 304044,
  hasNext: false,
  hasPrevious: true,
  items: [],
  totalCount: 306508,
  totalPages: 111436,
};
```

## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `currentPage`                                        | *number*                                             | :heavy_check_mark:                                   | Current page number                                  |
| `hasNext`                                            | *boolean*                                            | :heavy_check_mark:                                   | Whether there is a next page                         |
| `hasPrevious`                                        | *boolean*                                            | :heavy_check_mark:                                   | Whether there is a previous page                     |
| `items`                                              | [models.SnapshotIssue](../models/snapshotissue.md)[] | :heavy_check_mark:                                   | N/A                                                  |
| `totalCount`                                         | *number*                                             | :heavy_check_mark:                                   | Total number of items                                |
| `totalPages`                                         | *number*                                             | :heavy_check_mark:                                   | Total number of pages                                |