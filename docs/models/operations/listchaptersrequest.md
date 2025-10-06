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
| `ordering`                                                                         | [operations.ListChaptersOrdering](../../models/operations/listchaptersordering.md) | :heavy_minus_sign:                                                                 | Ordering field                                                                     |
| `page`                                                                             | *number*                                                                           | :heavy_minus_sign:                                                                 | Page number                                                                        |
| `pageSize`                                                                         | *number*                                                                           | :heavy_minus_sign:                                                                 | Number of items per page                                                           |