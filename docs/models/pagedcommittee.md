# PagedCommittee

## Example Usage

```typescript
import { PagedCommittee } from "owasp-nest/models";

let value: PagedCommittee = {
  currentPage: 585123,
  hasNext: false,
  hasPrevious: false,
  items: [
    {
      createdAt: new Date("2025-03-01T07:23:53.276Z"),
      key: "<key>",
      name: "<value>",
      updatedAt: new Date("2024-07-23T00:36:15.882Z"),
    },
  ],
  totalCount: 177312,
  totalPages: 997895,
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `currentPage`                                | *number*                                     | :heavy_check_mark:                           | Current page number                          |
| `hasNext`                                    | *boolean*                                    | :heavy_check_mark:                           | Whether there is a next page                 |
| `hasPrevious`                                | *boolean*                                    | :heavy_check_mark:                           | Whether there is a previous page             |
| `items`                                      | [models.Committee](../models/committee.md)[] | :heavy_check_mark:                           | N/A                                          |
| `totalCount`                                 | *number*                                     | :heavy_check_mark:                           | Total number of items                        |
| `totalPages`                                 | *number*                                     | :heavy_check_mark:                           | Total number of pages                        |