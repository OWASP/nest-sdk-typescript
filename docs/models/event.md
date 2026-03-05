# Event

Schema for Event (minimal fields for list display).

## Example Usage

```typescript
import { Event } from "owasp-nest/models";

let value: Event = {
  key: "<key>",
  name: "<value>",
  startDate: "<value>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `endDate`          | *string*           | :heavy_minus_sign: | N/A                |
| `key`              | *string*           | :heavy_check_mark: | N/A                |
| `latitude`         | *number*           | :heavy_minus_sign: | N/A                |
| `longitude`        | *number*           | :heavy_minus_sign: | N/A                |
| `name`             | *string*           | :heavy_check_mark: | N/A                |
| `startDate`        | *string*           | :heavy_check_mark: | N/A                |
| `url`              | *string*           | :heavy_minus_sign: | N/A                |