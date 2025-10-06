# PagedOrganization

## Example Usage

```typescript
import { PagedOrganization } from "owasp-nest/models";

let value: PagedOrganization = {
  currentPage: 928953,
  hasNext: false,
  hasPrevious: true,
  items: [],
  totalCount: 755135,
  totalPages: 410410,
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `currentPage`                                      | *number*                                           | :heavy_check_mark:                                 | Current page number                                |
| `hasNext`                                          | *boolean*                                          | :heavy_check_mark:                                 | Whether there is a next page                       |
| `hasPrevious`                                      | *boolean*                                          | :heavy_check_mark:                                 | Whether there is a previous page                   |
| `items`                                            | [models.Organization](../models/organization.md)[] | :heavy_check_mark:                                 | N/A                                                |
| `totalCount`                                       | *number*                                           | :heavy_check_mark:                                 | Total number of items                              |
| `totalPages`                                       | *number*                                           | :heavy_check_mark:                                 | Total number of pages                              |