# SnapshotDetail

Detail schema for Snapshot (used in single item endpoints).

## Example Usage

```typescript
import { SnapshotDetail } from "owasp-nest/models";

let value: SnapshotDetail = {
  createdAt: new Date("2024-07-02T07:36:59.091Z"),
  endAt: new Date("2024-06-12T21:48:22.996Z"),
  key: "<key>",
  startAt: new Date("2023-01-06T17:37:42.508Z"),
  title: "<value>",
  updatedAt: new Date("2025-05-05T00:55:41.870Z"),
  newChaptersCount: 74470,
  newIssuesCount: 304545,
  newProjectsCount: 117420,
  newReleasesCount: 865381,
  newUsersCount: 423280,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `endAt`                                                                                       | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `key`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `startAt`                                                                                     | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `title`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `newChaptersCount`                                                                            | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `newIssuesCount`                                                                              | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `newProjectsCount`                                                                            | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `newReleasesCount`                                                                            | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `newUsersCount`                                                                               | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |