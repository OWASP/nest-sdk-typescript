# SnapshotRelease

Schema for Snapshot Release (used in list endpoints).

## Example Usage

```typescript
import { SnapshotRelease } from "owasp-nest/models";

let value: SnapshotRelease = {
  createdAt: new Date("2025-07-29T10:25:28.786Z"),
  name: "<value>",
  tagName: "<value>",
  organizationLogin: "<value>",
  repositoryName: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `publishedAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `tagName`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `organizationLogin`                                                                           | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `repositoryName`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |