# PagedChapterSchema

## Example Usage

```typescript
import { PagedChapterSchema } from "owasp-nest/models";

let value: PagedChapterSchema = {
  items: [
    {
      country: "Turkmenistan",
      createdAt: new Date("2025-01-19T23:22:53.336Z"),
      name: "<value>",
      region: "<value>",
      updatedAt: new Date("2024-05-30T21:12:40.343Z"),
    },
  ],
  count: 814801,
};
```

## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `items`                                              | [models.ChapterSchema](../models/chapterschema.md)[] | :heavy_check_mark:                                   | N/A                                                  |
| `count`                                              | *number*                                             | :heavy_check_mark:                                   | N/A                                                  |