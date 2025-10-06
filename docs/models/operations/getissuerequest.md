# GetIssueRequest

## Example Usage

```typescript
import { GetIssueRequest } from "owasp-nest/models/operations";

let value: GetIssueRequest = {
  organizationId: "OWASP",
  repositoryId: "Nest",
  issueId: 1234,
};
```

## Fields

| Field              | Type               | Required           | Description        | Example            |
| ------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| `organizationId`   | *string*           | :heavy_check_mark: | N/A                | OWASP              |
| `repositoryId`     | *string*           | :heavy_check_mark: | N/A                | Nest               |
| `issueId`          | *number*           | :heavy_check_mark: | N/A                | 1234               |