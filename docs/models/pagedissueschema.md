# PagedIssueSchema

## Example Usage

```typescript
import { PagedIssueSchema } from "owasp-nest/models";

let value: PagedIssueSchema = {
  items: [
    {
      body: "<value>",
      createdAt: new Date("2025-02-26T23:44:11.290Z"),
      title: "<value>",
      state: "open",
      updatedAt: new Date("2024-09-13T08:50:21.939Z"),
      url: "https://improbable-ravioli.org",
    },
  ],
  count: 610144,
};
```

## Fields

| Field                                            | Type                                             | Required                                         | Description                                      |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| `items`                                          | [models.IssueSchema](../models/issueschema.md)[] | :heavy_check_mark:                               | N/A                                              |
| `count`                                          | *number*                                         | :heavy_check_mark:                               | N/A                                              |