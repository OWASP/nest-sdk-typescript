# PagedProject

## Example Usage

```typescript
import { PagedProject } from "owasp-nest/models";

let value: PagedProject = {
  currentPage: 936419,
  hasNext: true,
  hasPrevious: true,
  items: [
    {
      createdAt: new Date("2024-10-08T08:28:59.534Z"),
      key: "<key>",
      level: "flagship",
      name: "<value>",
      type: "other",
      updatedAt: new Date("2024-10-04T03:24:43.718Z"),
    },
  ],
  totalCount: 805365,
  totalPages: 938852,
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `currentPage`                            | *number*                                 | :heavy_check_mark:                       | Current page number                      |
| `hasNext`                                | *boolean*                                | :heavy_check_mark:                       | Whether there is a next page             |
| `hasPrevious`                            | *boolean*                                | :heavy_check_mark:                       | Whether there is a previous page         |
| `items`                                  | [models.Project](../models/project.md)[] | :heavy_check_mark:                       | N/A                                      |
| `totalCount`                             | *number*                                 | :heavy_check_mark:                       | Total number of items                    |
| `totalPages`                             | *number*                                 | :heavy_check_mark:                       | Total number of pages                    |