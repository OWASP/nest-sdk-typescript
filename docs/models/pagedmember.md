# PagedMember

## Example Usage

```typescript
import { PagedMember } from "owasp-nest/models";

let value: PagedMember = {
  currentPage: 457047,
  hasNext: true,
  hasPrevious: false,
  items: [
    {
      avatarUrl: "https://definite-labourer.biz/",
      createdAt: new Date("2024-01-13T05:15:14.872Z"),
      login: "Myriam73",
      name: "<value>",
      updatedAt: new Date("2024-05-27T09:47:03.747Z"),
      url: "https://poor-smog.info",
    },
  ],
  totalCount: 248927,
  totalPages: 385539,
};
```

## Fields

| Field                                  | Type                                   | Required                               | Description                            |
| -------------------------------------- | -------------------------------------- | -------------------------------------- | -------------------------------------- |
| `currentPage`                          | *number*                               | :heavy_check_mark:                     | Current page number                    |
| `hasNext`                              | *boolean*                              | :heavy_check_mark:                     | Whether there is a next page           |
| `hasPrevious`                          | *boolean*                              | :heavy_check_mark:                     | Whether there is a previous page       |
| `items`                                | [models.Member](../models/member.md)[] | :heavy_check_mark:                     | N/A                                    |
| `totalCount`                           | *number*                               | :heavy_check_mark:                     | Total number of items                  |
| `totalPages`                           | *number*                               | :heavy_check_mark:                     | Total number of pages                  |