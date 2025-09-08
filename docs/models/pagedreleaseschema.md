# PagedReleaseSchema

## Example Usage

```typescript
import { PagedReleaseSchema } from "owasp-nest/models";

let value: PagedReleaseSchema = {
  items: [
    {
      createdAt: new Date("2023-02-07T09:08:55.719Z"),
      description:
        "when prioritize quarrelsomely regular marksman brr um round inwardly",
      name: "<value>",
      publishedAt: new Date("2023-04-21T20:42:25.857Z"),
      tagName: "<value>",
    },
  ],
  count: 918074,
};
```

## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `items`                                              | [models.ReleaseSchema](../models/releaseschema.md)[] | :heavy_check_mark:                                   | N/A                                                  |
| `count`                                              | *number*                                             | :heavy_check_mark:                                   | N/A                                                  |