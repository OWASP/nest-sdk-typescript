# ProjectSchema

Schema for Project.

## Example Usage

```typescript
import { ProjectSchema } from "owasp-nest/models";

let value: ProjectSchema = {
  createdAt: new Date("2023-10-07T05:43:04.973Z"),
  description: "heighten adventurously lest",
  level: "production",
  name: "<value>",
  updatedAt: new Date("2023-01-13T14:30:43.398Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `level`                                                                                       | [models.ProjectLevel](../models/projectlevel.md)                                              | :heavy_check_mark:                                                                            | Enum for OWASP project levels.                                                                |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |