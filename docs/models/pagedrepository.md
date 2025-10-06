# PagedRepository

## Example Usage

```typescript
import { PagedRepository } from "owasp-nest/models";

let value: PagedRepository = {
  currentPage: 348670,
  hasNext: false,
  hasPrevious: false,
  items: [],
  totalCount: 513317,
  totalPages: 981023,
};
```

## Fields

| Field                                          | Type                                           | Required                                       | Description                                    |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| `currentPage`                                  | *number*                                       | :heavy_check_mark:                             | Current page number                            |
| `hasNext`                                      | *boolean*                                      | :heavy_check_mark:                             | Whether there is a next page                   |
| `hasPrevious`                                  | *boolean*                                      | :heavy_check_mark:                             | Whether there is a previous page               |
| `items`                                        | [models.Repository](../models/repository.md)[] | :heavy_check_mark:                             | N/A                                            |
| `totalCount`                                   | *number*                                       | :heavy_check_mark:                             | Total number of items                          |
| `totalPages`                                   | *number*                                       | :heavy_check_mark:                             | Total number of pages                          |