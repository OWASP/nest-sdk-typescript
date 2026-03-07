# ListProjectsRequest

## Example Usage

```typescript
import { ListProjectsRequest } from "owasp-nest/models/operations";

let value: ListProjectsRequest = {};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `level`                                                                            | [models.ProjectLevel](../../models/projectlevel.md)                                | :heavy_minus_sign:                                                                 | Level of the project                                                               |
| `q`                                                                                | *string*                                                                           | :heavy_minus_sign:                                                                 | Structured search query (e.g. 'name:security stars:>100')                          |
| `type`                                                                             | [models.ProjectType](../../models/projecttype.md)[]                                | :heavy_minus_sign:                                                                 | Type of the project                                                                |
| `ordering`                                                                         | [operations.ListProjectsOrdering](../../models/operations/listprojectsordering.md) | :heavy_minus_sign:                                                                 | Ordering field                                                                     |
| `page`                                                                             | *number*                                                                           | :heavy_minus_sign:                                                                 | Page number                                                                        |
| `pageSize`                                                                         | *number*                                                                           | :heavy_minus_sign:                                                                 | Number of items per page                                                           |