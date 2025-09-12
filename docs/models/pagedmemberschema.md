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
      followersCount: 829556,
      followingCount: 427273,
      location: "<value>",
      login: "Reyes.Cartwright",
      name: "<value>",
      publicRepositoriesCount: 571919,
      title: "<value>",
      twitterUsername: "<value>",
      updatedAt: new Date("2023-05-20T04:41:05.495Z"),
      url: "https://mundane-junior.net/",
    },
  ],
  count: 260998,
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `items`                                            | [models.MemberSchema](../models/memberschema.md)[] | :heavy_check_mark:                                 | N/A                                                |
| `count`                                            | *number*                                           | :heavy_check_mark:                                 | N/A                                                |