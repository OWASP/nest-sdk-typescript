# ListIssuesRequest

## Example Usage

```typescript
import { ListIssuesRequest } from "owasp-nest/models/operations";

let value: ListIssuesRequest = {};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `state`                                                                        | [models.State](../../models/state.md)                                          | :heavy_minus_sign:                                                             | State of the issue                                                             |
| `ordering`                                                                     | [operations.ListIssuesOrdering](../../models/operations/listissuesordering.md) | :heavy_minus_sign:                                                             | Ordering field                                                                 |
| `page`                                                                         | *number*                                                                       | :heavy_minus_sign:                                                             | N/A                                                                            |
| `pageSize`                                                                     | *number*                                                                       | :heavy_minus_sign:                                                             | N/A                                                                            |