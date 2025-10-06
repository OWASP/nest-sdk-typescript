# ListIssuesRequest

## Example Usage

```typescript
import { ListIssuesRequest } from "owasp-nest/models/operations";

let value: ListIssuesRequest = {
  organization: "OWASP",
  repository: "Nest",
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    | Example                                                                        |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `organization`                                                                 | *string*                                                                       | :heavy_minus_sign:                                                             | Organization that issues belong to (filtered by repository owner)              | OWASP                                                                          |
| `repository`                                                                   | *string*                                                                       | :heavy_minus_sign:                                                             | Repository that issues belong to                                               | Nest                                                                           |
| `state`                                                                        | [models.State](../../models/state.md)                                          | :heavy_minus_sign:                                                             | Issue state                                                                    |                                                                                |
| `ordering`                                                                     | [operations.ListIssuesOrdering](../../models/operations/listissuesordering.md) | :heavy_minus_sign:                                                             | Ordering field                                                                 |                                                                                |
| `page`                                                                         | *number*                                                                       | :heavy_minus_sign:                                                             | Page number                                                                    |                                                                                |
| `pageSize`                                                                     | *number*                                                                       | :heavy_minus_sign:                                                             | Number of items per page                                                       |                                                                                |