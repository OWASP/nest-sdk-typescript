# ListChaptersRequest

## Example Usage

```typescript
import { ListChaptersRequest } from "owasp-nest/models/operations";

let value: ListChaptersRequest = {};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `latitudeGte`                                                                      | *number*                                                                           | :heavy_minus_sign:                                                                 | Latitude greater than or equal to                                                  |
| `latitudeLte`                                                                      | *number*                                                                           | :heavy_minus_sign:                                                                 | Latitude less than or equal to                                                     |
| `longitudeGte`                                                                     | *number*                                                                           | :heavy_minus_sign:                                                                 | Longitude greater than or equal to                                                 |
| `longitudeLte`                                                                     | *number*                                                                           | :heavy_minus_sign:                                                                 | Longitude less than or equal to                                                    |
| `country`                                                                          | *string*                                                                           | :heavy_minus_sign:                                                                 | Country of the chapter                                                             |
| `ordering`                                                                         | [operations.ListChaptersOrdering](../../models/operations/listchaptersordering.md) | :heavy_minus_sign:                                                                 | Ordering field                                                                     |
| `page`                                                                             | *number*                                                                           | :heavy_minus_sign:                                                                 | Page number                                                                        |
| `pageSize`                                                                         | *number*                                                                           | :heavy_minus_sign:                                                                 | Number of items per page                                                           |