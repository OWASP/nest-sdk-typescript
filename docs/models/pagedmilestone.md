# PagedMilestone

## Example Usage

```typescript
import { PagedMilestone } from "owasp-nest/models";

let value: PagedMilestone = {
  currentPage: 390809,
  hasNext: false,
  hasPrevious: false,
  items: [],
  totalCount: 216620,
  totalPages: 481624,
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `currentPage`                                | *number*                                     | :heavy_check_mark:                           | Current page number                          |
| `hasNext`                                    | *boolean*                                    | :heavy_check_mark:                           | Whether there is a next page                 |
| `hasPrevious`                                | *boolean*                                    | :heavy_check_mark:                           | Whether there is a previous page             |
| `items`                                      | [models.Milestone](../models/milestone.md)[] | :heavy_check_mark:                           | N/A                                          |
| `totalCount`                                 | *number*                                     | :heavy_check_mark:                           | Total number of items                        |
| `totalPages`                                 | *number*                                     | :heavy_check_mark:                           | Total number of pages                        |