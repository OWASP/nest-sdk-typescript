# PagedMemberSchema

## Example Usage

```typescript
import { PagedMemberSchema } from "owasp-nest/models";

let value: PagedMemberSchema = {
  items: [
    {
      avatarUrl: "https://perfumed-impostor.info",
      bio: "<value>",
      company: "O'Conner and Sons",
      createdAt: new Date("2025-02-16T10:32:59.432Z"),
      email: "Hester.Connelly@hotmail.com",
      followersCount: 377760,
      followingCount: 571919,
      location: "<value>",
      login: "Brandt.Lemke67",
      name: "<value>",
      publicRepositoriesCount: 105649,
      title: "<value>",
      twitterUsername: "<value>",
      updatedAt: new Date("2024-12-14T02:43:08.321Z"),
      url: "https://outlying-iridescence.org/",
    },
  ],
  count: 488848,
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `items`                                            | [models.MemberSchema](../models/memberschema.md)[] | :heavy_check_mark:                                 | N/A                                                |
| `count`                                            | *number*                                           | :heavy_check_mark:                                 | N/A                                                |