# SponsorDetail

Detail schema for Sponsor (used in single item endpoints).

## Example Usage

```typescript
import { SponsorDetail } from "owasp-nest/models";

let value: SponsorDetail = {
  imageUrl: "https://whimsical-topsail.name/",
  key: "<key>",
  name: "<value>",
  sponsorType: "<value>",
  url: "https://growing-planula.org",
  description:
    "anenst augment hole restructure rudely tag stark gracefully modulo pull",
  isMember: false,
  jobUrl: "https://whispered-arcade.biz",
  memberType: "<value>",
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
| `description`      | *string*           | :heavy_check_mark: | N/A                |
| `isMember`         | *boolean*          | :heavy_check_mark: | N/A                |
| `jobUrl`           | *string*           | :heavy_check_mark: | N/A                |
| `memberType`       | *string*           | :heavy_check_mark: | N/A                |