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
  updatedAt: new Date("2025-05-07T21:49:39.702Z"),
  description:
    "present unfortunate while back furthermore calmly extent upright failing",
  leaders: [
    {
      name: "<value>",
    },
  ],
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `key`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `level`                                                                                       | [models.ProjectLevel](../models/projectlevel.md)                                              | :heavy_check_mark:                                                                            | Enum for OWASP project levels.                                                                |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `leaders`                                                                                     | [models.Leader](../models/leader.md)[]                                                        | :heavy_check_mark:                                                                            | N/A                                                                                           |