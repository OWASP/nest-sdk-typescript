# PagedEvent

## Example Usage

```typescript
import { PagedEvent } from "owasp-nest/models";

let value: PagedEvent = {
  currentPage: 718613,
  hasNext: false,
  hasPrevious: true,
  items: [
    {
      key: "<key>",
      name: "<value>",
      startDate: new Date("2025-07-04T19:18:18.407Z"),
    },
  ],
  totalCount: 781208,
  totalPages: 877785,
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `currentPage`                        | *number*                             | :heavy_check_mark:                   | Current page number                  |
| `hasNext`                            | *boolean*                            | :heavy_check_mark:                   | Whether there is a next page         |
| `hasPrevious`                        | *boolean*                            | :heavy_check_mark:                   | Whether there is a previous page     |
| `items`                              | [models.Event](../models/event.md)[] | :heavy_check_mark:                   | N/A                                  |
| `totalCount`                         | *number*                             | :heavy_check_mark:                   | Total number of items                |
| `totalPages`                         | *number*                             | :heavy_check_mark:                   | Total number of pages                |