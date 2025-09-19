# PagedSponsorSchema

## Example Usage

```typescript
import { PagedSponsorSchema } from "owasp-nest/models";

let value: PagedSponsorSchema = {
  items: [
    {
      description: "apricot why always er for bid yellow tomorrow zowie gah",
      imageUrl: "https://male-loyalty.net",
      isMember: true,
      jobUrl: "https://passionate-sand.name",
      key: "<key>",
      memberType: "<value>",
      name: "<value>",
      sponsorType: "<value>",
      url: "https://sure-footed-marathon.biz/",
    },
  ],
  count: 974582,
};
```

## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `items`                                              | [models.SponsorSchema](../models/sponsorschema.md)[] | :heavy_check_mark:                                   | N/A                                                  |
| `count`                                              | *number*                                             | :heavy_check_mark:                                   | N/A                                                  |