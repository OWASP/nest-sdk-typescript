# Project

Schema for Project (minimal fields for list display).

## Example Usage

```typescript
import { Project } from "owasp-nest/models";

let value: Project = {
  createdAt: new Date("2026-06-12T00:25:18.992Z"),
  key: "<key>",
  level: "lab",
  name: "<value>",
  type: "tool",
  updatedAt: new Date("2025-05-28T09:16:17.673Z"),
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