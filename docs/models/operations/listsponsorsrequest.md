# ListSponsorsRequest

## Example Usage

```typescript
import { ListSponsorsRequest } from "owasp-nest/models/operations";

let value: ListSponsorsRequest = {
  sponsorType: "Silver",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        | Example                                                                            |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `isMember`                                                                         | *boolean*                                                                          | :heavy_minus_sign:                                                                 | Member status of the sponsor                                                       |                                                                                    |
| `memberType`                                                                       | [models.MemberType](../../models/membertype.md)                                    | :heavy_minus_sign:                                                                 | Member type of the sponsor                                                         |                                                                                    |
| `sponsorType`                                                                      | *string*                                                                           | :heavy_minus_sign:                                                                 | Filter by the type of sponsorship (e.g., Gold, Silver, Platinum).                  | Silver                                                                             |
| `ordering`                                                                         | [operations.ListSponsorsOrdering](../../models/operations/listsponsorsordering.md) | :heavy_minus_sign:                                                                 | Ordering field                                                                     |                                                                                    |
| `page`                                                                             | *number*                                                                           | :heavy_minus_sign:                                                                 | Page number                                                                        |                                                                                    |
| `pageSize`                                                                         | *number*                                                                           | :heavy_minus_sign:                                                                 | Number of items per page                                                           |                                                                                    |