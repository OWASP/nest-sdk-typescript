# ProjectDetail

Detail schema for Project (used in single item endpoints).

## Example Usage

```typescript
import { ProjectDetail } from "owasp-nest/models";

let value: ProjectDetail = {
  createdAt: new Date("2026-06-22T18:16:33.527Z"),
  key: "<key>",
  level: "incubator",
  name: "<value>",
  type: "documentation",
  updatedAt: new Date("2026-07-18T20:40:33.712Z"),
  description:
    "ill cumbersome guest through quietly incidentally ack hunt minus",
  leaders: [],
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `key`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `level`                                                                                       | [models.ProjectLevel](../models/projectlevel.md)                                              | :heavy_check_mark:                                                                            | Enum for OWASP project levels.                                                                |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `type`                                                                                        | [models.ProjectType](../models/projecttype.md)                                                | :heavy_check_mark:                                                                            | Enum for OWASP project types.                                                                 |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `leaders`                                                                                     | [models.Leader](../models/leader.md)[]                                                        | :heavy_check_mark:                                                                            | N/A                                                                                           |