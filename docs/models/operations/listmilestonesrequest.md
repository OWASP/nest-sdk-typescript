# ListMilestonesRequest

## Example Usage

```typescript
import { ListMilestonesRequest } from "owasp-nest/models/operations";

let value: ListMilestonesRequest = {
  organization: "OWASP",
  repository: "Nest",
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            | Example                                                                                |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `organization`                                                                         | *string*                                                                               | :heavy_minus_sign:                                                                     | Organization that milestones belong to (filtered by repository owner)                  | OWASP                                                                                  |
| `repository`                                                                           | *string*                                                                               | :heavy_minus_sign:                                                                     | Repository that milestones belong to                                                   | Nest                                                                                   |
| `state`                                                                                | [models.State](../../models/state.md)                                                  | :heavy_minus_sign:                                                                     | Milestone state                                                                        |                                                                                        |
| `ordering`                                                                             | [operations.ListMilestonesOrdering](../../models/operations/listmilestonesordering.md) | :heavy_minus_sign:                                                                     | N/A                                                                                    |                                                                                        |
| `page`                                                                                 | *number*                                                                               | :heavy_minus_sign:                                                                     | Page number                                                                            |                                                                                        |
| `pageSize`                                                                             | *number*                                                                               | :heavy_minus_sign:                                                                     | Number of items per page                                                               |                                                                                        |