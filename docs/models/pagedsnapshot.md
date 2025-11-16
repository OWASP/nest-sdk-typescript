# PagedSnapshot

## Example Usage

```typescript
import { PagedSnapshot } from "owasp-nest/models";

let value: PagedSnapshot = {
  currentPage: 317377,
  hasNext: false,
  hasPrevious: true,
  items: [
    {
      createdAt: new Date("2023-03-16T10:50:03.254Z"),
      endAt: new Date("2023-02-24T20:39:48.804Z"),
      key: "<key>",
      startAt: new Date("2024-07-24T02:37:25.982Z"),
      title: "<value>",
      updatedAt: new Date("2023-12-24T23:47:48.240Z"),
    },
  ],
  totalCount: 666191,
  totalPages: 504040,
};
```

## Fields

| Field                                      | Type                                       | Required                                   | Description                                |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `currentPage`                              | *number*                                   | :heavy_check_mark:                         | Current page number                        |
| `hasNext`                                  | *boolean*                                  | :heavy_check_mark:                         | Whether there is a next page               |
| `hasPrevious`                              | *boolean*                                  | :heavy_check_mark:                         | Whether there is a previous page           |
| `items`                                    | [models.Snapshot](../models/snapshot.md)[] | :heavy_check_mark:                         | N/A                                        |
| `totalCount`                               | *number*                                   | :heavy_check_mark:                         | Total number of items                      |
| `totalPages`                               | *number*                                   | :heavy_check_mark:                         | Total number of pages                      |