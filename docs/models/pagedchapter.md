# PagedChapter

## Example Usage

```typescript
import { PagedChapter } from "owasp-nest/models";

let value: PagedChapter = {
  currentPage: 50738,
  hasNext: false,
  hasPrevious: true,
  items: [
    {
      createdAt: new Date("2026-09-08T18:06:51.442Z"),
      key: "<key>",
      name: "<value>",
      updatedAt: new Date("2024-09-27T03:38:15.337Z"),
    },
  ],
  totalCount: 95908,
  totalPages: 4065,
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `currentPage`                            | *number*                                 | :heavy_check_mark:                       | Current page number                      |
| `hasNext`                                | *boolean*                                | :heavy_check_mark:                       | Whether there is a next page             |
| `hasPrevious`                            | *boolean*                                | :heavy_check_mark:                       | Whether there is a previous page         |
| `items`                                  | [models.Chapter](../models/chapter.md)[] | :heavy_check_mark:                       | N/A                                      |
| `totalCount`                             | *number*                                 | :heavy_check_mark:                       | Total number of items                    |
| `totalPages`                             | *number*                                 | :heavy_check_mark:                       | Total number of pages                    |