# ListMembersRequest

## Example Usage

```typescript
import { ListMembersRequest } from "owasp-nest/models/operations";

let value: ListMembersRequest = {
  location: "India",
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      | Example                                                                          |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `company`                                                                        | *string*                                                                         | :heavy_minus_sign:                                                               | Company of the user                                                              |                                                                                  |
| `location`                                                                       | *string*                                                                         | :heavy_minus_sign:                                                               | Location of the member                                                           | India                                                                            |
| `ordering`                                                                       | [operations.ListMembersOrdering](../../models/operations/listmembersordering.md) | :heavy_minus_sign:                                                               | Ordering field                                                                   |                                                                                  |
| `page`                                                                           | *number*                                                                         | :heavy_minus_sign:                                                               | N/A                                                                              |                                                                                  |
| `pageSize`                                                                       | *number*                                                                         | :heavy_minus_sign:                                                               | N/A                                                                              |                                                                                  |