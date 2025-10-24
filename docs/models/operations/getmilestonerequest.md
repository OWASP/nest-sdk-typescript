# GetMilestoneRequest

## Example Usage

```typescript
import { GetMilestoneRequest } from "owasp-nest/models/operations";

let value: GetMilestoneRequest = {
  organizationId: "OWASP",
  repositoryId: "Nest",
  milestoneId: 1,
};
```

## Fields

| Field              | Type               | Required           | Description        | Example            |
| ------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| `organizationId`   | *string*           | :heavy_check_mark: | N/A                | OWASP              |
| `repositoryId`     | *string*           | :heavy_check_mark: | N/A                | Nest               |
| `milestoneId`      | *number*           | :heavy_check_mark: | N/A                | 1                  |