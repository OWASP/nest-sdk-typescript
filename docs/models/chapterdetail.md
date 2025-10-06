# ChapterDetail

Detail schema for Chapter (used in single item endpoints).

## Example Usage

```typescript
import { ChapterDetail } from "owasp-nest/models";

let value: ChapterDetail = {
  createdAt: new Date("2025-09-09T23:26:57.287Z"),
  key: "<key>",
  name: "<value>",
  updatedAt: new Date("2023-06-01T19:42:37.953Z"),
  country: "Burundi",
  region: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `key`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `country`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `region`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |