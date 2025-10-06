# IssueDetail

Detail schema for Issue (used in single item endpoints).

## Example Usage

```typescript
import { IssueDetail } from "owasp-nest/models";

let value: IssueDetail = {
  createdAt: new Date("2025-03-17T01:51:24.196Z"),
  state: "open",
  title: "<value>",
  updatedAt: new Date("2025-10-25T04:19:33.685Z"),
  url: "https://trivial-smog.org",
  body: "<value>",
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
| `body`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |