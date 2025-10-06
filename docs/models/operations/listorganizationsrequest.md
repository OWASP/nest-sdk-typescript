# ListOrganizationsRequest

## Example Usage

```typescript
import { ListOrganizationsRequest } from "owasp-nest/models/operations";

let value: ListOrganizationsRequest = {
  location: "United States of America",
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  | Example                                                                                      |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `location`                                                                                   | *string*                                                                                     | :heavy_minus_sign:                                                                           | Location of the organization                                                                 | United States of America                                                                     |
| `ordering`                                                                                   | [operations.ListOrganizationsOrdering](../../models/operations/listorganizationsordering.md) | :heavy_minus_sign:                                                                           | Ordering field                                                                               |                                                                                              |
| `page`                                                                                       | *number*                                                                                     | :heavy_minus_sign:                                                                           | Page number                                                                                  |                                                                                              |
| `pageSize`                                                                                   | *number*                                                                                     | :heavy_minus_sign:                                                                           | Number of items per page                                                                     |                                                                                              |