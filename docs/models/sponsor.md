# Sponsor

Schema for Sponsor (minimal fields for list display).

## Example Usage

```typescript
import { Sponsor } from "owasp-nest/models";

let value: Sponsor = {
  imageUrl: "https://sick-yogurt.net",
  key: "<key>",
  name: "<value>",
  sponsorType: "<value>",
  url: "https://boring-seagull.biz/",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `imageUrl`         | *string*           | :heavy_check_mark: | N/A                |
| `key`              | *string*           | :heavy_check_mark: | N/A                |
| `name`             | *string*           | :heavy_check_mark: | N/A                |
| `sponsorType`      | *string*           | :heavy_check_mark: | N/A                |
| `url`              | *string*           | :heavy_check_mark: | N/A                |