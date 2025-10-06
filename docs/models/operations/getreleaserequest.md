# GetReleaseRequest

## Example Usage

```typescript
import { GetReleaseRequest } from "owasp-nest/models/operations";

let value: GetReleaseRequest = {
  organizationId: "OWASP",
  repositoryId: "Nest",
  releaseId: "0.2.10",
};
```

## Fields

| Field              | Type               | Required           | Description        | Example            |
| ------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| `organizationId`   | *string*           | :heavy_check_mark: | N/A                | OWASP              |
| `repositoryId`     | *string*           | :heavy_check_mark: | N/A                | Nest               |
| `releaseId`        | *string*           | :heavy_check_mark: | N/A                | 0.2.10             |