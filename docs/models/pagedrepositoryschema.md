# PagedRepositorySchema

## Example Usage

```typescript
import { PagedRepositorySchema } from "owasp-nest/models";

let value: PagedRepositorySchema = {
  items: [
    {
      createdAt: new Date("2023-12-10T05:24:03.979Z"),
      description: "once sociable sudden limply reach convection mystify oof",
      name: "<value>",
      updatedAt: new Date("2024-07-07T07:22:26.204Z"),
    },
  ],
  count: 158070,
};
```

## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `items`                                                    | [models.RepositorySchema](../models/repositoryschema.md)[] | :heavy_check_mark:                                         | N/A                                                        |
| `count`                                                    | *number*                                                   | :heavy_check_mark:                                         | N/A                                                        |