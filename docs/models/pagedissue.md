# PagedIssue

## Example Usage

```typescript
import { PagedIssue } from "owasp-nest/models";

let value: PagedIssue = {
  currentPage: 315892,
  hasNext: true,
  hasPrevious: false,
  items: [],
  totalCount: 485755,
  totalPages: 557563,
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `currentPage`                        | *number*                             | :heavy_check_mark:                   | Current page number                  |
| `hasNext`                            | *boolean*                            | :heavy_check_mark:                   | Whether there is a next page         |
| `hasPrevious`                        | *boolean*                            | :heavy_check_mark:                   | Whether there is a previous page     |
| `items`                              | [models.Issue](../models/issue.md)[] | :heavy_check_mark:                   | N/A                                  |
| `totalCount`                         | *number*                             | :heavy_check_mark:                   | Total number of items                |
| `totalPages`                         | *number*                             | :heavy_check_mark:                   | Total number of pages                |