# PagedRelease

## Example Usage

```typescript
import { PagedRelease } from "owasp-nest/models";

let value: PagedRelease = {
  currentPage: 661268,
  hasNext: false,
  hasPrevious: true,
  items: [
    {
      createdAt: new Date("2025-04-23T19:00:35.027Z"),
      name: "<value>",
      tagName: "<value>",
    },
  ],
  totalCount: 667044,
  totalPages: 165116,
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `currentPage`                            | *number*                                 | :heavy_check_mark:                       | Current page number                      |
| `hasNext`                                | *boolean*                                | :heavy_check_mark:                       | Whether there is a next page             |
| `hasPrevious`                            | *boolean*                                | :heavy_check_mark:                       | Whether there is a previous page         |
| `items`                                  | [models.Release](../models/release.md)[] | :heavy_check_mark:                       | N/A                                      |
| `totalCount`                             | *number*                                 | :heavy_check_mark:                       | Total number of items                    |
| `totalPages`                             | *number*                                 | :heavy_check_mark:                       | Total number of pages                    |