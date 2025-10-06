# ListProjectsRequest

## Example Usage

```typescript
import { ListProjectsRequest } from "owasp-nest/models/operations";

let value: ListProjectsRequest = {
  ordering: "-created_at",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        | Example                                                                            |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `level`                                                                            | [models.ProjectLevel](../../models/projectlevel.md)                                | :heavy_minus_sign:                                                                 | Level of the project                                                               |                                                                                    |
| `ordering`                                                                         | [operations.ListProjectsOrdering](../../models/operations/listprojectsordering.md) | :heavy_minus_sign:                                                                 | Ordering field                                                                     | -created_at                                                                        |
| `page`                                                                             | *number*                                                                           | :heavy_minus_sign:                                                                 | Page number                                                                        |                                                                                    |
| `pageSize`                                                                         | *number*                                                                           | :heavy_minus_sign:                                                                 | Number of items per page                                                           |                                                                                    |