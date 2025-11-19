# ListEventsRequest

## Example Usage

```typescript
import { ListEventsRequest } from "owasp-nest/models/operations";

let value: ListEventsRequest = {};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `latitudeGte`                                                                  | *number*                                                                       | :heavy_minus_sign:                                                             | Latitude greater than or equal to                                              |
| `latitudeLte`                                                                  | *number*                                                                       | :heavy_minus_sign:                                                             | Latitude less than or equal to                                                 |
| `longitudeGte`                                                                 | *number*                                                                       | :heavy_minus_sign:                                                             | Longitude greater than or equal to                                             |
| `longitudeLte`                                                                 | *number*                                                                       | :heavy_minus_sign:                                                             | Longitude less than or equal to                                                |
| `ordering`                                                                     | [operations.ListEventsOrdering](../../models/operations/listeventsordering.md) | :heavy_minus_sign:                                                             | Ordering field                                                                 |
| `isUpcoming`                                                                   | *boolean*                                                                      | :heavy_minus_sign:                                                             | Filter for upcoming events                                                     |
| `page`                                                                         | *number*                                                                       | :heavy_minus_sign:                                                             | Page number                                                                    |
| `pageSize`                                                                     | *number*                                                                       | :heavy_minus_sign:                                                             | Number of items per page                                                       |