# ListChaptersRequest

## Example Usage

```typescript
import { ListChaptersRequest } from "owasp-nest/models/operations";

let value: ListChaptersRequest = {};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `country`                                                                          | *string*                                                                           | :heavy_minus_sign:                                                                 | Country of the chapter                                                             |
| `region`                                                                           | *string*                                                                           | :heavy_minus_sign:                                                                 | Region of the chapter                                                              |
| `ordering`                                                                         | [operations.ListChaptersOrdering](../../models/operations/listchaptersordering.md) | :heavy_minus_sign:                                                                 | Ordering field                                                                     |
| `page`                                                                             | *number*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |
| `pageSize`                                                                         | *number*                                                                           | :heavy_minus_sign:                                                                 | N/A                                                                                |