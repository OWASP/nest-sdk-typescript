# ListMembersRequest

## Example Usage

```typescript
import { ListMembersRequest } from "owasp-nest/models/operations";

let value: ListMembersRequest = {};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `company`                                                                        | *string*                                                                         | :heavy_minus_sign:                                                               | Company of the user                                                              |
| `location`                                                                       | *string*                                                                         | :heavy_minus_sign:                                                               | Location of the member                                                           |
| `ordering`                                                                       | [operations.ListMembersOrdering](../../models/operations/listmembersordering.md) | :heavy_minus_sign:                                                               | Ordering field                                                                   |
| `page`                                                                           | *number*                                                                         | :heavy_minus_sign:                                                               | Page number                                                                      |
| `pageSize`                                                                       | *number*                                                                         | :heavy_minus_sign:                                                               | Number of items per page                                                         |