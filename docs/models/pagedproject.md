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
      updatedAt: new Date("2026-02-01T10:06:36.962Z"),
    },
  ],
  totalCount: 252867,
  totalPages: 805365,
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