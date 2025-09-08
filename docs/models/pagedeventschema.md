# PagedEventSchema

## Example Usage

```typescript
import { PagedEventSchema } from "owasp-nest/models";

let value: PagedEventSchema = {
  items: [
    {
      description: "terrible yowza machine between um optimistically extension",
      name: "<value>",
      endDate: new Date("2024-12-01T23:16:53.781Z"),
      startDate: new Date("2023-02-19T12:22:26.535Z"),
      url: "https://oval-making.biz",
    },
  ],
  count: 900925,
};
```

## Fields

| Field                                            | Type                                             | Required                                         | Description                                      |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| `items`                                          | [models.EventSchema](../models/eventschema.md)[] | :heavy_check_mark:                               | N/A                                              |
| `count`                                          | *number*                                         | :heavy_check_mark:                               | N/A                                              |