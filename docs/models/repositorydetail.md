# RepositoryDetail

Detail schema for Repository (used in single item endpoints).

## Example Usage

```typescript
import { RepositoryDetail } from "owasp-nest/models";

let value: RepositoryDetail = {
  createdAt: new Date("2025-06-19T15:24:46.169Z"),
  name: "<value>",
  updatedAt: new Date("2023-03-04T21:33:33.510Z"),
  commitsCount: 91245,
  contributorsCount: 470659,
  forksCount: 448126,
  openIssuesCount: 52164,
  starsCount: 447779,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `commitsCount`                                                                                | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `contributorsCount`                                                                           | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `description`                                                                                 | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `forksCount`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `openIssuesCount`                                                                             | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `starsCount`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |