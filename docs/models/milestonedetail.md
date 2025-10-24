# MilestoneDetail

Detail schema for Milestone (used in single item endpoints).

## Example Usage

```typescript
import { MilestoneDetail } from "owasp-nest/models";

let value: MilestoneDetail = {
  createdAt: new Date("2025-03-26T22:14:21.027Z"),
  number: 866324,
  state: "closed",
  title: "<value>",
  updatedAt: new Date("2025-07-03T06:33:16.416Z"),
  url: "https://similar-annual.com/",
  body: "<value>",
  closedIssuesCount: 809666,
  dueOn: new Date("2024-12-17T17:43:12.045Z"),
  openIssuesCount: 433448,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `number`                                                                                      | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `state`                                                                                       | [models.State](../models/state.md)                                                            | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `title`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `url`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `body`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `closedIssuesCount`                                                                           | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `dueOn`                                                                                       | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `openIssuesCount`                                                                             | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |