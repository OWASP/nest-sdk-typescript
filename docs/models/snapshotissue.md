# SnapshotIssue

Schema for Snapshot Issue (used in list endpoints).

## Example Usage

```typescript
import { SnapshotIssue } from "owasp-nest/models";

let value: SnapshotIssue = {
  createdAt: new Date("2026-02-17T11:13:22.712Z"),
  state: "closed",
  title: "<value>",
  updatedAt: new Date("2026-12-28T06:30:36.486Z"),
  url: "https://wrathful-couch.net",
  organizationLogin: "<value>",
  repositoryName: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `state`                                                                                       | [models.State](../models/state.md)                                                            | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `title`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `url`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `organizationLogin`                                                                           | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `repositoryName`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |