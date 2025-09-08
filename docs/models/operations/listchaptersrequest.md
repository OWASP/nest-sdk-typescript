# ListChaptersRequest

## Example Usage

```typescript
import { ListChaptersRequest } from "owasp-nest/models/operations";

let value: ListChaptersRequest = {
  country: "India",
  region: "Asia",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        | Example                                                                            |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `country`                                                                          | *string*                                                                           | :heavy_minus_sign:                                                                 | Country of the chapter                                                             | India                                                                              |
| `region`                                                                           | *string*                                                                           | :heavy_minus_sign:                                                                 | Region of the chapter                                                              | Asia                                                                               |
| `ordering`                                                                         | [operations.ListChaptersOrdering](../../models/operations/listchaptersordering.md) | :heavy_minus_sign:                                                                 | Ordering field                                                                     |                                                                                    |
| `page`                                                                             | *number*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |                                                                                    |
| `pageSize`                                                                         | *number*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |                                                                                    |