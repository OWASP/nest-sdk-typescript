# PagedProjectSchema

## Example Usage

```typescript
import { PagedProjectSchema } from "owasp-nest/models";

let value: PagedProjectSchema = {
  items: [],
  count: 876276,
};
```

## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `items`                                              | [models.ProjectSchema](../models/projectschema.md)[] | :heavy_check_mark:                                   | N/A                                                  |
| `count`                                              | *number*                                             | :heavy_check_mark:                                   | N/A                                                  |