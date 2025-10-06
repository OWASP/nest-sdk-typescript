# ListEventsRequest

## Example Usage

```typescript
import { ListEventsRequest } from "owasp-nest/models/operations";

let value: ListEventsRequest = {};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `ordering`                                                                     | [operations.ListEventsOrdering](../../models/operations/listeventsordering.md) | :heavy_minus_sign:                                                             | Ordering field                                                                 |
| `page`                                                                         | *number*                                                                       | :heavy_minus_sign:                                                             | Page number                                                                    |
| `pageSize`                                                                     | *number*                                                                       | :heavy_minus_sign:                                                             | Number of items per page                                                       |