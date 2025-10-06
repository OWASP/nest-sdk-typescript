# PagedSponsor

## Example Usage

```typescript
import { PagedSponsor } from "owasp-nest/models";

let value: PagedSponsor = {
  currentPage: 417532,
  hasNext: true,
  hasPrevious: true,
  items: [],
  totalCount: 210051,
  totalPages: 782475,
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `currentPage`                            | *number*                                 | :heavy_check_mark:                       | Current page number                      |
| `hasNext`                                | *boolean*                                | :heavy_check_mark:                       | Whether there is a next page             |
| `hasPrevious`                            | *boolean*                                | :heavy_check_mark:                       | Whether there is a previous page         |
| `items`                                  | [models.Sponsor](../models/sponsor.md)[] | :heavy_check_mark:                       | N/A                                      |
| `totalCount`                             | *number*                                 | :heavy_check_mark:                       | Total number of items                    |
| `totalPages`                             | *number*                                 | :heavy_check_mark:                       | Total number of pages                    |